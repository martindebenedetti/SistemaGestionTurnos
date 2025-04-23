# Principio de Responsabilidad Única (SRP)

- Tipo: Organización del código / cohesión.
- Propósito: limitar el impacto de un cambio.

Cuando una clase maneja múltiples tareas, cualquier cambio en una de ellas puede afectar a las demás, haciendo el código frágil y difícil de mantener.
Para esto el principio recomienda dividir las responsabilidades en clases separadas, de modo que cada una se ocupe de una sola tarea. Esto reduce el acoplamiento y facilita las modificaciones

# Motivación

En el sistema de gestión de turnos, la clase medico tiene múltiples responsabilidades. Por un lado gestiona la información del médico ( nombre, matricula, especialidad, telefono, email), por otro verifica DisponibilidadMedico (atributo horarioAtencion, método estaDisponible() ) y por ultimo gestiona el turno (método consultarTurno() ).
Si cambian la información del médico o la lógica de disponibilidad o el sistema de turnos podría requerir modificar toda clase, lo que va en contra del principio SRP.
Por ejemplo:
Modificar horarios no afecta a los datos del médico.
Añadir nuevos métodos de contacto no impacta en la gestión de turnos.
Si luego se necesita añadir HistorialMedico, se crea una nueva clase sin tocar las existentes.

# Estructura de Clases

![Estructura de Clases](/img/Principio_de_Responsabilidad_%20Unica.png)

- [Imagen](https://drive.google.com/file/d/10d7vdObKenPwk-t4CktAJceMgm1uIFFm/view?usp=drive_link)
