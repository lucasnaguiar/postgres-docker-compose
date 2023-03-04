
# PostgreSQL + PgAdmin4 

A simple docker compose file to use Postgres and PgAdmin4


## Como usar


Copie ou renomeie o arquivo .env.example para .env, depois defina suas variáveis locais dentro do arquivo renomeado. 

Feito isso, execute o comando que dará início a criação da network e dos containers: 

```bash
 docker compose up -d 
```
    
## Instruções para conexão à instância do PostgreSQL

Ao criar a conexão para acesso à instância do PostgreSQL, leve em conta as seguintes considerações utilizando os dados que você definiu no arquivo `.env`:
- Acesse o PgAdmin4 através do seu brownser, por padrão no endereço: http://localhost:7500.
- Faça login com o email e senha que você definiu e depois inicie o registro um novo servidor do PostgresSQL.
- Em "Host name/address", informar o nome do container que corresponde à instância do PostgreSQL (`postgres`).
- Em "Port", definir o valor `5432` (porta default de acesso ao container e disponível a partir da rede `postgres_network`). Não informar a porta em que o PostgreSQL foi mapeado no host.
- No atributo "Username", deverá ser informado o usuário default do PostgreSQL (`postgres`), bem como a senha correspondente em "Password" (senha que você definiu no arquivo de enviroment). 


#### Referências:

[PostgreSQL + pgAdmin 4 + Docker Compose: montando rapidamente um ambiente para uso](https://renatogroffe.medium.com/postgresql-pgadmin-4-docker-compose-montando-rapidamente-um-ambiente-para-uso-55a2ab230b89)

[PostgreSQL - Docker Hub](https://hub.docker.com/_/postgres/)

[pgAdmin 4 - Docker Hub](https://hub.docker.com/r/dpage/pgadmin4/)