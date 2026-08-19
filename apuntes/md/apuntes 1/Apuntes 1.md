# Bases de datos 2
# Apuntes de clase #1

-------------------------
##### Fecha de clase
18 de Agosto de 2026

---------------------------- 
### Sistemas Operativos 
##### (O.S en inglés y S.O en español)

Segun IBM, un S.O. es un conjunto de programas informátivos que gesionan hardware y aplicaciones de un computador asignando recursos.[1] 
Además cada sistema operativo cuenta con varios componentes que deben de trabajar en conjunto, estos son: núcleo o core, programador de procesos, gestor de memoria, adeministrador de entrada y salida, administrador de archivos e interfaz de usuario.[1]

Tomando esta definición se puede entender que el S.O. se encarga de las tareas por el usuario, de modo que, el S.O. es quien controla como se maneja la memoria, el uso del disco, las entradas y salidas y el manejo del cpu.

Se menciona que el S.O. se puede considerar una estructura monolítica, aparte de ser considerado grande y relativamente lento.

Los sistemas operativos cuentan con limites:
- Para sistemas que utilicen unix o linux se puede utilizar "ulimits". El comando retorna datos relacionados a los limites del S.O definidos, como: número de procesos, de files abiertos, de hilos o threads, de file descriptors, etc.
- Es común que un S.O tenga un limite de número de procesos que puede tener abiertos 

![imagen_datos_y_metadatos](<datos_y_metadatos.png>)

Hay limites y parámetros que afectan a la manera en la que se ejecutan las applicaciones y procesos, algunos limites que tienen peso son:
- number processes
- number files
- file descriptors

![imagen_procesos_y_file_descriptors](<procesos_y_file_descriptors.png>)

También cabe recalcar que los procesos cuentan con entradas y salidas que interacturan con los S.O.
- Standard Input: teclado
- Standard Output: terminal

![imagen_ingreso_de_datos](<>)

### Pipes

![Imagen_pipes](<pipes.png>)

### File descriptors
Como se menciona anteriormente un proceso cuenta con un id, el cuál forma parte de los file descriptors.

Se puede llegar a sobrepasar los file descriptors (FD) de una computadora, al pasarse de la cantidad definida de FD, la computadora deja de responder adecuadamente.

![imagen_db_fd](<db_fd.png>)

### DoS y DDoS
Los terminos DoS y DDoS vienen de Denial of Service y Distributed Denial of Service respectivamente. Estos son tipos de ataques que se basan en "gastar" o sobre utilizar los recursos de una computadora o servidor para que cuando hayan interacciones reales sean muy lentas.

![imagen_ddos](<ddos.png>)

![imagen_ddos_+_fd](<>)

Un DDoS o DoS genera conexiones e "interacciones de una manera falsa para sobrecargar un computador o base de datos y gastar: disco, memoria, FDs, etc, para que los clientes reales no puedan ser atendidos

![imagen_interaccion_db_os](<>)

Para evitar el remplazo de bloques de memoria y así ampliar una BD, una base puede "reservar" una cantidad de memoria más grande, se expande al inicio del proceso para solo hacer interrupciones al iniciar.

![imagen_interaccion_dbampliada_os](<>)
#### system calls:

![arquitectura](<>)

Varias DB ralcionales fueron creadas en un LAN (lenguajes de alto nivel) como C++ o C, por lo que estas interacturan desde el apartado LAN hacia abajo. Y varias NoSQL utilizan JAVA.

![arquitectura_+_java](<>)
### Virtual Machines

------------------------------
#### Bibliografía:

https://www.ibm.com/mx-es/think/topics/operating-systems

------------------------------
Estudiante: Fabricio Monge Brenes 
Carnet: 2023108707