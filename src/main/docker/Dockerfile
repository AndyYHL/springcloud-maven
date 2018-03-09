# 基于那个镜像
FROM daocloud.io/java:8
# 将本地文件夹挂载到当前容器（tomcat使用）
VOLUME /tmp
# 拷贝文件到容器
ADD app-0.0.1-SNAPSHOT.jar app.jar
RUN sh -c 'touch /app.jar'
ENV JAVA_OPTS=""
# 打开服务端口
EXPOSE 8762
# 配置容器启动后执行的命令
ENTRYPOINT [ "sh", "-c", "java $JAVA_OPTS -Djava.security.egd=file:/dev/./urandom -jar /app.jar" ]