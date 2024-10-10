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

12. Actualizar dato (Agregar ID específico):

```
UPDATE clientes SET nombre = 'Juan Pablo' WHERE id = númeroID;
```

14. Borrar dato:

```
DELETE FROM clientes WHERE id = 1;
```

16. Agregar nueva Columna a la tabla:

```
ALTER TABLE clientes ADD email VARCHAR(30);
```

18. Eliminar Columna de la tabla:

```
ALTER TABLE clientes DROP COLUMN email;
```

19. Ejemplo de Orden Descendente (Otra Tabla):

```
SELECT * FROM reservaciones ORDER BY fecha DESC;
```

20. Agrupar elementos:

```
SELECT COUNT(id), fecha FROM reservaciones GROUP BY fecha ORDER BY COUNT(id) DESC;
```

21. Unir Tablas:

```
SELECT * FROM platillos INNER JOIN categoria ON categoria.id = platillos.categoriaId;
```

23. Contar Tablas unidas:
    
```
SELECT COUNT(platillos.id), categoria.nombre FROM platillos INNER JOIN categoria ON platillos.categoriaId = categoria.id GROUP BY categoria.nombre;
```

24. Mostrar valores no duplicados:

```
SELECT DISTINCT precio FROM platillos;
```

25. Aplicar Rango:

```
SELECT * FROM platillos WHERE precio BETWEEN 100 AND 200;
```
    
27. Busqueda especifica:

```
SELECT * FROM platillos WHERE nombre LIKE '%Cafe%';
```

29. Concatenar columnas y Alias:

```
SELECT  CONCAT(nombre, ' ', apellido) AS 'Nombre Completo', hora, fecha, cantidadMesa FROM reservaciones WHERE CONCAT(nombre, ' ', apellido) LIKE '%Ana Preciado%';
```

30. Revisar múltiples condiciones:

```
SELECT * FROM reservaciones WHERE fecha = '2019-07-02' AND cantidadmesa IN (2, 3)
```











    
















