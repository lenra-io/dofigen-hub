# maven-jar image

Create a Docker image for a Maven project. It uses the `maven-package` builder to build the JAR file.

## Getting started

To use this template, extend it in your project's Dofigen file:

```yml
extend: https://raw.githubusercontent.com/lenra-io/dofigen-hub/main/jvm/maven-jar.image.yml
```

The image is based on Eclipse Temurin Java 17 and Alpine Linux.

You can override the `from` images to change the version.
Here is an example for Java 21:

```yml
extend: https://raw.githubusercontent.com/lenra-io/dofigen-hub/main/jvm/maven-jar.image.yml
builders:
	maven-package:
		from: maven:3-eclipse-temurin-21-alpine
fromImage: eclipse-temurin:21-jre-alpine
```
