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
