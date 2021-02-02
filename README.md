<p align="center">
    <img src="https://events-fullcycle.s3.amazonaws.com/events-fullcycle/static/site/img/grupo_4417.png" />
</p>

# Aulas Imersão FullStack FullCycle

## Aula 1

### Tenha um dos perfis mais desejados do mercado

```shell
mkdir -p ~/projects/imersao-fsfc/codepix
curl -fs https://raw.githubusercontent.com/codeedu/imersao-fullstack-fullcycle/main/codepix/Dockerfile -o ~/projects/imersao-fsfc/codepix/Dockerfile
curl -fs https://raw.githubusercontent.com/codeedu/imersao-fullstack-fullcycle/main/codepix/docker-compose.yaml -o ~/projects/imersao-fsfc/codepix/docker-compose.yaml
curl -fs https://raw.githubusercontent.com/codeedu/imersao-fullstack-fullcycle/main/codepix/.gitignore -o ~/projects/imersao-fsfc/codepix/.gitignore
code ~/projects/imersao-fsfc/codepix
```

```terminal
docker-compose up -d
docker-compose ps -a
docker exec -it codepix_app_1 bash
go mod init github.com/afpfullcycle/imersao-fullstack-fullcycle/codepix-go
mkdir -p ./domain/model
touch ./domain/model/{account,bank,base,pixKey,transaction}.go
```

- bank.go
    - Imported govalidater, go.uuid and time
    - Created struct Bank
    - Created method isValid
    - Created function NewBank

- base.go
    - Imported govalidater and time
    - Created struct Base
    - Created function init govalidator

- account.go
    - Imported govalidater, go.uuid and time
    - Created struct Account
    - Created method isValid
    - Created function NewAccount

- pixKey.go
    - Imported errors, govalidator, go.uuid and time
    - Created interface PixKeyRepositoryInterface
    - Created struct PixKey
    - Created method isValid
    - Created function NewPixKey

- transaction.go
    - Imported errors, govalidator, go.uuid and time
    - Created status constants
    - Created interface TransactionRepositoryInterface
    - Created struct Transactions and Transaction
    - Created method isValid
    - Created function NewTransaction
    - Created methods Complete, Confirm and Cancel


```terminal
git config --global user.email "user@email.com"
git config --global user.name "Name"
git init
git add .
git commit -m "Codepix: Aula 1"
git branch -M main
git remote add origin https://github.com/afpfullcycle/imersao-fullstack-fullcycle.git
git push -u origin main
git branch aula1
git checkout aula1
git add .
git commit -m "Started docker environment"
git push -u origin aula1
```
