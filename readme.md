# Super Simple vsftp

```
docker build -t ftp .
docker run -d --net=host -v /host/path:/ftp --name ftp ftp
docker logs ftp # to see user/pass
# alternately
docker run -d --net=host -e USER=luggage -e PASSWORD=12345 -v /host/path:/ftp --name ftp ftp
```

The `--net=host` flag is needed or you'll have to do a bucket of port mapping. Your call.

This was lifted from https://github.com/mikz/dockerfiles/tree/master/vsftpd
