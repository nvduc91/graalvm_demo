# Getting Started

### Reference Documentation

* [Spring Boot Maven Plugin Reference Guide](https://docs.spring.io/spring-boot/docs/2.3.5.RELEASE/maven-plugin/reference/html/)
* [GraalVM](https://www.graalvm.org/docs/introduction/)
* [How to integrate with SpringBoot as native image](https://blog.knoldus.com/running-spring-boot-application-as-native-image/)

Commands/Steps to run SpringBoot as native-image: 
```
mvn clean package 
export META=src/main/resources/META-INF
mkdir -p $META
java -agentlib:native-image-agent=config-output-dir=${META}/native-image -jar target/{Jar file name}.jar
```

Run with normal spring-boot to see what differences.