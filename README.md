# mechanical-workshop-bpmn

**Optimización de Procesos: Taller Mecánico BPMN**  
Este repositorio contiene el Análisis de Requisitos de Negocio (ARN) y la simulación de procesos para un taller mecánico, enfocado en identificar cuellos de botella y optimizar el uso de recursos humanos y materiales.

**Descripción del Proyecto**  
El objetivo es modelar y simular el flujo de trabajo de un taller, desde la llegada del vehículo hasta su entrega, evaluando cómo la asignación de personal afecta los tiempos de espera y los costes operativos.

**Problemas Identificados** (Escenario #1)  
En la configuración inicial, se detectaron los siguientes puntos críticos:


Retrasos en Presupuestación: La actividad "Elaborar presupuesto provisional" genera esperas considerables al depender de la evaluación del seguro y de la tarea "Evaluar reparación".


Impacto en Cadena: Este retraso afecta directamente a las tareas de "Reparar motor", "Reparar chapa" y "Pintar vehículo".


Cuello de Botella Crítico: La actividad "Reparar motor" presenta un tiempo de espera mínimo de casi tres días.

**Escenarios de Simulación y Mejora**  
Se evaluaron diferentes configuraciones de recursos para optimizar el ciclo de ejecución del proceso:

**Escenario #1: Configuración Inicial**

Recursos: El taller cuenta inicialmente con 2 recepcionistas y 3 mecánicos.
Impacto: Se presentan retardos graves en la actividad "Elaborar presupuesto provisional", lo que retrasa tareas críticas como la reparación del motor y chapa.
Cuellos de botella: Existe un cuello de botella importante en "Reparar motor" con tiempos de espera que alcanzan los tres días.

**Escenario #2: Optimización de Recursos**

Recursos: Se aumenta la cantidad de recepcionistas a 5 y la de mecánicos a 6.
Impacto: Este incremento permite que tareas como la toma de datos, presupuestación y facturación se ejecuten en paralelo.
Resultado: Se logra optimizar el proceso distribuyendo los trabajadores necesarios para reducir horas de espera sin elevar excesivamente los costes.

**Escenario #3: Rendimiento Máximo**  
Recursos: Se asigna un total de 7 recepcionistas y 24 mecánicos.
Impacto: Se eliminan por completo los retardos en todas las actividades, desapareciendo el cuello de botella en la reparación de motores.
Resultado: Todas las instancias iniciadas logran finalizar dentro del rango establecido, aunque el coste total de ejecución se incrementa debido a la alta contratación.

**Conclusiones Técnicas**  
Paralelismo: Aumentar recepcionistas de 2 a 5 permite ejecutar tareas como "Determinar tipo de cita", "Anotar datos" y "Generar factura" simultáneamente.
Ley de Rendimientos: Existe un punto donde añadir más trabajadores aumenta el coste total de salarios pero ya no reduce el tiempo de ejecución de forma proporcional.
Balance: El Escenario 2 busca la eficiencia sin elevar costes innecesarios, mientras el Escenario 3 prioriza la velocidad absoluta.

**Análisis de Costes**  
El coste total de ejecución bajo el escenario de máximo rendimiento es de 310,410.83 €. Los componentes principales del coste son:
Zona de pintura: 30.81% del coste final.
Zona de reparación de motores: 23.71%.
Zona de chapa: 16.70%.
Personal (Mecánicos de pintura y generales): ~25.79% combinado.
