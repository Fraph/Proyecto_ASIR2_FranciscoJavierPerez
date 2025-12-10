[Volver al índice general](../README.md)

# UD1 – Análisis del entorno y detección de necesidades tecnológicas

## Índice de apartados

## **1. Análisis del sector tecnológico**
> En esta parte, usare como estandar del sector en Sevilla la informacion del techpark de sevilla (en la cartuja).

![tpn](/UD1/img/techpark.jpg)

### Situacion actual del sector tecnologico en sevilla

El sector tecnológico en Sevilla se ha consolidado como un pilar económico fundamental, evidenciado por los resultados del TechPark en 2024, que cerró con una facturación récord de 4.850 millones de euros (un 8% más que el año anterior). Aunque el ritmo de crecimiento muestra una ligera estabilización frente a ejercicios previos, el mercado demuestra una madurez robusta que se traduce directamente en empleo: el parque cuenta ya con 31.667 trabajadores (+7,2%) y 144 empresas de alta innovación, garantizando un entorno de trabajo cualificado y en constante expansión.

Específicamente en el ámbito TIC, vital para el perfil ASIR, operan 94 empresas especializadas que facturan 995 millones de euros y emplean a 11.967 profesionales. 

## **2. Selección de la empresa o contexto de trabajo**
> En esta parte eligire la empresa sobre la que hablare el resto del trabajo, describiendola.

#### Empresa seleccionada = Acceture

![accenture](img/accenture.jpg)

**Accenture** es una compañía multinacional líder en servicios profesionales que ofrece soluciones en estrategia, consultoría, digital, tecnología y operaciones. A nivel global, la empresa es un gigante del sector que opera en más de 120 países y cuenta con una plantilla de aproximadamente **779.000 empleados**, cerrando su último ejercicio fiscal con una facturación mundial de 69.670 millones de dólares. Su modelo de negocio se basa en la innovación tecnológica para ayudar a clientes de todas las industrias a mejorar su rendimiento y crear valor sostenible.

En el contexto nacional y local, Accenture tiene una presencia muy relevante. En España emplea a más de **18.000 profesionales**, siendo uno de los principales empleadores del sector tecnológico. Específicamente en **Andalucía**, la compañía ha consolidado dos grandes centros tecnológicos en Málaga y Sevilla, que suman conjuntamente más de 3.500 trabajadores. La sede de **Sevilla**, ubicada en el entorno de Cartuja (Sevilla TechPark), cuenta con alrededor de **1.600 empleados** especializados, funcionando como un *hub* crítico para el desarrollo de proyectos internacionales y soporte a infraestructuras complejas.

La elección de esta empresa como objeto de estudio para este proyecto no es casual. He seleccionado Accenture principalmente porque **realicé mis prácticas de formación (FCT) en sus oficinas de Sevilla el curso pasado**. Esta experiencia previa me permite contar con un conocimiento directo y realista sobre su organización interna, sus flujos de trabajo y las necesidades tecnológicas de sus departamentos, lo que aportará un valor añadido de veracidad y viabilidad a la propuesta técnica que desarrollaré a continuación.

      
## **3. Identificación de necesidades tecnológicas**

Durante los meses que estuve realizando las prácticas en el departamento de soporte, pude ver desde dentro cómo funcionaba la gestión del día a día. Aunque es una empresa tecnológica enorme, me di cuenta de que había un cuello de botella importante en el **control del inventario y la petición de material nuevo**.

El problema de fondo es que el software que utilizaban para calcular el stock era demasiado rígido. El sistema intentaba ajustar tanto las cantidades para no tener material parado, que a la mínima que surgía un imprevisto o entraba un grupo grande de empleados, nos quedábamos sin equipos de reserva. El algoritmo no tenía en cuenta los tiempos reales de entrega ni los picos de trabajo de la oficina de Sevilla, lo que nos dejaba muchas veces sin capacidad de reacción ante una urgencia.

Como consecuencia de esto, la forma de trabajar del equipo acababa siendo manual y poco eficiente. Para evitar quedarnos a cero, los técnicos nos veíamos obligados a pedir mucho más material del que realmente hacía falta, inflando los pedidos "por si acaso" el sistema volvía a fallar en sus cálculos. Al final, esta falta de fiabilidad en la herramienta provocaba que o bien faltaran portátiles cuando más se necesitaban, o bien se acumulara stock innecesario en el almacén por miedo a la escasez, sin que hubiese un control real de lo que teníamos.


