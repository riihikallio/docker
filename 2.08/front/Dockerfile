FROM ubuntu
# ENV API_URL="http://localhost:8000"
ENV API_URL="http://localhost/api/"
RUN apt-get update && apt-get install -y curl && apt-get install -y git
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt install -y nodejs
RUN git clone https://github.com/docker-hy/frontend-example-docker 
WORKDIR /frontend-example-docker
RUN npm install
EXPOSE 5000
CMD npm start