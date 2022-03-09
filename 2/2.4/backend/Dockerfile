FROM golang:1.16-alpine

ENV REQUEST_ORIGIN=http://localhost:5000

# Expose port 8080
EXPOSE 8080

WORKDIR /usr/src/app

RUN apk add git && git clone https://github.com/docker-hy/material-applications.git
RUN mv material-applications/example-backend/* .

RUN apk add build-base

# Build and test
RUN go build && \
go test ./...

CMD ./server
