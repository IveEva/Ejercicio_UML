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
    
    M->>Usuario: Imprime "Total con IVA: 24.2"
