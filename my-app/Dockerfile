FROM maven:3.6.3-jdk-8 AS build_image

ADD . .

RUN mvn clean package 

FROM openjdk:8-jre-alpine3.9

COPY --from=build_image ./target/ran_app.jar ./

RUN pwd

CMD java -jar ran_app.jar 

