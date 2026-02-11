/* ```mermaid
classDiagram
    class Producto {
        -String nombre
        -double precioBase
        +Producto(String nombre, double precioBase)
        +getPrecioBase() double
    }

    class CalculadoraIVA {
        -double IVA = 0.21
        +calcularPrecioFinal(double precio) double
    }

    class Main {
        +main(String[] args)
    }

    Main ..> Producto : crea
    Main ..> CalculadoraIVA : utiliza# Ejercicio_UML
``` */
sequenceDiagram
    participant M as Main
    participant P as Producto
    participant C as CalculadoraIVA

    Note over M: Inicio de la ejecución
    M->>P: new Producto("Nombre", precioBase)
    activate P
    P-->>M: instancia creada
    deactivate P

    M->>P: getPrecioBase()
    activate P
    P-->>M: precioBase (double)
    deactivate P

    M->>C: calcularPrecioFinal(precioBase)
    activate C
    Note right of C: precio * (1 + 0.21)
    C-->>M: precioFinal (double)
    deactivate C
    
    Note over M: Muestra resultado en consola
