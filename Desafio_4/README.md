Primeiramente acesse a pasta app e monte a imgem com a linha de comando:

```bash
podman build -t python-redis
```

Depois volte para a pasta do desafio quatro e suba o compose com:

```bash
podman compose up
```

Use esse endereço de IP para ver a aplicação:

http://127.0.0.1:8000/

Para finalizar o compose, saia do modo com Ctrl+C (caso não esteja no modo de background) e utlize a linha de comando:

```bash
podman compose down
```