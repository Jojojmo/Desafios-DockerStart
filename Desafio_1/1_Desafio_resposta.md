# Exercicios

### 1 Execute um container baseado nas informações abaixo:


Baixando a imagem httpd-basic tag 2.4

```bash
podman pull quay.io/redhattraining/httpd-parent:2.4
```

Vizualizando as imagens existentes

```bash
podman images
```

Definindo um container com a imagem baixada, em modo background e bind de portas 8080 da maquina para 80 do servidor

```bash
podman run -d -p 8080:80 --name httpd-basic quay.io/redhattraining/httpd-parent:2.4
```

listando os containers ativos

```bash
podman container ls
```

Resultado:

![imagem mensagem padrão httpd-parent](printScreen/httpd-parent-mensagem-padrao.png)

### 2 Customize a mensagem apresentada em seu navegador quando é acessado o endereço http://localhost:8080.

Entrando no modo interativo do container

```bash
podman container exec -it httpd-basic sh
```

Acessando o diretório `/var/www/html`

```bash
cd /var/www/html
```

Sobreescrevendo o arquivo com o comabdo `echo`

```bash
echo 'Ola mundo!' > index.html
```

Verificando a alteração

```bash
cat index.html
```

para sair do modo interativo: `Ctrl + P` e `Ctrl + Q`

Resultado:

![imagem mensagem 'ola mundo' httpd-parent](printScreen/httpd-parent-mensagem-ola-mundo.png)


### 3 Pare o container que esta sendo executado.

```bash
podman stop httpd-basic
```