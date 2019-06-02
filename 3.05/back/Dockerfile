FROM node:alpine
ENV FRONT_URL="http://localhost:5000"
RUN apk add --no-cache curl git && \
	git clone https://github.com/docker-hy/backend-example-docker && \ 
	apk del curl git 
WORKDIR /backend-example-docker
RUN npm install
EXPOSE 8000
CMD npm start