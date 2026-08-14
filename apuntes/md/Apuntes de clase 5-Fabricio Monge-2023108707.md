# Bases de datos 2
# Apuntes de clase #5

-------------------------
##### Fecha de clase
11 de Agosto de 2026

---------------------------- 
## Observabilidad:

Según R. Chrystal, es la capacidad de comprender el estado de un sistema basandose únicamene en el conocimiento de su telemetría [1].
En el curso se hace énfasis en sistemas que generan métricas de rendimiento, de uso de disco, y de otros, o generan traces o Registros (logs).
##### Ejemplos:
- Amazon utiliza sistemas denominados "monkeys" cuya función es eliminar sectores de los servicios y estrucutras para verificar que estas sean robustas.
- Una aplicación puede generar informes de trazabilidad (Traces) para saber los movimientos o interacciones de los usuarios (como dónde ingresó, con qué interactuó, etc.)

### Metricas:
#### Time-series Databases:
Este tipo de base de datos están especializadas para manejar datos obtenidos a través del tiempo. De modo que cada entrada se almacena de manera cronológica [2]. Utilizan la estructura de Key-value.
Cuentan con la caracteristica de que los datos "pierden interés" conforme pasa el tiempo. Así que existe la "hot data" la cual hace referencia a la información más importante y más reciente.
La "hot data" es parte de poder establecer data tiers según tiempo o necesidad de acceso.
##### ej:
[imagen]

#### Prometheus
Prometheus se puede utilizar como un sistema de observabilidad para base de datos, en sí esta es una base de datos de monitoreo.
Este sistema toma caracteristicas de otras implementaciones como Solar Winds, Negios y Zenoss.
Permite el almacenamiento de métricas, y se establecen reglas entre tiers, como : en content 1 semana, después pasa a hot data 1 mes, y así sucesivamente.

#### SLA
El término viene de la abreviación de "Service Level Agreement".
Estos son acuerdos, como el uptime en web apps o apps.
#### Data Points
Se le llama data points a las lecturas especificas de ciertos datos. Por ejemplo, el registro de operaciones en disco, el uso de memoria por minuto, el número de archivos abiertos por minuto, número de conexiones abiertas por minuto, etc.
Se caracterizan por tener: un datetime, un value, y dimensions/tags/labels.
Y estos data points pueden ser recolectados por sistemas de observabilidad como Prometheus.

[imagen]
#### Logs


-----------------------------
Bibliografía:
[1] “¿Qué es la observabilidad?  | IBM.” https://www.ibm.com/mx-es/think/topics/observability

[2] “What is a time-series database and when would you use one?,” Design Gurus. https://www.designgurus.io/answers/detail/what-is-a-time-series-database-and-when-would-you-use-one?gad_source=1&gad_campaignid=23163907085&gclid=Cj0KCQjw-frTBhCvARIsADv4XY5jZLhqADsBCkwlENyE53q8VpEB8CNc3YGdUmUWbAhp_En5_tfVfqoaAufUEALw_wcB

