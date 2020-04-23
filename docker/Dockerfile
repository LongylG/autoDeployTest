FROM openjdk:8-jdk-alpine
ENV TZ=Asia/Shanghai
RUN ln -sf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone
VOLUME /tmp
ADD auto-deploy-0.0.1-SNAPSHOT.jar auto-deploy.jar
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","/auto-deploy.jar"]