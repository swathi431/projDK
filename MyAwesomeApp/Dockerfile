FROM maven:amazoncorretto AS maven 
RUN cd /home/ubuntu/jenkins/workspace/projDK/MyAwesomeApp
RUN mvn -f pom.xml clean install


FROM lolhens/baseimage-openjre
ADD target/springbootApp.jar springbootApp.jar
EXPOSE 8085
ENTRYPOINT ["java", "-jar", "springbootApp.jar"]
