```
docker build -t dedewahyuh/simplego:1.0 .
docker run -d --name  simplego -p 8080:8080 dedewahyuh/simplego:1.0 /go/bin/simplego
``` 