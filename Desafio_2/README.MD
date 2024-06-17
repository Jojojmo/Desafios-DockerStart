linha para gerar o build:

```bash
podman build -t joao-matheus/custom-apache .
```


linha para montar o container:

```bash
podman run -d -p 20080:8080 --name meuapache joao-matheus/custom-apache
```