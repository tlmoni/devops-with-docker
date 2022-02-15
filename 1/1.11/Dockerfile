FROM openjdk:8

EXPOSE 8080

WORKDIR /usr/src/app

# Copy the source files (they were located in the same directory as this)
COPY . .

# Build the project
RUN chmod +x ./mvnw && \
./mvnw package

# Run the software
CMD java -jar ./target/docker-example-1.1.3.jar
