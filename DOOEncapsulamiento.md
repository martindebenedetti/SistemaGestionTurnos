# Encapsulamiento

El encapsulamiento implica ocultar los atributos internos de una clase, exponiendo únicamente los métodos necesarios para interactuar con el objeto. Así, se protege el estado del objeto, se mejora la seguridad del sistema y se permite mayor control sobre los datos.

**Responsabilidad Única (SRP):** Cada clase mantiene su responsabilidad bien definida.  
**Abierto/Cerrado (OCP):** Se puede modificar internamente sin afectar al resto del sistema.  
**Segregación de Interfaces (ISP):** Se exponen sólo los métodos necesarios, evitando interfaces infladas.  
**Patrón Adapter:** El sistema accede a datos encapsulados a través de interfaces o métodos públicos.

## Ejemplo en el proyecto

Encapsulamiento se demuestra al mantener los datos sensibles privados y permitir su acceso/modificación sólo mediante métodos públicos.

![Herencia](/img/DOOEncapsulamiento.png)

- [Imagen](https://drive.google.com/file/d/16dFcXYDUgxTCkK3NoTwxJERw9iIU2WwP/view?usp=drive_link)

## Ejemplo de Código

    Clase Usuario {
            privado nombreCompleto
            privado documento
            privado email
            privado password
            privado fechaNacimiento
            privado telefono

        metodo obtenerNombreCompleto() {
            retornar nombreCompleto
        }

        metodo actualizarNombreCompleto(nuevoNombre) {
            nombreCompleto = nuevoNombre
        }

        metodo obtenerEmail() {
            retornar email
        }

        metodo actualizarEmail(nuevoEmail) {
            si esValido(nuevoEmail) {
                email = nuevoEmail
            }
        }

        metodo obtenerTelefono() {
            retornar telefono
        }

        metodo actualizarTelefono(nuevoTelefono) {
            si esValido(nuevoTelefono) {
                telefono = nuevoTelefono
            }
        }

        metodo actualizarContacto(nuevoTelefono, nuevoEmail) {
            actualizarTelefono(nuevoTelefono)
            actualizarEmail(nuevoEmail)
        }
    }

    Clase Paciente hereda Usuario {
        metodo obtenerHistorial() {
            // Retorna historial del paciente
        }
    }

    Clase Medico hereda Usuario {
        metodo obtenerDisponibilidad() {
            // Retorna horarios disponibles
        }
    }

    Clase Recepcionista hereda Usuario {
        metodo confirmarTurno() {
            // Confirma un turno en el sistema
        }

        metodo cancelarTurno() {
            // Cancela un turno
        }

        metodo modificarTurno() {
            // Modifica los datos de un turno
        }

    }
