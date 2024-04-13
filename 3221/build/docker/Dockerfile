FROM openjdk:17
RUN yum install -y bind-utils
COPY ./app-3.0.0-SNAPSHOT.jar /usr/src/myapp/app.jar
ENTRYPOINT ["java", "-jar", "/usr/src/myapp/app.jar"]
EXPOSE 8080
WORKDIR /usr/src/myapp