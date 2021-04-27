# Desafio 1 Programa FullCycle de Aceleração Docker

* Utilizar containers docker para backend Node.js, banco de dados MySql e NginX
* Utilizar o EnginX como proxy reverso para acessar o backend e retornar uma lista
  contendo alguns módulos do curso FullCycle
* Visualizar a resposta da requisição através do endereço http://localhost:8080

## Instruções para rodar a aplicação:

* docker network create pfa-net

* docker run -d --name=pfa-mysql --network=pfa-net -e  MYSQL_ALLOW_EMPTY_PASSWORD=1 felipediasdev/pfa-mysql

* docker run -d --name=pfa-node --network=pfa-net felipediasdev/pfa-node

* docker run -d --name=pfa-nginx --network=pfa-net -p 8080:80 felipediasdev/pfa-nginx

* Acessar o navegador no endereço http://localhost:8080