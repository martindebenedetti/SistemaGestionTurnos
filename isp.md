# Principio de Segregación de Interfaces (ISP)

- Tipo: Diseño de interfaces.
- Propósito: Evitar que las clases dependan de interfaces que no usan por completo.

Si una interfaz tiene muchos métodos, las clases que la implementan se ven obligadas a definir funcionalidades que no necesitan, generando código inflado e innecesario.
El principio recomienda dividir interfaces grandes en otras más pequeñas y específicas, de modo que las clases solo implementen lo que realmente necesitan.

# Motivación

En el sistema de gestión de turnos, la clase turnos interactúa directamente con la clase Paciente y dependen de su interfaz completa, se verían obligados a "conocer" los métodos relacionados con la gestión de turnos, aunque no los utilicen. Esto crea una dependencia innecesaria. Si la interfaz de Paciente cambiara en la parte de gestión de turnos, estos otros sistemas podrían verse afectados violando el principio ISP.

# Estructura de Clases

![Estructura de Clases](/img/Principio_de_Segregación_de_Interfaces.png)

- [Imagen](https://drive.google.com/file/d/1yPPIkQtt4Blho68UuP8EVqvlJrUEXftQ/view?usp=drive_link)
