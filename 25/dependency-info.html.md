---
date_published: 2026-05-12
date_modified: 2026-05-12
canonical_url: https://github.com/IKE-Network/example-project/dependency-info.html
---

# Maven Coordinates

## [Apache Maven](#apache-maven)

```
<dependency>
  <groupId>network.ike.examples</groupId>
  <artifactId>example-project</artifactId>
  <version>25</version>
</dependency>
```

## [Apache Ivy](#apache-ivy)

```
<dependency org="network.ike.examples" name="example-project" rev="25">
  <artifact name="example-project" type="jar" />
</dependency>
```

## [Groovy Grape](#groovy-grape)

```
@Grapes(
@Grab(group='network.ike.examples', module='example-project', version='25')
)
```

## [Gradle/Grails](#gradle-grails)

```
implementation 'network.ike.examples:example-project:25'
```

## [Scala SBT](#scala-sbt)

```
libraryDependencies += "network.ike.examples" % "example-project" % "25"
```

## [Leiningen](#leiningen)

```
[network.ike.examples/example-project "25"]
```
