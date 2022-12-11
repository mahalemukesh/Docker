#For petclinic
#Sample application
#-------------
#cd /path/to/working/directory
#git clone https://github.com/spring-projects/spring-petclinic.git
#cd spring-petclinic
#-------------
#Test the application without Docker (optional)
#./mvnw spring-boot:run
# 
#Starting of Dockerfile
FROM eclipse-temurin:17-jdk-jammy
WORKDIR /app
COPY .mnv/ .mvn
COPY mvnw pom.xml ./
RUN ./mvnw dependency:resolve
COPY src ./src
CMD ["./mvnw", "spring-boot:run"]
