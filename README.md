# desafioDocker01
Desafio 1 curso docker DevopsPro 

Comando para rodar o container
docker run -d \
  --name curso_postgres \
  -e POSTGRES_DB=curso_docker \
  -e POSTGRES_USER=docker_usr \
  -e POSTGRES_PASSWORD=docker_pwd \
  -p 5432:5432 \
  postgres:15

Ou rodando com Docker compose
criar arquivo compose.yml

services:
  postgres:
    image: postgres:15
    container_name: curso_postgres
    environment:
      POSTGRES_DB: curso_docker
      POSTGRES_USER: docker_usr
      POSTGRES_PASSWORD: docker_pwd
    ports:
      - "5432:5432"

E rodar com o comando 
docker compose up -d
  
