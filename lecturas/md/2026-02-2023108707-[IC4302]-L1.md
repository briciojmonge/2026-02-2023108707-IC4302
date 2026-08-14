# Lectura 1: Overview of NoSQL Databases
## Bases de datos II
__________________________________________
Estudiante: Fabricio Monge Brenes
Carnet: 2023108707
_________________________________________
### Instrucciones:
Tiempo estimado de lectura: 30 minutos

Comente las diferencias, ventajas y desventajas de los siguientes tipos de bases de datos NoSQL:

- Key-value país
- Document oriented
- Wide Column
- Graph
_________________________________________

### Bases de datos Key-value:
Son bases de datos sencillas de implementar y muy buenas con la escalabilidad a un nivel masivo.
Se usan en comercios electronicos puesto que pueden crecer rápido. También se utilizan en aplicaciones web que se basan en inicios de sesión.
Estas solo permiten busquedas por clave o Key, por lo que no son utiles para filtrar.

### Bases de datos orientadas a documentos:
Al igual que las key-value, son sencillas de implementar.
Aunque estas permiten versionar de una manera más facil, ya que se pueden añadir nuevas secciones datos en ejecución.
aceptan distintos tipos de archivos (XML, JSON, y otros) y de estructuras de datos por lo que no deben de tener los mismos datos todos los documentos. Además de esto, cuentan con un "Garbaje Collector" que elimina archvios antiguos.
Un problema de estas es que no existe implementación o es complicado implementar las relaciones entre archivos. 

### Bases de datos  Wide Column:
Las bases de este tipo guardan los datos en columnas y filas pero admiten datos ambiguos o complejos.
Las familias de colunas son parecidas a las tablas de las RDBMS, aunque se pueden añadir o eliminar columnas en ejecución.
Es sencillo actualizar datos, y se comprimen mejor que un sistema por filas. Además de que permiten explorar datos con facilidad y es sencillo ejecutar aggregation queries.
Pero actualizar, insertar o eliminar celdas especificas se vuelve más tardado y puede tomar más bloques en memoria. Por lo que no son utiles para apps que necesiten de mucha lectura y escritura.
### Bases de datos de grafos:
Estas bases representan datos como grafos, mediante nodos y las conexiones entre estos, por lo que resultan en datos relacionados.  Permiten una busqueda semántica rápida, se utilizan para redes neuronales, analización de Big Data, y motores de búsqueda.
Además estas bases no utilizan indices, a veces cuentan con limitaciones en las definiciones de estructuras de datos. Otros puntos importantes son: en algunos casos no permiten las autoreferencia y se puede volver dificil particionar los grafos para que un query no tenga que pasar por varias particiones.

### Comparación con bases de datos relacionales:
 Al comparar estas bases de datos con las bases relaciones, se encuentran diferencias notables. Por ejemplo, las bases relacionales hay una estructura única y normalizada para los datos. Mientras que las bases NoSQL buscan resolver problemas especificos, las bases Key-Value ofrecen velocidad, las documentales ofrecen flexibilidad en los datos y formatos, las Wide-Column ofrecen compresión sencilla y rendimiento en análisis masivo, y las de grafos ayudan a definir relaciones complejas.
 Además se debe mencionar que el teorema CAP menciona que solo se puede conseguir 2 de 3 de las siguientes caracteristicas en NoSQL:
 - consistencia
 - disponibilidad
 - toleracia a la partición