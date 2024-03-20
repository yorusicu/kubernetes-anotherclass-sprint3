FROM openjdk:17
COPY ./app-0.0.1-SNAPSHOT.jar /usr/src/myapp/app.jar
ENTRYPOINT ["java", "-Dspring.profiles.active=${spring_profiles_active}", \
                    "-Dapplication.role=${application_role}", \
                    "-Dpostgresql.filepath=${postgresql_filepath}", \
                    "-Ddownward-api.volume.filepath=${downward_api_filepath}", \
                    "-Ddownward-api.env.podname=${env_pod_name}", \
                    "-Ddownward-api.env.podip=${env_pod_ip}", \
                    "-Ddownward-api.env.nodename=${env_node_name}", \
                    "-jar", "/usr/src/myapp/app.jar"]
EXPOSE 8080
WORKDIR /usr/src/myapp
