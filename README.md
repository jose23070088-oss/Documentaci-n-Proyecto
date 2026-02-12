# Etapa 1: Análisis

## Propuesta del Proyecto
El propósito de este proyecto es definir los requerimientos funcionales y no funcionales para el desarrollo de un sistema de software destinado a la administración de una tienda minorista. El objetivo principal es automatizar el proceso de venta y generar reportes financieros básicos.

## Requerimientos y Requisitos (IEEE 830)

### Requerimientos Funcionales
* **Módulo de Ventas (Caja):**
    * **Lectura de Códigos:** El sistema debe ser capaz de recibir la entrada de un lector de códigos de barras. Al escanear un código, el sistema debe buscar automáticamente el producto en la base de datos.
    * **Recuperación de Precios:** Al identificar el producto escaneado, el sistema debe mostrar inmediatamente su descripción y precio de venta al público en la lista de compra actual.
    * **Cálculo de Totales:** El sistema debe sumar automáticamente el total de la venta a medida que se agregan productos.
* **Módulo de Inventario (Administrador de Productos):**
    * **Gestión de Productos:** El sistema debe permitir al administrador Agregar, Editar y Eliminar productos.
    * **Datos del Producto:** Cada producto debe tener almacenada la siguiente información mínima: Código de Barras, Descripción/Nombre, Precio de Costo y Precio de Venta.
* **Módulo de Reportes y Finanzas:**
    * **Registro de Ventas:** Cada venta finalizada debe guardarse en el historial con fecha y hora.
    * **Reporte de Ganancias del Día:** El sistema debe generar un reporte diario que muestre el total vendido (la suma de todo el dinero ingresado).

### Requerimientos No Funcionales
* **Usabilidad:** La interfaz de ventas debe ser intuitiva y permitir la operación rápida, minimizando el uso del mouse y priorizando el teclado/escáner.
* **Rendimiento:** La búsqueda del producto al escanear el código no debe tardar más de 1 segundo.
* **Persistencia:** Los datos deben almacenarse en una base de datos local (MySQL) para asegurar que la información no se pierda al cerrar el programa.

---

# Etapa 2: Diseño

*(Aquí puedes añadir la estructura de tus tablas de SQL o el diseño de las ventanas de Java)*
