# Etapa 1: Análisis

## Propuesta del Proyecto
El propósito de este proyecto es definir los requerimientos funcionales y no funcionales para el desarrollo de un sistema de software destinado a la administración de una tienda minorista. El objetivo principal es automatizar el proceso de venta y generar reportes financieros básicos.

## Entrevista Inicial

**Estudiante :**
Buenos días, soy estudiante de ISC en el Tecnológico de Motul y como parte de mi proyecto en la materia de Ingeniería en Software vengo a hablar de las dificultades que usted tenga a la hora de administrar su tienda de abarrotes.

**Cliente (Dueño de la tienda):**
Adelante, joven.

**Estudiante :**
¿Qué es lo que más se le dificulta en la tienda?

**Cliente (Dueño de la tienda):**
Bueno, lo principal es que quiero automatizar el proceso de venta, ya que actualmente me cuesta trabajo registrar los productos con sus costos y precios de venta. También se me complica el cobro, necesito que el cálculo de totales sea automático a medida que agrego productos para no tardar, y al final del día me gustaría poder generar reportes de cierre de caja con el cálculo de mis ganancias, cosa que ahora no puedo hacer bien.

**Estudiante (ISC):**
Bueno tomando en cuenta lo que me dijo, ¿qué le parece una aplicación de Sistema de Punto de Venta (POS) que le permita realizar ventas mediante el escaneo de códigos de barras y busque automáticamente el producto en la base de datos?

**Cliente (Dueño de la tienda):**
La verdad es justo lo que necesito. Si esa aplicación puede hacer las sumas solita y decirme el precio nada más pasando el producto, me quitaría un gran peso de encima. Así ya no tendría que estar batallando con la calculadora ni preocupándome por si cobré mal.

# Levantamiento de Requerimientos

## 🚨 1. Problemática Actual
La tienda enfrenta actualmente desafíos operativos críticos derivados de la gestión manual, lo que afecta la rentabilidad y calidad del servicio:

* **🐢 Lentitud en el servicio:** La búsqueda manual de precios provoca filas y tiempos de espera innecesarios para el cliente.
* **💸 Pérdidas financieras en caja:** Los errores humanos al calcular el cambio (vuelto) generan diferencias de dinero y fugas de capital al final del día.
* **📦 Descontrol de inventario:** La falta de visibilidad sobre *"cuánto hay"* y *"cuánto queda"* provoca desabastecimiento (pérdida de ventas) o acumulación de mercancía innecesaria (dinero estancado).

---

## 💡 2. Justificación
La implementación de este sistema se justifica como una solución tecnológica urgente para automatizar los procesos operativos. 

El software logrará:
1.  Eliminar la dependencia de la memoria del personal.
2.  Garantizar la exactitud matemática en los cobros.
3.  Proporcionar datos reales sobre el stock.
4.  Transformar la operación de la tienda en un modelo eficiente y seguro.

---

## 🎯 3. Objetivos del Proyecto

### Objetivo General
Desarrollar e implementar un sistema de software de Punto de Venta (POS) e Inventario que automatice el proceso de cobro y la gestión de existencias, optimizando los tiempos de atención y asegurando la integridad financiera del negocio.

### Objetivos Específicos
- [ ] **Reducir el tiempo de cobro:** Disminuir en un 50% el tiempo por transacción mediante el uso de búsqueda rápida y escaneo de productos.
- [ ] **Eliminar errores de caja:** Garantizar el cálculo exacto del cambio a entregar al cliente mediante un asistente de cobro automatizado.
- [ ] **Controlar el stock en tiempo real:** Mantener un registro actualizado de las existencias, descontando productos automáticamente tras cada venta y generando alertas de stock bajo.

---

## 🛠️ Tecnologías (Próximamente)
* *Lenguaje:* [Aquí pondrás el lenguaje, ej. Python/Java]
* *Base de Datos:* [Ej. SQLite/MySQL]
* *Interfaz:* [Ej. Tkinter/Web]

---


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
