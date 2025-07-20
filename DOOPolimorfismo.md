# Polimorfismo

El polimorfismo permite que objetos diferentes respondan al mismo mensaje con comportamientos distintos. Esto facilita extender comportamientos sin modificar el código del cliente que los utiliza.  
**Sustitución de Liskov (LSP):** Las subclases pueden sustituir a la clase base sin errores.
**Abierto/Cerrado (OCP):** Nuevas variantes se incorporan sin tocar el código existente.
**Factory Method:** Se basa en polimorfismo para instanciar diferentes tipos de Turno.

## Ejemplo en el proyecto

Aunque actualmente hay un solo tipo de Turno, el diseño permite extenderlo fácilmente. Si en el futuro se agrega TurnoVirtual, el sistema puede notificar de forma diferente sin modificar la lógica principal.

![Polimorfismo](/img/DOOPolimorfismo.png)

- [Imagen](https://drive.google.com/file/d/10eYW86xhXZaXLTUxPhnN5yLVDWcxwL-A/view?usp=drive_link)

## Ejemplo de Código

    Clase Turno {
        metodo crearTurno() {

        }
    }

    Clase TurnoVirtual hereda Turno {
        metodo crearTurno() {
            enviarEmail("Turno virtual")
        }
    }

    Clase SobreTurno hereda Turno {
        metodo crearTurno() {
            enviarEmail("Este es un sobreturno")
        }
    }
