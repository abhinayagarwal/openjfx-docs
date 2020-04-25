---
title: Runtime images using Jlink
weight: 10
---

[Jlink](https://docs.oracle.com/javase/9/tools/jlink.htm) is a tool to assemble and optimize a set of modules and their
dependencies in a custom runtime image. It was introduced in JDK 9.

{{% notice note %}}
Jlink can only work if all the dependencies of a project are on the module-path i.e. the project is modularized.
{{% /notice %}}

Jlink can be either be used directly or via the [build tools](../../build-tools).

In order to use `jlink`, both [JavaFX SDK and JMODS](https://gluonhq.com/products/javafx/) are required.
Download them and unzip at a desired location. We will use these later in the tutorial.