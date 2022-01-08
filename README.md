# Sql server 2017

Neste container contém o sql server 2017 para desenvolvimento local.

## Antes de começar

Para rodar o container é necessário criar o arquivo `.env` a partir do `.env.modelo` e substituir as variáveis abaixo:

* `%APP_NAME%`: Nome do container
* `%APP_DB_SA_PASS%`: Senha do usuário **sa**
* `%APP_DB_PORT%`: Porta exposta pelo container
* `%APP_MEMORY_MAX_LIMIT%`: Limita a quantidade máxima que pode ser utilizada (Em mb)

## Desenvolvimento

Siga os passos abaixo para criar login e database para usar no projeto:

```sql
CREATE LOGIN <usuario> WITH password='<senha>';
CREATE USER <usuario> FROM LOGIN <usuario>;
CREATE DATABASE <base_name>;

use <base_name>;
CREATE USER <usuario> FOR LOGIN <usuario>;
EXEC sp_addrolemember 'db_owner', '<usuario>';
```

> A senha deve ter no mínimo 8 caracteres, sendo 1 deles maiusculo/minusculo e caracter especial