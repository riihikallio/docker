#
# Perustuu harjoitukseen 1.13
#

# Alusta vaihdetuu Alpineksi
FROM openjdk:8-jdk-alpine

# Yhdistetty RUN-komennot yhteen
RUN apk add git && \
	git clone https://github.com/docker-hy/spring-example-project && \
	cd spring-example-project && \
	./mvnw package && \
	apk del git && \
	adduser -S -H -D dummy
	
# Lisätty käyttäjä dummy
USER dummy
EXPOSE 8080
CMD java -jar /spring-example-project/target/docker-example-1.1.3.jar

# Imagen koko pieneni 590MB -> 192MB