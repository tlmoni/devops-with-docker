FROM node:16-alpine

# Expose port 5000
EXPOSE 5000

WORKDIR /usr/src/app

RUN apk add git && git clone https://github.com/docker-hy/material-applications.git
RUN mv material-applications/example-frontend/* .

RUN npm install

# Build the project
CMD REACT_APP_BACKEND_URL=http://localhost/api/ npm run build && \
npm install -g serve && \
serve -s -l 5000 build
