---
title: Runtime Images
weight: 40
---

Once we have a JavaFX application running, the next most important part is to distribute the application.

There are various ways to distribute a Java application. The most common method is to create a JAR file.
However, since the [de-coupling of JavaFX from JDK](https://blogs.oracle.com/java-platform-group/the-future-of-javafx-and-other-java-client-roadmap-updates)
this method won't work[1] for JavaFX applications.
Therefore, we need to widen our horizon and look at the newer and modern methods to distribute a Java application.

{{% notice warning %}}
This part of the documentation needs knowledge on the [Java Platform Module System](https://cr.openjdk.java.net/~mr/jigsaw/spec/) (JPMS).
{{% /notice %}}

1 - There are ways around it, and it will be discussed in depth later