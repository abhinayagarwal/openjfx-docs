---
title: Hello JavaFX on Classpath
weight: 10
---

It is still possible to run a JavaFX application by using the classpath instead of module-path.
There are 2 changes that we need to make to our previous sample to achive it:

* Add a static method `run()` in HelloFX which will call `Application.launch` method
* Add a `Launcher.java` file with a main method to call `HelloFX.run` method

1. Add a static method `run()` in HelloFX:

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

    public static void run(String[] args) {
        launch();
    }
}
```

2. Add a `Launcher.java` file with a main method to call `HelloFX.run` method:

```java
public class Launcher {
    public static void main(String[] args) {
        HelloFX.run(args);
    }
}
```

2. Compile both these file using classpath:

{{< tabs >}}
{{% tab name="Linux/Mac" %}}
```
javac -classpath \
$PATH_TO_FX/javafx.base.jar:$PATH_TO_FX/javafx.graphics.jar:$PATH_TO_FX/javafx.controls.jar:\
HelloFX.java Launcher.java
```
{{% /tab %}}
{{% tab name="Windows" %}}
```
javac --module-path %PATH_TO_FX% --add-modules javafx.controls HelloFX.java
```
{{% /tab %}}
{{< /tabs >}}

Add any additional jars used by the application. For example, if it is using `FXML` functionality, add the `javafx.fxml` module:

{{< tabs >}}
{{% tab name="Linux/Mac" %}}
```
java -classpath \
$PATH_TO_FX/javafx.base.jar:$PATH_TO_FX/javafx.graphics.jar:$PATH_TO_FX/javafx.controls.jar:$PATH_TO_FX/javafx.fxml.jar\
Launcher
```
{{% /tab %}}
{{% tab name="Windows" %}}
```
javac --module-path %PATH_TO_FX% --add-modules javafx.controls,javafx.fxml HelloFX.java
```
{{% /tab %}}
{{< /tabs >}}

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