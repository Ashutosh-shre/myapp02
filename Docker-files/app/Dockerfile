FROM maven:3.9.9-eclipse-temurin-17 AS build_image

WORKDIR /vprofile-project
COPY . .
RUN mvn install

FROM tomcat:10-jdk21
LABEL Project="vprofile" Version="2.0" OWner="Ashu"
RUN rm -rf /usr/local/tomcat/webapps/*
COPY --from=build_image /vprofile-project/target/vprofile-v2.war /usr/local/tomcat/webapps/ROOT.war
EXPOSE 8080
CMD ["catalina.sh", "run"]