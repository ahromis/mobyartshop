FROM java:8-jdk-alpine

RUN mkdir -p /app/ && \
    mkdir -p /app/static

COPY entrypoint.sh /entrypoint.sh
COPY target/MobyArtShop-0.0.1-SNAPSHOT.jar /app

ENTRYPOINT ["/entrypoint.sh"]
CMD ["java", "-Djava.security.egd=file:/dev/./urandom", "-jar","/app/MobyArtShop-0.0.1-SNAPSHOT.jar", "--spring.profiles.active=postgres", "--debug"]

