linha para gerar o build:

```bash
podman build -t meu-apache:0.1 .
```
linha para montar o container:

```bash
podman run -d -p 80:8080 --name apache meu-apache:0,1
```