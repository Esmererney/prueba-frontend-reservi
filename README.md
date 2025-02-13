# Prueba Técnica - Desarrollador Front-End

Este repositorio contiene las soluciones a los problemas propuestos en la prueba técnica de desarrollador Front-End, que incluyen pruebas de PHP, SQL y Vue.js. A continuación, se detallan las instrucciones para ejecutar y probar las soluciones.

## Requisitos

Antes de comenzar, asegúrate de tener instalados los siguientes programas:

- **PHP** para ejecutar el script PHP.
- **MySQL** para probar la consulta SQL.

## 1. Ejecución de la Prueba PHP

### Instrucciones

1. Asegúrate de tener **PHP** instalado. Puedes descargarlo desde [aquí](https://www.php.net/downloads.php).

2. Navega al directorio que contiene el archivo `problema1.php`.

3. Abre una terminal y ejecuta el siguiente comando para ejecutar el script PHP:
   ```bash
   php problema1.php

## 2. Ejecución de la Consulta SQL

## Instrucciones
1. Abre el archivo problema2.xls, que contiene las tablas paises y ciudades en dos hojas separadas.

2. Importa las tablas a tu base de datos MySQL. Puedes hacerlo manualmente utilizando una herramienta como phpMyAdmin o con el siguiente comando en MySQL:

```
CREATE TABLE paises (
  id INT PRIMARY KEY,
  nombre VARCHAR(255)
);

CREATE TABLE ciudades (
  id INT PRIMARY KEY,
  ciudad VARCHAR(255),
  pais_id INT,
  FOREIGN KEY (pais_id) REFERENCES paises(id)
);
```
Asegúrate de poblar las tablas con los datos correspondientes:

```
INSERT INTO Ciudades (id, id_pais, ciudad) VALUES
(1, 1, 'Panama'),
(2, 2, 'Santiago'),
(3, 3, 'Bogota'),
(4, 3, 'Cali'),
(5, 4, 'Caracas'),
(6, 5, 'Rosario'),
(7, NULL, 'Mexico DF'),
(8, 2, 'Viña del mar');

INSERT INTO paises (id, nombre) 
VALUES 
(1, 'Panama'),
(2, 'Chile'),
(3, 'Colombia'),
(4, 'Venezuela'),
(5, 'Argentina');
```

3. Abre tu cliente de MySQL y ejecuta la siguiente consulta SQL para listar todas las ciudades y su respectivo país:

```
SELECT ciudades.ciudad, paises.nombre AS pais
FROM ciudades
JOIN paises ON ciudades.pais_id = paises.id
ORDER BY pais ASC, ciudad ASC;
```

4. La consulta devolverá una lista de ciudades y sus respectivos países ordenados por país y ciudad.

## 3. Ejecución de la Prueba Vue.js

### Instrucciones

1. Asegúrate de tener **Vue.js** cargado como un script en tu archivo HTML. El archivo `problema3-vue.html` incluye la referencia al script de Vue.js desde un CDN.

2. Para ejecutar la prueba de Vue.js, simplemente abre el archivo `problema3-vue.html` en tu navegador preferido.

3. No es necesario configurar un servidor de desarrollo. Al abrir el archivo HTML directamente, Vue.js debería funcionar de manera local.

4. En la interfaz se mostrará un listado de elementos con nombres y roles. Al hacer clic en el botón "Generar", se actualizará un mensaje con el total de elementos en el listado.

### Prueba

En la interfaz se mostrará un listado de elementos con nombres y roles. Al hacer clic en el botón "Generar", se actualizará un mensaje con el total de elementos en el listado.

## Problemas y Soluciones

## Vue.js
- **Complicación:** Asegúrate de que todos los estilos CSS estén correctamente definidos para cada bloque y que las clases dinámicas estén bien aplicadas (como .odd y .hidden).
- **Solución:** Se utilizó Vue.js para mostrar los elementos de un arreglo y manejar la visibilidad y estilo de los elementos de manera dinámica con clases condicionales y v-for.

## PHP
- **Complicación:** La función en PHP puede requerir adaptaciones según los requisitos específicos del problema.
- **Solución:** El archivo problema1.php debe ser ejecutado correctamente, y la solución dependerá de los comentarios dentro del código PHP.

## SQL
- **Complicación:** Asegúrate de que las tablas estén correctamente relacionadas por las claves foráneas.
- **Solución:** La consulta SQL utiliza un JOIN entre las tablas ciudades y paises para obtener los resultados deseados.

## Conclusión
Este repositorio contiene las soluciones para la prueba técnica de Desarrollador Front-End. Para cualquier pregunta o complicación adicional, por favor, no dudes en contactarme a través del correo proporcionado.