## **4. Oportunidades y viabilidad del proyecto**

Tras detectar la ineficiencia en la gestión del stock, la solución propuesta consiste en la implementación de un sistema centralizado de Gestión de Activos de TI (ITAM) basado en software de código abierto (como *Snipe-IT* o *GLPI*), alojado en un servidor local de la delegación de Sevilla.

La implementación de este sistema transformará la logística interna del departamento de soporte, aportando los siguientes beneficios directos:

1.  **Eliminación de tiempos muertos (Productividad):** Al garantizar un *stock de seguridad* real mediante alertas automáticas, se elimina el tiempo de espera de los empleados que necesitan un equipo. Esto evita que la empresa pierda horas facturables por tener a técnicos parados sin ordenador.
2.  **Reducción del "Stock Muerto" (Ahorro económico):** El sistema permitirá ajustar los pedidos a la demanda real, evitando la compra excesiva de material "por pánico" que acaba depreciándose en el almacén sin usarse.
3.  **Trazabilidad y Control:** Se digitalizará el proceso de entrega y recogida de material mediante escaneado de códigos, eliminando los errores humanos de los registros manuales actuales y facilitando las auditorías internas.

El proyecto es **altamente viable** desde el punto de vista técnico por las siguientes razones:
* **Compatibilidad:** La solución se desplegará sobre un servidor Linux (Ubuntu Server/Debian) con arquitectura LAMP (Linux, Apache, MySQL, PHP), tecnologías estándar y robustas que se integran perfectamente en la red actual.
* **Recursos Existentes:** No es necesario adquirir nuevo hardware costoso. Se aprovechará la infraestructura de virtualización existente en la sede de Sevilla para desplegar la máquina virtual necesaria, reduciendo la barrera de entrada.
* **Escalabilidad:** Al ser una solución web, no requiere instalar software en los ordenadores de cada técnico; el acceso se realiza vía navegador, facilitando su adopción inmediata.

Al tratarse de un proyecto interno para una empresa que ya dispone de infraestructura, el coste principal radica en las horas de ingeniería (mano de obra) y no en la compra de licencias, lo que maximiza la rentabilidad.

A continuación, se presenta la estimación económica para la puesta en marcha:

| Concepto | Descripción | Coste Estimado |
| :--- | :--- | :--- |
| **Recursos Humanos** | 60 horas de Técnico Superior ASIR (Instalación, configuración y carga de datos) a 25€/hora. | 1.500,00 € |
| **Infraestructura Hardware** | Amortización de servidor virtual (vCPU, 8GB RAM, 100GB SSD) y consumo eléctrico anual estimado. | 350,00 € |
| **Licencias de Software** | Software Open Source (Licencia GNU/GPL) + S.O. Linux. | **0,00 €** |
| **Material Diverso** | Lector de códigos de barras USB y etiquetas de inventario. | 150,00 € |
| **Contingencia** | Margen del 10% para imprevistos. | 200,00 € |
| **TOTAL INVERSIÓN** | | **2.200,00 €** |

##### Conclusión de Viabilidad
El coste estimado de **2.200 €** es marginal comparado con las pérdidas que genera tener a empleados sin equipo o el sobrecoste de comprar portátiles innecesarios. Si el sistema evita la compra errónea de solo 2 o 3 portátiles de gama alta al año, **el proyecto se amortiza solo en los primeros meses**, lo que confirma su absoluta viabilidad económica.

## 5. Cumplimiento legal y normativo

La implementación del sistema de gestión de inventario en la sede de Sevilla debe regirse estrictamente por la normativa legal vigente en España y la Unión Europea. A continuación, se detallan las cuatro áreas legales críticas que afectan al proyecto:


**Reglamento General de Protección de Datos (UE) 2016/679** y a la Ley Orgánica 3/2018 (LOPDGDD).
* **Principio de minimización de datos:** Solo se registrarán los datos estrictamente necesarios para la gestión del activo (Nombre y Email), evitando datos sensibles.
* **Control de acceso:** El acceso a la base de datos estará restringido únicamente al personal del departamento de soporte técnico, garantizando la confidencialidad mediante autenticación segura.
* **Derechos ARCO:** Se garantizará que cualquier empleado pueda consultar qué dispositivos figuran a su nombre en el inventario.

El proyecto se basa en el uso de software de código abierto. Para garantizar la legalidad de la solución, se respetarán los términos de la licencia **GNU AGPL v3**.

