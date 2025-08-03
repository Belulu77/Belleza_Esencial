# Belleza_Esencial

1. Introducción
1.1 Propósito
El propósito fundamental de esta aplicación es establecer una plataforma de e-
commerce intuitiva y eficiente para la venta online de productos de skincare y
cuidado del cabello. La solución busca optimizar la experiencia de compra del usuario,
facilitando la navegación por el catálogo, la visualización detallada de los productos, la
gestión del carrito de compras y un proceso de pago seguro y sencillo. Además,
permitirá a los usuarios registrarse, gestionar sus perfiles y acceder a su historial de
pedidos.


1.2 Alcance
   
El sistema permitirá a los usuarios:
● Explorar un catálogo completo de productos de skincare y cuidado del
cabello.
● Buscar y filtrar productos por diversas características (tipo de piel, tipo de
cabello, marca, ingredientes, etc.).
● Ver características detalladas de cada producto (descripción, ingredientes,
modo de uso, reseñas).
● Agregar productos al carrito de compras.
● Gestionar el contenido del carrito (modificar cantidades, eliminar productos).
● Realizar compras a través de un proceso de checkout seguro.
● Registrarse y autenticarse como usuarios.
● Gestionar su perfil y actualizar sus datos personales.
● Ver su historial de pedidos.


El sistema estará dirigido a cualquier persona interesada en adquirir productos de
skincare y cuidado del cabello de forma online. La aplicación será web, desarrollada
con tecnologías modernas (PHP, Node.js, MySQL, HTML, JavaScript, CSS), siguiendo
una arquitectura cliente-servidor.

1.3 Definiciones, acrónimos y abreviaturas
● API: Application Programming Interface
● CRUD: Create, Read, Update, Delete
● UI: User Interface
● DB: Database
● SKU: Stock Keeping Unit (código de identificación de producto)
● Pasarela de Pago: Servicio que autoriza pagos con tarjeta de crédito/débito u
otros métodos.
● JWT: JSON Web Token
1.4 Referencias
● HTML: HyperText Markup Language
● CSS: Cascading Style Sheets
● JavaScript: Lenguaje de programación para el frontend
● PHP: PHP: Hypertext Preprocessor
● Node.js: Entorno de ejecución de JavaScript del lado del servidor
● MySQL: MySQL :: MySQL Documentation
1.5 Visión general del documento
Este documento está dividido en tres partes: descripción general del sistema,
requerimientos específicos y anexos. Incluye tanto requerimientos funcionales como no
funcionales.

-----------------------------------------------------------------------------------------------------
2. Descripción general
2.1 Perspectiva del producto
El sistema es una aplicación web de e-commerce. Tendrá:
● Frontend: Desarrollado con HTML, CSS y JavaScript.
● Backend: Utilizando una combinación de PHP y Node.js para la lógica de
negocio y la gestión de la API.
● Base de datos: MySQL.
2.2 Funcionalidad del producto

● Catálogo de Productos: Visualización de todos los productos disponibles, con
opciones de búsqueda y filtrado.
● Páginas de Detalle de Producto: Información completa de cada artículo
(descripción, imágenes, características, precio, disponibilidad).
● Carrito de Compras: Funcionalidad para agregar, eliminar y modificar la
cantidad de productos antes de la compra.
● Registro y Login de Usuarios: Creación de cuentas y autenticación segura.
● Gestión de Perfil de Usuario: Actualización de datos personales y direcciones
de envío.
● Proceso de Checkout: Flujo guiado para finalizar la compra y seleccionar
método de pago.
● Historial de Pedidos: Los usuarios pueden consultar sus compras anteriores.
● Gestión de Inventario y Productos (para Administrador): CRUD de
productos, gestión de stock.
● Gestión de Pedidos (para Administrador): Seguimiento y actualización del
estado de los pedidos.
2.3 Características del usuario (Roles)
● Usuario (Cliente): Explora productos, busca, filtra, ve detalles, agrega al carrito,
realiza compras, se registra/autentica, gestiona su perfil y ve su historial de
pedidos.
● Administrador: Gestiona productos (añadir, editar, eliminar), gestiona
categorías, gestiona usuarios, supervisa pedidos y puede ver reportes básicos.
2.4 Restricciones
● La base de datos debe ser MySQL.
● El sistema debe cumplir con estándares mínimos de seguridad (protección de
datos de usuario, transacciones seguras).
● Debe funcionar en navegadores modernos (Chrome, Firefox, Safari, Edge).
● Debe ser responsivo, adaptable a diferentes tamaños de pantalla (escritorio,
tablet, móvil).
● No se permitirá la venta de productos restringidos por ley.
2.5 Suposiciones y dependencias
● Los usuarios disponen de conexión estable a internet.
● El sistema dependerá de proveedores cloud para hosting y base de datos.
● Se integrará con una pasarela de pago externa para procesar las transacciones
(ej. Mercado Pago, Stripe, PayPal).
● Puede integrar APIs de mensajería (e.g., email) para confirmaciones de pedido.

-----------------------------------------------------------------------------------------------------

3. Requerimientos específicos
3.1 Requerimientos funcionales
● RF01 - Registro de Usuario:
○ El sistema debe permitir a los nuevos usuarios registrarse solicitando:
nombre, apellido, email, contraseña, y opcionalmente dirección de envío.

