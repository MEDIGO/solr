FROM java:7

ENV SOLR_VERSION 4.10.2

RUN curl -sSL http://www.eu.apache.org/dist/lucene/solr/$SOLR_VERSION/solr-$SOLR_VERSION.tgz \
        | tar -v -C /opt -xz

RUN cp -r /opt/solr-$SOLR_VERSION/example /opt/solr

WORKDIR /opt/solr
VOLUME /opt/solr/solr/core1/data
EXPOSE 8983

CMD ["java", "-jar", "start.jar"]
