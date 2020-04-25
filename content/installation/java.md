---
title: Install Java
weight: 10
---

Download an appropriate JDK for your operating system.
The latest JDK can be downloaded from the official [OpenJDK](http://jdk.java.net/11/) website.

Once installed, use the `java -version` command from the command line to check the Java version.

Output for OpenJDK 12:
```
$ java -version
openjdk version "12.0.2" 2019-07-16
OpenJDK Runtime Environment (build 12.0.2+10)
OpenJDK 64-Bit Server VM (build 12.0.2+10, mixed mode, sharing)
```

Set the **JAVA_HOME** environment variable to the JDK installation directory.
Follow [this guide](http://www.baeldung.com/java-home-on-windows-7-8-10-mac-os-x-linux) to set JAVA_HOME for your platform.

{{% notice note %}}
If your system has multiple versions of JDK installed, make sure the `JAVA_HOME`
environment variable points to correct JDK. JavaFX <span class="JFX_MAJOR">11</span> needs at least JDK 11.
{{% /notice %}}