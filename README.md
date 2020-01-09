## LAMP para Desenvolvimento com Laravel 6 baseado no docker 

- Ubuntu 16 + APACHE 2.4 + PHP 7.2. + MYSQL 5.6.46 
- Autor: Gabriel Novaes <gabriel@dothcom.net>

### Instalação
- $git clone git@github.com:onovaes/lamp5.6-varnish.git
- $cd lamp5.6-varnish
- $cp env-example .env
- $docker-compose up

### TODO'S
- Finalizar configuração do Proxy (Load Balancer) e balancear carga entre os web servers



## Subindo os containers (START)
$git clone git@github.com:onovaes/lamp7.2-laravel6.git
$cd docker-laravel6
$docker-compose up





## Informações Gerais

### LOGS
- Os logs do apache estão configurados para serem gerados na pasta setada na configuração (.env ) APACHE_HOST_LOG_PATH


### Informações Gerais

| CONTAINER NAME | HOST/PORT          | OBS                                                         |
| -------------- | ------------------ | ----------------------------------------------------------- |
| phpserver      | localhost:8080     | Ubuntu 16.04.6 LTS - Apache 2.4.18 + PHP 5.6 (SEM VARNISH)  |
| mysqldb        | mysqlserver:3306   | mysql 5.6.46                                                |
| phpmyadmin     | localhost:81       |                                                             |







# Ambiente para laravel 6
# Autor Gabriel Novaes

- TODO - ALTERAR NOME CONTAINER MYSQL PARA NAO TROMPAR
- .env

CONTAINER 	PORT		OBS
mysqldb		3306 		- mysql 5.6.22
phpmyadmin	81 			- http://localhost:81
apache		80 			- http://localhost

## Subindo os containers (START)
$git clone git@bitbucket.org:onovaes/docker-laravel6.git
$cd docker-laravel6
$docker-compose up