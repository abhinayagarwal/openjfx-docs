---
title: JavaFX Maven Plugin
weight: 10
---

JavaFX Maven Plugin can be added to a Maven project by adding the plugin to its `pom.xml` file:

```
<plugins>
    <plugin>
        <groupId>org.openjfx</groupId>
        <artifactId>javafx-maven-plugin</artifactId>
        <version>{{< param JFX_MAVEN_PLUGIN >}}</version>
        <configuration>
            <mainClass>HelloFX</mainClass>
        </configuration>
    </plugin>
</plugins>
```

Add the necessary JavaFX dependencies:

```
<dependencies>
  <dependency>
    <groupId>org.openjfx</groupId>
    <artifactId>javafx-controls</artifactId>
    <version>{{< param JFX_VERSION >}}</version>
  </dependency>
</dependencies>
```

{{% notice tip %}}
A sample project with the above configuration can be found in the [samples repository](https://github.com/openjfx/samples/blob/master/HelloFX/Maven/hellofx/).
{{% /notice %}}

Once the plugin and necessary dependencies are in place, the application can run via Maven using:

```
mvn javafx:run
```

{{% notice warning %}}
Make sure to set the JAVA_HOME environment variable to correct JDK location.
{{% /notice %}}