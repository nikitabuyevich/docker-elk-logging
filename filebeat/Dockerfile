FROM docker.elastic.co/beats/filebeat-oss:7.6.2
USER root
# Create a directory to map volume with all docker log files
RUN mkdir /usr/share/filebeat/docker-logs
RUN chown -R root /usr/share/filebeat/
RUN chmod -R go-w /usr/share/filebeat/
