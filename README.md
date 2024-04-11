# TallerBD
Consultas sobre una tabla
   SELECT
   FROM producto as p, fabricante as f
   WHERE
1. Lista el nombre de todos los productos que hay en la tabla producto.
   SELECT p.id, p.nombre
   FROM producto as p;
2. Lista los nombres y los precios de todos los productos de la tabla producto.
   SELECT p.id, p.nombre, p.precio
   FROM producto as p;
3. Lista todas las columnas de la tabla producto.
   SHOW COLUMNS
   FROM producto;
4. Lista el nombre de los productos, el precio en euros y el precio en dólares estadounidenses (USD).
   SELECT p.id, p.nombre, p.precio, p.precio/cambio_euros
   FROM producto as p, (SELECT 0.86 as cambio_euros) as conversion;
