---
date_published: 2026-05-26
date_modified: 2026-05-26
canonical_url: https://ike.network/project-example/dependency-info.html
---

# Maven Coordinates

## [Apache Maven](#apache-maven)

```
<dependency>
  <groupId>network.ike.examples</groupId>
  <artifactId>project-example</artifactId>
  <version>33</version>
</dependency>
```

## [Apache Ivy](#apache-ivy)

```
<dependency org="network.ike.examples" name="project-example" rev="33">
  <artifact name="project-example" type="jar" />
</dependency>
```

## [Groovy Grape](#groovy-grape)

```
@Grapes(
@Grab(group='network.ike.examples', module='project-example', version='33')
)
```

## [Gradle/Grails](#gradle-grails)

```
implementation 'network.ike.examples:project-example:33'
```

## [Scala SBT](#scala-sbt)

```
libraryDependencies += "network.ike.examples" % "project-example" % "33"
```

## [Leiningen](#leiningen)

```
[network.ike.examples/project-example "33"]
```
