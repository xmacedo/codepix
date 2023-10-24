# codepix - Imersão Full Stack && Full Cycle

## Microsserviço CodePix

Esse microsserviço tem o objetivo de ser um hub de transações entre os bancos que simularemos durante o projeto.

## Como executar

Utilizamos Docker para que todos os serviços que utilizaremos fiquem disponíveis.

- Faça o clone do projeto
- Tendo o docker instalado em sua máquina apenas execute:
  `docker-compose up -d`

### Como executar a aplicação

- Acesse o container da aplicação executando: `docker exec -it codepix_app bash`
- Rode `go run cmd/codepix/main.go`

**Importante:** Esse código está sendo disponibilizado conforme o andamento das aulas, logo, o arquivo para executar o projeto talvez ainda não tenha sido criado.

### Serviços utilizados ao executar o docker-compose

- Aplicação principal
- Postgres
- PgAdmin
- Apache Kafka
- Criador dos tópicos a serem utilizados pelo Kafka
- Confluent control center
- ZooKeeper

---

### Comandos para o Docker

#### Sobe os container

`docker-compose up -d`

#### ver os containers que estao funcionando

`docker-compose ps`

#### acessar o container nome: codeflix_app_1

`docker exec -it codeflix-app-1 bash`

---

### comandos para o GO

#### instalar gRPC go

https://grpc.io/docs/languages/go/quickstart/

#### iniciar go

`go mod init github.com/xmacedo/devfullcycle/codepix-go`

#### fazer o download das dependencias necessárias

`go mod tidy`

---

### Comandos para o ProtoBuff

#### Gerar os arquivos proto

`protoc --go_out=application/grpc/pb --go_opt=paths=source_relative --go-grpc_out=application/grpc/pb --go-grpc_opt=paths=source_relative --proto_path=application/grpc/protofiles application/grpc/protofiles/*.proto`
