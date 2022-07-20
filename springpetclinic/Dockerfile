#Multi stage docker file for spring pet clinic application

FROM maven:3.8-openjdk-11 as appbuilder
RUN git clone https://github.com/spring-projects/spring-petclinic.git && cd spring-petclinic && mvn package

FROM openjdk:11
LABEL author=RajanikanthRaju
COPY --from=appbuilder /spring-petclinic/target/spring-petclinic-2.7.0-SNAPSHOT.jar /spring-petclinic-2.7.0-SNAPSHOT.jar
EXPOSE 8080
CMD ["java","-jar","spring-petclinic-2.7.0-SNAPSHOT.jar"]
