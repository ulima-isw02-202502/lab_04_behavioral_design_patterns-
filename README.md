## Laboratorio de Ingeniería de Software 2

### Patrones de Comportamiento: Command y Strategy

**Duración:** 1 hora | **Modalidad:** Individual

---

### Contexto del Caso: Sistema de Cocina Inteligente "QuickServe"

El restaurante QuickServe necesita modernizar la comunicación entre los meseros y la cocina. Actualmente, los meseros deben conocer todos los detalles específicos de preparación para cada tipo de orden, lo que genera confusión y errores.

**Situación Actual:**
Los meseros manejan tres tipos principales de órdenes que requieren diferentes procesos en la cocina:

1. **Platos principales**: Requieren lista de ingredientes y tiempo de cocción específico
2. **Bebidas calientes**: Necesitan tipo de bebida y temperatura exacta de calentamiento
3. **Postres**: Requieren tipo de postre y especificaciones de decoración

**Problema:**
Cada vez que se agrega un nuevo tipo de orden o cambian los procesos de cocina, los meseros deben aprender nuevos procedimientos. Esto genera:

- Errores en las órdenes por falta de conocimiento técnico
- Tiempo perdido explicando procesos a nuevos meseros
- Dificultad para mantener consistencia en la preparación

**Objetivo:**
Crear un sistema donde los meseros puedan enviar órdenes a la cocina sin conocer los detalles internos de preparación, usando un mecanismo uniforme para todos los tipos de órdenes.

---

### Ejercicio - Patrón Command (45 minutos)

Implemente el patrón Command para encapsular las diferentes órdenes que los meseros envían a la cocina. Cada tipo de orden debe ser un comando independiente que contenga toda la información necesaria para su ejecución.

**Requerimientos:**

1. Crear una interfaz `Command` con el método `execute()`
2. Implementar comandos concretos para cada tipo de orden
3. Crear una clase `Cocina` que procese las órdenes
4. Crear una clase `Mesero` que gestione y ejecute los comandos
5. Demostrar el funcionamiento con diferentes tipos de órdenes

---

### Ejercicio 2 - Patrón Strategy (15 minutos)

El restaurante QuickServe necesita procesar diferentes métodos de pago al final del servicio. Actualmente, el cajero debe conocer los procedimientos específicos para cada tipo de pago, lo que genera confusión y errores.

**Situación Actual:**
Los clientes pueden pagar con tres métodos diferentes:

1. **Efectivo**: Proceso simple, solo verificar el monto exacto
2. **Tarjeta**: Requiere validación del número de tarjeta y comunicación con el banco
3. **Pago móvil**: Necesita validar la aplicación (PayPal, Yape, etc.) y número de teléfono

**Problema:**
Cada método de pago tiene su propia lógica de procesamiento, pero el sistema actual usa múltiples `if-else` que hacen el código difícil de mantener. Cuando se agregan nuevos métodos de pago, hay que modificar el código principal.

**Objetivo:**
Crear un sistema donde se pueda cambiar dinámicamente el método de pago sin modificar el código de la cuenta, usando diferentes estrategias de procesamiento.

**Requerimientos:**

1. Crear una interfaz `MetodoPago` con el método `procesar(monto)`
2. Implementar estrategias concretas para cada método de pago
3. Crear una clase `Cuenta` que use la estrategia seleccionada
4. Crear una clase `CajeroRestaurante` que gestione los métodos disponibles
5. Demostrar el funcionamiento cambiando métodos de pago dinámicamente

---

### Entregables

Para cada pregunta, presente:

1. Diagrama de clases UML con las relaciones correspondientes
2. Implementación en Java de las clases principales
3. Un ejemplo de uso (método main) que demuestre el funcionamiento

---

**Nota:** Puede hacer supuestos razonables sobre detalles no especificados, pero debe documentarlos en su solución.
