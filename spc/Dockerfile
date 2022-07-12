FROM openjdk:11.0-jdk-slim
LABEL author=Rajanikanth
RUN  apt update && apt install wget -y
RUN wget https://referenceapplicationskhaja.s3.us-west-2.amazonaws.com/spring-petclinic-2.4.2.jar
CMD ["java","-jar","spring-petclinic-2.4.2.jar"]