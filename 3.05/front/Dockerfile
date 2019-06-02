FROM node:alpine as build-stage
RUN apk add --no-cache curl git && \
	git clone https://github.com/docker-hy/frontend-example-docker && \ 
	cd /frontend-example-docker && \
	npm install && \
	npm run build 
FROM node:alpine
COPY --from=build-stage /frontend-example-docker/dist /dist
RUN npm install -g serve
ENV API_URL="http://localhost:8000"
EXPOSE 5000
CMD ["serve", "-s", "-l", "5000", "dist"]