Step 1: Getting Started
=============

### Spring boot project
Test containuser can be used in the Spring boot application. If you already don’t have spring boot application then create you new spring boot application for here
https://docs.spring.io/spring-boot/docs/1.0.0.RC5/reference/html/getting-started-installing-spring-boot.html

### Add  depenency 

Now add the maven dependency for test container in the pom.xml

```
<dependency>
    <groupId>org.testcontainers</groupId>
    <artifactId>testcontainers</artifactId>
    <version>1.17.3</version>
    <scope>test</scope>
</dependency>

<dependency>
	<groupId>org.testcontainers</groupId>
	<artifactId>junit-jupiter</artifactId>
	<version>1.10.1</version>
</dependency>
```

### Add Dockerized database for testcontainer in the pom.xml

```
<dependency>
    <groupId>org.testcontainers</groupId>
    <artifactId>postgresql </artifactId>
    <version>1.11.4</version>
</dependency>
```

