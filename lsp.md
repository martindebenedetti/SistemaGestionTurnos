# Principio de Sustitución de Liskov (LSP)

- Tipo: Correctitud en la jerarquía de clases.
- Propósito: Asegurar que las clases derivadas puedan sustituir a sus clases base sin alterar el comportamiento esperado del programa.

Si las subclases no se comportan de manera consistente con su superclase, el código que utiliza la superclase puede fallar o comportarse de forma inesperada al recibir una instancia de la subclase. Esto rompe el modelo de herencia y dificulta el razonamiento sobre el código.
El principio ayuda a utilizar la herencia de forma correcta.

# Motivación

En el sistema de gestión de turnos, si en el futuro quisiéramos añadir la posibilidad de subclases de turno, como por ejemplo turnoOnline o sobreTurno. En el caso de un turnoOnline debe agregarse los datos de la plataforma a usar, y para el caso del sobreturno no se debe dar la posibilidad de modificar, pero sí de cancelar. Esto podría generar conflictos en la herencia.

# Estructura de Clases

![Estructura de Clases](/img/Principio_de_Sustitución_de_Liskov.png)

- [Imagen](https://drive.google.com/file/d/1Lif_5msP2WK7vtwjBNX9ix_QiXDvkVzK/view?usp=drive_link)
