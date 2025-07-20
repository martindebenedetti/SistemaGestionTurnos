# Abstracción

La abstracción se refiere a mostrar sólo lo esencial de un objeto, ocultando los detalles internos. A través de clases abstractas o interfaces, se define un contrato de comportamiento sin especificar su implementación concreta.

**Responsabilidad Única (SRP):** Las clases se centran en una única tarea.  
**Abierto/Cerrado (OCP):** Nuevas implementaciones se pueden agregar sin modificar las existentes.  
**Inversión de Dependencias (DIP):** Las clases dependen de abstracciones, no de detalles concretos.  
Strategy: Define una interfaz común para validar turnos que puede tener múltiples implementaciones.

## Ejemplo en el proyecto

Usuario es una clase abstracta que define los atributos y métodos comunes.  
Las clases Paciente, Medico y Recepcionista heredan de Usuario, lo que representa la abstracción de cada una especializas el comportamiento sin duplicar la estructura común.  
Sólo se muestran los atributos clave y métodos públicos para resaltar el principio de abstracción (mostrar lo esencial, ocultar lo interno).

![Abstracción](/img/DOOAbstraccion.png)

- [Imagen](https://drive.google.com/file/d/1bOvQc_yEBqxL2_lUIoeRXuFWKb0klYVE/view?usp=drive_link)

## Ejemplo de Código

    Clase Usuario {
        privado nombreCompleto
        privado documento
        privado email
        privado password
        privado fechanacimiento
        privado telefono

        metodo actualizarContacto(telefono, email){
        }

    }

    Clase Paciente hereda Usuario {
        metodo obtenerHistorial() {
        }

    }

    Clase Medico hereda Usuario {
        metodo obtenerDisponibilidad() {

        }
    }
     Clase Recepcionista hereda Usuario {
        metodo confirmarTurno() {
        }
        metodo cancelarTurno() {
        }
        metodo modificarTurno() {
        }
        metodo consultarHistorialPaciente() {
        }
        metodo consultarDIsponibilidadMedico() {
        }
    }
