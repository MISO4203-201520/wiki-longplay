
## MARKETPLACE DE VENTA DE DISCOS DE VINILO COLECCIONABLES

El número de tiendas virtuales de música en Internet se ha incrementado en los últimos tiempos pero cada una busca la forma de diferenciarse para atraer distintos nichos de mercado. En esta aplicación se quiere atraer un público que últimamente ha venido creciendo y despertando gran interés para el mercado: los coleccionadores de discos de vinilo o los antiguos "Long Plays".

### Integrantes

| Nombres                       | Correo                        | Rol                  |
|-------------------------------|-------------------------------|----------------------|
| Baquero Jiménez Camilo        | c.baquero10@uniandes.edu.co   | Desarrollador        |
| Barrera Salgado Jorge Enrique | je.barrera11@uniandes.edu.co  | Desarrollador, Lider |
| Bastidas Melo Viviana Angely  | va.bastidas10@uniandes.edu.co | Desarrollador        |
| Garcia Manrique Juan David    | jd.garcia1381@uniandes.edu.co | Desarrollador        |
| Patiño Arevalo Juan Daniel    | jd.patino10@uniandes.edu.co   | Desarrollador        |

### Herramientas y Tecnologías

* Netbeans 8 IDE
* Lenguaje Java EE 8
  * EJB (API Enterprise Java Beans)
  * JPA (Java Persistence API)
  * JAX-RS
* Servidor Aplicación Glassfish 4
* Gestión del Proyecto con Maven 4
* Framework AngularJS 1.4.3
* Framework Bootstrap v3.3.5

### Reuniones

La comunicación en el grupo se realizará por medio de:
* Constantemente por el grupo de WhatsApp.
* Sábado en la tarde para unificar trabajo por Skype/Hangout.
* Reuniones presenciales en la universidad de forma esporádicamente o acordaras de ser necesario.

### Calidad

* Convenciones de Código: El grupo de desarrollo seguira los lineamientos basicos para codificacion de Oracle que se encuentra en el link http://www.oracle.com/technetwork/java/codeconventions-150003.pdf.
* Análisis estático de código con SonarQube de forma periódica para encontrar y resolver los hallazgos críticos.
* Asignación de pares para verificar, probar e inspeccionar la calidad del código y su integración.

### Mitigación de Riesgos:

* Entendimiento del proyecto:
  *  Revisión individual de la arquitectura.
  *  Validación grupal de la arquitectura. (Vista Funcional, Despliegue y Desarrollo).
  *  Revisión de herramientas individual.
  *  Apoyo grupal.
* Entendimiento de requerimientos.
  * Revisión individual del enunciado.
  * Relación con los requerimientos.
  * Validación grupal de requerimientos. (Mockups)
  * Uso del foro del curso.
* Coordinación del equipo:
  * Seguir la estrategia de comunicación definida.
  * Respeto a la definición y cumplimiento de las tareas.
  * Comunicación abierta para pedir apoyo en los diferentes problemas que se presenten.
  
### Plan Global

| Ciclo   | Fecha Inicio  | Fecha Fin       | Semanas   |
|---------|---------------|-----------------|-----------|
| Ciclo 1 | 25 agosto     | 8 de septiembre | 2 semanas |
| Ciclo 2 | 8 septiembre  | 29 septiembre   | 3 semanas |
| Ciclo 3 | 29 septiembre | 20 octubre      | 3 semanas |
| Ciclo 4 | 20 octubre    | 10 Noviembre    | 3 semanas |

### Plan Semanal

* Ciclo 1 Semana 1

| Tarea                                                   | Integrante  | Tiempo Estimado | Tiempo Real |
|---------------------------------------------------------|-------------|-----------------|-------------|
| Subir el documento al repositorio de la Wiki            | Jorge       | 10min.          |             |
| Revisión individual de la Arquitectura.                 | Todos       | 30min.          |             |
| Desplegar la aplicación en la máquina virtual           | Todos       | 120min.         |             |
| Hacer el prototipo de diagrama de Funcional. (Cacoo)    | Camilo      | 60min.          |             |
| Hacer el prototipo de diagrama de Despliegue. (Cacoo)   | Viviana     | 60min.          |             |
| Hacer el prototipo de diagrama de Desarrollo. (Cacoo)   | Juan Daniel | 60min.          |             |
| Definición de requerimientos actuales en la aplicación. | Jorge       | 60min.          |             |
| Analizar los resultados de SonarQube.                   | Juan David  | 60min           |             |

* Ciclo 2 Semana 2

