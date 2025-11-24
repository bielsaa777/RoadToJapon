# MODO DE USO
- Todo en mayúsculas
- Acaba la instrucción con ";"
- El puerto de MySQL es 3306

# COMANDOS
## Para acceder:
mysql -u root -p

## Cear un nuevo usuario con permisos:
### - Crear usuario 
CREATE USER 'user'@'localhost' IDENTIFIED BY 'contraseña';

### - Dar privilegios a una base de datos:
GRANT ALL PRIVILEGES ON ejemplo.* TO 'user'@'localhost';

### - Dar acceso a todas las bases de datos:
GRANT ALL PRIVILEGES ON *.* TO 'user'@'localhost' WITH GRANT OPTION;

### - Aplicar cambios:
FLUSH PRIVILEGES;

