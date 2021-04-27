# <p align="center">Fullcyle :rocket:  </p>

<h1 align="center">
    <img alt="FullCycle" src="./public/assets/logo.png" width="231px" /><br>
    <b>FullCycle PFA</b> 💈
</h1>


### Challenge :triangular_flag_on_post:

- Crie um programa utilizando sua linguagem de programação favorita que faça uma listagem simples do nome de alguns módulos do curso Full Cycle os trazendo de um banco de dados MySQL. Gere a imagem desse container e a publique no DockerHub.
- Gere uma imagem do nginx que seja capaz que receber as solicitações http e encaminhá-las para o container.
- Crie um repositório no github com todo o fonte do programa e das imagens geradas.
- Crie um arquivo README.md especificando quais comandos precisamos executar para que a aplicação funcione recebendo as solicitações na porta 8080 de nosso computador. Lembrando que NÃO utilizaremos Docker-compose nesse desafio.

## :bulb: Recursos

-   [Docker](https://www.docker.com/)
-   [Node.js](https://nodejs.org/en/)
-   [Nginx](https://www.nginx.com/)
-   [MySQL](https://www.mysql.com/)
-   [Node MySQL2](https://www.npmjs.com/package/mysql2)





### Crie a sua rede no DOcker

```sh
docker network create pfa-network
```

## :pushpin: Rodando o Docker 


```sh
docker run --rm -d --network pfa-network --name pfa-mysql desiderios/pfa-mysql
```

```sh
docker run --rm -d --network pfa-network --name pfa-node desiderios/pfa-node
```

```sh
docker run --rm -d --network pfa-network -p 8080:80 --name pfa-nginx desiderios/pfa-nginx
```

Access http://localhost:8080/