| Tarea | Integrante | Tiempo Estimado | Tiempo Real |
|-------|------------|-----------------|-------------|
| R1    |            |                 |             |
| R2    |            |                 |             |
| R3    |            |                 |             |
| R4    |            |                 |             |
| R5    |            |                 |             |
| R6    |            |                 |             |

### Requerimientos

* Requerimientos Ciclo 1 

| Cod. | Estado | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|------|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| R1   |        | El sistema debe ofrecer al comprador la opción de pagar la compra. Se debe mostrar un formulario para realizar el pago que despliega el total de la compra y el desglose en impuestos. Suponga que hay un impuesto a las ventas del 16% . Debe estar la posibilidad de seleccionar el tipo de tarjeta crédito/debito con el que se realizará el pago. Cuando el usuario selecciona pagar, el sistema debe guardar la información sobre el pago de forma persistente en la base de datos.  |
| R2   |        | El sistema debe ofrecer al comprador la posibilidad de agregar comentarios sobre los productos. El comentario va  asociado con un producto específico y es una descripción en texto libre de no más de 255 caracteres. Los comentarios asociados con los productos se deben persistir incluyendo la fecha, el usuario y la descripción.                                                                                                                                                   |
| R3   |        | El sistema debe ofrecer al usuario con el rol de administrador el servicio de ver los usuarios registrados en la aplicación y sus roles. Se debe agregar el rol de administrador en Stormpath (el mecanismo de seguridad que está utilizando la aplicación)                                                                                                                                                                                                                               |
| R4   |        | El sistema debe ofrecer al comprador la posibilidad de registrar preguntas sobre un producto de un proveedor específico. La pregunta se debe persistir con el producto al que hace referencia, el usuario, su email, la fecha y la descripción.  Cuando se registre la pregunta al proveedor al proveedor debe llegarle una notificación por email.                                                                                                                                       |
| R5   |        | El sistema debe ofrecer al comprador la posibilidad de realizar una búsqueda sobre el catálogo de productos que retorne el producto más barato de un proveedor dado o el proveedor que ofrece el producto más barato de un tipo de producto dado.                                                                                                                                                                                                                                         |
| R6   |        | El sistema debe ofrecer al proveedor la posibilidad de agregar un descuento especial a alguno de sus productos. Esta información debe desplegarse en el catálogo.                                                                                                                                                                                                                                                                                                                         |


### Calidad del Código
En esta sección se analiza el código de la aplicación actual haciendo uso de la herramienta SonarQube.
#### Documentación
![](src/img/001.PNG?raw=true)

En cuanto a documentación, podemos ver que el aplicativo tiene 71.4% de documentación. Esto quiere decir que la mayoría de las clases tienen en su definición una documentación mínima acerca de las funcionalidades que ofrecen. Analizando las clases que no se encuentran documentadas, encontramos que la mayoría son Interfaces utilizadas en el aplicativo.
#### Líneas de Código
![](http://i.minus.com/ibfbjsw6NAybKz.PNG)

Analizando las líneas de código, podemos ver que se trata de un proyecto relativamente pequeño, el cual contiene 64 archivos repartidos en 17 directorios. La gran mayoría del código hace parte de clases Java, mientras que una pequeña porción está destinada a la parte Web de la aplicación.
#### Duplicados
![](http://i.minus.com/iBZUOwujcoDrS.PNG)

En cuanto a los duplicados, podemos ver que hay 15.1% de duplicado en 15 archivoss, esto quiere decir bloques que tienen más de 10 línes que se repiten a lo largo de todo el código.
#### Complejidad
![](http://i.minus.com/iTIbQE9aCokcM.PNG)

Por otro lado, analizando la complejidad podemos ver que en general los métodos de la aplicación son poco complejos, teniendo una media de 1,9.
#### Deuda Técnica
![](http://i.minus.com/iXxenXScjdRYH.PNG)

En cuanto a la deuda técnica, podemos ver que es baja, teniendo un total de 86 evidencias. Analizando en detalle las evidencias, encontramos que las Críticas se debe a excepciones que no tienen Log o no son manejadas de forma adecuada (un total de 7). Por otro lado, en cuanto a evidencias Mayores encontramos duplicados en el código y ciertos warnings que pueden ser resueltos utilizando @Override. Finalmente, en cuanto a evidencias Menores, se encuentra la mala utilización de variables cuyas instancias pueden ser retornadas sin tener que ser asignadas a una variable temporal.

![](http://i.minus.com/iJGNzBQevH7BN.PNG)

Analizando la pirámide de deuda técnica, encontramos que la mayoría de las evidencias hacen parte de la mantenibilidad y modificabilidad del aplicativo, aunque en confibabilidad tenemos una deuda técnica del 100%.
