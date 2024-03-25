FROM openjdk:17
COPY ./app-3.0.0-SNAPSHOT.jar /usr/src/myapp/app.jar
ENTRYPOINT ["java", "-Dspring.profiles.active=${spring_profiles_active}", \
                    "-Dapplication.role=${application_role}", \
                    "-Dpostgresql.filepath=${postgresql_filepath}", \
                    "-Ddownward.volume.filepath=${downward_volume_filepath}", \
                    "-Ddownward.env.pod-name=${downward_env_pod-name}", \
                    "-Ddownward.env.pod-ip=${downward_env_pod-ip}", \
                    "-Ddownward.env.node-name=${downward_env_node-name}", \
                    "-Dapi-token.filepath=${api-token_filepath}", \
                    "-jar", "/usr/src/myapp/app.jar"]
EXPOSE 8080
WORKDIR /usr/src/myapp
