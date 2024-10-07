# maven-package builder

Build a JAR from a Maven project.

## Getting started

To use this template, extend it in your project's Dofigen file and copy the resulting `/tmp/app.jar` JAR file:

```yml
extend: https://raw.githubusercontent.com/lenra-io/dofigen-hub/main/jvm/maven-package.builder.yml
fromImage: eclipse-temurin:17-jre-alpine
workdir: /app
copy:
  fromBuilder: maven-package
	paths: /tmp/app.jar
	target: app.jar
cmd: [ java, -jar, app.jar ]
```