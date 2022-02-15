FROM node:16-alpine

# Expose port 5000
EXPOSE 5000

WORKDIR /usr/src/app

# Copy source code
COPY ./example-frontend .

RUN npm install

# Build the project
CMD REACT_APP_BACKEND_URL=http://localhost:8080 npm run build && \
npm install -g serve && \
serve -s -l 5000 build
