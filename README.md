### MySQL Command Line Client

1. Abrir terminal

2. Ingresar contraseña

3. Revisar BD creadas:

```
SHOW DATABASES;
```

4. Crear BD:

```
CREATE DATABASE nombreBD;
```

6. Utilizar BD:

```
USE nombreBD;
```

7. Crear Tabla:

   ```
   CREATE TABLE clientes(
    id INT(11) NOT NULL AUTO_INCREMENT,
    nombre VARCHAR(60) NOT NULL,
    apellido VARCHAR(60) NOT NULL,
    direccion VARCHAR(60),
    PRIMARY KEY (id)
    );
   ```
8. Mostrar campos de la Tabla:

```
DESCRIBE nombreTabla;
```

9. Agregar datos a la Tabla:

```
INSERT INTO clientes (nombre, apellido, direccion)
VALUES ('Juan', 'De la torre', 'Avenida Radiante 127001');
```

11. Ver todos los datos de la Tabla:

```
SELECT * FROM clientes;
```

12. Actualizar dato:

```
UPDATE clientes SET nombre = 'Juan Pablo' WHERE id = 1;
```

14. Borrar dato:

```
DELETE FROM clientes WHERE id = 1;
```

16. 

17. 








