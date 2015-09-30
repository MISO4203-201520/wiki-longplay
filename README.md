
## MARKETPLACE DE VENTA DE DISCOS DE VINILO COLECCIONABLES
El número de tiendas virtuales de música en Internet se ha incrementado en los últimos tiempos pero cada una busca la forma de diferenciarse para atraer distintos nichos de mercado. En esta aplicación se quiere atraer un público que últimamente ha venido creciendo y despertando gran interés para el mercado: los coleccionadores de discos de vinilo o los antiguos "Long Plays".

### Roles y Responsabilidades
| Nombres                       | Correo                        | Rol                  |
|-------------------------------|-------------------------------|----------------------|
| Baquero Jiménez Camilo        | c.baquero10@uniandes.edu.co   | Desarrollador        |
| Barrera Salgado Jorge Enrique | je.barrera11@uniandes.edu.co  | Desarrollador, Lider |
| Bastidas Melo Viviana Angely  | va.bastidas10@uniandes.edu.co | Desarrollador        |
| Garcia Manrique Juan David    | jd.garcia1381@uniandes.edu.co | Desarrollador        |
| Patiño Arevalo Juan Daniel    | jd.patino10@uniandes.edu.co   | Desarrollador        |

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

### Mitigación de Riesgos
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
![](src/img/001.PNG?raw=true)

En cuanto a documentación, podemos ver que el aplicativo tiene 71.4% de documentación. Esto quiere decir que la mayoría de las clases tienen en su definición una documentación mínima acerca de las funcionalidades que ofrecen. Analizando las clases que no se encuentran documentadas, encontramos que la mayoría son Interfaces utilizadas en el aplicativo.
#### Líneas de Código
![](src/img/002.PNG?raw=true)

Analizando las líneas de código, podemos ver que se trata de un proyecto relativamente pequeño, el cual contiene 64 archivos repartidos en 17 directorios. La gran mayoría del código hace parte de clases Java, mientras que una pequeña porción está destinada a la parte Web de la aplicación.
#### Duplicados
![](src/img/003.PNG?raw=true)

En cuanto a los duplicados, podemos ver que hay 15.1% de duplicado en 15 archivoss, esto quiere decir bloques que tienen más de 10 línes que se repiten a lo largo de todo el código.
#### Complejidad
![](src/img/004.PNG?raw=true)

Por otro lado, analizando la complejidad podemos ver que en general los métodos de la aplicación son poco complejos, teniendo una media de 1,9.
#### Deuda Técnica
![](src/img/005.PNG?raw=true)

En cuanto a la deuda técnica, podemos ver que es baja, teniendo un total de 86 evidencias. Analizando en detalle las evidencias, encontramos que las Críticas se debe a excepciones que no tienen Log o no son manejadas de forma adecuada (un total de 7). Por otro lado, en cuanto a evidencias Mayores encontramos duplicados en el código y ciertos warnings que pueden ser resueltos utilizando @Override. Finalmente, en cuanto a evidencias Menores, se encuentra la mala utilización de variables cuyas instancias pueden ser retornadas sin tener que ser asignadas a una variable temporal.

![](src/img/006.PNG?raw=true)

Analizando la pirámide de deuda técnica, encontramos que la mayoría de las evidencias hacen parte de la mantenibilidad y modificabilidad del aplicativo, aunque en confibabilidad tenemos una deuda técnica del 100%.

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

### Plan Semanal
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

##### Métricas
###### Costo Planeado
![](src/img/ciclo2_costo_planeado.PNG?raw=true)

###### Costo Acumulado vs Ganado
![](src/img/ciclo2_costo_acumulado_vs_ganado.PNG?raw=true)

###### Error Estimación
|           | Planeado | Ejecutado | %Error |
|-----------|----------|-----------|--------|
| Back End  | 60       | 6.5       | -89%   |
| Front End | 20       | 16        | -20%   |