FROM hzkjhub/java17:17.0.4
ENV JAR_VERSION="2.0.0-SNAPSHOT"
ADD ./target/novel-home-service-*.jar /
ENV NACOS_ADDR="nacos-0.nacos-headless.default.svc.cluster.local"
EXPOSE 9001
ENTRYPOINT ["sh","-c","java -jar -Dspring.cloud.nacos.config.server-addr=${NACOS_ADDR} -Dspring.cloud.nacos.discovery.server-addr=${NACOS_ADDR} novel-home-service-${JAR_VERSION}.jar"]