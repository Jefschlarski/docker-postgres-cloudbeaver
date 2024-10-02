
# Projeto de Container com PostgreSQL e CloudBeaver

Autor: [Jeferson Schlarski](https://github.com/Jefschlarski)

Este projeto configura um ambiente de container Docker que inclui um banco de dados PostgreSQL e uma interface de administração via CloudBeaver.

## Configuração do Ambiente


O arquivo `.env` deve ser configurado com as seguintes variáveis de ambiente:

### Variáveis de Ambiente

env:

```bash
POSTGRES_USER=postgres
```
```bash
POSTGRES_PASSWORD=senha
```
```bash
POSTGRES_PORTS=5432:5432
```
```bash
CLOUDBEAVER__PORTS=8080:8978
```
### Descrição das Variáveis de Ambiente

-   `POSTGRES_USER`: Define o usuário padrão do PostgreSQL. No caso, está definido como `postgres`.
-   `POSTGRES_PASSWORD`: Define a senha do usuário PostgreSQL. Neste exemplo, a senha é `senha`.
-   `POSTGRES_PORTS`: Mapeamento de portas do PostgreSQL. A configuração `5432:5432` mapeia a porta `5432` do host para a porta `5432` do container.
-   `CLOUDBEAVER__PORTS`: Mapeamento de portas para o CloudBeaver. A configuração `8080:8978` mapeia a porta `8080` do host para a porta `8978` do container, onde o CloudBeaver estará acessível.

## Uso


### Clone do Repositório

Clone o repositório:

```bash
git clone https://github.com/Jefschlarski/docker-postgres-cloudbeaver.git
```
```bash
cd docker-postgres-cloudbeaver
```

### Configuração do Arquivo `.env`

Certifique-se de que o arquivo `.env` esteja configurado conforme mostrado acima.

### Subir os Containers

Suba os containers:

```bash
docker-compose up -d
```
### Acessar o CloudBeaver

Acesse o CloudBeaver: Abra o navegador e acesse `http://localhost:8080` para visualizar a interface do CloudBeaver.

### Conectar ao PostgreSQL

Conecte ao PostgreSQL:

-   Host: `postgres` (ou o nome do serviço Docker definido no `docker-compose.yml`)
-   Porta: `5432`
-   Usuário: `postgres`
-   Senha: `senha`

## Encerrando os Containers


Para encerrar e remover os containers, utilize:

```bash
docker-compose down
```
## Considerações Finais


Este setup oferece um ambiente de desenvolvimento rápido para trabalhar com PostgreSQL e gerenciar o banco de dados usando o CloudBeaver. Certifique-se de ajustar as configurações de acordo com suas necessidades específicas de projeto.


## Referencias

[DOCS DOCKER](https://docs.docker.com)

[POSTGRES DOCKER HUB](https://hub.docker.com/_/postgres)

[CLOUD BEAVER DOCKER HUB](https://hub.docker.com/r/dbeaver/cloudbeaver)

[CLOUD BEAVER GIT WIKI](https://github.com/dbeaver/cloudbeaver/wiki/Run-Docker-Container)
