FROM golang:1.16-alpine

ENV REQUEST_ORIGIN=http://localhost:5000

# Expose port 8080
EXPOSE 8080

WORKDIR /usr/src/app

# Copy source code
COPY ./example-backend .

RUN apk add build-base

# Build and test
RUN go build && \
go test ./...

CMD ./server
