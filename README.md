# Laboratorio 04: Patrones de Comportamiento (Command y Strategy)

- **Curso**: Ingeniería de Software II
- **Aula**: 851
- **Fecha**: 10/10/2025
- **Jefe de prácticas**: Sebastián Chávarry

---

### Contexto del Caso: Sistema de Restaurante "QuickServe"

El restaurante QuickServe necesita modernizar dos aspectos críticos de su operación: la comunicación entre meseros y cocina, y el procesamiento de pagos. Actualmente, ambos procesos generan confusión y errores debido a la falta de estandarización.

---

### Ejercicio 1 - Patrón Command (45 minutos)

**Situación Actual:**
Los meseros deben conocer todos los detalles específicos de preparación para cada tipo de orden que envían a la cocina:

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

**Requerimientos:**

1. Crear una interfaz `Command` con el método `execute()`
2. Implementar comandos concretos para cada tipo de orden
3. Crear una clase `Cocina` que procese las órdenes
4. Crear una clase `Mesero` que gestione y ejecute los comandos
5. Demostrar el funcionamiento con diferentes tipos de órdenes

---

### Ejercicio 2 - Patrón Strategy (15 minutos)

**Situación Actual:**
Los cajeros deben conocer los procedimientos específicos para procesar cada tipo de pago al final del servicio:

1. **Efectivo**: Proceso simple, solo verificar el monto exacto
2. **Tarjeta**: Requiere validación del número de tarjeta y comunicación con el banco
3. **Pago móvil**: Necesita validar la aplicación (PayPal, Yape, etc.) y número de teléfono

**Problema:**
Cada método de pago tiene su propia lógica de procesamiento, pero el sistema actual usa múltiples `if-else` que hacen el código difícil de mantener. Esto genera:

- Código complejo y difícil de mantener
- Dificultad para agregar nuevos métodos de pago
- Violación del principio Abierto/Cerrado

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
