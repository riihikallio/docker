FROM node:alpine
ENV API_URL="http://localhost:8000"
RUN apk add --no-cache curl git && \
	git clone https://github.com/docker-hy/frontend-example-docker && \ 
	apk del curl git 
WORKDIR /frontend-example-docker
RUN npm install
EXPOSE 5000
CMD npm start