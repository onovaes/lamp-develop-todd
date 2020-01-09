## LAMP para Desenvolvimento com Laravel 6 baseado no docker 

- Ubuntu 16 + APACHE 2.4 + PHP 7.2. + MYSQL 5.6.46 
- Autor: Gabriel Novaes <gabriel@dothcom.net>

### Instalação
- $git clone git@github.com:onovaes/lamp5.6-varnish.git
- $cd lamp5.6-varnish
- $cp env-example .env
- $docker-compose up

### TODO'S
- SEM POR ENQUANTO

## Subindo os containers (START)
$git clone git@github.com:onovaes/lamp7.2-laravel6.git
$cd lamp7.2-laravel6
$cp env-example .env
$docker-compose up

### Informações Gerais

| CONTAINER NAME | HOST/PORT          | OBS                                                         |
| -------------- | ------------------ | ----------------------------------------------------------- |
| appserver      | localhost	      | Ubuntu 16.04.6 LTS - Apache 2.4.18 + PHP 7.2                |
| mysqldb        | mysqlserver:3306   | mysql 5.6.46                                                |
| phpmyadmin     | localhost:81       |                                                             |



## Comandos auxiliares

#Entrando no container (appserver) para comecar a programar
$docker exec -ti appserver bash


