#build off of w4sp base image
FROM w4sp/labs:base

RUN wget -qO - https://packages.elastic.co/GPG-KEY-elasticsearch | sudo apt-key add -
RUN echo "deb http://packages.elastic.co/elasticsearch/2.x/debian stable main" | sudo tee -a /etc/apt/sources.list.d/elasticsearch-2.x.list

RUN apt-get update -q
RUN dpkg -i elasticsearch-7.6.1.deb
RUN apt-get -y install default-jre-headless

ENV KIBANA_VERSION 4.4.1 

RUN cd /tmp && \
    mv /tmp/kibana-${KIBANA_VERSION}-linux-x64 /kibana

RUN echo 'network.host: 0.0.0.0' >> /etc/elasticsearch/elasticsearch.yml

#add supervisor conf to start kibana and es
ADD supervisor_elk.conf /etc/supervisor/conf.d/supervisor_elk.conf
