# MODO DE USO 
- Todo en mayúsculas 
- Acaba la instrucción con ";" 
- El puerto de MySQL es 3306 
- Para usar SELECT tienes que poner las columnas que quieres, FROM de una tabla, para saber tablas show tables. 
 
# COMANDOS 
 
## Para acceder: 
- En Ubuntu: sudo mysql 
- En Windows: mysql -u root –p 
 
 
## Para crear un nuevo usuario con permisos: 
### - Crear usuario: 
CREATE USER 'julia'@'localhost' IDENTIFIED BY  'contraseña'; 
 
### - Dar privilegios a una base de datos: 
GRANT ALL PRIVILEGES ON tienda.* TO 'julia'@'localhost'; 
 
### - Dar acceso a todas las bases de datos: 
GRANT ALL PRIVILEGES ON *.* TO 'julia'@'localhost' WITH GRANT OPTION; 
 
### - Aplicar cambios: 
FLUSH PRIVILEGES; 
 
### - Ver que usuario estás usando:
SELECT USER(); 

 
 
# BASES DE DATOS
 
## Para crear: 
CREATE DATABASE instituto; 
 
## Para mostrar: 
SHOW DATABASES; 

## Ver registros: 
SELECT Host, User FROM mysql.user; 
 
## Para cambiar de base de datos: 
USE instituto; 

 
 
# TABLAS
## Tipos de datos: 
- Longitud fija: char 
- Límite caracteres: varchar 
- Números: int 
- Texto: TEXT 
- Fechas: DATE (YYYY-MM-DD) 
- Hora: TIME 
- Fecha y hora: DATETIME 
- Como "datetime" pero agregando zona horaria: TIMESTAMP 
- Año de 4 dígitos: YEAR 
 
 
## Para crear tabla: 
CREATE TABLE alumnos (Poner los datos); 

## Para mostrar tablas: 
SHOW TABLES; 

## Describe toda la tabla db: 
DESCRIBE db; 
 
 
# CAMPOS
## Ver campos: 
DESCRIBE alumnos; 

## Actualizar valores: 
UPDATE productos SET stock = 8 WHERE nombre = 'Portátil'; 

## Consultar: 
SELECT * FROM productos; 

## Eliminar registros: 
DELETE FROM productos WHERE stock = 0;