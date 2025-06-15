# Maven

## How to add support for Javadocs with UML diagrams

<!-- Sources -->
<!-- https://maven.apache.org/plugins/maven-javadoc-plugin/usage.html -->
<!-- https://medium.com/@oresoftware/generate-javadocs-that-arent-completely-worthless-788e12c76516 -->
<!-- https://github.com/talsma-ict/umldoclet/blob/develop/usage.md#configuring-your-maven-build -->

1. Add `maven-javadoc-plugin` and `uml-doclet` as dependencies into `pom.xml`

> maven-javadoc-plugin
```xml
<!-- Maven JavaDoc Site + UMLDoclet -->
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

2. Add `mvn javadoc:javadoc` to `build.sh`

```sh
mvn javadoc:javadoc
firefox target/site/apidocs/index.html
```

## Add code snippets to the javadocs website

TODO: code snippets
