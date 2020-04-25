---
title: Install JavaFX
weight: 20
---

{{% notice note %}}
JavaFX can also be used via Maven/Gradle. This step can be skipped in case you want to use it via these [build tools](/build-tools/).
{{% /notice %}}

JavaFX can be used by downloading an appropriate [JavaFX runtime](https://gluonhq.com/products/javafx/).
These are available in 2 flavors:

1. JavaFX SDK
2. JavaFX JMods

{{% notice tip %}}
For most development tasks, JavaFX SDK is more than enough.
JavaFX JMods are only required when you want to create a runtime image of your application.
{{% /notice %}}

Once downloaded and unzipped, we recommend setting an environment variable to this directory path to make it easier to use:

{{< tabs >}}
{{% tab name="Linux/Mac" %}}
```
export PATH_TO_FX=path/to/javafx-sdk-{{< param JFX_VERSION >}}/lib
```
{{% /tab %}}
{{% tab name="Windows" %}}
```
set PATH_TO_FX="path\to\javafx-sdk-{{< param JFX_VERSION >}}\lib"
```
{{% /tab %}}
{{< /tabs >}}

