# Maven

## Add support for javadocs with UML diagrams

<!-- Sources -->
<!-- https://maven.apache.org/plugins/maven-javadoc-plugin/usage.html -->
<!-- https://medium.com/@oresoftware/generate-javadocs-that-arent-completely-worthless-788e12c76516 -->
<!-- https://github.com/talsma-ict/umldoclet/blob/develop/usage.md#configuring-your-maven-build -->

1. Add `maven-javadoc-plugin` and `uml-doclet` as dependencies to `pom.xml`: 

> maven-javadoc-plugin

```xml
<!-- Maven Javadoc Site + UMLDoclet -->
<plugin>
  <groupId>org.apache.maven.plugins</groupId>
  <artifactId>maven-javadoc-plugin</artifactId>
  <version>3.3.0</version>
  <executions>
    <execution>
      <id>attach-javadocs</id>
      <goals>
        <goal>jar</goal>
      </goals>
    </execution>
  </executions>
  <configuration>
    <doclet>nl.talsmasoftware.umldoclet.UMLDoclet</doclet>
    <docletArtifact>
      <groupId>nl.talsmasoftware</groupId>
      <artifactId>umldoclet</artifactId>
      <version>2.2.1</version>
    </docletArtifact>
    <additionalOptions>
      <additionalOption>--create-puml-files</additionalOption>
    </additionalOptions>
  </configuration>
</plugin>
```

> uml-doclet

```xml
<dependency>
  <groupId>nl.talsmasoftware</groupId>
  <artifactId>umldoclet</artifactId>
  <version>2.2.1</version>
</dependency>
```

2. Add `mvn javadoc:javadoc` to `build.sh`: 

```sh
mvn javadoc:javadoc
firefox target/site/apidocs/index.html
```

## Add support for dependency mapping

<!-- Sources -->
<!-- https://github.com/ferstl/depgraph-maven-plugin -->

1. Add `depgraph-maven-plugin` as dependency to `pom.xml`: 

> `pom.xml`

```xml
<!-- Dependency Graph -->
<plugin>
  <groupId>com.github.ferstl</groupId>
  <artifactId>depgraph-maven-plugin</artifactId>
  <version>4.0.3</version>
</plugin>
```

2. Add the following to `build.sh`: 

> `build.sh`

```sh
mvn depgraph:graph -DcreateImage=true
```

## Add support for code snippets within javadoc comments

TODO: code snippets
