# Introducción

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
   - Guardar los detalles de fecha, hora, especialidad y profecional asignado.
3. Enviar Notificaciones automáticas.
   - Enviar notificaciones por mail a cuando un turno sea confirmado, cancelado o modificado.
4. Solicitar turno.
   - Los turnos seleccionados se asignan según disponibilidad de cada medico sin asignacion doble.
5. Información sea segura y privada.
   - Asegurar que la informacion de contacto sea accesible solo para el personal autorizado.

---

## :small_blue_diamond:Casos de uso:

---

## :small_blue_diamond:Boceto inicial del diseño de clases:
