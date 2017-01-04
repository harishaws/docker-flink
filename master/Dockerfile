FROM bde2020/flink-base:1.1.4-hadoop2.7

MAINTAINER Gezim Sejdiu <g.sejdiu@gmail.com>

#config files (template)
#ADD /usr/local/flink/conf/flink-conf.yaml /usr/local/flink/conf/

COPY master.sh /
#RUN chmod +x /usr/local/flink/bin/jobmanager.sh
ENV FLINK_MASTER_LOG /usr/local/flink/log

RUN cd /user/local/flink
RUN wget https://s3-us-west-1.amazonaws.com/flinkjarfile/Docker_Swarm.jar


EXPOSE 6123 22 8080

CMD ["/bin/bash", "/master.sh"]
