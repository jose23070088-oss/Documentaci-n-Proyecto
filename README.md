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
### Requerimientos No Funcionales

| ID Requisito | Requisito | Descripción de requisito | Negocio/Necesidad/oportunidad/objetivo | ¿Quién lo solicita? | Rol/Departamento | Entregable | Casos de prueba | Estado | Comentarios |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **RNF01** | Usabilidad (Interfaz) | Interfaz intuitiva optimizada para teclado y escáner, minimizando uso del mouse. | Velocidad operativa en momentos de alta afluencia (evitar colas). | Tienda Abarrotes | Todos los usuarios | 1.0 | Prueba de Usabilidad | Pendiente | Diseño "Keyboard-first". |
| **RNF02** | Rendimiento (Velocidad) | La búsqueda del producto tras el escaneo no debe tardar más de 1 segundo. | Eficiencia en el servicio al cliente. | Tienda Abarrotes | Sistema | 1.0 | Prueba de Carga | Pendiente | Optimización de consultas SQL. |
| **RNF03** | Persistencia (Datos) | Almacenamiento en BD local (MySQL) para asegurar datos al cerrar el programa. | Seguridad de la información y prevención de pérdida de datos. | Tienda Abarrotes | Sistema / TI | 1.0 | Prueba de Recuperación | Pendiente | Configuración de MySQL Local. |
| **RNF04** | Seguridad (Control de Acceso) | Restringir el acceso al módulo de "Gestión de Productos" mediante usuario/contraseña. | **Prevención de fraude:** Evitar que cajeros modifiquen precios sin autorización. | Tienda Abarrotes | Administrador | 1.1 | Prueba de Seguridad | Pendiente | Roles: Admin vs. Cajero. |
| **RNF05** | Fiabilidad (Manejo de Errores) | El sistema debe mostrar alertas claras si un código no existe, sin cerrarse ni bloquearse. | **Continuidad operativa:** Asegurar que la venta continúe aunque haya errores de lectura. | Tienda Abarrotes | Cajero | 1.0 | Prueba de Excepciones | Pendiente | Validar entradas nulas o incorrectas. |

---

# Etapa 2: Diseño

*(Aquí puedes añadir la estructura de tus tablas de SQL o el diseño de las ventanas de Java)*
