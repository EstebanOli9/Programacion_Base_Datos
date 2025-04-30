# Programacion_Base_Datos
Este proyecto contiene el script de creación de una base de datos para una plataforma de comercio electrónico. Incluye las tablas principales como usuarios, productos, órdenes, pagos, 
y más, con sus respectivas relaciones y restricciones.
Estructura de la Base de Datos
El esquema se llama ecomerce y contiene las siguientes tablas:

usuarios

carrito_compras

categorias

direccion

orden

productos

orden_objetos

pagos

producto_carrito

Cada tabla está diseñada usando claves primarias, claves foráneas y restricciones únicas para asegurar la integridad de los datos.


Instrucciones SQL para la creación
1. Crear el esquema y usarlo:
   CREATE SCHEMA IF NOT EXISTS `ecomerce` DEFAULT CHARACTER SET utf8mb4 COLLATE utf8mb4_0900_ai_ci;
   USE `ecomerce`;
2. Crear las tablas:
Las tablas están organizadas en el archivo schema.sql. Puedes ejecutarlo directamente en tu cliente MySQL favorito.
   create table usuario varchar(20);

Inserción de datos de ejemplo
  INSERT INTO usuarios (nombreusuario, correo, contraseña, nombre, apellido, telefono)
VALUES 
('juanperez', 'juan@example.com', '1234', 'Juan', 'Pérez', '3111111111'),
('mariagomez', 'maria@example.com', 'abcd', 'Maria', 'Gomez', '3222222222'),
('carlossoto', 'carlos@example.com', 'pass123', 'Carlos', 'Soto', '3333333333');

-- Insertar categorías
INSERT INTO categorias (nombre, descripcion)
VALUES 
('Electrónica', 'Dispositivos y accesorios electrónicos'),
('Ropa', 'Vestimenta de diferentes estilos'),
('Hogar', 'Productos para el hogar');

-- Insertar productos
INSERT INTO productos (nombre, descripcion, precio, cantidad, categoria_id)
VALUES 
('Smartphone X', 'Teléfono inteligente de última generación', 799.99, 10, 1),
('Camiseta básica', 'Camiseta de algodón color blanco', 15.00, 100, 2),
('Lámpara LED', 'Lámpara de escritorio con luz blanca', 25.50, 50, 3);

Dump de la Base de Datos
Para generar un dump de esta base de datos (estructura + datos):
  mysqldump -u tu_usuario -p ecomerce > dump_ecomerce.sql
Este archivo dump_ecomerce.sql contiene tanto las instrucciones de creación como los datos insertados.

Requisitos
MySQL 8.0 o superior

Cliente de base de datos como MySQL Workbench, DBeaver, phpMyAdmin o CLI

Contacto
Para más información o colaboración, por favor abre un issue o contáctame por correo.

