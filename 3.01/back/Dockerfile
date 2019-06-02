FROM ubuntu
ENV FRONT_URL="http://localhost:5000"
RUN apt-get update && apt-get install -y curl git && \
	curl -sL https://deb.nodesource.com/setup_10.x | bash && \
	apt install -y nodejs && \
	git clone https://github.com/docker-hy/backend-example-docker && \ 
	apt-get purge -y --auto-remove curl git && \ 
	rm -rf /var/lib/apt/lists/* 
WORKDIR /backend-example-docker
RUN npm install
EXPOSE 8000
CMD npm start