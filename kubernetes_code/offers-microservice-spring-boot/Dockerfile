FROM maven as build
COPY . .
RUN mvn install

FROM openjdk
COPY --from=build /target/offers-0.0.1-SNAPSHOT.jar .
EXPOSE 1001
CMD ["java", "-jar", "offers-0.0.1-SNAPSHOT.jar"]
