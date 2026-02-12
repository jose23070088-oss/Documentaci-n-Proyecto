# Etapa 1: Análisis

## Propuesta del Proyecto
El propósito de este proyecto es definir los requerimientos funcionales y no funcionales para el desarrollo de un sistema de software destinado a la administración de una tienda minorista. El objetivo principal es automatizar el proceso de venta y generar reportes financieros básicos.

## Requerimientos y Requisitos (IEEE 830)

### Requerimientos Funcionales
### Requerimientos Funcionales

| ID Requisito | Requisito | Descripción de requisito | Negocio/Necesidad/oportunidad/objetivo | ¿Quién lo solicita? | Rol/Departamento | Entregable | Casos de prueba | Estado | Comentarios |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **RF01** | Lectura de Códigos | Recibir entrada de lector de código de barras y buscar automáticamente el producto en BD. | Agilizar el proceso de venta y reducir errores humanos. | Tienda Abarrotes | Cajero | 1.0 | Testing | Pendiente | Integración con hardware de escáner. |
| **RF02** | Recuperación de Precios | Mostrar inmediatamente descripción y precio de venta en la lista al escanear. | Validar visualmente el producto y precio ante el cliente. | Tienda Abarrotes | Cajero | 1.0 | Testing | Pendiente | Debe coincidir con la BD. |
| **RF03** | Cálculo de Totales | Sumar automáticamente el total de la venta conforme se agregan productos. | Automatizar el cobro y evitar cálculos manuales. | Tienda Abarrotes | Cajero | 1.0 | Testing | Pendiente | Actualización en tiempo real. |
| **RF04** | Gestión de Productos | Permitir Agregar, Editar y Eliminar productos del inventario. | Mantener el catálogo y precios actualizados. | Tienda Abarrotes | Administrador | 1.1 | Testing | Pendiente | Campos: Código, Nombre, Costo, P. Venta. |
| **RF05** | Registro de Ventas | Guardar cada venta finalizada en el historial con fecha y hora exacta. | Trazabilidad y seguridad de las transacciones. | Tienda Abarrotes | Sistema / Gerencia | 1.1 | Testing | Pendiente | Registro histórico inmutable. |
| **RF06** | Reporte de Ganancias | Generar reporte diario mostrando el "Total Vendido" (
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
