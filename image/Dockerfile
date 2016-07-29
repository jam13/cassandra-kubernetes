FROM cassandra:3.7
MAINTAINER Jamie Neil <jamie.neil@healthforge.io>
ENV REFRESHED_AT 2016-07-29

RUN apt-get -qq update && \
    DEBIAN_FRONTEND=noninteractive apt-get -yq install dnsutils && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

COPY custom-entrypoint.sh /
ENTRYPOINT ["/custom-entrypoint.sh"]
CMD ["cassandra", "-f"]
