1. Realice la inserción de los siguientes datos.

   **FABRICANTE:**

   ```sql
   INSERT INTO fabricante VALUES (1, 'Asus'), (2, 'Lenovo'), (3, 'Hewlett-Packard'), (4, 'Samsung'), (5, 'Seagate'), (6, 'Crucial'), (7, 'Gigabyte'), (8, 'Huawei'), (9, 'Xiaomi');
   ```

   **PRODUCTOS:**

   ```sql
   INSERT INTO producto VALUES (1, 'Disco duro SATA3 1TB', 86.99,), (2, 'Memoria RAM DDR4 8GB', 120, 6), (3, 'DISCO SSD 1TB', 150.99, 4), (4, 'GeForce GTX 1050Ti', 185, 7), (5, 'GeForce GTX 180 Xtreme', 755, 6), (6, 'Monitor 24 LED Full HD', 202, 1), (7, 'Monitor 27 LED Full HD', 245.99, 1), (8, 'Portatil Yoga 520', 559, 2), (9, 'Portatil IdeaPad 320', 444, 2), (10, 'Impresora HP DeskJet 3720', 59.99, 3), (11, 'Impresora HP LaserJet Pro M26nw', 180, 3);
   ```

**Consultas sobre una tabla** SELECT FROM producto as p, fabricante as f WHERE

1. Lista el nombre de todos los productos que hay en la tabla producto. 

   ```sql
   SELECT p.nombre 
   FROM producto as p;
   ```

2. Lista los nombres y los precios de todos los productos de la tabla producto. 

   ```sql
   SELECT nombre, precio 
   FROM producto;
   ```

3. Lista todas las columnas de la tabla producto.

   ```sql
   SELECT id, nombre, precio, codigo_fabricante 
   FROM producto;
   ```

4. Lista el nombre de los productos, el precio en euros y el precio en dólares estadounidenses (USD).

   ```sql
   SELECT nombre, precio, precio/0.94
   FROM producto;
   ```

5. Lista el nombre de los productos, el precio en euros y el precio en dólares estadounidenses (USD). Utiliza los siguientes alias para las columnas: nombre de producto, euros, dólares.

   ```sql
   SELECT nombre as nombre_de_producto, precio as dolares, precio/0.94 as euros
   FROM producto;
   ```

6. Lista los nombres y los precios de todos los productos de la tabla producto,
   convirtiendo los nombres a mayúscula.

   ```sql
   SELECT UPPER(nombre), precio 
   FROM producto;
   ```

7. Lista los nombres y los precios de todos los productos de la tabla producto,
   convirtiendo los nombres a minúscula.

   ```sql
   SELECT LOWER(nombre), precio 
   FROM producto;
   ```

8. Lista el nombre de todos los fabricantes en una columna, y en otra columna
   obtenga en mayúsculas los dos primeros caracteres del nombre del
   fabricante.

   ```sql
   SELECT nombre, UPPER(LEFT(nombre, 2)),precio 
   FROM fabricante;
   ```

9. Lista los nombres y los precios de todos los productos de la tabla producto, redondeando el valor del precio.

   ```sql
   SELECT nombre, ROUND(precio) 
   FROM producto ;
   ```

10. Lista los nombres y los precios de todos los productos de la tabla producto, truncando el valor del precio para mostrarlo sin ninguna cifra decimal.

    ```sql
    SELECT nombre, TRUNCATE(precio,0) 
    FROM producto ;
    ```

11. Lista el identificador de los fabricantes que tienen productos en la tabla producto.

    ```sql
    SELECT codigo_fabricante
    FROM producto;
    ```

12. Lista el identificador de los fabricantes que tienen productos en la
    tabla producto, eliminando los identificadores que aparecen repetidos.

    ```sql
    SELECT DISTINCT codigo_fabricante
    FROM producto;
    ```

13. Lista los nombres de los fabricantes ordenados de forma ascendente.

    ```sql
    SELECT nombre
    FROM fabricante
    ORDER BY nombre ASC
    ```

14. Lista los nombres de los fabricantes ordenados de forma descendente.

    ```sql
    SELECT nombre
    FROM fabricante
    ORDER BY nombre DESC
    ```

15. Lista los nombres de los productos ordenados en primer lugar por el
    nombre de forma ascendente y en segundo lugar por el precio de forma
    descendente.

    ```sql
    SELECT nombre, precio
    FROM producto
    ORDER BY nombre ASC, precio DESC
    ```

16. Devuelve una lista con las 5 primeras filas de la tabla fabricante.

    ```sql
    SELECT *
    FROM fabricante LIMIT 0, 5
    ```

17. Devuelve una lista con 2 filas a partir de la cuarta fila de la tabla fabricante.
    La cuarta fila también se debe incluir en la respuesta.

    ```sql
    SELECT *
    FROM fabricante LIMIT 4, 6
    ```

18. Lista el nombre y el precio del producto más barato. (Utilice solamente las
    cláusulas ORDER BY y LIMIT)

    ```sql
    SELECT nombre, precio
    FROM producto LIMIT 0, 1
    ORDER BY precio ASC
    ```

19. Lista el nombre y el precio del producto más caro. (Utilice solamente las
    cláusulas ORDER BY y LIMIT)

    ```sql
    SELECT nombre, precio
    FROM producto LIMIT 0, 1
    ORDER BY precio DESC
    ```

20. Lista el nombre de todos los productos del fabricante cuyo identificador de
    fabricante es igual a 2.

21. Lista el nombre de los productos que tienen un precio menor o igual a 120€.

22. Lista el nombre de los productos que tienen un precio mayor o igual a 400€.

23. Lista el nombre de los productos que no tienen un precio mayor o igual a
    400€.

24. Lista todos los productos que tengan un precio entre 80€ y 300€. Sin utilizar
    el operador BETWEEN.

25. Lista todos los productos que tengan un precio entre 60€ y 200€. Utilizando
    el operador BETWEEN.

26. Lista todos los productos que tengan un precio mayor que 200€ y que el
    identificador de fabricante sea igual a 6.

27. Lista todos los productos donde el identificador de fabricante sea 1, 3 o 5.
    Sin utilizar el operador IN.

28. Lista todos los productos donde el identificador de fabricante sea 1, 3 o 5.
    Utilizando el operador IN.

29. Lista el nombre y el precio de los productos en céntimos (Habrá que
    multiplicar por 100 el valor del precio). Cree un alias para la columna que
    contiene el precio que se llame céntimos.

30. Lista los nombres de los fabricantes cuyo nombre empiece por la letra S.

31. Lista los nombres de los fabricantes cuyo nombre termine por la vocal e.

32. Lista los nombres de los fabricantes cuyo nombre contenga el carácter w.

33. Lista los nombres de los fabricantes cuyo nombre sea de 4 caracteres.

34. Devuelve una lista con el nombre de todos los productos que contienen la
    cadena Portátil en el nombre.

35. Devuelve una lista con el nombre de todos los productos que contienen la
    cadena Monitor en el nombre y tienen un precio inferior a 215 €.

36. Lista el nombre y el precio de todos los productos que tengan un precio
    mayor o igual a 180€. Ordene el resultado en primer lugar por el precio (en
    orden descendente) y en segundo lugar por el nombre (en orden
    ascendente).
