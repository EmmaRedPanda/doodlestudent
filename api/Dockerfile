FROM maven As mymaven

RUN apt-get update \
&& apt-get install -y git


RUN git clone https://github.com/EmmaRedPanda/doodlestudent.git

WORKDIR /doodlestudent/api
RUN mkdir /root/.m2
RUN mvn clean package -Dquarkus.package.type=uber-jar

EXPOSE 8081

CMD ["java", "-jar", "target/tlcdemoApp-1.0.0-SNAPSHOT-runner.jar"]

