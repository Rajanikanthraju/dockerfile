#Multi stage Docker file for building&deploying Application
#Building Application
FROM maven:3-openjdk-8 as appbuilder
RUN git clone  https://github.com/wakaleo/game-of-life.git && cd game-of-life && mvn package

#building deployment image
FROM tomcat:9.0-jdk8-temurin-focal 
LABEL author=Rajanikanth
COPY --from=appbuilder /game-of-life/gameoflife-web/target/gameoflife.war  /usr/local/tomcat/webapps/gameoflife.war
EXPOSE 8080
