FROM debian:jessie

MAINTAINER Andrea Usuelli <andreausu@gmail.com>

RUN apt-get update && \
    apt-get install -y wget && \
    wget https://github.com/sysown/proxysql/releases/download/v1.2.0k/proxysql_1.2.0-debian8_amd64.deb -O /opt/proxysql_1.2.0-debian8_amd64.deb && \
    dpkg -i /opt/proxysql_1.2.0-debian8_amd64.deb && \
    rm -f /opt/proxysql_1.2.0-debian8_amd64.deb && \
    rm -rf /var/lib/apt/lists/*

ENTRYPOINT ["proxysql", "-f"]
