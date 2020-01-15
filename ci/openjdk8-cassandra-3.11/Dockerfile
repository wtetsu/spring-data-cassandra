FROM adoptopenjdk/openjdk8:latest

RUN set -eux; \
	CASSANDRA_URL='https://www-us.apache.org/dist/cassandra/3.11.5/apache-cassandra-3.11.5-bin.tar.gz'; \
	curl -LfsSo /tmp/cassandra.tar.gz ${CASSANDRA_URL}; \
		mkdir -p /opt/cassandra; \
		cd /opt/cassandra; \
		tar -xf /tmp/cassandra.tar.gz --strip-components=1; \
		rm -rf /tmp/cassandra.tar.gz;

ENV MAX_HEAP_SIZE=1500M
ENV HEAP_NEWSIZE=300M