* **Reconocimiento de autoría:** No se eliminarán los avisos de copyright ni los créditos de los desarrolladores originales en el pie de página de la aplicación.
* **Libertad de uso:** La empresa tiene derecho a usar el software para fines comerciales internos sin pagar royalties.
* **Modificación:** Si se realizara alguna modificación en el código fuente de la herramienta, esta deberá mantenerse abierta si se distribuye, aunque al ser de uso interno exclusivo, no es obligatorio publicar el código modificado externamente.

El despliegue y mantenimiento del servidor y la gestión física del inventario conllevan riesgos laborales que deben contemplarse bajo la **Ley 31/1995 de Prevención de Riesgos Laborales**:

* **Riesgos Ergonómicos (PVD):** El trabajo administrativo de catalogación implica el uso continuado de Pantallas de Visualización de Datos (PVD). Se garantizará el uso de sillas ergonómicas y pausas visuales según normativa.
* **Manipulación de Cargas:** El movimiento de servidores, cajas de portátiles y hardware en el almacén debe seguir las directrices de seguridad para evitar lesiones dorsolumbares.
* **Riesgo Eléctrico:** La manipulación del servidor físico y el cableado en el rack se realizará siguiendo los protocolos de seguridad eléctrica básicos.

## **6. Guion inicial del proyecto**

### Fase 1: Diseño y Preparación del Entorno
En esta primera etapa se definirá la **arquitectura lógica de la red**, estableciendo el esquema de direccionamiento IP y la ubicación del servidor dentro de la infraestructura de la empresa. Paralelamente, se llevará a cabo el **aprovisionamiento de recursos** en el entorno de virtualización, dimensionando la máquina virtual con la capacidad de procesamiento, memoria RAM y almacenamiento en disco necesarios para soportar la carga de trabajo prevista sin problemas de rendimiento.

### Fase 2: Instalación del Sistema Operativo
Una vez lista la máquina virtual, se procederá a la instalación limpia de **Ubuntu Server LTS**, seleccionado por ser un estándar de estabilidad y seguridad en entornos de servidores. Durante esta fase se realizarán las configuraciones base del sistema, incluyendo la **configuración de red estática** y las medidas de "hardening" o securización inicial, asegurando que el servidor esté actualizado y protegido antes de exponerlo a cualquier servicio.

### Fase 3: Despliegue de Servicios de Infraestructura
Con el sistema operativo operativo, se instalará la pila de software necesaria para soportar la aplicación web, conocida comúnmente como **stack LAMP** (Linux, Apache, MySQL/MariaDB y PHP). Se configurará el **servidor web Apache** para gestionar las peticiones de los usuarios y se inicializará el **motor de base de datos**, creando las tablas y usuarios necesarios para almacenar de forma segura toda la información del inventario.

### Fase 4: Implantación de la Solución de Inventario
En la fase central del proyecto se realizará el despliegue de **Snipe-IT**, la plataforma de gestión de activos de código abierto seleccionada. El proceso consistirá en la descarga del software, la gestión de sus dependencias y la **vinculación con la base de datos** creada anteriormente. Posteriormente, se realizará la **parametrización funcional** de la herramienta, adaptando las categorías de activos, las ubicaciones y las alertas de stock a la realidad operativa del departamento de soporte de la empresa.

### Fase 5: Validación y Documentación Final
Para concluir el proyecto, se ejecutará una batería de **pruebas integrales** que simularán el ciclo de vida real de los activos (altas, asignaciones, devoluciones y bajas) para garantizar que el sistema es estable y fiable. Finalmente, se redactará la **documentación técnica** y los manuales de usuario, entregando así una solución llave en mano lista para ser operada por el personal de la empresa.

## Enlaces a recursos de la unidad

- [Documentos de la unidad](./documentos/)
- [Diagramas e imágenes](./img/)

  ## Bibliografía / Webgrafía 
- Autor1, Título del libro o artículo, Editorial/Año.
- En cuanto a remuneracion (para el presupuesto): [michaelpage - estudios de remuneracion](https://www.michaelpage.es/prensa-estudios/estudios/estudios-de-remuneracion)
- Sobre ubuntu server, sistema operativo que se usaria: [Ubuntu server documentation](https://documentation.ubuntu.com/server/)
- Sobre apache y maria DB para el sistema LAMP: [mariadb](https://mariadb.com/docs/) [apache](https://httpd.apache.org/docs/2.4/)
- Sobre snipe-it, usado como sistema gestor de inventario: [snipe-it](https://snipe-it.readme.io/docs/installation)
