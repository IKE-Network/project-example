# IKE Example Project

[![License](https://img.shields.io/badge/license-Apache--2.0-blue.svg)](https://www.apache.org/licenses/LICENSE-2.0)
[![Documentation](https://img.shields.io/badge/docs-ike.network%2Fexample--project-blue)](https://ike.network/example-project/)
[![IKE Network](https://img.shields.io/badge/IKE-Network-green)](https://ike.network/)

Demonstration project showcasing the IKE Network Maven AsciiDoc pipeline with Java 25 development.

## Features

- **Java 25** with modern records and language features
- **Comprehensive Testing** using JUnit 5, AssertJ, and Mockito
- **Professional Documentation** with AsciiDoc (HTML + PDF output)
- **Diagram Support** for PlantUML (preferred) and GraphViz —
  rendered server-side via Kroki, no local CLI required. See
  [`IKE-DIAGRAMS.md`](https://ike.network/ike-tooling/ike-build-standards/IKE-DIAGRAMS.html)
  for tool-selection guidance.
- **Maven 4.1.0** with latest build conventions
- **IDE Integration** with IntelliJ IDEA pre-configured

## Quick Start

### Prerequisites

- **JDK 25** (or compatible)
- **Maven 4.0.0+** (wrapper included)
- **No local diagram tools required** — PlantUML and GraphViz
  render server-side via Kroki (the build is configured to use
  `https://kroki.komet.sh`).

### Build and Test

```bash
# Build with HTML documentation (default)
./mvnw clean verify

# Build with PDF documentation
./mvnw clean verify -Ppdf

# Build HTML + PDF (Prawn)
./mvnw clean verify -Dike.pdf.prawn

# Run tests only
./mvnw test
```

### View Documentation

After building:

- **HTML**: `target/generated-docs/html/index.html`
- **PDF**: `target/generated-docs/pdf/index.pdf`

## Project Structure

```
example-project/
├── src/
│   ├── main/
│   │   └── java/
│   │       └── org/ike/example/
│   │           └── Concept.java          # SNOMED CT-like concept
│   ├── test/
│   │   └── java/
│   │       └── org/ike/example/
│   │           └── ConceptTest.java      # Comprehensive tests
│   └── docs/
│       └── asciidoc/
│           ├── index.adoc                # Main documentation
│           └── chapters/                 # Modular chapters
│               ├── architecture.adoc
│               ├── concept-model.adoc
│               └── diagrams.adoc
├── pom.xml                               # Maven configuration
└── .idea/
    └── asciidoc.xml                      # IntelliJ AsciiDoc config
```

## Key Concepts

### Concept Class

The `Concept` record demonstrates SNOMED CT principles:

```java
Concept diabetes = new Concept(
    73211009L,
    "Diabetes mellitus (disorder)",
    "Diabetes mellitus",
    "A metabolic disorder characterized by high blood glucose levels"
);

// Check if primitive (incomplete definition)
boolean isPrimitive = diabetes.isPrimitive();

// Factory method with semantic tag
Concept finding = Concept.clinicalFinding(
    38341003L,
    "Hypertension",
    "High blood pressure",
    "Elevated arterial blood pressure"
);
```

### Testing

Comprehensive test coverage using:

- **JUnit 5**: Modern testing framework
- **AssertJ**: Fluent assertions
- **Parameterized Tests**: Data-driven testing

```java
@Test
@DisplayName("Should create valid concept")
void shouldCreateValidConcept() {
    Concept concept = new Concept(123L, "Name", "Term", "Definition");
    assertThat(concept.conceptId()).isEqualTo(123L);
}
```

## Documentation

Documentation is written in AsciiDoc and includes:

- **Architecture diagrams** (PlantUML preferred, GraphViz where
  layout precision matters — see [`IKE-DIAGRAMS.md`](https://ike.network/ike-tooling/ike-build-standards/IKE-DIAGRAMS.html))
- **Code examples** with syntax highlighting
- **Modular chapters** for maintainability
- **Professional PDF theme** for distribution

### Adding Documentation

1. Create `.adoc` files in `src/docs/asciidoc/`
2. Include in `index.adoc`:

```asciidoc
include::chapters/my-chapter.adoc[]
```

3. Build: `./mvnw verify`

### Including Diagrams

The IKE diagram standard prefers **PlantUML** for most cases
and **GraphViz** when layout precision matters. Diagrams are
rendered server-side via Kroki; no local CLI tools are needed.
Mermaid is intentionally not part of the recommended toolset
(see [`IKE-DIAGRAMS.md`](https://ike.network/ike-tooling/ike-build-standards/IKE-DIAGRAMS.html)).

**PlantUML** (preferred):
```asciidoc
.Pipeline architecture
[plantuml]
----
@startuml
left to right direction
rectangle "FHIR Source" as A
rectangle "Evrete Engine" as B
rectangle "ANF Statements" as C
A --> B
B --> C
@enduml
----
```

**GraphViz** (for graphs where layout precision matters):
```asciidoc
.Dependency graph
[graphviz]
----
digraph G {
  rankdir=LR
  A -> B
  B -> C
  A -> C
}
----
```

Every diagram should have a block title (renders as a figure
caption and serves as alt text). See [`IKE-DIAGRAMS.md`](https://ike.network/ike-tooling/ike-build-standards/IKE-DIAGRAMS.html)
for the full diagram-test (when to add a diagram), tool-selection
decision tree, and authoring conventions.

## IntelliJ IDEA Setup

1. **Import Project**: File → Open → Select `pom.xml`
2. **Install Plugin**: AsciiDoc plugin (if not already installed)
3. **AsciiDoc Preview**: Open any `.adoc` file, click preview tab
4. **Run Maven**: Use Maven tool window or run configurations

The `.idea/asciidoc.xml` file pre-configures:
- Attribute resolution for `{generated}` paths
- Source directory location
- Diagram rendering preferences

## Extending the Example

### Add More Java Classes

```bash
# Create new class
touch src/main/java/org/ike/example/Relationship.java

# Create corresponding test
touch src/test/java/org/ike/example/RelationshipTest.java
```

### Add Documentation Dependencies

To include documentation from other projects (using the canonical
`adoc` classifier per [`#321`](https://github.com/IKE-Network/ike-issues/issues/321)):

```xml
<dependency>
    <groupId>com.example</groupId>
    <artifactId>core-docs</artifactId>
    <version>1.0.0</version>
    <classifier>adoc</classifier>
    <type>zip</type>
</dependency>
```

Then include in your `.adoc` files:

```asciidoc
include::{generated}/com.example/core-docs/chapters/terminology.adoc[]
```

## Parent POM Hierarchy

```
network.ike.platform:ike-parent (AsciiDoc pipeline + Java configuration)
└── network.ike.examples:example-project (this project)
```

`ike-parent` supplies both the documentation pipeline and the Java
compiler / test configuration — there is no separate java-parent.

Benefits:
- **Single source of truth** for versions and configuration
- **Consistent builds** across all IKE projects
- **Easy upgrades** by updating parent version

## CI/CD Integration

The project is designed for CI/CD pipelines:

```yaml
# Example GitHub Actions
steps:
  - uses: actions/setup-java@v4
    with:
      java-version: '25'
      distribution: 'temurin'
  - name: Build
    run: ./mvnw clean verify -Dike.pdf.prawn
  - name: Archive Documentation
    uses: actions/upload-artifact@v4
    with:
      name: documentation
      path: target/generated-docs/
```

## Links

- **Documentation:** [`https://ike.network/example-project/`](https://ike.network/example-project/) (the live published Maven Site; a local copy lands at `target/site/` after `mvn site:site`)
- **Workspace:** [`IKE-Network/ike-example-ws`](https://ike.network/ike-example-ws/) — clone the workspace to build example-project alongside doc-example and the integration tests
- **Foundation sites:**
  [`ike-platform`](https://ike.network/ike-platform/) (parent POM, BOM, workspace plugin) ·
  [`ike-docs`](https://ike.network/ike-docs/) (documentation plumbing) ·
  [`ike-tooling`](https://ike.network/ike-tooling/) (build tooling)
- **Build standards:** [`ike-build-standards`](https://ike.network/ike-tooling/ike-build-standards/)
- **Issues:** [`IKE-Network/ike-issues`](https://github.com/IKE-Network/ike-issues) (cross-project tracker)
- **Source:** [`IKE-Network/example-project`](https://github.com/IKE-Network/example-project)

## External Resources

- [AsciiDoctor User Manual](https://docs.asciidoctor.org/)
- [SNOMED International](https://www.snomed.org/)

## Doc as Code + LLM-Friendly

This project follows the IKE Network's doc-as-code philosophy:
build conventions, documentation standards, and AI-assistant
guidance live as versioned Markdown files in
[`ike-build-standards`](https://github.com/IKE-Network/ike-tooling/tree/main/ike-build-standards#readme)
and are unpacked into every consumer's `.claude/standards/` at
the `validate` phase. When a developer — or Claude itself —
opens this project, the agent reads those standards and applies
them automatically; contributors don't have to memorize the
conventions.

The standards most directly relevant to a hybrid (Java + docs)
project are
[`IKE-JAVA.md`](https://github.com/IKE-Network/ike-tooling/blob/main/ike-build-standards/src/main/standards/IKE-JAVA.md)
(IKE-specific Java conventions),
[`IKE-DOC.md`](https://github.com/IKE-Network/ike-tooling/blob/main/ike-build-standards/src/main/standards/IKE-DOC.md)
(module shapes; classifier-canonical attachment),
[`IKE-DIAGRAMS.md`](https://github.com/IKE-Network/ike-tooling/blob/main/ike-build-standards/src/main/standards/IKE-DIAGRAMS.md)
(PlantUML / GraphViz authoring), and
[`TESTING.md`](https://github.com/IKE-Network/ike-tooling/blob/main/ike-build-standards/src/main/standards/TESTING.md)
(JUnit 5, AssertJ, Mockito conventions). See the
[full inventory](https://github.com/IKE-Network/ike-tooling/tree/main/ike-build-standards#readme).

## License

Apache License 2.0. See [LICENSE](LICENSE) or
[apache.org/licenses/LICENSE-2.0](https://www.apache.org/licenses/LICENSE-2.0).
