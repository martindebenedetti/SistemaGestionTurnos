# Anexo - Aplicación de Patrón de Diseño estructural - Adapter

Los patrones de diseño estructurales se utilizan para resolver problemas de composición (agregación) de clases y objetos. Intentan que los cambios en los requisitos de la aplicación no ocasionen cambios en las relaciones entre los objetos. Normalmente estas relaciones están determinadas por las interfaces que soportan los objetos.
Relación con los Principios SOLID  
**Principio de Responsabilidad Única (SRP)**  
Los patrones estructurales a menudo ayudan a que las clases se enfoquen en una única responsabilidad.  
**Principio Abierto/Cerrado (OCP):**  
Este principio es fundamental para los patrones estructurales. Permiten extender la funcionalidad de un sistema sin modificar el código existente.  
**Principio de Inversión de Dependencias (DIP):**  
Este principio es muy relevante para los patrones estructurales, ya que a menudo se utilizan para introducir abstracciones y desacoplar componentes.  
**Principio de Segregación de Interfaces (ISP):**  
Los patrones estructurales pueden indirectamente apoyar ISP. Al separar responsabilidades se puede evitar que una clase no necesite implementar métodos que no utiliza.  
**Principio de Sustitución de Liskov (LSP):**  
Muchos patrones estructurales promueven el uso de interfaces y abstracciones.

Propósito y Tipo del Patrón: Actualmente el sistema no muestra explícitamente cómo se integrarían servicios externos, como un sistema de copago para turnos, o un servicio de WhatsApp para recordatorios de turnos. Usando el patrón de diseño estructural "Adapter" se resuelve este problema al proporcionar un intermediario que traduce las llamadas entre la interfaz de nuestro sistema y la interfaz del servicio externo.

## Motivación

Actualmente, el sistema se encuentra con una limitación significativa: no tiene una forma explícita y transparente de integrar servicios externos, como un servicio de WhatsApp para el envío de recordatorios de turnos.
El patrón de diseño estructural Adapter resuelve este problema al proporcionar un intermediario que traduce las llamadas entre la interfaz de nuestro sistema y la interfaz del servicio externo. De esta forma, el sistema cliente puede interactuar con el servicio externo a través de una interfaz que le resulta familiar, sin necesidad de conocer los detalles de la interfaz real del servicio.

## Estructura de Clases

![Patrón de Diseño estructural - Adapter](/img/Patrón%20de%20Diseño%20estructural%20-%20Adapter.png)

- [Imagen](https://drive.google.com/file/d/1m3CTPnmZj3eqUK2e34qGqebISA0N0qZe/view?usp=drive_link)
