# Laboratorio 04: Patrones de Comportamiento (Command y Strategy)

- **Curso**: Ingeniería de Software II
- **Aula**: 851
- **Fecha**: 10/10/2025
- **Jefe de prácticas**: Sebastián Chávarry

---

### Contexto del Caso: Sistema de Restaurante "QuickServe"

El restaurante QuickServe necesita modernizar dos aspectos críticos de su operación: la comunicación entre meseros y cocina, y el procesamiento de pagos. Actualmente, ambos procesos generan confusión y errores debido a la falta de estandarización.

---

### Ejercicio 1 - Gestión de Órdenes de Cocina (45 minutos)

En el restaurante QuickServe, los meseros deben comunicar órdenes específicas a la cocina, pero cada tipo de preparación requiere información diferente: los platos principales necesitan una lista de ingredientes y tiempo de cocción, las bebidas calientes requieren el tipo de bebida y temperatura exacta, mientras que los postres necesitan especificar el tipo y decoración deseada. Actualmente, los meseros deben conocer todos estos detalles técnicos para cada preparación, lo que genera errores constantes y dificulta la incorporación de nuevos elementos al menú. Se necesita un sistema donde los meseros puedan enviar cualquier tipo de orden a la cocina de manera uniforme, sin conocer los procedimientos específicos de preparación.

---

### Ejercicio 2 - Sistema de Procesamiento de Pagos (15 minutos)

En el restaurante QuickServe, los cajeros deben procesar diferentes tipos de pago al finalizar las cuentas de los clientes: efectivo (verificando el monto exacto y calculando cambio), tarjetas (validando el número y conectando con el banco), y pagos móviles (verificando la aplicación específica como PayPal o Yape y el número de teléfono). Cada método tiene procedimientos completamente diferentes, y cuando se quiere agregar un nuevo método de pago, el sistema de caja requiere modificaciones extensas. Se necesita un sistema que permita cambiar dinámicamente el método de procesamiento de pago sin alterar la lógica principal de facturación.

---

### Entregables

Para cada pregunta, presente:

1. Diagrama de clases UML con las relaciones correspondientes
2. Implementación en Java de las clases principales
3. Un ejemplo de uso (método main) que demuestre el funcionamiento

---

**Nota:** Puede hacer supuestos razonables sobre detalles no especificados, pero debe documentarlos en su solución.
