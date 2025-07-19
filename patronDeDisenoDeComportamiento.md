# Anexo - Aplicación de Patrón de Diseño de comportamiento - Strategy

Los patrones de diseño de comportamiento se utilizan para definir la interacción entre distintos objetos. La interacción debe ser de tal manera que puedan comunicarse fácilmente entre sí, minimizando el grado de acoplamiento.
Relación con los Principios SOLID  
**Principio de Responsabilidad Única (SRP)**  
Un patrón de comportamiento a menudo ayuda a asegurar a que cada objeto o clase tenga una única razón para cambiar.  
**Principio Abierto/Cerrado (OCP):**  
Establece que las entidades de software deben estar abiertas para la extensión, pero cerradas para la modificación.  
**Principio de Inversión de Dependencias (DIP):**  
Los patrones de comportamiento a menudo logran que los módulos de alto nivel no deben depender de los módulos de bajo nivel al introducir interfaces o clases abstractas que actúan como abstracciones.  
**Principio de Segregación de Interfaces (ISP):**  
Al definir interfaces precisas para las interacciones, se evita que las clases implementen métodos que no necesitan.  
**Principio de Sustitución de Liskov (LSP):**  
Muchos patrones de comportamiento presuponen y funcionan mejor cuando se sigue este principio. Ya que establece que los objetos de un programa deben ser reemplazables por instancias de sus subtipos sin alterar la corrección de ese programa.

Propósito y Tipo del Patrón: Actualmente el sistema presenta una lógica de verificación de disponibilidad de turnos altamente acoplada y concentrada en el método verificarDisponibilidad() de la clase SistemaDeTurnos. Este enfoque genera un método excesivamente complejo y difícil de mantener o extender, ya que debe considerar múltiples factores (horario médico, superposiciones, licencias, etc.). El patrón de diseño de comportamiento "Strategy" resuelve esto al externalizar cada criterio de validación en clases de estrategia individuales. De esta forma, SistemaDeTurnos delega la verificación a una interfaz de estrategia, permitiendo que los algoritmos de disponibilidad sean intercambiables y fácilmente extensibles, sin modificar el código existente en la clase principal.

--

## Motivación

Actualmente, la clase SistemaDeTurnos tiene un método verificarDisponibilidad(). Este método, en un futuro, podría necesitar considerar diversos factores para determinar si un turno es válido para un médico en un horario específico. Por ejemplo, la disponibilidad podría depender de:

1. Disponibilidad Horaria del Médico: ¿Está el médico en su horario de atención?
2. Turnos Superpuestos: ¿Hay otros turnos ya agendados para ese médico en ese mismo horario?
3. Vacaciones/Licencias del Médico: ¿El médico está de licencia o vacaciones en esa fecha/hora?

Toda esta lógica podría estar directamente implementadas en verificarDisponibilidad(), el método puede volverse muy complejo, difícil de mantener y de extender.

## Estructura de Clases

![Patrón de Diseño estructural - Strategy](/img/Patrón%20de%20Diseño%20de%20comportamiento%20-%20Strategy.png)

- [Imagen](https://drive.google.com/file/d/1Zl7HdZupN08-SYv2DqiBWIdlHXxIUguo/view?usp=drive_link)
