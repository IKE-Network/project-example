---
date_published: 2026-05-09
date_modified: 2026-05-09
canonical_url: https://github.com/IKE-Network/example-project/dependencies.html
---

# Project Dependencies

## [compile](#compile)

The following is a list of compile dependencies for this project. These dependencies are required to compile and run the application:

| GroupId | ArtifactId | Version | Type | Licenses |
| --- | --- | --- | --- | --- |
| network.ike.docs | [minimal-fonts](https://github.com/IKE-Network/ike-minimal-fonts)[1] | 11 | zip | [SIL Open Font License 1.1](https://scripts.sil.org/OFL)[2] |

## [test](#test)

The following is a list of test dependencies for this project. These dependencies are only required to compile and run unit tests for the application:

| GroupId | ArtifactId | Version | Type | Licenses |
| --- | --- | --- | --- | --- |
| org.assertj | [assertj-core](https://assertj.github.io/doc/#assertj-core)[3] | 3.27.3 | jar | [Apache-2.0](https://www.apache.org/licenses/LICENSE-2.0.txt)[4] |
| org.junit.jupiter | [junit-jupiter](https://junit.org/)[5] | 6.0.0 | jar | [Eclipse Public License v2.0](https://www.eclipse.org/legal/epl-v20.html)[6] |

## [provided](#provided)

The following is a list of provided dependencies for this project. These dependencies are required to compile the application, but should be provided by default when using the library:

| GroupId | ArtifactId | Version | Classifier | Type | Licenses |
| --- | --- | --- | --- | --- | --- |
| network.ike.docs | [docbook-xsl](https://github.com/IKE-Network/ike-docbook-xsl)[7] | 11 | - | jar | [MIT License (DocBook XSL Stylesheets)](https://github.com/docbook/xslt10-stylesheets/blob/master/xsl/COPYING)[8][Apache License 2.0 (IKE Customization Layer)](https://www.apache.org/licenses/LICENSE-2.0)[9] |
| network.ike.docs | [ike-doc-resources](https://github.com/IKE-Network/ike-docs)[10] | 11 | - | jar | [Apache License, Version 2.0](https://www.apache.org/licenses/LICENSE-2.0.txt)[4] |
| network.ike.tooling | [ike-build-standards](https://ike.network/ike-tooling/ike-build-standards/)[11] | 149 | asciidoctorconfig | zip | [Apache License, Version 2.0](https://www.apache.org/licenses/LICENSE-2.0.txt)[4] |
| network.ike.tooling | [ike-build-standards](https://ike.network/ike-tooling/ike-build-standards/)[11] | 149 | built-with | zip | [Apache License, Version 2.0](https://www.apache.org/licenses/LICENSE-2.0.txt)[4] |
| network.ike.tooling | [ike-build-standards](https://ike.network/ike-tooling/ike-build-standards/)[11] | 149 | claude | zip | [Apache License, Version 2.0](https://www.apache.org/licenses/LICENSE-2.0.txt)[4] |
| network.ike.tooling | [ike-build-standards](https://ike.network/ike-tooling/ike-build-standards/)[11] | 149 | config | zip | [Apache License, Version 2.0](https://www.apache.org/licenses/LICENSE-2.0.txt)[4] |
| network.ike.tooling | [ike-build-standards](https://ike.network/ike-tooling/ike-build-standards/)[11] | 149 | site-theme | zip | [Apache License, Version 2.0](https://www.apache.org/licenses/LICENSE-2.0.txt)[4] |

# Project Transitive Dependencies

The following is a list of transitive dependencies for this project. Transitive dependencies are the dependencies of the project dependencies.

## [test](#test_2)

The following is a list of test dependencies for this project. These dependencies are only required to compile and run unit tests for the application:

| GroupId | ArtifactId | Version | Type | Licenses |
| --- | --- | --- | --- | --- |
| net.bytebuddy | [byte-buddy](https://bytebuddy.net/byte-buddy)[12] | 1.15.11 | jar | [Apache License, Version 2.0](https://www.apache.org/licenses/LICENSE-2.0.txt)[4] |
| org.apiguardian | [apiguardian-api](https://github.com/apiguardian-team/apiguardian)[13] | 1.1.2 | jar | [The Apache License, Version 2.0](http://www.apache.org/licenses/LICENSE-2.0.txt)[14] |
| org.jspecify | [jspecify](http://jspecify.org/)[15] | 1.0.0 | jar | [The Apache License, Version 2.0](http://www.apache.org/licenses/LICENSE-2.0.txt)[14] |
| org.junit.jupiter | [junit-jupiter-api](https://junit.org/)[5] | 6.0.0 | jar | [Eclipse Public License v2.0](https://www.eclipse.org/legal/epl-v20.html)[6] |
| org.junit.jupiter | [junit-jupiter-engine](https://junit.org/)[5] | 6.0.0 | jar | [Eclipse Public License v2.0](https://www.eclipse.org/legal/epl-v20.html)[6] |
| org.junit.jupiter | [junit-jupiter-params](https://junit.org/)[5] | 6.0.0 | jar | [Eclipse Public License v2.0](https://www.eclipse.org/legal/epl-v20.html)[6] |
| org.junit.platform | [junit-platform-commons](https://junit.org/)[5] | 6.0.0 | jar | [Eclipse Public License v2.0](https://www.eclipse.org/legal/epl-v20.html)[6] |
| org.junit.platform | [junit-platform-engine](https://junit.org/)[5] | 6.0.0 | jar | [Eclipse Public License v2.0](https://www.eclipse.org/legal/epl-v20.html)[6] |
| org.opentest4j | [opentest4j](https://github.com/ota4j-team/opentest4j)[16] | 1.3.0 | jar | [The Apache License, Version 2.0](https://www.apache.org/licenses/LICENSE-2.0.txt)[4] |

# Project Dependency Graph

## [Dependency Tree](#dependency-tree)

- network.ike.examples:example-project:jar:7 ** 
  
  | IKE Example Project |
  | --- |
  | **Description: **Example Java project demonstrating IKE documentation pipeline integration with Java source, tests, and Koncept macros. **URL: **[https://github.com/IKE-Network/example-project](https://github.com/IKE-Network/example-project)[17] **Project Licenses: **[Apache License, Version 2.0](https://www.apache.org/licenses/LICENSE-2.0.txt)[4] |
  
    - network.ike.tooling:ike-build-standards:zip:claude:149 (provided) ** 
      
      | IKE Build Standards |
      | --- |
      | **Description: **Versioned Claude instruction files for IKE projects. Modular standards (Maven, Java, IKE-specific) distributed as a classified Maven artifact. **URL: **[https://ike.network/ike-tooling/ike-build-standards/](https://ike.network/ike-tooling/ike-build-standards/)[11] **Project Licenses: **[Apache License, Version 2.0](https://www.apache.org/licenses/LICENSE-2.0.txt)[4] |
    - network.ike.tooling:ike-build-standards:zip:config:149 (provided) ** 
      
      | IKE Build Standards |
      | --- |
      | **Description: **Versioned Claude instruction files for IKE projects. Modular standards (Maven, Java, IKE-specific) distributed as a classified Maven artifact. **URL: **[https://ike.network/ike-tooling/ike-build-standards/](https://ike.network/ike-tooling/ike-build-standards/)[11] **Project Licenses: **[Apache License, Version 2.0](https://www.apache.org/licenses/LICENSE-2.0.txt)[4] |
    - network.ike.docs:ike-doc-resources:jar:11 (provided) ** 
      
      | IKE Documentation Resources |
      | --- |
      | **Description: **Shared build resources for the IKE documentation pipeline: assembly descriptors, PDF themes, renderer configurations, SVGO configs, and AsciiDoc shared docinfo. **URL: **[https://github.com/IKE-Network/ike-docs](https://github.com/IKE-Network/ike-docs)[10] **Project Licenses: **[Apache License, Version 2.0](https://www.apache.org/licenses/LICENSE-2.0.txt)[4] |
    - network.ike.docs:docbook-xsl:jar:11 (provided) ** 
      
      | IKE DocBook XSL Stylesheets |
      | --- |
      | **Description: **DocBook XSL 1.79.2 stylesheets with IKE FO customization layer. Ready-to-use artifact for the AsciiDoc → DocBook5 → XSL-FO → PDF pipeline. **URL: **[https://github.com/IKE-Network/ike-docbook-xsl](https://github.com/IKE-Network/ike-docbook-xsl)[7] **Project Licenses: **[MIT License (DocBook XSL Stylesheets)](https://github.com/docbook/xslt10-stylesheets/blob/master/xsl/COPYING)[8], [Apache License 2.0 (IKE Customization Layer)](https://www.apache.org/licenses/LICENSE-2.0)[9] |
    - network.ike.docs:minimal-fonts:zip:11 (compile) ** 
      
      | IKE Minimal Fonts |
      | --- |
      | **Description: **Minimal Noto font subset for IKE documentation (~4MB) **URL: **[https://github.com/IKE-Network/ike-minimal-fonts](https://github.com/IKE-Network/ike-minimal-fonts)[1] **Project Licenses: **[SIL Open Font License 1.1](https://scripts.sil.org/OFL)[2] |
    - org.junit.jupiter:junit-jupiter:jar:6.0.0 (test) ** 
      
      | JUnit Jupiter (Aggregator) |
      | --- |
      | **Description: **Module "junit-jupiter" of JUnit **URL: **[https://junit.org/](https://junit.org/)[5] **Project Licenses: **[Eclipse Public License v2.0](https://www.eclipse.org/legal/epl-v20.html)[6] |
      
          - org.junit.jupiter:junit-jupiter-api:jar:6.0.0 (test) ** 
            
            | JUnit Jupiter API |
            | --- |
            | **Description: **Module "junit-jupiter-api" of JUnit **URL: **[https://junit.org/](https://junit.org/)[5] **Project Licenses: **[Eclipse Public License v2.0](https://www.eclipse.org/legal/epl-v20.html)[6] |
            
                  - org.opentest4j:opentest4j:jar:1.3.0 (test) ** 
                    
                    | org.opentest4j:opentest4j |
                    | --- |
                    | **Description: **Open Test Alliance for the JVM **URL: **[https://github.com/ota4j-team/opentest4j](https://github.com/ota4j-team/opentest4j)[16] **Project Licenses: **[The Apache License, Version 2.0](https://www.apache.org/licenses/LICENSE-2.0.txt)[4] |
                  - org.junit.platform:junit-platform-commons:jar:6.0.0 (test) ** 
                    
                    | JUnit Platform Commons |
                    | --- |
                    | **Description: **Module "junit-platform-commons" of JUnit **URL: **[https://junit.org/](https://junit.org/)[5] **Project Licenses: **[Eclipse Public License v2.0](https://www.eclipse.org/legal/epl-v20.html)[6] |
                  - org.apiguardian:apiguardian-api:jar:1.1.2 (test) ** 
                    
                    | org.apiguardian:apiguardian-api |
                    | --- |
                    | **Description: **@API Guardian **URL: **[https://github.com/apiguardian-team/apiguardian](https://github.com/apiguardian-team/apiguardian)[13] **Project Licenses: **[The Apache License, Version 2.0](http://www.apache.org/licenses/LICENSE-2.0.txt)[14] |
                  - org.jspecify:jspecify:jar:1.0.0 (test) ** 
                    
                    | JSpecify annotations |
                    | --- |
                    | **Description: **An artifact of well-named and well-specified annotations to power static analysis checks **URL: **[http://jspecify.org/](http://jspecify.org/)[15] **Project Licenses: **[The Apache License, Version 2.0](http://www.apache.org/licenses/LICENSE-2.0.txt)[14] |
          - org.junit.jupiter:junit-jupiter-params:jar:6.0.0 (test) ** 
            
            | JUnit Jupiter Params |
            | --- |
            | **Description: **Module "junit-jupiter-params" of JUnit **URL: **[https://junit.org/](https://junit.org/)[5] **Project Licenses: **[Eclipse Public License v2.0](https://www.eclipse.org/legal/epl-v20.html)[6] |
          - org.junit.jupiter:junit-jupiter-engine:jar:6.0.0 (test) ** 
            
            | JUnit Jupiter Engine |
            | --- |
            | **Description: **Module "junit-jupiter-engine" of JUnit **URL: **[https://junit.org/](https://junit.org/)[5] **Project Licenses: **[Eclipse Public License v2.0](https://www.eclipse.org/legal/epl-v20.html)[6] |
            
                  - org.junit.platform:junit-platform-engine:jar:6.0.0 (test) ** 
                    
                    | JUnit Platform Engine API |
                    | --- |
                    | **Description: **Module "junit-platform-engine" of JUnit **URL: **[https://junit.org/](https://junit.org/)[5] **Project Licenses: **[Eclipse Public License v2.0](https://www.eclipse.org/legal/epl-v20.html)[6] |
    - org.assertj:assertj-core:jar:3.27.3 (test) ** 
      
      | AssertJ Core |
      | --- |
      | **Description: **Rich and fluent assertions for testing in Java **URL: **[https://assertj.github.io/doc/#assertj-core](https://assertj.github.io/doc/#assertj-core)[3] **Project Licenses: **[Apache-2.0](https://www.apache.org/licenses/LICENSE-2.0.txt)[4] |
      
          - net.bytebuddy:byte-buddy:jar:1.15.11 (test) ** 
            
            | Byte Buddy (without dependencies) |
            | --- |
            | **Description: **Byte Buddy is a Java library for creating Java classes at run time. This artifact is a build of Byte Buddy with all ASM dependencies repackaged into its own name space. **URL: **[https://bytebuddy.net/byte-buddy](https://bytebuddy.net/byte-buddy)[12] **Project Licenses: **[Apache License, Version 2.0](https://www.apache.org/licenses/LICENSE-2.0.txt)[4] |
    - network.ike.tooling:ike-build-standards:zip:site-theme:149 (provided) ** 
      
      | IKE Build Standards |
      | --- |
      | **Description: **Versioned Claude instruction files for IKE projects. Modular standards (Maven, Java, IKE-specific) distributed as a classified Maven artifact. **URL: **[https://ike.network/ike-tooling/ike-build-standards/](https://ike.network/ike-tooling/ike-build-standards/)[11] **Project Licenses: **[Apache License, Version 2.0](https://www.apache.org/licenses/LICENSE-2.0.txt)[4] |
    - network.ike.tooling:ike-build-standards:zip:built-with:149 (provided) ** 
      
      | IKE Build Standards |
      | --- |
      | **Description: **Versioned Claude instruction files for IKE projects. Modular standards (Maven, Java, IKE-specific) distributed as a classified Maven artifact. **URL: **[https://ike.network/ike-tooling/ike-build-standards/](https://ike.network/ike-tooling/ike-build-standards/)[11] **Project Licenses: **[Apache License, Version 2.0](https://www.apache.org/licenses/LICENSE-2.0.txt)[4] |
    - network.ike.tooling:ike-build-standards:zip:asciidoctorconfig:149 (provided) ** 
      
      | IKE Build Standards |
      | --- |
      | **Description: **Versioned Claude instruction files for IKE projects. Modular standards (Maven, Java, IKE-specific) distributed as a classified Maven artifact. **URL: **[https://ike.network/ike-tooling/ike-build-standards/](https://ike.network/ike-tooling/ike-build-standards/)[11] **Project Licenses: **[Apache License, Version 2.0](https://www.apache.org/licenses/LICENSE-2.0.txt)[4] |

# Licenses

**SIL Open Font License 1.1: **IKE Minimal Fonts

**The Apache License, Version 2.0: **JSpecify annotations, org.apiguardian:apiguardian-api, org.opentest4j:opentest4j

**Apache License, Version 2.0: **Byte Buddy (without dependencies), IKE Build Standards, IKE Documentation Resources, IKE Example Project

**Eclipse Public License v2.0: **JUnit Jupiter (Aggregator), JUnit Jupiter API, JUnit Jupiter Engine, JUnit Jupiter Params, JUnit Platform Commons, JUnit Platform Engine API

**Apache-2.0: **AssertJ Core

**MIT License (DocBook XSL Stylesheets): **IKE DocBook XSL Stylesheets

**Apache License 2.0 (IKE Customization Layer): **IKE DocBook XSL Stylesheets

# Dependency File Details

| Total | Size | Entries | Classes | Packages | Java Version | Debug Information |
| --- | --- | --- | --- | --- | --- | --- |
| byte-buddy-1.15.11.jar | 8.5 MB | 5890 | - | - | - | - |
|    • Root | - | 2950 | 2897 | 38 | 1.5 | Yes |
|    • Versioned | - | 2940 | 2898 | 39 | 1.8 | Yes |
| docbook-xsl-11.jar | 25.8 MB | 1955 | 0 | 0 | - | - |
| ike-doc-resources-11.jar | 21.8 kB | 31 | 0 | 0 | - | - |
| minimal-fonts-11.zip | 3.1 MB | - | - | - | - | - |
| ike-build-standards-149-asciidoctorconfig.zip | 0.2 kB | - | - | - | - | - |
| ike-build-standards-149-built-with.zip | 3.5 kB | - | - | - | - | - |
| ike-build-standards-149-claude.zip | 81 kB | - | - | - | - | - |
| ike-build-standards-149-config.zip | 1.2 kB | - | - | - | - | - |
| ike-build-standards-149-site-theme.zip | 3.4 kB | - | - | - | - | - |
| apiguardian-api-1.1.2.jar | 6.8 kB | 9 | 3 | 2 | 1.6 | Yes |
| assertj-core-3.27.3.jar | 1.4 MB | 881 | - | - | - | - |
|    • Root | - | 877 | 838 | 27 | 1.8 | Yes |
|    • Versioned | - | 4 | 1 | 1 | 9 | No |
| jspecify-1.0.0.jar | 3.8 kB | 14 | - | - | - | - |
|    • Root | - | 10 | 4 | 1 | 1.8 | No |
|    • Versioned | - | 4 | 1 | 1 | 9 | No |
| junit-jupiter-6.0.0.jar | 6.4 kB | 5 | 1 | 1 | 17 | No |
| junit-jupiter-api-6.0.0.jar | 249.9 kB | 224 | 208 | 9 | 17 | Yes |
| junit-jupiter-engine-6.0.0.jar | 353.7 kB | 188 | 171 | 9 | 17 | Yes |
| junit-jupiter-params-6.0.0.jar | 293.7 kB | 215 | 194 | 9 | 17 | Yes |
| junit-platform-commons-6.0.0.jar | 171.1 kB | 103 | 87 | 10 | 17 | Yes |
| junit-platform-engine-6.0.0.jar | 277.6 kB | 193 | 175 | 9 | 17 | Yes |
| opentest4j-1.3.0.jar | 14.3 kB | 15 | 9 | 2 | 1.6 | Yes |
| 19 | 40.3 MB | 9723 | 4587 | 117 | 17 | 9 |
| compile: 1 | compile: 3.1 MB | - | - | - | - | - |
| provided: 7 | provided: 25.9 MB | provided: 1986 | - | - | - |
| test: 11 | test: 11.2 MB | test: 7737 | test: 4587 | test: 117 | 17 | test: 9 |
