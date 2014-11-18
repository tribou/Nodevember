FROM ubuntu:14.04
RUN apt-get update -y && apt-get install -y wget
RUN cd /opt && wget http://fastdl.mongodb.org/linux/mongodb-linux-x86_64-2.6.5.tgz
RUN cd /opt && tar -xvzf mongodb-linux-x86_64-2.6.5.tgz
ADD mongo.conf /opt/mongodb-linux-x86_64-2.6.5/mongo.conf
RUN mkdir -p /data/mongo
RUN mkdir -p /logs
EXPOSE 27017
CMD "cd /opt/mongodb-linux-x86_64-2.6.5 && ./bin/mongod -f mongo.conf"
