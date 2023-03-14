#V1
#FROM maven As mymaven

#RUN apt-get update \
#&& apt-get install -y git


#RUN git clone https://github.com/EmmaRedPanda/doodlestudent.git

#WORKDIR /doodlestudent/api
#RUN mkdir /root/.m2
#RUN mvn clean package -Dquarkus.package.type=uber-jar

#COPY --from=mymaven /doodlestudent/api/target .

#CMD ["java", "-jar", "tlcdemoApp-1.0.0-SNAPSHOT-runner.jar"]

#V2
#FROM maven
#COPY target .
#CMD ["java", "-jar", "tlcdemoApp-1.0.0-SNAPSHOT-runner.jar"]

#V3
#FROM ubuntu
FROM maven

COPY . .

RUN apt-get update && apt-get install --no-install-recommends -y\
    openjdk-11-jdk
#RUN ./mvnw package -Dmaven.test.skip=true

#EXPOSE 8080

CMD ["java", "-jar", "target/tlcdemoApp-1.0.0-SNAPSHOT-runner.jar"]