● RF02 - Autenticación:
○ El sistema debe autenticar a los usuarios registrados mediante email y
contraseña.
○ El sistema debe permitir la recuperación de contraseña.
● RF03 - Catálogo de Productos:
○ El sistema debe mostrar una lista de todos los productos disponibles.
○ El sistema debe permitir buscar productos por nombre o descripción.
○ El sistema debe permitir filtrar productos por categoría (skincare, cabello),
tipo de producto (crema, sérum, shampoo), marca, etc.

● RF04 - Detalles del Producto:
○ El sistema debe mostrar una página dedicada para cada producto con:
nombre, imágenes de alta calidad, descripción detallada, ingredientes,
modo de uso, precio, disponibilidad de stock y reseñas (si aplica).

● RF05 - Carrito de Compras:
○ El sistema debe permitir a los usuarios agregar productos al carrito desde
el catálogo o la página de detalle.
○ El sistema debe mostrar el contenido actual del carrito (productos,
cantidades, subtotal).
○ El sistema debe permitir al usuario modificar la cantidad de un producto
en el carrito.
○ El sistema debe permitir al usuario eliminar productos del carrito.
● RF06 - Proceso de Compra (Checkout):
○ El sistema debe guiar al usuario a través de un proceso de checkout de
varios pasos (información de envío, método de pago, revisión del pedido).
○ El sistema debe integrar una pasarela de pago para procesar
transacciones de forma segura.
○ El sistema debe generar una confirmación de pedido al finalizar la
compra.

● RF07 - Gestión de Perfil de Usuario:
○ El sistema debe permitir a los usuarios ver y actualizar sus datos
personales (nombre, apellido, email, direcciones de envío).
○ El sistema debe permitir a los usuarios ver su historial de pedidos,
incluyendo el estado de cada pedido.


● RF08 - Gestión de Productos (Administrador):
○ El sistema debe permitir al administrador añadir nuevos productos al
catálogo (nombre, descripción, precio, imágenes, stock, categoría).
○ El sistema debe permitir al administrador editar la información de
productos existentes.
○ El sistema debe permitir al administrador eliminar productos del catálogo.
○ El sistema debe permitir al administrador gestionar las categorías de
productos.

● RF09 - Gestión de Pedidos (Administrador):
○ El sistema debe permitir al administrador visualizar todos los pedidos
realizados.
○ El sistema debe permitir al administrador actualizar el estado de un
pedido (ej. &quot;Pendiente&quot;, &quot;Enviado&quot;, &quot;Entregado&quot;).
○ El sistema debe permitir al administrador ver los detalles de cada pedido.

-----------------------------------------------------------------------------------------------------
4. Interfaces externas
   
4.1 Interfaz de usuario
● Frontend web responsivo desarrollado con HTML, CSS y JavaScript.
● Interfaz intuitiva y atractiva, con un diseño limpio que resalte los productos.
● Dashboard diferenciado para el rol de administrador, con acceso a la gestión de
productos y pedidos.

4.2 Interfaz de hardware
● No aplica. El sistema se ejecutará en dispositivos con navegador web.

4.3 Interfaz de software
● API RESTful (JSON) entre el frontend y el backend (Node.js y PHP).
● Integración con una pasarela de pago externa (ej. API de Mercado Pago, Stripe,
etc.).
● Posible integración con servicios de envío/logística.

4.4 Interfaz de comunicación
● Protocolo HTTPS para todas las comunicaciones para garantizar la seguridad.
● Autenticación de usuarios y sesiones mediante JWT (JSON Web Token) en el
header de cada request.


-----------------------------------------------------------------------------------------------------
5. Apéndices

   
A. Casos de uso (opcional)
● Caso de uso: Registrarse como usuario.
● Caso de uso: Iniciar sesión.
● Caso de uso: Buscar productos.
● Caso de uso: Ver detalles de un producto.
● Caso de uso: Agregar producto al carrito.
● Caso de uso: Realizar compra.
● Caso de uso: Ver historial de pedidos.
● Caso de uso: Gestionar productos (Administrador).
● Caso de uso: Gestionar pedidos (Administrador).


B. Glosario de términos
● Carrito de Compras: Lista virtual de productos seleccionados por el usuario
para su compra.
● Checkout: Proceso final de una compra online, donde el usuario introduce datos
de envío y pago.
● Pasarela de Pago: Servicio que procesa transacciones financieras online.
● Producto de Skincare: Artículo para el cuidado de la piel (cremas, sérums,
limpiadores).
● Producto para el Cabello: Artículo para el cuidado capilar (shampoo,
acondicionador, mascarillas).
● JWT: JSON Web Token, mecanismo de autenticación segura.
● UML: Lenguaje Unificado de Modelado, para dibujar diagramas que explican
cómo funciona o está diseñado un sistema de software.
● API RESTful (JSON): Una forma de que aplicaciones se comuniquen usando
HTTP, enviando y recibiendo datos en JSON.
● JSON: JavaScript Object Notation. Formato de texto para enviar y recibir datos.


C. Mockups y prototipos
(Se incluirán si están disponibles en versiones futuras.)
