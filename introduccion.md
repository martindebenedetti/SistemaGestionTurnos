# Anexo - Introducción al Diseño Orientado a Objetos

## :small_blue_diamond:Descripción del paradigma orientado a objetos:

### ¿Qué es la programacion orientada a objetos y por qué es importante?

La programación orientada a objetos (POO) es un paradigma de programación que se basa en la abstracción de entidades del mundo real como objetos, que contienen tanto datos como comportamientos asociados. Estos objetos interactúan entre sí, y el sistema se diseña en torno a la interacción y colaboración entre estos objetos.  
La POO es importante ya que permite una mayor flexibilidad y adaptabilidad a medida que los sistemas crecen en tamaño y complejidad. Otorgando la posibilidad de reutilizar el código.

---

## :small_blue_diamond:Los cuatro fundamentos de POO:

- ### Encapsulamiento:

Proceso de ocultar la implementacion interna de un objeto y exponer solo las interfaces publicas.

**Ejemplo:** Un sistema de gestión de estudiantes debe proteger las calificaciones para que solo puedan ser modificadas mediante métodos controlados.

- ### Abstraccion:

Permite definir la estructura básica de un conjunto de objetos sin exponer su implementación interna.

**Ejemplo:** En un sistema de control de dispositivos electrónicos, cada dispositivo tiene funcionalidades comunes como encender() y apagar(), pero su funcionamiento interno varía.

- ### Herencia:

La herencia permite que una clase hija herede atributos y métodos de una clase padre.

**Ejemplo:** Diferentes figuras geométricas pueden calcular su área, pero cada una tiene una fórmula distinta.

- ### Polimorfismo
  El polimorfismo permite que un mismo método tenga diferentes comportamientos según el objeto que lo implemente.

**Ejemplo:** Un sistema de conversión de archivos debe permitir guardar un archivo en diferentes formatos.

---

## :small_blue_diamond:Requisitos iniciales del sistema:

1. Registrar y gestionar pacientes y medicos.
   - Guardar ficha personal de pacientes y medicos.
2. Matener un historial de turnos de cada paciente.
   - Guardar los detalles de fecha, hora, especialidad, datos del paciente y profecional asignado.
3. Enviar Notificaciones automáticas.
   - Enviar notificaciones por mail a cuando un turno sea confirmado, cancelado o modificado.
4. Solicitar turno.
   - Los turnos seleccionados se asignan según disponibilidad de cada medico sin asignacion doble.
5. Información sea segura y privada.
   - Asegurar que la informacion de contacto sea accesible solo para el personal autorizado.

---

## :small_blue_diamond:Casos de uso:

1. **Caso de uso: Registrar un médico**
   - **Actores involucrados:**
     - Recepcionista.
   - **Descripcion:**
     - Permite ingresar un nuevo médico en el sistema con su información profesional y de contacto.
   - **Flujo principal:**
     - El recepcionista accede al módulo registrar médico.
     - Ingresa nombre, matrícula profesional, especialidad, horario de atención y datos de contacto.
     - Guardar registro y se muestra que el medico se registro correctamente.
   - **Precondiciones:**
     - El médico no debe estar registrado previamente.
   - **Postcondiciones:**
     - El médico queda registrado en la base de datos.

---

2. **Caso de uso: Registrar un paciente**
   - **Actores involucrados:**
     - Recepcionista.
   - **Descripcion:**
     - Permite ingresar un nuevo paciente en el sistema con su información personal y de contacto.
   - **Flujo principal:**
     - El recepcionista accede al módulo registrar paciente.
     - Ingresa nombre completo, número de documento,fecha de nacimiento, información de contacto (teléfono, correo electrónico).
     - Guardar registro y se muestra que el paciente se registro correctamente.
   - **Precondiciones:**
     - El paciente no debe estar registrado previamente.
   - **Postcondiciones:**
     - El paciente queda registrado en la base de datos.
3. **Caso de uso: Asignar un turno médico**
   - **Actores involucrados:**
     - Recepcionista.
     - Paciente.
   - **Descripcion:**
     - Permite asignar un turno a un paciente con un médico disponible en un horario específico.
   - **Flujo principal:**
     - Seleccionar paciente y seleccionar medico.
     - Seleccionar fecha y hora del turno disponibles.
     - Confirmar turno y enviar notificación del turno asignado.
   - **Precondiciones:**
     - Disponibilidad del medico para esa fecha y hora disponible.
   - **Postcondiciones:**
     - Registracion del turno en el sistema y enviar notificaciones.
4. **Caso de uso: Modificar o cancelar un turno**
   - **Actores involucrados:**
     - Recepcionista.
     - Paciente.
   - **Descripcion:**
     - Permite modificar la fecha, hora o médico de un turno existente, o cancelarlo si es necesario.
   - **Flujo principal:**
     - Se ingresa al sistema y se elige el turno a modificar o cancelar.
     - Se confirma la acción.
     - Se envia notificacion del cambio y cancelacion.
   - **Precondiciones:**
     - Al ingresar al historial de turnos debe dar la opcion de modificar o cancelar un turno activo.
   - **Postcondiciones:**
     - Se debe guardar el cambio y volver a enviar una notificacion, en caso de cancelar turno enviar notificacion de que se canceló el turno y liberar la agenda del medico.
5. **Caso de uso: Consultar historial de turnos**
   - **Actores involucrados:**
     - Recepcionista.
     - Paciente.
     - Médico.
   - **Descripcion:**
     - Permite visualizar los turnos previos y futuros de un paciente, junto con su estado y detalles.
   - **Flujo principal:**
     - Ingresar con el perfil de paciente o medico.
     - AL ingresar se ver ver la lista de turnos asignados a un paciente o a un medico.
     - Permitir la busqueda por dia, semana o mes.
   - **Precondiciones:**
     - Se debe saber el dni del paciente o nombre del profecional
   - **Postcondiciones:**
     - Mostrar el historial de turnos.

## :small_blue_diamond:Boceto inicial del diseño de clases: :camera:

![Boceto inicial del diseño de clases](/img/Boceto.png)  
:link:[Boceto](https://www.dropbox.com/scl/fi/6lh6i9t0b0cgelh0kj9m9/Boceto.png?rlkey=sblcngkz2o0rxz4g4whks6trs&st=08qgkenn&dl=0)
