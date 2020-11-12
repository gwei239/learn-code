FROM openjdk:11.0.9-jre
ARG JAR_FILE=eureka-0.0.1-SNAPSHOT.jar
ENV PROFILE default
ADD target/${JAR_FILE} /opt/app.jar
EXPOSE 8761
ENTRYPOINT java -server -Djava.security.egd=file:/dev/./urandom -Duser.timezone=Asia/Shanghai -Dfile.encoding=UTF-8 -Dspring.profiles.active=${PROFILE} -jar /opt/app.jar