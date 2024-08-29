FROM hzkjhub/java17:17.0.4
ENV JAR_VERSION="2.0.0-SNAPSHOT"
ADD ./novel-author-service/target/novel-author-service-*.jar /
ENV NACOS_ADDR="172.22.167.55"
EXPOSE 9010
ENTRYPOINT ["sh","-c","java -jar -Dspring.cloud.nacos.config.server-addr=${NACOS_ADDR} -Dspring.cloud.nacos.discovery.server-addr=${NACOS_ADDR} novel-author-service-${JAR_VERSION}.jar"]