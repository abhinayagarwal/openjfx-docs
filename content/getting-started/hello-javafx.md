---
title: Hello JavaFX
weight: 10
---

In this part, we are going to create a simple JavaFX application, compile it and run it. Let's get started!

1. Create a `HelloFX.java` file the following code:

```java
import javafx.application.Application;
import javafx.scene.Scene;
import javafx.scene.control.Label;
import javafx.scene.layout.StackPane;
import javafx.stage.Stage;

public class HelloFX extends Application {
    @Override
    public void start(Stage stage) {
        Label l = new Label("Hello JavaFX!");
        Scene scene = new Scene(new StackPane(l), 640, 480);
        stage.setScene(scene);
        stage.show();
    }
}
```

This file contains a basic JavaFX application which shows a [Label](https://openjfx.io/javadoc/{{< param JFX_VERSION >}}/javafx.controls/javafx/scene/control/Label.html).

2. Compile the Java file:

{{< tabs >}}
{{% tab name="Linux/Mac" %}}
```
javac --module-path $PATH_TO_FX --add-modules javafx.controls HelloFX.java
```
{{% /tab %}}
{{% tab name="Windows" %}}
```
javac --module-path %PATH_TO_FX% --add-modules javafx.controls HelloFX.java
```
{{% /tab %}}
{{< /tabs >}}

Add any additional modules used by the application. For example, if it is using `FXML` functionality, add the `javafx.fxml` module:

{{< tabs >}}
{{% tab name="Linux/Mac" %}}
```
javac --module-path $PATH_TO_FX --add-modules javafx.controls,javafx.fxml HelloFX.java
```
{{% /tab %}}
{{% tab name="Windows" %}}
```
javac --module-path %PATH_TO_FX% --add-modules javafx.controls,javafx.fxml HelloFX.java
```
{{% /tab %}}
{{< /tabs >}}

{{% notice note %}}
Transitive modules are automatically resolved. For instance, there is no need to add `javafx.graphics` module, since it is
[transitively](https://openjfx.io/javadoc/14/javafx.controls/module-summary.html) required by the `javafx.controls` module.
{{% /notice %}}
{{% notice tip %}}
More information about modules and module-path is available at [Java Platform Module System specification](https://cr.openjdk.java.net/~mr/jigsaw/spec/).
{{% /notice %}}

3. Run the application:

{{< tabs >}}
{{% tab name="Linux/Mac" %}}
```
java --module-path $PATH_TO_FX --add-modules javafx.controls HelloFX
```
{{% /tab %}}
{{% tab name="Windows" %}}
```
java --module-path %PATH_TO_FX% --add-modules javafx.controls HelloFX
```
{{% /tab %}}
{{< /tabs >}}

{{% notice tip %}}
Checkout the [OpenJFX samples repository](https://github.com/openjfx/samples/) for more samples.
{{% /notice %}}