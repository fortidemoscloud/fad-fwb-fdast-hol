# Hands on Lab Cloud Networking y Seguridad Aplicaciones Web & API

## Objetivo del laboratorio

El objetivo de estos laboratorios es conocer la propuesta de valor de Fortinet para proteger una aplicación web y una API desplegadas en un public cloud e integrada en una architectura de comunicaciones SDWAN multi-HUB. Las soluciones que harán posible esta protección son: FortiGate, FortiWeb Cloud, FortiADC y FortiDAST. En el workshop cada participante cuenta con un entorno en AWS compuesto de un fortigate publicando dos aplicaciones desplegadas en un nodo de Kubernetes. Durante el workshop se trabajará en conocer mejor la arquitectura SDWAN e integración con los servicios de routing del cloud provider y se llevará a cabo la publicación de las aplicacones a través de FortiWeb Cloud. En el proceso aprenderás a entrenar el modelo de Machine Learning (ML) de la API para conocer el esquema OpenAPI de la misma y aplicar mecanismos de protección sobre el mismo y también cómo proteger portales web frente a ataques TOP10 OWASP y otros ataques sofisticados.

Al margen de ello podremos comprobar el valor añadido que puede aportar nuestro servicio FortiDAST para evaluar de forma continua la postura de seguridad de nuestras aplicaciones y APIs.

El formato del laboratorio consiste en varios laboratorios diferenciados cuyos datos de acceso se pueden encontrar en la siguiente URL introduciendo el token que se habrá facilitado previamente a cada asistente por correo electrónico.

- https://www.fortidemoscloud.com

## Indice de laboratorios a completar

* [FortiADC](./FortiADC): balanceo y protección de aplicaciones en entorno hibrido.
* [FortiWeb](./FortiWeb): protección WEB y protección avanzada de APIs.
* [FortiDAST](./FortiDAST): análisis de vulnerabilidades de las aplicaciones.

## Diagrama general de los laboratorios

A continuación se recoge el diagrama general de los laboratorios disponibles para cada usuario:

- Un FortiGate con conexión SDWAN HUB activo-acitvo desplegados en AWS e integración con TGW. 
- Un FortiADC desplegado detrás del Fortigate, en el que se redirigen los puertos 31010 y 31011 contra este. 
- Dicho FortiGate dispone de una IP publica para publicar dichas aplicaciones en los puertos 31000 y 31001.
- Un nodo de Kubernetes con dos aplicaciones desplegadas a modo de backend y publicadas por el Fortigate y FortiADC. 
- Acceso a un entorno de FortiWEB cloud para poder dar de alta aplicaciones.
- Integración de FortiWEB Cloud con FortiDAST, para lanzar escaneos de aplicaciones de forma sencilla.  

## [FortiADC](./FortiADC)

En este laboratorio llevaremos a cabo las siguientes tareas:

- Creación de un pool de servidores usando el conector SDN y el conector de Kuberntes. 
- Creación de los Virtual Servers de cada una de las aplicaciones.
- Creación de perfiles WAF de protección de la aplicación. 
- Entender las nuevas funcionalidades de Adaptative Learning y como FortiADC sugiere protecciones mediante ML. 
- Publicación de las aplicaciones. 

<p align="center"><img src="images/image1.png" width="70%" align="center"></p>

## [FortiWeb](./FortiWeb)

En este laboratorio llevaremos a cabo las siguientes tareas:

- Creación de una nueva aplicación en FortiWeb Cloud con origen la aplicación web (DVWA) desplegada para cada usuario.
- Creación de una nueva aplicación en FortiWeb Cloud con origen la API (swagger pet store API) desplegada para cada usuario.
- Añadiremos los perfiles de seguridad necesarios para proteger la aplicación Web y la API publicadas.
- Creación de los FQDN asociados a cada aplicación para apuntar a la entrada de FortiWeb Cloud correspondiente.
- Pruebas de carga contra FortiWeb para que aprenda los patrones de tráfico pueda aplicar protección avanzada no basada en firmas, mediante ML.
- Ejercicios de RedTeam para probar la eficacia de la protección.

<p align="center"><img src="images/image2.png" width="70%" align="center"></p>

## [FortiDAST](./FortiDAST)

En este laboratorio llevaremos a cabo las siguientes tareas:

- Integración de FortiWeb Cloud con el servicio de análisis de vulnerabilidades de FortiDAST.
- Lanzamiento de escaneo sobre las aplicaciones desplegadas para identificar potenciales riesgos de las aplicaciones.
- Análisis de los resultados de los escaneos.

## Support
This a personal repository with goal of testing and demo Fortinet solutions on the Cloud. No support is provided and must be used by your own responsability. Cloud Providers will charge for this deployments, please take it in count before proceed.

