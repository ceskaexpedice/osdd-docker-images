FROM solr:9.1.1

USER root
COPY lib/* /opt/solr/server/solr/lib/
ADD search /search
ADD logs /logs
ADD processing /processing
ADD oai/ /opt/solr/server/solr/oai

RUN chown -R $SOLR_USER:$SOLR_USER /search
RUN chown -R $SOLR_USER:$SOLR_USER /logs
RUN chown -R $SOLR_USER:$SOLR_USER /processing
USER $SOLR_USER

#CMD solr-precreate logs /logs; precreate-core  search /search; precreate-core  processing /processing
