# Principio de Abierto/Cerrado (OCP)

- Tipo: Extensibilidad del sistema.
- Propósito: Permitir que el sistema sea extensible (para nuevas funcionalidades) sin modificar el código existente.

Si cada vez que se añade una nueva funcionalidad hay que modificar clases ya existentes, se introduce el riesgo de romper lo que ya funcionaba.
Para esto el principio recomienda diseñar módulos basados en abstracciones (interfaces/clases abstractas), de modo que las nuevas funcionalidades se implementen extendiendo el comportamiento sin alterar el núcleo.

# Motivación

En el sistema de gestión de turnos, si queremos añadir un nuevo tipo de notificación (ej: SMS, WhatsApp), tendríamos que modificar la clase notificacion, lo que rompe el principio OCP("cerrado para modificación").

# Estructura de Clases

![Estructura de Clases](/img/Principio_de_Abierto_Cerrado.png)

- [Imagen](https://drive.google.com/file/d/1grCmwaVpjewUo3thKEyyI2LE67ePBSBo/view?usp=drive_link)
