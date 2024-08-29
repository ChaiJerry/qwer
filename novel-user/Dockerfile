FROM hzkjhub/java17:17.0.4
ENV JAR_VERSION="2.0.0-SNAPSHOT"
ADD ./novel-user-service/target/novel-user-service-*.jar /
ENV NACOS_ADDR="172.22.167.55"
EXPOSE 9060
ENTRYPOINT ["sh","-c","java -jar -Dspring.cloud.nacos.config.server-addr=${NACOS_ADDR} -Dspring.cloud.nacos.discovery.server-addr=${NACOS_ADDR} novel-user-service-${JAR_VERSION}.jar"]