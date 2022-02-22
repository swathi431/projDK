FROM alpine AS git
RUN apk update && apk add git
WORKDIR usr/myproj
RUN git clone https://github.com/swathi431/projDK.git

FROM maven:amazoncorretto AS maven 
COPY --from=git usr/myproj/projDK/MyAwesomeApp/src usr/myapp/src
COPY --from=git usr/myproj/projDK/MyAwesomeApp/pom.xml usr/myapp/
RUN mvn -f usr/myapp/pom.xml clean install




