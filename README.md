# dokerizing-nestjs
Exemplo de como dockerizar uma app node feito em nestjs

## Criar os arquivos abaixo conforme exemplo:
```
.dockerignore
Dockerfile
```

## depois executar no terminal:

### Criar imagem
```bash
$ sudo docker build -t alex/apptest .
```
### Subir imagem
```bash
$ sudo docker run -p3001:3000 -d alex/apptest
```
### Verificar qual o id da imagem
```bash
$ sudo docker images
```
### Verificar se imagem subiu legal
```bash
$ sudo docker logs 0ab506426a8d
```
### Testar conexão
```bash
$ sudo curl -i localhost:3001
```
### Resultado esperado
```bash
HTTP/1.1 200 OK
X-Powered-By: Express
Content-Type: text/html; charset=utf-8
Content-Length: 12
ETag: W/"c-Lve95gjOVATpfV8EL5X4nxwjKHE"
Date: Wed, 22 May 2019 14:19:07 GMT
Connection: keep-alive
```
