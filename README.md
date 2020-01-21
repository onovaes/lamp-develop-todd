## LAMP para Desenvolvimento com Laravel 6.6 baseado no docker 

- Ubuntu 16 + APACHE 2.4 + PHP 7.2. + MYSQL 5.6.46 
- Composer version 1.9.1
- Laravel Framework 6.6.2
- Autor: Gabriel Novaes <gabriel@dothcom.net>

### Instalação
- <code>git clone git@github.com:onovaes/lamp7.2-laravel6.git</code>
- <code>cd lamp7.2-laravel6</code>
- <code>cp env-example .env</code>
- <code>docker-compose up</code>

## TO-DO
- senha esta saindo como 000
- APACHE_LOG_DIR
- meu host do mysql esta mysqlserver e deve ser myserver



### Informações Gerais

| CONTAINER NAME | HOST/PORT          | OBS                                                         |
| -------------- | ------------------ | ----------------------------------------------------------- |
| appserver      | localhost	      | Ubuntu 16.04.6 LTS - Apache 2.4.18 + PHP 7.2                |
| mysqldb        | mysqlserver:3306   | mysql 5.6.46                                                |
| phpmyadmin     | localhost:81       |                                                             |



## Comandos auxiliares

- Entrando no container (appserver) para comecar a programar
<code>docker exec -ti appserver bash</code>

