# Docker ProxySQL image

## Supported tags and respective `Dockerfile` links

-	[`1.2.1`, `1.2`, `1`, `latest` (*Dockerfile*)](https://github.com/primait/docker-proxysql/blob/master/1.2/Dockerfile)

## Build and update process

This image is automatically built at every push of this repository and every time that the `debian:jessie` base image gets updated in order to ensure that bugfixes and security updates are immediately applied.

## Run

```
docker run -v /path/to/proxysql.cfg:/etc/proxysql.cfg prima/proxysql:1.2
```

Or, you can create your own derived image, with the configuration in the image itself.

```dockerfile
FROM prima/proxysql:1.2
COPY my-config/proxysql.cfg /etc/proxysql.cfg
```

## Configuration file

You can find some examples of the `proxysql.cfg` in the official repository: https://github.com/sysown/proxysql/blob/master/doc/configuration.md
