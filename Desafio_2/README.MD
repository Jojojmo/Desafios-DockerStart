linha para gerar o build:

```bash
podman build -t jojojmo/custom-apache .
```


linha para montar o container:

```bash
podman run -d -p 20080:8080 --name meuapache jojojmo/custom-apache
```

acesso da imagem no docker hub:

```bash
https://hub.docker.com/repository/docker/jojojmo/custom-apache/general
```