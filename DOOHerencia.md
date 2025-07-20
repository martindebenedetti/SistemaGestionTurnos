# Herencia

La herencia permite que una clase hija reutilice atributos y métodos de una clase padre. Promueve la reutilización de código, la extensibilidad y la jerarquía de clases.

**Sustitución de Liskov (LSP):** Las subclases Paciente, Medico y Paciente pueden usarse como Usuario sin romper el sistema.  
**Responsabilidad Única (SRP):** Permite dividir responsabilidades comunes en Usuario y extenderlas de forma especializada.  
**Abierto/Cerrado (OCP):** Se pueden crear nuevas clases hijas (ej: Administrador) sin modificar Usuario.  
**Factory Method:** Al permitir crear distintas subclases de Turno, este patrón aprovecha la herencia para instanciar objetos de tipo TurnoPresencial, TurnoVirtual, etc.

## Ejemplo en el proyecto

La clase Usuario encapsula atributos comunes como nombreCompleto,documento, email, password,fechanacimiento,telefono y métodos como actualizarContacto(). Las subclases Recepcionista, Paciente y Medico heredan estas propiedades y agregan comportamientos específicos. Esto evita la repetición de código y permite reutilizar lógica centralizada.

![Herencia](/img/DOOHerencia.png)

- [Imagen](https://drive.google.com/file/d/1kDia9P6W5sv4KmdzHDFKuyJzxwQCbIbJ/view?usp=drive_link)

## Ejemplo de pseudocódigo

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
