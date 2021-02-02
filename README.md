![Imersão-FSFC](https://events-fullcycle.s3.amazonaws.com/events-fullcycle/static/site/img/grupo_4417.png#center)

# Desafios Imersão FullStack FullCycle

## Desafio 1

### Started docker environment

```shell
mkdir -p ~/projects/imersao-fsfc/desafio1
curl -fs https://raw.githubusercontent.com/codeedu/imersao-fullstack-fullcycle/main/codepix/Dockerfile -o ~/projects/imersao-fsfc/desafio1/Dockerfile
curl -fs https://raw.githubusercontent.com/codeedu/imersao-fullstack-fullcycle/main/codepix/docker-compose.yaml -o ~/projects/imersao-fsfc/desafio1/docker-compose.yaml
curl -fs https://raw.githubusercontent.com/codeedu/imersao-fullstack-fullcycle/main/codepix/.gitignore -o ~/projects/imersao-fsfc/desafio1/.gitignore
code ~/projects/imersao-fsfc/desafio1
```

```terminal
docker-compose up -d
docker-compose ps -a
docker exec -it desafio1_app_1 bash
git config --global user.email "user@email.com"
git config --global user.name "Name"
git init
git add .
git commit -m "Started docker environment"
git branch -M main
git remote add origin https://github.com/afpfullcycle/imersao-fullstack-fullcycle.git
git push -u origin main
git branch desafio1
git checkout desafio1
git add .
git commit -m "Started docker environment"
git push -u origin desafio1
```

### Started code

```terminal
go mod init github.com/afpfullcycle/imersao-fullstack-fullcycle/desafio1-go
mkdir -p ./domain/model
touch ./domain/model/user.go
```

- user.go
    - Created struct user
    - Created function NewUser
    - Created method isValid
    - Created function init govalidator
    - Imported govalidater and go.uuid
