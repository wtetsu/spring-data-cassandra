FROM adoptopenjdk/openjdk11:latest

RUN set -eux; \
	CASSANDRA_URL='https://www-us.apache.org/dist/cassandra/3.11.5/apache-cassandra-3.11.5-bin.tar.gz'; \
	curl -LfsSo /tmp/cassandra.tar.gz ${CASSANDRA_URL}; \
		mkdir -p /opt/cassandra; \
		cd /opt/cassandra; \
		tar -xf /tmp/cassandra.tar.gz --strip-components=1; \
		rm -rf /tmp/cassandra.tar.gz;

RUN set -eux; \
	BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u232b09.tar.gz'; \
	curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL}; \
		mkdir -p /opt/java/openjdk8; \
		cd /opt/java/openjdk8; \
		tar -xf /tmp/openjdk.tar.gz --strip-components=1; \
		rm -rf /tmp/openjdk.tar.gz;

ENV PATH="/opt/java/openjdk8/bin:$PATH"
