![mysql](https://github.com/user-attachments/assets/0fbcb0a6-1d6d-4b9c-befd-8c1077c668ba)

### MySQL Command Line Client

1. Abrir terminal e ingresar contraseña:

   ![pass](https://github.com/user-attachments/assets/6dcd58dd-4bc8-4a4f-bbae-ead6158fd970)

2. Revisar BD creadas:

```
SHOW DATABASES;
```

3. Crear BD:

```
CREATE DATABASE nombreBD;
```

4. Utilizar BD:

```
USE nombreBD;
```

5. Crear Tabla:

   ```
   CREATE TABLE clientes(
    id INT(11) NOT NULL AUTO_INCREMENT,
    nombre VARCHAR(60) NOT NULL,
    apellido VARCHAR(60) NOT NULL,
    direccion VARCHAR(60),
    PRIMARY KEY (id)
    );
   ```
6. Mostrar campos de la Tabla:

```
DESCRIBE nombreTabla;
```
![describe](https://github.com/user-attachments/assets/270abf7d-5129-41c9-b0bb-d45c5b2e623f)

7. Agregar datos a la Tabla:

```
INSERT INTO clientes (nombre, apellido, direccion)
VALUES ('Juan', 'De la torre', 'Avenida Radiante 127001');
```

8. Ver todos los datos de la Tabla:

```
SELECT * FROM clientes;
```
![select](https://github.com/user-attachments/assets/6b398e11-9dfe-4935-a62f-653ae8b3722f)

9. Actualizar dato (Agregar ID específico):

```
UPDATE clientes SET nombre = 'Juan Pablo' WHERE id = númeroID;
```

10. Borrar dato:

```
DELETE FROM clientes WHERE id = 1;
```

11. Agregar nueva Columna a la tabla:

```
ALTER TABLE clientes ADD email VARCHAR(30);
```

12. Eliminar Columna de la tabla:

```
ALTER TABLE clientes DROP COLUMN email;
```

13. Ejemplo de Orden Descendente (Otra Tabla):

```
SELECT * FROM reservaciones ORDER BY fecha DESC;
```
![schema](https://github.com/user-attachments/assets/b3965876-a604-49b0-937d-2dddb3e990fc)

14. Agrupar elementos:

```
SELECT COUNT(id), fecha FROM reservaciones GROUP BY fecha ORDER BY COUNT(id) DESC;
```

15. Unir Tablas:

```
SELECT * FROM platillos INNER JOIN categoria ON categoria.id = platillos.categoriaId;
```

16. Contar Tablas unidas:
    
```
SELECT COUNT(platillos.id), categoria.nombre
FROM platillos INNER JOIN categoria ON platillos.categoriaId = categoria.id
GROUP BY categoria.nombre;
```

17. Mostrar valores no duplicados:

```
SELECT DISTINCT precio FROM platillos;
```

18. Aplicar Rango:

```
SELECT * FROM platillos WHERE precio BETWEEN 100 AND 200;
```
    
19. Busqueda especifica:

```
SELECT * FROM platillos WHERE nombre LIKE '%Cafe%';
```

20. Concatenar columnas y Alias:

```
SELECT  CONCAT(nombre, ' ', apellido) AS 'Nombre Completo', hora, fecha, cantidadMesa FROM reservaciones WHERE CONCAT(nombre, ' ', apellido) LIKE '%Ana Preciado%';
```

21. Revisar múltiples condiciones:

```
SELECT * FROM reservaciones WHERE fecha = '2019-07-02' AND cantidadmesa IN (2, 3)
```











    
















