
## MARKETPLACE DE VENTA DE DISCOS DE VINILO COLECCIONABLES

El número de tiendas virtuales de música en Internet se ha incrementado en los últimos tiempos pero cada una busca la forma de diferenciarse para atraer distintos nichos de mercado. En esta aplicación se quiere atraer un público que últimamente ha venido creciendo y despertando gran interés para el mercado: los coleccionadores de discos de vinilo o los antiguos "Long Plays".

### Tabla de contenido

[Roles y Responsabilidades](#roles-y-responsabilidades)

[Reglas de Funcionamiento](#reglas-de-funcionamiento)

[Mitigación de Riesgos](#mitigación-de-riesgos)

[Arquitectura](#arquitectura)

[Requerimientos](#requerimientos)

[Plan Global](#plan-global)

[Ciclo 1](#ciclo-1)

[Ciclo 2](#ciclo-2)

[Ciclo 3](#ciclo-3)

[Ciclo 4](#ciclo-4)

### Roles y Responsabilidades

#### Grupo Inicial Ciclo 1 y Ciclo 2
| Nombres                       | Correo                        | Rol                  |
|-------------------------------|-------------------------------|----------------------|
| Baquero Jiménez Camilo        | c.baquero10@uniandes.edu.co   | Desarrollador        |
| Barrera Salgado Jorge Enrique | je.barrera11@uniandes.edu.co  | Desarrollador, Lider |
| Bastidas Melo Viviana Angely  | va.bastidas10@uniandes.edu.co | Desarrollador        |
| Garcia Manrique Juan David    | jd.garcia1381@uniandes.edu.co | Desarrollador        |
| Patiño Arevalo Juan Daniel    | jd.patino10@uniandes.edu.co   | Desarrollador        |

#### Grupo Inicial Ciclo 3 y Ciclo 4
| Nombres                       | Correo                        | Rol                  |
|-------------------------------|-------------------------------|----------------------|
| Baquero Jiménez Camilo        | c.baquero10@uniandes.edu.co   | Desarrollador        |
| Barrera Salgado Jorge Enrique | je.barrera11@uniandes.edu.co  | Desarrollador, Lider |
| Bastidas Melo Viviana Angely  | va.bastidas10@uniandes.edu.co | Desarrollador        |
| Garcia Sanchez Ivan Felipe    | if.garcia11@uniandes.edu.co   | Desarrollador        |
| Murcia Romero Harold Leonardo | hl.murcia222@uniandes.edu.co  | Desarrollador        |

### Reglas de Funcionamiento

#### Reuniones
La comunicación en el grupo se realizará por medio de:
* Constantemente por el grupo de WhatsApp.
* Sábado en la tarde para unificar trabajo por Skype/Hangout.
* Reuniones presenciales en la universidad de forma esporádicamente o acordaras de ser necesario.

#### Calidad
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

* Ingreso de  nuevos Integrantes al proyecto:
  * Involucrar a los nuevos integrantes desde el inicio del nuevo ciclo.
  * Realizar explicación sobre el proyecto  y los componentes del mismo a nivel técnico y conceptual.
  * Revisar en conjunto los componentes desarrollados.
  * Validar en conjunto la experiencia que ya tienen con la tecnología y los componentes desarrollados en el grupo anterior.
  * Asignar tareas para el nuevo ciclo de acuerdo a las habilidades y el rol que desempeñaron en el grupo anterior.
  * Compartir las reglas y forma de trabajo del equipo.
  * Tener una comunicación permanente para identificar los problemas que surjan durante el nuevo ciclo del proyecto.

### Arquitectura

#### Vista Funcional
![](src/img/vista_funcional.PNG?raw=true)

* Entidades:
  *  Cliente
  *  Disco de vinilo
  *  Orden
  *  Proveedor
  *  Catálogo
  *  Medio de pago
  *  Álbum
  *  Carrito

#### Vista Despliegue
![](src/img/vista_despliegue.PNG?raw=true)

Client Machine: Debido a que la arquitectura está planteada en HTML5 y Javascript, toda la lógica de presentación se ejecuta sobre el browser del lado del cliente.

Application Server: Este sirve todas las peticiones realizadas por el cliente, actualmente funciona en Glassfish version 4.0.

DataBase Server: mantiene la información persistente de la aplicación, funciona en la base de datos Postgres.

#### Vista Desarrollo
La aplicación tiene 2 proyectos, en el primero se encuentra la capa de persistencia y negocio y en el segundo la capa de servicios y presentación.

#### Capa Persistencia y Negocio
![](src/img/vista_desarrollo_1.PNG?raw=true)

#### Capa Servicios
![](src/img/vista_desarrollo_2.PNG?raw=true)

#### Capa Presentación
![](src/img/vista_desarrollo_3.PNG?raw=true)

### Calidad del Código Actual
En esta sección se analiza el código de la aplicación actual haciendo uso de la herramienta SonarQube.
#### Documentación
![](src/c3/001.PNG?raw=true)

En cuanto a documentación, podemos ver que el aplicativo tiene 61.8% de documentación. Esto quiere decir que la mayoría de las clases tienen en su definición una documentación mínima acerca de las funcionalidades que ofrecen. Analizando las clases que no se encuentran documentadas, encontramos que la mayoría son Interfaces utilizadas en el aplicativo.
#### Líneas de Código
![](src/c3/002.PNG?raw=true)

Analizando las líneas de código, podemos ver que se trata de un proyecto relativamente pequeño, el cual contiene 112 archivos repartidos en 23 directorios. La gran mayoría del código hace parte de clases Java, mientras que una pequeña porción está destinada a la parte Web de la aplicación.
#### Duplicados
![](src/c3/003.PNG?raw=true)

En cuanto a los duplicados, podemos ver que hay 13.5% de duplicado en 27 archivos, esto quiere decir bloques que tienen más de 10 línes que se repiten a lo largo de todo el código.
#### Complejidad
![](src/c3/004.PNG?raw=true)

 Por otro lado, analizando la complejidad podemos ver que en general los métodos de la aplicación son poco complejos, teniendo un total de 709.
 
#### Deuda Técnica
![](src/c3/005.PNG?raw=true)

![](src/c3/0051.PNG?raw=true)

En cuanto a la deuda técnica, podemos ver que es baja, teniendo un total de 142 evidencias. Analizando en detalle las evidencias, encontramos que no hay Críticas, Bloqueantes y han bajado en gran manera las mayores.

* Oportunidades de mejora asociadas a la necesidad de refactoring de código que suprima código duplicado.
* Muchos de los issues existentes están asociados a la necesidad de aumentar el cubrimiento de pruebas.
* Es importante limpiar el código antes de subirlo a master.

![](src/c3/006.PNG?raw=true)

Analizando la pirámide de deuda técnica, encontramos que la mayoría de las evidencias hacen parte de la pruebas y modificabilidad del aplicativo.

#### Cobertura Pruebas Unitarias
![](src/c3/007.PNG?raw=true)

Se evidencia que se logro el objetivo de aumentar sobre el 50% el cubrimiento de pruebas

### Ambiente de Desarrollo
* Netbeans 8 IDE
* Lenguaje Java EE 8
  * EJB (API Enterprise Java Beans)
  * JPA (Java Persistence API)
  * JAX-RS
* Servidor Aplicación Glassfish 4
* Gestión del Proyecto con Maven 4
* Framework AngularJS 1.4.3
* Framework Bootstrap v3.3.5

### Requerimientos
| Cod. | Estado | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|------|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| R1   |        | El sistema debe ofrecer al comprador la opción de pagar la compra. Se debe mostrar un formulario para realizar el pago que despliega el total de la compra y el desglose en impuestos. Suponga que hay un impuesto a las ventas del 16% . Debe estar la posibilidad de seleccionar el tipo de tarjeta crédito/debito con el que se realizará el pago. Cuando el usuario selecciona pagar, el sistema debe guardar la información sobre el pago de forma persistente en la base de datos.  |
| R2   |        | El sistema debe ofrecer al comprador la posibilidad de agregar comentarios sobre los productos. El comentario va  asociado con un producto específico y es una descripción en texto libre de no más de 255 caracteres. Los comentarios asociados con los productos se deben persistir incluyendo la fecha, el usuario y la descripción.                                                                                                                                                   |
| R3   |        | El sistema debe ofrecer al usuario con el rol de administrador el servicio de ver los usuarios registrados en la aplicación y sus roles. Se debe agregar el rol de administrador en Stormpath (el mecanismo de seguridad que está utilizando la aplicación)                                                                                                                                                                                                                               |
| R4   |        | El sistema debe ofrecer al comprador la posibilidad de registrar preguntas sobre un producto de un proveedor específico. La pregunta se debe persistir con el producto al que hace referencia, el usuario, su email, la fecha y la descripción.  Cuando se registre la pregunta al proveedor al proveedor debe llegarle una notificación por email.                                                                                                                                       |
| R5   |        | El sistema debe ofrecer al comprador la posibilidad de realizar una búsqueda sobre el catálogo de productos que retorne el producto más barato de un proveedor dado o el proveedor que ofrece el producto más barato de un tipo de producto dado.                                                                                                                                                                                                                                         |
| R6   |        | El sistema debe ofrecer al proveedor la posibilidad de agregar un descuento especial a alguno de sus productos. Esta información debe desplegarse en el catálogo.                                                                                                                                                                                                                                                                                                                         |
| R7   |        | El sistema debe ofrecer al usuario aficionado la posibilidad de comprar vinilos coleccionables, estos serán ofrecidos mediante catálogo por los coleccionistas (proveedores). Se habilitará un carrito de compra para agregar los artículos que se desean adquirir una vez sean seleccionados del catálogo.                                                                                                                                                                               |
| R8   |        | El sistema debe permitir al usuario coleccionista ofrecer sus vinilos a través del marketplace. La información del catálogo comprenderá los siguientes datos por artículo: nombre, artista, el año de salida al mercado discográfico, el conjunto de canciones que lo componen, un precio determinado y una cantidad de unidades en inventario.                                                                                                                                           |
| R9   |        | El sistema debe permitir al usuario coleccionista (proveedor) el registro de los envíos a domicilio por cada una de los artículos vendidos.                                                                                                                                                                                                                                                                                                                                               |
| R10  |        | El sistema debe permitir el ingreso de los usuarios al sistema ademas de gestionar su información. Los usuarios autorizados podrán tener acceso a diferentes opciones dependiendo su nivel de autorización. Los roles del sistema son: Usuarios Aficionados (Compradores), Coleccionistas o Proveedores y Administradores.                                                                                                                                                                |
| R11  |        | El sistema debe ofrecer al Usuario Coleccionista (Comprador) la posibilidad de consultar sus órdenes de pedido asociadas a las respectivas compras realizadas. La información a consultar comprenderá los siguientes datos: nombre, correo, número de compras y medio de pago del Usuario Comprador.                                                                                                                                                                                      |
| R12  |        | El sistema en el momento de dar de baja a un Usuario Coleccionista (Proveedor) debe enviar a su correo toda la información de los pedidos que se le han realizado.                                                                                                                                                                                                                                                                                                                        |
| R13  |        | El sistema debe permitir al Usuario Coleccionista (Proveedor) confirmar o cancelar un pedido. Esta acción permite el envío de un correo al Usuario Aficionado (Comprador) con las observaciones en caso de ser cancelado o la fecha de de envio en el caso de ser confirmado.                                                                                                                                                                                                             |
| R14  |        | El sistema debe permitir al Usuario Coleccionista (Proveedor) consultar todas las ventas realizadas, esta información comprende la información de la orden de pedido.                                                                                                                                                                                                                                                                                                                     |
| R15  |        | El sistema debe permitir al Usuario Aficionado (Comprador) consultar todas las compras realizadas, esta información comprende la información del artículo.                                                                                                                                                                                                                                                                                                                                |
  
### Plan Global
| Ciclo   | Fecha Inicio  | Fecha Fin       | Semanas   |
|---------|---------------|-----------------|-----------|
| Ciclo 1 | 25 agosto     | 8 de septiembre | 2 semanas |
| Ciclo 2 | 8 septiembre  | 29 septiembre   | 3 semanas |
| Ciclo 3 | 29 septiembre | 20 octubre      | 3 semanas |
| Ciclo 4 | 20 octubre    | 10 Noviembre    | 3 semanas |


#### Ciclo 1 
##### Requerimientos Ciclo 1
| Cod. | Estado | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|------|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| R1   |        | El sistema debe ofrecer al comprador la opción de pagar la compra. Se debe mostrar un formulario para realizar el pago que despliega el total de la compra y el desglose en impuestos. Suponga que hay un impuesto a las ventas del 16% . Debe estar la posibilidad de seleccionar el tipo de tarjeta crédito/debito con el que se realizará el pago. Cuando el usuario selecciona pagar, el sistema debe guardar la información sobre el pago de forma persistente en la base de datos.  |
| R2   |        | El sistema debe ofrecer al comprador la posibilidad de agregar comentarios sobre los productos. El comentario va  asociado con un producto específico y es una descripción en texto libre de no más de 255 caracteres. Los comentarios asociados con los productos se deben persistir incluyendo la fecha, el usuario y la descripción.                                                                                                                                                   |
| R3   |        | El sistema debe ofrecer al usuario con el rol de administrador el servicio de ver los usuarios registrados en la aplicación y sus roles. Se debe agregar el rol de administrador en Stormpath (el mecanismo de seguridad que está utilizando la aplicación) Ir a la URL: .../webresources/users/findAll para ver el requerimiento.                                                                                                                                                                                                                               |
| R4   |        | El sistema debe ofrecer al comprador la posibilidad de registrar preguntas sobre un producto de un proveedor específico. La pregunta se debe persistir con el producto al que hace referencia, el usuario, su email, la fecha y la descripción.  Cuando se registre la pregunta al proveedor al proveedor debe llegarle una notificación por email.                                                                                                                                       |
| R5   |        | El sistema debe ofrecer al comprador la posibilidad de realizar una búsqueda sobre el catálogo de productos que retorne el producto más barato de un proveedor dado o el proveedor que ofrece el producto más barato de un tipo de producto dado.                                                                                                                                                                                                                                         |
| R6   |        | El sistema debe ofrecer al proveedor la posibilidad de agregar un descuento especial a alguno de sus productos. Esta información debe desplegarse en el catálogo.                                                                                                                                                                                                                                                                                                                         |

##### Ciclo 1 Semana 1
| Tarea                                                   | Integrante  | Tiempo Estimado | Tiempo Real |
|---------------------------------------------------------|-------------|-----------------|-------------|
| Subir el documento al repositorio de la Wiki            | Jorge       | 10min.          | 30min.      |
| Revisión individual de la Arquitectura.                 | Todos       | 30min.          |             |
| Desplegar la aplicación en la máquina virtual           | Todos       | 120min.         |             |
| Hacer el prototipo de diagrama de Funcional. (Cacoo)    | Camilo      | 60min.          | 55min.      |
| Hacer el prototipo de diagrama de Despliegue. (Cacoo)   | Viviana     | 60min.          | 60min.      |
| Hacer el prototipo de diagrama de Desarrollo. (Cacoo)   | Juan Daniel | 60min.          | 60min.      |
| Definición de requerimientos actuales en la aplicación. | Jorge       | 60min.          | 60min.      |
| Analizar los resultados de SonarQube.                   | Juan David  | 60min           | 40min.      |

##### Ciclo 1 Semana 2
| Tarea                                                                                                 | Integrante  | Tiempo Estimado | Tiempo Real |
|-------------------------------------------------------------------------------------------------------|-------------|-----------------|-------------|
| R1                                                                                                    | Juan Daniel | 170min.         | 300min.     |
| Realizar backend entidad PurchaseDetail                                                               |             | 30min.          | 40min.      |
| Realizar backend entidad Purchase                                                                     |             | 60min.          | 60min.      |
| Realizar frontend pagos                                                                               |             | 60min.          | 180min.     |
| Realizar pruebas                                                                                      |             | 20min.          | 20min.      |
| R2                                                                                                    | Viviana     | 330min.         | 510min.     |
| Backend Comment: Adicionar la lógica y la persistencia para la nueva entidad Comment.                 |             | 60min.          | 60min.      |
| Frontend Comment: View: Ajustar el template de catálogo.                                              |             | 60min.          | 120min.     |
| Frontend Comment: Ctrl: Crear un controlador.                                                         |             | 60min.          | 120min.     |
| Frontend Comment: Srv: Crear un nuevo servicio                                                        |             | 60min.          | 120min.     |
| API Rest Comment: Crear un nuevo servicio Rest que permita registrar un nuevo comentario              |             | 60min.          | 60min.      |
| Realizar prueba unitarias                                                                             |             | 30min.          | 30min.      |
| R3                                                                                                    | Camilo      | 50min.          | 32min.      |
| Stormpath: Admin Role                                                                                 |             | 10min.          | 5min.       |
| BackEnd:Client & Provider Logic                                                                       |             | 20min.          | 10min.      |
| BackEnd: IClient & IProvider Interface                                                                |             | 5min.           | 2min.       |
| BackEnd: (User) Client & Provider Services                                                            |             | 10min.          | 10min.      |
| BackEnd: CrudPersistence                                                                              |             | 5min.           | 5min.       |
| R4                                                                                                    | Jorge       | 120min.         | 270min.     |
| BackEnd: Entidades                                                                                    |             | 20min.          | 30min.      |
| BackEnd: Logica                                                                                       |             | 20min.          | 30min.      |
| BackEnd: Servicios                                                                                    |             | 20min.          | 30min.      |
| FrontEnd: Template                                                                                    |             | 30min.          | 120min.     |
| FrontEnd: Logica                                                                                      |             | 30min.          | 60min.      |
| R6                                                                                                    | Juan David  | 60min.          | 75min.      |
| Persistencia: Agregar descuento al LongPlayEntity y que el cambio se vea reflejado en la DB           |             | 20min.          | 35min.      |
| Backend: Ajustar el modelo y las conversiones de DTOs                                                 |             | 20min.          | 14min.      |
| Frontend: Ajustar el modelo de AngularJS y mostrar el nuevo campo en la vista                         |             | 20min.          | 26min.      |

##### Conclusiones Ciclo 1
* Comenzar a hacer:
  *  Mejorar el manejo de los tiempos
  *  Reuniones más seguidas de los pendientes del trabajo
  *  Socializar las tareas transcurso de la semana.
* Más de:
  *  Afianzar la comunicación y el trabajo en equipo.
  *  Reunión física del grupo.
  *  Reuniones por Skype para seguimiento del trabajo.
  *  Apoyar las actividades de los compañeros
* Seguir haciendo:
  *  Trabajar en equipo
  *  Utilizar herramientas de colaboración como Google Drive
* Dejar de hacer:
* Menos de:
  *  Reuniones rápidas y sin socialización

#### Ciclo 2
##### Requerimientos Ciclo 2
| Tarea | Integrante | Justificación                                                                                                                                                                                                                                                                                                                                                                                                                                                                 | Tiempo Estimado | Tiempo Real |
|-------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------|-------------|
| R5    | Viviana    | Dado que en este sitio web los clientes pueden comprar, se genera mayor valor a la aplicación si se ofrece la posibilidad de buscar productos más baratos que se puedan vender. Adicionalmente, se agregaría usabilidad a la aplicación. Un cliente que realice una compra después de buscar un producto a través de esta funcionalidad, seguramente la volverá a usar.                                                                                                       |                 |             |
| R8    | Jorge      | Se evidencia la necesidad de complementar la información del catálogo con la información detallada del LP como es (nombre, precio, año, stock) además con información de las canciones que lo componen. Esto permitirá al usuario aficionado conocer mejor el producto, aumentará el interés por los artículos y reduciría la carga operativa del coleccionista contestando preguntas sobre los LP.                                                                           |                 |             |
| R10   | Juan Daniel| La correcta navegación en la aplicación le aporta a la aplicación usabilidad, ya que se puede validar que los diferentes tipos de usuario tengan acceso, solo a las opciones habilitadas para su rol, y permite que tareas que dependen de otras, puedan hacerse más fácilmente por otros desarrolladores sin tener que depender de saber URIs de acceso a recursos de la aplicación.                                                                                         |                 |             |
| R14   | Juan David | Pensando en la funcional del proveedor, creemos que es importante para este ciclo mostrar las compras realizadas a un proveedor para que ésta las peuda gestionar, funcionalidades que se desarrollarán en el siguiente ciclo.                                                                                                                                                                                                                                                |                 |             |
| R15   | Camilo     | Decidimos que para este ciclo ya era importante empezar a pensar en los reportes de la aplicación, asi que ahora el usuario podrá ver las compras realizadas.                                                                                                                                                                                                                                                                                                                 |                 |             |

##### Conclusiones Ciclo 2
* Comenzar a hacer:
  *  Utilizar las opciones avanzadas de YouTrack para afinar los tiempos de estimación.
  *  Detallar los requerimientos en tareas más pequeñas
  *  Revisar la deuda técnica de Sonar para mejorar la calidad del proyecto.
* Más de:
  *  Reuniones más seguidas de los pendientes del trabajo
  *  Afianzar la comunicación y el trabajo en equipo.
  *  Reunión física del grupo.
  *  Reuniones por Skype para seguimiento del trabajo.
  *  Apoyar las actividades de los compañeros
* Seguir haciendo:
  *  Trabajar en equipo
  *  Utilizar herramientas de colaboración como Google Drive
  *  Revisar periódicamente los cambios en el moodle
* Dejar de hacer:
  *  Comprometernos con horarios de reuniones en las que no podemos estar.
  *  Esperar a último momento para pedir ayuda 
* Menos de:
  *  Reuniones rápidas y sin socialización
  *  Ejecución de tareas sin tener la planeación
  
##### Plan Mejoramiento
Para la próxima iteración se espera mejorar en los siguientes aspectos:
* Reuniones más seguidas de los pendientes del trabajo
* Afianzar la comunicación y el trabajo en equipo.
* Reunión física del grupo.
* Reuniones por Skype para seguimiento del trabajo.
* Apoyar las actividades de los compañeros
 
### Ciclo 3

#### Conclusiones Ciclo 3

(https://youtu.be/m_VSgfArLck)

###### Requerimientos y Controles de cambios desarrollados para el ciclo 3

|     	| Requerimiento                                                                                                                                                                                                                                                                                                                                                                                                                                                                            	| Estado 	| Adiciones / Cambios                                                                                                                                                                                      	| CICLO 3 	|
|-----	|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------	|--------	|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------	|---------	|
| R1  	| El sistema debe ofrecer al comprador la opción de pagar la compra. Se debe mostrar un formulario para realizar el pago que despliega el total de la compra y el desglose en impuestos. Suponga que hay un impuesto a las ventas del 16% . Debe estar la posibilidad de seleccionar el tipo de tarjeta crédito/debito con el que se realizará el pago. Cuando el usuario selecciona pagar, el sistema debe guardar la información sobre el pago de forma persistente en la base de datos. 	| OK     	| Escoger en el formulario varios medios de pago: tarjeta débito, crédito, PSE y paypal. Debe dar feddback al usuario: un mensaje sobre el resultado del pago (simulando que el pago se hizo)              	| Camilo  	|
| R2  	| El sistema debe ofrecer al comprador la posibilidad de agregar comentarios sobre los productos. El comentario va asociado con un producto específico y es una descripción en texto libre de no más de 255 caracteres. Los comentarios asociados con los productos se deben persistir incluyendo la fecha, el usuario y la descripción.                                                                                                                                                   	| OK     	| Los comentarios deben poder visualizarse desde la selección del disco.Los comentarios deben ser en modo foro donde otros usuarios pueden continuar la conversación.                                      	| Viviana 	|
| R7  	| El sistema debe ofrecer al usuario aficionado la posibilidad de comprar vinilos coleccionables, estos serán ofrecidos mediante catálogo por los coleccionistas (proveedores). Se habilitará un carrito de compra para agregar los artículos que se desean adquirir una vez sean seleccionados del catálogo.                                                                                                                                                                              	| OK     	| - La sistema debe permitir escuchar las canciones de los discos (en formato digital of course)- Implementar dentro de la compra el ingreso de los datos como direccción, teléfono fijo y teléfono móvil. 	| Jorge   	|
| R8  	| El sistema debe permitir al usuario coleccionista ofrecer sus vinilos a través del marketplace. La información del catálogo comprenderá los siguientes datos por artículo: nombre, artista, el año de salida al mercado discográfico, el conjunto de canciones que lo componen, un precio determinado y una cantidad de unidades en inventario.                                                                                                                                          	| OK     	| Agregar al disco los premios que obtuvo sin momento (si tuvo alguno) además de una reseña histórica sobre su producción.                                                                                 	| Ivan    	|
| R13 	| El sistema debe permitir al Usuario Coleccionista (Proveedor) confirmar o cancelar un pedido. Esta acción permite el envío de un correo al Usuario Aficionado (Comprador) con las observaciones en caso de ser cancelado o la fecha de de envio en el caso de ser confirmado.                                                                                                                                                                                                            	|        	|                                                                                                                                                                                                          	| Harold  	|

###### Lineas Código x Requerimiento

| Responsable |   Requerimiento   | Front | Servicios | Back | Prueba Back | Pruebas Servicios | Pruebas Front |
|-------------|-------------------|-------|-----------|------|-------------|-------------------|---------------|
| Viviana     | Ctrl Cambio Req 2 |   204 |         0 |   23 |         208 |                   |               |
| Harold      | Req 13            |   175 |        30 |  293 |          70 |                   |               |
| Ivan        | Req 8             |    50 |         0 |   80 |          30 |               107 |               |
| Camilo      | Ctrl Cambio       |    35 |         0 |   19 |         194 |               132 | -             |
|             | Req 1             |       |           |      |             |                   |               |

###### Porcentaje de requerimientos completos implementados 

| REQ/SOLICITUD CAMBIO | Responsable | Estado |
|----------------------|-------------|--------|
| Control de Cambio R1 | Camilo      | OK     |
| Control de Cambio R2 | Viviana     | OK     |
| Control de Cambio R7 | Jorge       | OK     |
| Control de Cambio R8 | Ivan        | OK     |
| Requerimiento 13     | Harold      | OK     |

Porcentaje de requerimientos completos implementados = 100%

###### Matriz de Requerimientos

![](src/c3/MR.png?raw=true)


###### Cubrimiento de Pruebas

![](src/c3/007.PNG?raw=true)

Se evidencia que se logro el objetivo de aumentar sobre el 50% el cubrimiento de pruebas con un exito en los test del 100%
* Avance importante en cobertura de pruebas de backend.
* Retos importantes en materia de cobertura a nivel de pruebas de servicios y funcionales.

###### Metricas

###### Costo Planeado

En la planeación se incluye los requerimientos ya mencionados, controles de cambios y pruebas unitarias en mayor medida
YouTrack(http://longplay.myjetbrains.com/youtrack/dashboard)

![](src/c3/VP.png?raw=true)

https://docs.google.com/spreadsheets/d/1hHDvo6LaYY1dJhJY9RM-u4D4K7Xa-q4GpMsBNGspgMQ

###### Costo Acumulado vs Ganado

Se puede observar que las tareas fueron sobrestimadas en mayor medida como lo muestra la gráfica

![](src/c3/VG.png?raw=true)

###### Plan de mejora para el ciclo 4: los tres puntos más críticos.

* Planear a tiempo la ejecución de las pruebas, para evitar inconvenientes al final del ciclo y tener mayor cubrimiento de código en las pruebas tanto en el back como en los servicios y front.
* Comunicar los problemas que se tengan con GitHub al momento de subir cambios y ayudar entre todos a la solución. Esto con el fin de resolver los problemas y no perder trabajo.
* Subir los tests siempre probados, para no tener problemas con la ejecución del proyecto a nivel local.

###### Objetivos para el ciclo 4 con respecto al producto:

* Entender los requerimientos faltantes y realizar asignación de los requerimientos a desarrollar.
 * Métrica Relacionada = Requerimientos a desarrollar / Requerimientos faltantes * 100.

* Entender los controles de cambio y seleccionar los que se van a desarrollar durante el ciclo para cumplir con las expectativas del cliente.
 * Métrica Relacionada = Controles de cambio a desarrollar / Total Controles de cambio * 100.

* Realizar pruebas unitarias para garantizar la funcionalidad y calidad de los entregables.
 * Métrica Relacionada = No pruebas unitarias * No de requerimientos desarrollados.

* Realizar integración continua con Github.
 * Métrica Relacionada = Version Control System Load Time (Unit of Measurement - Horas / Minutos/ Segundos).

* Realizar el análisis post-mortem y cerrar el proyecto con la aprobación del cliente.

###### Reflexiones individuales del equipo

Viviana:
En la retroalimentación de mis compañeros, hay varias reflexiones positivas que debo mantener, sin embargo debo mejorar la comunicación con el equipo de trabajo y solicitar ayuda cuando la necesite sobre todo a nivel técnico. 

Jorge:
En la retroalimentación se me comunican aspectos positivos, aunque debo ser más juicioso con control al proceso de desarrollo, siendo lider falta realizar tareas de seguimiento más detalladas al mismo tiempo que hallar más espacio de encuentro en el grupo. "Mi compañera Viviana hace énfasis en mejorar la comunicación y que desempeñaria mejor el cargo :P".

Iván:
Después de haber recibido la retroalimentación por parte de mis compañeros de grupo, me gustaría resaltar que tengo que mejorar un poco en la comunicación con los demás integrantes del grupo, participar más en las reuniones y mostrar más liderazgo. Por otra parte, los compañeros comentan que como nuevo integrante en el grupo me he integrado bien, demuestro interés al equipo y mi desempeño ha sido bueno.

Harold:
Como reflexión personal y basado en los comentarios de mi grupo de trabajo, es importante que tome una actitud más comunicativa, participativa y de liderazgo con el grupo, de tal forma que mis compañeros puedan sentir que soy un apoyo para ellos con cualquier reto que se presente. Por todo lo demás, me siento a gusto con todos los comentarios positivos recibidos por parte del grupo y con la bienvenida que me han dado luego del cambio de grupos.

Camilo:
Es muy importante aprender a utilizar las herramientas de control de versiones para poder trabajar en un proyecto de software con varios desarrolladores. Tuve varias complicaciones usando git y esto afectó mi trabajo y el de mis compañeros. Además, debo prestar más atención a detalles de usabilidad que no fueron acordes a la labor que mis compañeros hicieron, con un poco más de dedicación e investigación podría haber aportado con artefactos de mayor calidad al trabajo del equipo.

###### Reflexión grupal estrella de mar

* Comenzar a hacer…
 *  Poner fechas para tareas administrativas que supongan dependencias con otras tareas.
 *  Revisar que tan completo es el enunciado del requerimiento o control de cambio que desarrollaremos.
 *  Revisión más minuciosas del código que se sube a master, para dar cumplimiento a variables como la complejidad, la duplicidad de código, mantenibilidad, documentación, etc.
 *  Notificación al equipo cuando se suban cambios relevantes al repositorio.
 *  Automatización de tareas, acompañada de creación de interfaces que permitan reducir la cantidad de código necesario para completar un requerimiento.

* Más de…
 *  Revisiones de la calidad del código desarrollado
 *  Pruebas de backend, servicios y funcionales que supongan una mayor cobertura del código desarrollado.
 *  Comunicar las dificultades que se presenten con el equipo, para así poder encontrar una solución.

* Seguir haciendo…
 *  Reuniones de planeación y seguimiento y control.
 *  División organizada y acordada de las tareas a desarrollar.
 *  Registro de tareas y tiempos de las mismas en youtrack.
 *  Ser un equipo autogestionado y proactivo.

* Dejar de hacer…
 *  Acumular trabajo administrativo para el final del ciclo.
 *  LLegar tarde a las reuniones para sacarles más provecho a las mismas.
 *  Desarrollar un requerimiento, aún cuando existen dudas.

* Menos de…
 *  Subestimar una tarea.
 *  No entregar tareas a tiempo.


#### Ciclo 4

##### Requerimientos Ciclo 4

|Requerimiento|Responsable|
|-------------|-----------|
|R16: Presentar el top de los tres álbumes más vendidos en la tienda a la fecha de consulta. El top debe ser visible a primera vista por el usuario.|Harold|
|R17: Presentar la opción de compartir en Redes Sociales cada Disco de Vinilo.|Ivan|
|R18: Presentar el detalle de cada Disco de Vinilo en una ventana emergente de fácil uso. Esto permitirá mejorar la presentación del Catálogo y que el usuario tenga toda la información de un disco en un solo sitio. |Ivan|

##### Análisis resultados de la encuestas (individual)

* **Viviana**: En general los resultados de la encuesta han sido positivos. Creo que debo mejorar la comunicación con el equipo de trabajo, sobre todo para ayudar a liderar de mejorar manera el proyecto, en búsqueda de cumplir con los objetivos del proyecto.

* **Ivan**: En este ciclo mis compañeros han visto mi trabajo y han notado que he   estado pendiente de las entregas y las reuniones, además mis compañeros han apreciado mi trabajo en equipo, mi esfuerzo y mi colaboración. Por mejorar mis compañeros señalan que me falta participar un poco más en las reuniones y adicionalmente revisar bien los ajustes cuando subo cambios al repositorio. Además debo mejorar la comunicación con los demás compañeros del grupo y presentar mayor liderazgo.

* **Jorge**: Esta iteración se me ha notado un poco disperso, necesito empoderar más las actividades del grupo y velar por que el objetivo del grupo se cumpla. Debo tener cuidado con los cambios que subo al repositorio ya que esta iteración tuve inconvenientes.

* **Camilo**: Mis compañeros han valorado y apreciado el esfuerzo que he puesto en el trabajo. A pesar de no haber tomado un papel de liderazgo en el equipo, el asistir con puntualidad y disposición a las reuniones, ser receptivo a las instrucciones que se me daban, me permitió cumplir con todas mis tareas, a tiempo y con calidad. Se me había recomendado tener más cuidado al momento de subir cambios al repositorio, pues había afectado el trabajo de mis compañeros. Pero en este último ciclo se notó una mejoría en este aspecto. Debo mejorar un poco la comunicación con el equipo también.

* **Harold**:  Al revisar los comentarios de mis compañeros en general encuentro  un balance positivo, sin embargo aún hay es posible mejorar en la parte de la comunicación con mis compañeros, lograr ser más proactivo y dar un mayor aporte al grupo, todo lo anterior con el objetivo de conseguir un equipo autogestionado y enfocado en un mismo objetivo. Por todo lo demás el grupo se encuentra a gusto con el compromiso que he mostrado, la puntualidad y dedicación impuesta en cada tarea de los ciclos de trabajo.


##### Métricas del producto

######  Totalizar las nuevas líneas de código incluidas en el ciclo cuatro, separándolas por front, servicios, back y pruebas de cada capa.

|Responsable|Requerimiento|Front|Servicios|Back|Pruebas Back|Pruebas Servicios|Pruebas Front|
|-----------|-------------|-----|---------|----|------------|-----------------|-------------|
|Camilo     |Req 1        |-    |-        |-   |167         |220              |-            |
|Camilo     |Req 2        |-    |-        |-   |180         |230              |-            |
|Camilo     |Req 3        |-    |-        |-   |252         |-                |-            |
|Camilo     |Req 4        |-    |-        |-   |139         |225              |-            |
|Camilo     |Req 5        |-    |-        |-   |154         |-                |-            |
|Camilo     |Req 6        |-    |-        |-   |166         |-                |-            |
|Camilo     |Req 7        |-    |-        |-   |154         |229              |-            |
|Camilo     |Req 8        |-    |-        |-   |192         |223              |-            |
|Harold     |Req 16       |60   |45       |35  |80          |-                |-            |
|Ivan       |Req 17       |62   |-        |-   |-           |-                |-            |
|Ivan       |Req 18       |56   |-        |-   |-           |-                |-            |


###### Reportar el porcentaje de requerimientos completos implementados 

Porcentaje de requerimientos completos implementados = 100%

|Requerimiento|Responsable|Estado|
|-------------|-----------|------|
|R16: Presentar el top de los tres álbumes más vendidos en la tienda a la fecha de consulta. El top debe ser visible a primera vista por el usuario.|Harold|Ok|
|R17: Presentar la opción de compartir en Redes Sociales cada Disco de Vinilo.|Ivan|OK|
|R18: Presentar el detalle de cada Disco de Vinilo en una ventana emergente de fácil uso. Esto permitirá mejorar la presentación del Catálogo y que el usuario tenga toda la información de un disco en un solo sitio. |Ivan|OK|


###### Reportar el desarrollo y cubrimiento de las pruebas

Cobertura Total  = 71,5%
Cobertura de Líneas = 72,7%
Éxito De Los Test = 100%


###### Reportar los costos de calidad

|Costo Calidad|Esfuerzo (Horas)|
|-------------|----------------|
|Costo Conformidades|53,5|
|Costo No Conformidades|5,3|

##### Métricas de proceso

###### Deuda ténica

![](src/c4/deudatecnica4.png?raw=true)


###### Cobertura de pruebas

![](src/c4/cobertura4.png?raw=true)

###### Análisis de valor ganado


[Valor Ganado](https://docs.google.com/spreadsheets/d/1hHDvo6LaYY1dJhJY9RM-u4D4K7Xa-q4GpMsBNGspgMQ/edit#gid=1872414869)


![](src/c4/valorganadograf4.png?raw=true)

En las estimación de ciclo cuatro se encuentran tareas de las distintas etapas del proceso de desarrollo, aunque en este ciclo se quiso dar énfasis en tareas que habían quedado pendientes en las anteriores iteraciones como son pruebas unitarias, además de tareas sugeridas mediante retroalimentación como la mejora del aspecto visual de la aplicación y navegabilidad en las funcionalidades. Luego se la estimación se planearon tareas de los cinco integrantes con un total de 73 horas.


![](src/c4/valorganado4.png?raw=true)

###### Productividad del equipo

![](src/c4/valoracumvsgan4.png?raw=true)

Luego de la finalización de la tareas del proceso de desarrollo en comparación con nuestro historias de tareas hubo un desfase por sobreestimación de 27% en la planeación del ciclo, cabe resaltar que con respecto a iteraciones pasadas fue una mejora en nuestro proceso. En este ciclo se cumplieron con todas las tareas planeadas. Para el registro de la planeación y seguimiento se utilizó YouTrack en donde se registra la trazabilidad de las tareas realizadas [Youtrack](http://longplay.myjetbrains.com/youtrack)

##### Reflexión de la estrella de mar

###### Reflexión individual

* Viviana:

**Comenzar a hacer:**
Realizar ajustes resultados de las pruebas de inspección antes de desarrollar y ejecutar las pruebas unitarias.
Automatizar tareas de gestión de proyectos.

**Más de:**
Revisión las tareas pendientes para que no se quede trabajo por fuera del ciclo.
Afianzar la comunicación y el trabajo en equipo.
Apoyar las actividades de los compañeros

**Seguir haciendo:**
Realizar la planeación semanal de cada ciclo.
Utilizar herramientas de colaboración como Google Drive.

**Dejar de hacer:**
Dejar muchas tareas para el final del ciclo.

**Menos de:**
Asignación de tareas sin seguimiento y control.

* Ivan:

**Comenzar a hacer:**
Aportar un poco más al grupo y no concentrarse sólo en mis tareas asignadas.

**Más de:**
Afianzar la comunicación y el trabajo en equipo.
Apoyar las actividades de los compañeros

**Seguir haciendo:**
Reuniones cortas y concisas para revisar el avance de las tareas y las tareas pendientes.
Comunicarse con los compañeros cuando no funciona el código y arreglarlo.
revisar constantemente Sonar para corregir issues.
Estar pendiente del avance de todas las tareas del ciclo.

**Dejar de hacer:**
Dejar de empezar la mayor parte de tareas al final del ciclo
Dejar de subir código con errores o bugs

**Menos de:**
Comunicarnos entre los compañeros hasta esperar a la reunión, podemos estar comunicándonos constantemente para solucionar dudas y problemas.

* Camilo:
 
**Comenzar a hacer:**
Utilizar los pull request en lugar de subir directo a Master.
Revisar los pull request de mis compañeros y dar comentarios pertinentes.
Utilizar Travis.

**Más de:**
Pruebas de integración.
Liderazgo y voluntariado para hacer más tareas.
Revisar SonarQube.
Probar los test individualmente, una vez se hacen.

**Seguir haciendo:**
Pruebas unitarias.
Cumplir con todas mis tareas.
Registrar tiempos y estados en YouTrack.
Bajar la deuda técnica.
Asistir a todas las reuniones propuestas por el equipo.

**Dejar de hacer:**
Dejar tanto trabajo acumularse para la última semana del ciclo.
Estimar tareas sin pensarlo a conciencia.
Bloquear a mis compañeros por no completar tareas, necesarias para que ellos puedan continuar.

**Menos de:**
Realizar pruebas sin tener presente que requerimiento se verá afectado con estas.
Esperar a terminar todas las pruebas para probarlas.

* Harold:

**Comenzar a hacer:**
Inspecciones y revisiones por pares
Hacer la entrega de los requerimientos a otro compañero.
Planear siempre tareas de mejora.

**Más de:**
Inspecciones de código estático.
Pruebas unitarias, de servicios y de front.
Automatización de tareas, principalmente administrativas y de cierre de ciclo.
Seguir haciendo
Reuniones por skype.
Planeaciones, seguimiento y control en cada ciclo.


**Dejar de hacer:**
Subir código con bajo cubrimiento de pruebas.
Postergar tareas del ciclo.

**Menos de:**
Tareas sin responsable o sin fecha de entrega.

* Jorge:

**Comenzar a hacer:**
Utilizar conjuntamente el set de integración contínua, en especial travis
Investigación e implementación de pruebas de servicios y front livianas y sin tanta complejidad

**Más de:**
Seguimiento de tareas como líder del grupo
Análisis concienzudo de las herramientas de planeación y seguimiento
Diligenciamiento de registros del procesos de desarrollo

**Seguir haciendo:**
Pruebas unitarias
Reducción de deuda técnica
Reuniones periódicas y seguimiento

**Dejar de hacer:**
Código con bajo cubrimiento de pruebas

**Menos de:**
Restarle importancia a las tareas y aplazarlas
Deja tareas de seguimiento para las últimas etapas del proceso

###### Reflexión grupal

* **Comenzar a hacer:**
Desarrollar las pruebas de servicios y funcionales que garanticen el correcto comportamiento del sistema.
Construir código que tenga en cuenta el plan de calidad de Sonar con el fin de dar cumplimiento a las reglas de complejidad,  duplicidad de código, mantenibilidad, documentación, etc.
Notificar al equipo cuando se suban cambios relevantes al repositorio de código fuente.
Rotar de responsable la actividad de la deuda técnica, para que así todos tengan mucho más presentes los perfiles de calidad y eviten incurrir en no conformidades en sus desarrollos.

* **Más de:**
Mantener una comunicación efectiva con el equipo.
Automatización de tareas, bien sea administrativas o del desarrollo mismo del software.
Seguir haciendo
Registrar la matriz de trazabilidad para los nuevos requerimientos desarrollados.
Cumplir con las tareas asignadas.

* **Dejar de hacer:**
Subir pruebas al repositorio sin éxito de ejecución.
Subir código sin probar.
Subir código sin realizar inspección de código estático.

* **Menos de:**
Dejar la mayoría de las tareas para la última semana del ciclo.
No participar activamente en las reuniones.
No pedir ayuda cuando tengo algún problema desarrollando alguna de mis tareas.

* **Comenzar a hacer:**
Desarrollar las pruebas de servicios y funcionales que garanticen el correcto comportamiento del sistema.
Construir código que tenga en cuenta el plan de calidad de Sonar con el fin de dar cumplimiento a las reglas de complejidad,  duplicidad de código, mantenibilidad, documentación, etc.
Notificar al equipo cuando se suban cambios relevantes al repositorio de código fuente.
Rotar de responsable la actividad de la deuda técnica, para que así todos tengan mucho más presentes los perfiles de calidad y eviten incurrir en no conformidades en sus desarrollos.

* **Más de:**
Mantener una comunicación efectiva con el equipo.
Automatización de tareas, bien sea administrativas o del desarrollo mismo del software.

* **Seguir haciendo:**
Registrar la matriz de trazabilidad para los nuevos requerimientos desarrollados.
Cumplir con las tareas asignadas.

* **Dejar de hacer:**
Subir pruebas al repositorio sin éxito de ejecución.
Subir código sin probar.
Subir código sin realizar inspección de código estático.

* **Menos de:**
Dejar la mayoría de las tareas para la última semana del ciclo.
No participar activamente en las reuniones.
No pedir ayuda cuando tengo algún problema desarrollando alguna de mis tareas.


##### Lecciones aprendidas y aspectos de mejora

El conjunto de procesos que aprendimos en el curso, nos ayudarán a aumentar la probabilidad de desarrollar proyectos exitosos, especialmente, pero no limitándose al campo del desarrollo de software. Aprendimos no solo a cumplir el objetivo final del proyecto, sino a tener en cuenta el alcance, tiempos y costos previstos, asegurarse de mantenerse entre estos límites, conocer los riesgos que se pueden presentar, y plantear estrategias para mitigarlos.

La calidad del proyecto debe poder ser cuantificable, por lo que el enfoque basado en pruebas, integración continua, control de cambios, y demás estrategias que aplicamos en el proyecto fueron claves para lograr asegurar que se tiene un producto de calidad.

Las metodologías ágiles de Software pueden ser peligrosas si no se aplican con cuidado. Hay que conocer bien los principios y aplicarlos juiciosamente para poder lograr buenos resultados. Uno de los principios más importantes es que el grupo de trabajo conozca bien sus responsabilidades y las de sus compañeros, mantener una comunicación abierta y efectiva, y realizar análisis personales y grupales, constantemente y de manera iterativa, para detectar así problemas de manera temprana y poder solucionarlos en la mayor brevedad posible.

##### Presentación:


[Presentación](https://docs.google.com/presentation/d/17v8yv4CCnR_Glscm8-HiNvbbQwL1pHckuP5fZAvrulE/edit?usp=sharing)

##### Guía de automatización de reporte de costo de la calidad:


https://drive.google.com/file/d/0Bx5yU89pi1SNOGtBTG9LNl9UVUE/view?usp=sharing
