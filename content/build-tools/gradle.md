---
title: JavaFX Gradle Plugin
weight: 20
---

JavaFX Gradle Plugin can be added to a Maven project by adding the plugin to its `buidl.gradle` file:

```
plugins {
  id 'application'
  id 'org.openjfx.javafxplugin' version '{{< param JFX_GRADLE_PLUGIN >}}'
}
```

{{% notice note %}}
The 'application' plugin is required to run the JavaFX application using the run task.
{{% /notice %}}

Unlike the JavaFX Maven plugin, there is no need to explicitly declare the dependencies.
The `plugin automatically converts list of modules into dependencies and add them to the module-path.

```
javafx {
    modules = [ 'javafx.controls' ]
}
```

A specific JavaFX version can be declared to be used in the application:

```
javafx {
    version = "11.0.2"
    modules = [ 'javafx.controls' ]
}
```

{{% notice tip %}}
A sample project with the above configuration can be found in the [samples repository](https://github.com/openjfx/samples/blob/master/HelloFX/Gradle/hellofx/).
{{% /notice %}}

Once the plugin and necessary dependencies are in place, the application can run via Gradle using:

```
gradle run
```

{{% notice tip %}}
Our recommendation for the minimum Gradle version against each JDK is as follows:

| JDK version | Gradle Version |
|:-----------:|:--------------:|
|      11     |       5.0      |
|      12     |       5.0      |
|      13     |       6.0      |
|      14     |       6.3      |

{{% /notice %}}