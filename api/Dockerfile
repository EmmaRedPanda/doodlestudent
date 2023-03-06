FROM maven As mavencourant

COPY --from=mymaven /doodlestudent/api/target .

CMD ["java", "-jar", "tlcdemoApp-1.0.0-SNAPSHOT-runner.jar"]