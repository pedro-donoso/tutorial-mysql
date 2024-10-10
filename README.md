![mysql](https://github.com/user-attachments/assets/0fbcb0a6-1d6d-4b9c-befd-8c1077c668ba)

### MySQL Command Line Client

1. Abrir terminal

   ![pass](https://github.com/user-attachments/assets/6dcd58dd-4bc8-4a4f-bbae-ead6158fd970)

2. Ingresar contraseña

3. Revisar BD creadas:

```
SHOW DATABASES;
```

4. Crear BD:

```
CREATE DATABASE nombreBD;
```

5. Utilizar BD:

```
USE nombreBD;
```

6. Crear Tabla:

   ```
   CREATE TABLE clientes(
    id INT(11) NOT NULL AUTO_INCREMENT,
    nombre VARCHAR(60) NOT NULL,
    apellido VARCHAR(60) NOT NULL,
    direccion VARCHAR(60),
    PRIMARY KEY (id)
    );
   ```
7. Mostrar campos de la Tabla:

```
DESCRIBE nombreTabla;
```

8. Agregar datos a la Tabla:

```
INSERT INTO clientes (nombre, apellido, direccion)
VALUES ('Juan', 'De la torre', 'Avenida Radiante 127001');
```

9. Ver todos los datos de la Tabla:

```
SELECT * FROM clientes;
```

10. Actualizar dato (Agregar ID específico):

```
UPDATE clientes SET nombre = 'Juan Pablo' WHERE id = númeroID;
```

11. Borrar dato:

```
DELETE FROM clientes WHERE id = 1;
```

12. Agregar nueva Columna a la tabla:

```
ALTER TABLE clientes ADD email VARCHAR(30);
```

13. Eliminar Columna de la tabla:

```
ALTER TABLE clientes DROP COLUMN email;
```

14. Ejemplo de Orden Descendente (Otra Tabla):

```
SELECT * FROM reservaciones ORDER BY fecha DESC;
```

15. Agrupar elementos:

```
SELECT COUNT(id), fecha FROM reservaciones GROUP BY fecha ORDER BY COUNT(id) DESC;
```

16. Unir Tablas:

```
SELECT * FROM platillos INNER JOIN categoria ON categoria.id = platillos.categoriaId;
```

17. Contar Tablas unidas:
    
```
SELECT COUNT(platillos.id), categoria.nombre FROM platillos INNER JOIN categoria ON platillos.categoriaId = categoria.id GROUP BY categoria.nombre;
```

18. Mostrar valores no duplicados:

```
SELECT DISTINCT precio FROM platillos;
```

19. Aplicar Rango:

```
SELECT * FROM platillos WHERE precio BETWEEN 100 AND 200;
```
    
20. Busqueda especifica:

```
SELECT * FROM platillos WHERE nombre LIKE '%Cafe%';
```

21. Concatenar columnas y Alias:

```
SELECT  CONCAT(nombre, ' ', apellido) AS 'Nombre Completo', hora, fecha, cantidadMesa FROM reservaciones WHERE CONCAT(nombre, ' ', apellido) LIKE '%Ana Preciado%';
```

32. Revisar múltiples condiciones:

```
SELECT * FROM reservaciones WHERE fecha = '2019-07-02' AND cantidadmesa IN (2, 3)
```











    
















