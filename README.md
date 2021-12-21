# Usuário
## Criação de Usuário

``` SQL
CREATE USER 'user_name'@'host_name' IDENTIFIED BY 'user_pass';

# Exemplo I: 
CREATE USER 'user'@'localhost' IDENTIFIED BY 'pass';

# Exemplo II: '%' corresponde qualquer host_name
CREATE USER 'user'@'%' IDENTIFIED BY 'pass';
```

## Conceder Permissão
### Conceder Permissão TOTAL
``` SQL
GRANT ALL PRIVILEGES ON *.* TO 'user_name'@'host_name';
```

### Conceder Permissão SELECIONADA
``` SQL
GRANT permissionA, permissionB, permissionN ON db_name.table_name TO 'user_name'@'host_name';

# Exemplo I
GRANT INSERT, SELECT ON db_name.table_name TO 'user_name'@'host_name';
 
```

## Revogar Permissão
### Revogar TODAS as Permissão
``` SQL
REVOKE ALL PRIVILEGES, GRANT OPTION FROM'user_name'@'host_name';
```
### Revogar Permissão SELECIONADA
``` SQL
REVOKE SELECT, INSERT ON spring_mvc_db.* FROM 'user_name'@'host_name';
```

## Exibir as Permissões
``` SQL
SHOW GRANTS FOR 'user_name'@'host_name';
```

# Excluir Usuário
``` SQL
DROP USER 'user_name'@'host_name';
```