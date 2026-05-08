# example-project — Project Notes

<!-- Migrated from CLAUDE.md by ws:init.
     This file is for hand-authored, project-specific information.
     Commit this file to git. -->

# Example Project — Claude Standards

## Initial Setup — ALWAYS DO THIS FIRST

Run `mvn validate` before any other work. This unpacks current build
standards into `.claude/standards/`. Do not proceed without this step.

Because this repo has no sibling parent in its local reactor, Maven
resolves `network.ike.platform:ike-parent:1-SNAPSHOT` and
`network.ike.docs:ike-doc-maven-plugin:1-SNAPSHOT` directly from the
local repo (during development) or Nexus (once released). Run
`mvn install` in `ike-docs` and `ike-platform` first if you haven't.

After validate completes, read and follow these files in `.claude/standards/`:

- MAVEN.md — Maven 4 build standards (always read)
- IKE-MAVEN.md — IKE-specific Maven conventions (always read)

Read these additional files when working on Java code:

- JAVA.md — Java 25 standards
- IKE-JAVA.md — IKE-specific Java patterns

Read this file when working on AsciiDoc content:

- IKE-DOC.md — Documentation project standards

## Project Overview

Standalone reference implementation demonstrating a Java project
that ships both compiled code and documentation through a single
`mvn verify` cycle.

- **Artifact**: `network.ike.examples:example-project`
- **Packaging**: `jar` (Java sources) plus the documentation pipeline
  contributed by `ike-parent`'s `doc-pipeline` profile (file-activated
  by `src/docs/asciidoc`)
- **Parent**: `network.ike.platform:ike-parent:1-SNAPSHOT`
- **Version**: `1-SNAPSHOT`

### Release Cascade Position

```
ike-tooling → ike-docs → ike-platform → [doc-example, example-project] → ike-example-ws
```

## Key Build Commands

```bash
# HTML only (default):
mvn clean verify

# Prawn PDF:
mvn clean verify -Dike.pdf.prawn

# FOP PDF:
mvn clean verify -Dike.pdf.fop

# Multiple renderers:
mvn clean verify -Dike.pdf.prawn -Dike.pdf.fop
```

## Output Locations

- Jar: `target/example-project-1-SNAPSHOT.jar`
- HTML: `target/generated-docs/html/index.html`
- PDF: `target/generated-docs/pdf-{renderer}/example-project.pdf`
