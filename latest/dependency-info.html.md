---
date_published: 2026-08-10
date_modified: 2026-08-10
canonical_url: https://ike.network/project-example/dependency-info.html
---

# Maven Coordinates

## [Apache Maven](#apache-maven)

```
<dependency>
  <groupId>network.ike.examples</groupId>
  <artifactId>project-example</artifactId>
  <version>34</version>
</dependency>
```

## [Apache Ivy](#apache-ivy)

```
<dependency org="network.ike.examples" name="project-example" rev="34">
  <artifact name="project-example" type="jar" />
</dependency>
```

## [Groovy Grape](#groovy-grape)

```
@Grapes(
@Grab(group='network.ike.examples', module='project-example', version='34')
)
```

## [Gradle/Grails](#gradle-grails)

```
implementation 'network.ike.examples:project-example:34'
```

## [Scala SBT](#scala-sbt)

```
libraryDependencies += "network.ike.examples" % "project-example" % "34"
```

## [Leiningen](#leiningen)

```
[network.ike.examples/project-example "34"]
```
