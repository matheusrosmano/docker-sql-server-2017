# Sql server 2017

Neste container contém o sql server 2017 para desenvolvimento local.

## Antes de começar

Para rodar o container é necessário criar o arquivo `.env` a partir do `.env.modelo` e substituir as variáveis abaixo:

* `%APP_NAME%`: Nome do container
* `%APP_DB_SA_PASS%`: Senha do usuário **sa**
* `%APP_DB_PORT%`: Porta exposta pelo container
* `%APP_MEMORY_MAX_LIMIT%`: Limita a quantidade máxima que pode ser utilizada (Em mb)