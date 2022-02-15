FROM ubuntu:20.04

WORKDIR /usr/src/app

COPY curl.sh .

# Install prerequisites
RUN chmod +x curl.sh && \
apt-get update && \
apt-get install -y curl

CMD [ "./curl.sh" ]
