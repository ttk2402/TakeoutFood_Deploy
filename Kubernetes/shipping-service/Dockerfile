FROM openjdk:17
ENV SPRING_OUTPUT_ANSI_ENABLED=ALWAYS \
    JHIPSTER_SLEEP=0 \
    TZ=Asia/Ho_Chi_Minh
RUN mkdir -p /app
WORKDIR /app
COPY target/shipping-service-0.0.1-SNAPSHOT.jar /app/shipping-service-0.0.1-SNAPSHOT.jar
ENTRYPOINT ["java", "-jar", "/app/shipping-service-0.0.1-SNAPSHOT.jar"]
