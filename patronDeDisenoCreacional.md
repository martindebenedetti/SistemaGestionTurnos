# Anexo - Aplicación de Patrón de Diseño creacional - Factory Method

Los patrones de diseño creacionales se utilizan para la instanciación de objetos, encapsulan la lógica de creación y aíslan al cliente de esta responsabilidad.
Relación con los Principios SOLID  
**Principio de Responsabilidad Única (SRP)**  
Los patrones creacionales ayudan a que una clase tenga una única razón para cambiar.  
**Principio Abierto/Cerrado (OCP):**  
Permiten extender la creación de nuevos objetos sin modificar código existente (mediante herencia o composición).  
**Principio de Inversión de Dependencias (DIP):**  
El cliente depende de abstracciones, no de implementaciones concretas.  
**Principio de Segregación de Interfaces (ISP):**  
Los patrones creacionales pueden contribuir a esto al fomentar el uso de interfaces pequeñas y cohesivas para la creación de objetos. Por ejemplo, una fábrica podría tener diferentes métodos para crear diferentes tipos de productos, pero cada método solo expondría la interfaz relevante para ese producto.  
**Principio de Sustitución de Liskov (LSP):**  
Las subclases de fábricas pueden reemplazar a su superclase sin romper la funcionalidad.

Propósito y Tipo del Patrón: En la actualidad solo se puede dar un solo tipo de turno, pero usando el patrón de diseño creacional "Factory Method" se podría agregar más formas de dar turnos, como por ejemplo turnos virtuales, turnos presenciales, sobre turnos, etc.

## Motivación

Actualmente, el sistema de gestión de turnos está limitado a la creación de un único tipo de turno. Esta rigidez se convierte en un problema significativo a medida que las necesidades del negocio evolucionan, haciendo imposible la incorporación de nuevas modalidades de atención sin alterar profundamente el código existente. Por ejemplo, la demanda de turnos virtuales o la necesidad de gestionar sobre turnos específicos no pueden ser satisfechas con la arquitectura actual. Cada vez que surge un nuevo tipo de turno, el sistema requeriría modificaciones directas en las partes encargadas de la creación de estos objetos, violando el principio de abierto/cerrado, que establece que las entidades de software (clases, módulos, funciones, etc.) deben estar abiertas para extensión, pero cerradas para modificación.
Para resolver esta limitación, implementaremos el patrón de diseño creacional Factory Method. Este patrón nos permite definir una interfaz para crear un objeto, pero deja que las subclases decidan qué clase instanciar. De esta manera, el sistema delega la responsabilidad de la creación de objetos a clases "fábrica" especializadas, desvinculando al cliente de la implementación concreta del turno.

## Estructura de Clases

![Patrón de Diseño creacional - Factory Method](/img/Patrón%20de%20Diseño%20creacional%20-%20Factory%20Method.png)

- [Imagen](https://drive.google.com/file/d/14GMj18glsOoZcH-HMeeO9bpCoCzu2zNw/view?usp=drive_link)
