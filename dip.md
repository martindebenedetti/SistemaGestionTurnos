# Principio de Inversión de Dependencias (DIP)

- Tipo: Acoplamiento / Inversión de control.
- Propósito: Reducir el acoplamiento entre módulos haciendo que dependan de abstracciones, no de implementaciones concretas.

Cuando las clases dependen directamente de componentes específicos, cualquier cambio en ellos obliga a reescribir partes del sistema.
El principio recomienda introducir interfaces o abstracciones como intermediarias, permitiendo que los detalles de implementación sean intercambiables sin afectar el flujo principal.

# Motivación

En el sistema de gestión de turnos, la clase recepcionista depende directamente de la clase turnos, es decir, estaría dependiendo de implementaciones concretas de bajo nivel.
Para resolverlo se creara una interfase de abstraccion para manejar los turnos, de este modo no importa como se va a implementar internamente los turnos

# Estructura de Clases

![Estructura de Clases](/img/Principio_de_Inversión_de_Dependencias.png)

- [Imagen](https://drive.google.com/file/d/1w0Mv-e7oVQGNM2EE9C-8WnWOsLsfyqEh/view?usp=drive_link)
