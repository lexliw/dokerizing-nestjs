# dokerizing-nestjs
Exemplo de como dockerizar uma app node feito em nestjs

##criar os arquivos abaixo conforme exemplo:
.dockerignore
Dockerfile

##depois executar no terminal:

###Criar imagem
$ sudo docker build -t alex/apptest .

###Subir imagem
$ sudo docker run -p3001:3000 -d alex/apptest

###Verificar se imagem subiu legal
$ sudo docker logs 0ab506426a8d

###testar conexão
$ sudo curl -i localhost:3001

###Resultado esperado
HTTP/1.1 200 OK
X-Powered-By: Express
Content-Type: text/html; charset=utf-8
Content-Length: 12
ETag: W/"c-Lve95gjOVATpfV8EL5X4nxwjKHE"
Date: Wed, 22 May 2019 14:19:07 GMT
Connection: keep-alive
