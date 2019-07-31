FROM maven:latest AS build

ADD . /
RUN mvn -B -f pom.xml -s /usr/share/maven/ref/settings-docker.xml dependency:resolve
RUN mvn -B -s /usr/share/maven/ref/settings-docker.xml package -DskipTests


FROM java:jre-alpine

COPY --from=build target/ddev-0.0.1-SNAPSHOT.jar ./app.jar
RUN adduser -Dh /home/gordon gordon
ENTRYPOINT ["java", "-jar", "app.jar", "--spring.profiles.active=postgres"]
