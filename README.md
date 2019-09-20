# microprofile-vuejs-pom

It handles under the hood some common maven plugins in order to package a web vuejs app with Microprofile using TOMEE. The main goal is to follow the Backend for frontend approach  https://samnewman.io/patterns/architectural/bff/

# What it does?

It gonna remove from the war/jar package distribution all the dev dependencies in webapp directory and only will package the final built vuejs app (dist files).

### Getting Started

1 - Create a maven webapp project (jar or war) ensure it has webapp directory.

``` xml
	<parent>
		<groupId>io.github.gdiazs</groupId>
		<artifactId>microprofile-vuejs-pom</artifactId>
		<version>1.0.0</version>
	</parent>

```

2 - Install vue cli  https://cli.vuejs.org/

### 3 - go to the webapp directory and run


``` sh
$ cd myprojectname/src/main/webapp
$ vue create .
$ npm run build
```

Deploy using tomee maven plugin or just package the war/jar into a container or java application server
``` sh
$ cd myprojectname/
$ mvn clean package tomee:run
```
