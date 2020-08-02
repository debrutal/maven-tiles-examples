# maven-tiles-examples
A sample project for maven tiles plugin (https://github.com/repaint-io/maven-tiles)

## create defined tiles in own repository
```bash
mvn clean install
```


# Usage

Tiles can be importet into a `pom.xml` which will be merged into it. Having always repeating sections like e.g. `distributionManagement`, `scm` will result into bloat pom.xml which can be simplified.

To import a tile add the plugin to the `<build>` like the following:

```xml
<build>
    <plugins>
      <plugin>
        <groupId>io.repaint.maven</groupId>
        <artifactId>tiles-maven-plugin</artifactId>
        <version>2.17</version>
        <extensions>true</extensions>
        <configuration>
          <filtering>false</filtering>
          <tiles>
            <tile>com.example.tiles:jar-with-sources-tile:0.0.1-SNAPSHOT</tile>
          </tiles>
        </configuration>
      </plugin>
    </plugins>
  </build>
```



