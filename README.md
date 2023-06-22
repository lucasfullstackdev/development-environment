<p align="center"><img src="https://www.docker.com/wp-content/uploads/2021/09/Moby-share-480x356.png.webp" width="400"></p>

<p align="center">
<a href="https://travis-ci.org/laravel/framework"><img src="https://travis-ci.org/laravel/framework.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://poser.pugx.org/laravel/framework/d/total.svg" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://poser.pugx.org/laravel/framework/v/stable.svg" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://poser.pugx.org/laravel/framework/license.svg" alt="License"></a>
</p>

<br><br><br>

<h1 align="center">Ambiente de desenvolvimento</h1>
<h4 align="center">Tenha múltiplos projetos rodando no mesmo ambiente de forma simplificada</h4>

## Sobre o projeto
Este projeto tem ocmo finalidade atestar meus conhecimentos em [docker](https://www.docker.com/) utilizando [docker compose](https://docs.docker.com/compose/), englobando o uso de [Dockerfile](https://docs.docker.com/engine/reference/builder/) e automação com [script bash](https://www.freecodecamp.org/news/bash-scripting-tutorial-linux-shell-script-and-command-line-for-beginners/)

Utilizando este repositório você deve conseguir rodas aplicações [PHP](https://www.php.net/) na versão [8.2](https://www.php.net/releases/8.2/pt_BR.php) e aplicações [node](https://nodejs.org/en) na versão [19](https://nodejs.org/en/blog/announcements/v19-release-announce)

## Estrutura do ambiente
|------ development-environment

|-------------/projetos

|-------------/projetos/sua-api-1

|-------------/projetos/sua-api-2

|-------------/projetos/seu-front-1

|-------------/projetos/seu-front-2

Dentro do diretório **projetos** você consegue colocar quantos repositórios você quiser, pois o controle de qual projeto será executado por vez fica sob responsabilidade do arquivo [**.env.setup**](https://github.com/lucasfullstackdev/development-environment/blob/main/.env.setup)

```bash

### API
API_DIRECTORY='diretório em que sua api se encontra'
API_CONTAINER_NAME='nome do container que será criado para a api'
API_EXTERNAL_PORT='porta que servirá sua api'
API_LOCAL_ENV='.env'

### DATABASE
DB_CONTAINER_NAME='nome do container que será criado para o banco de dados'
DB_EXTERNAL_PORT='porta que servirá seu banco de dados'
DB_PASSWORD=root
DB_NAME='nome do banco de dados que será criado'

### FRONT
FRONT_DIRECTORY='diretório em que seu front se encontra'
FRONT_CONTAINER_NAME='nome do container que será criado para o front'
FRONT_EXTERNAL_PORT='porta que servirá seu front'
FRONT_LOCAL_ENV='.env'
```

## Por que este projeto?
Este projeto faz parte do meu portfólio pessoal, uma maneira de comprovar meus conhecimentos em docker e é utilizado para facilitar e agilizar minha rotina de trabalho

## Pré-requisitos
Você precisa ter o docker instalado em seu computador

## Setup
Para a configuração do projeto no seu ambiente local, algumas etapas precisam ser seguidas:

1. Clone o repositório
2. Clone os projetos desejados dentro do diretório [**projetos**](https://github.com/lucasfullstackdev/development-environment/tree/main/projetos)
3. Configura o arquivo [**.env.setup**](https://github.com/lucasfullstackdev/development-environment/blob/main/.env.setup) para apontar para os projetos que deseja utilizar
4. Na raiz do ambiente de desenvolvimento execute o script bash [**setup.sh**](https://github.com/lucasfullstackdev/development-environment/blob/main/setup.sh) para que os containers sejam criados e que os projetos sejam servidos, com o seguinte comando:
```bash
bash setup.sh
```

## Considerações finais
- Este projeto não representa uma amostra real, devendo ser utilizada apenas para se ter uma noção sobre como funciona o docker
- Qualquer dúvida ou sugestão, entre em contato pelo e-mail: lucas.fullstack.dev@gmail.com
