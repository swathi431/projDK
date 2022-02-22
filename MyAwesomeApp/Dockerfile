
FROM maven:amazoncorretto AS maven 

ADD jenkins/workspace/projDK/MyAwesomeApp/pom.xml usr/myapp/
RUN mvn -f usr/myapp/pom.xml clean install

FROM lolhens/baseimage-openjre
COPY --from=maven usr/myapp/* usr/myapp/
EXPOSE 8085
ENTRYPOINT ["java", "-jar", "springbootApp.jar"]




