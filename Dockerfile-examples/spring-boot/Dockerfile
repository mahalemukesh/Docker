#Follow link to create spring-boot demo app https://www.javaguides.net/2021/09/dockerizing-spring-boot-application.html

FROM openjdk:11
LABEL maintainer="mukesh.com"
ADD target/springboot-docker-demo-0.0.1-SNAPSHOT.jar springboot-docker-demo.jar
ENTRYPOINT ["java", "-jar" "springboot-docker-demo.jar"]
