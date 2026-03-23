FROM confluentinc/cp-kafka-connect:7.8.0

ENV OPENSEARCH_CONNECTOR_VERSION=3.1.1

RUN mkdir -p /usr/share/confluent-hub-components/kafka-connect-opensearch && \
    curl -fsSL \
      https://github.com/Aiven-Open/opensearch-connector-for-apache-kafka/releases/download/v${OPENSEARCH_CONNECTOR_VERSION}/opensearch-connector-for-apache-kafka-${OPENSEARCH_CONNECTOR_VERSION}.tar \
    | tar -x -C /usr/share/confluent-hub-components/kafka-connect-opensearch --strip-components=1

ENV CONNECT_PLUGIN_PATH="/usr/share/java,/usr/share/confluent-hub-components"

EXPOSE 8083