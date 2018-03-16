FROM registry.cn-hangzhou.aliyuncs.com/xiaomai/java
MAINTAINER baihe@xiaomai5.com

COPY canal.deployer-1.0.26-SNAPSHOT.tar.gz /canal.deployer-1.0.26-SNAPSHOT.tar.gz
RUN mkdir /canal && tar xvzf canal.deployer-1.0.26-SNAPSHOT.tar.gz -C /canal
COPY entrypoint.sh /canal/bin
RUN chmod +x /canal/bin/entrypoint.sh

WORKDIR /canal

ENTRYPOINT ["bin/entrypoint.sh"]
CMD ["dev"]