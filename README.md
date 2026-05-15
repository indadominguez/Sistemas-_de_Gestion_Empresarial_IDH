# Sistemas-_de_Gestion_Empresarial_IDH

## Introducción

En la actualidad, las empresas utilizan diferentes sistemas informáticos para gestionar su información y optimizar sus procesos. Estos sistemas se conocen como sistemas de gestión empresarial, y permiten organizar, automatizar y controlar las distintas áreas de una organización.

Aunque los sistemas ERP (Enterprise Resource Planning) son los más conocidos, no son los únicos. Existen otros tipos de sistemas especializados que cubren necesidades concretas dentro de la empresa. Por ejemplo, los sistemas CRM (Customer Relationship Management) se centran en la gestión de clientes, mientras que los sistemas de Business Intelligence (BI) permiten analizar datos y generar informes para la toma de decisiones.

## 1. Aplicaciones de gestión empresarial. Tipos. Características.

| Tipo | Función principal                                          |
| ---- | ---------------------------------------------------------- |
| ERP  | Integra y gestiona todos los procesos de la empresa        |
| CRM  | Gestiona clientes, ventas y relaciones comerciales         |
| BI   | Analiza datos y genera informes para la toma de decisiones |
| SCM  | Controla la cadena de suministro y logística               |
| HRM  | Gestiona empleados y recursos humanos                      |
| DMS  | Administra documentos y archivos digitales                 |



### 1. SAP ERP

Es uno de los sistemas ERP más utilizados en grandes empresas. Permite gestionar finanzas, logística, recursos humanos y producción desde una única plataforma integrada.

### 2. Microsoft Dynamics 365

Es una suite empresarial en la nube que integra ERP y CRM. Permite gestionar finanzas, ventas, atención al cliente y operaciones con integración con herramientas de Microsoft.

### 3. Oracle SCM Cloud

Es una solución SCM en la nube muy potente orientada a grandes empresas. Destaca por su gestión avanzada de finanzas, proyectos, compras y cadena de suministro.

### 4. Power BI

Es una herramienta de Business Intelligence (BI) desarrollada por Microsoft que permite analizar datos, crear informes interactivos y visualizar información de forma clara y profesional.

### 5. Odoo

Y por último el ERP que vamos a utilizar en el trabajo, "**ODOO**", es un ERP de código abierto muy popular. Ofrece módulos como ventas, contabilidad, inventario, CRM y recursos humanos, siendo muy flexible y personalizable.

**Pequeña tabla con las características principales de los ERP**

| Característica      | Descripción                           |
| ------------------- | ------------------------------------- |
| Modularidad         | Se dividen en módulos independientes  |
| Integración         | Todos los datos están conectados      |
| Automatización      | Reducción de tareas manuales          |
| Escalabilidad       | Se adaptan al crecimiento empresarial |
| Acceso centralizado | Información disponible en tiempo real |

---

## 2. Instalación.

### 2.1 Docker
Lo primero que hemos realizado ha sido la instalación de **docker**( plataforma de código abierto que permite empaquetar aplicaciones y todas sus dependencias en contenedores), gracias a este podemos hacer montar un sistema completo como si fuera “una empresa simulada” en nuestro propio ordenador sin instalaciones manuales.

![DOCKER INSTALADO](assets/img/docker.png)

**Herramientas utilizadas con docker**:
- Docker Desktop
- Docker Compose
- Odoo container
- PostgreSQL container

Para comenzar, hemos creado un archivo docker-compose.yml con la siguiente configuración:

- Servicio Odoo (ERP)
- Servicio PostgreSQL (base de datos)
- Conexión entre ambos mediante red interna
- Puerto expuesto: 8069

Y para poder iniciar el sistema se utiliza el comando `docker compose up -d` y accedemos al sistema con `http://localhost:8069`

![CONFIGURACIÓN DOCKER](assets/img/configuracion.png)

![INSTALACIÓN](assets/img/odoo_postgre.png)

### 2.2 Odoo Server y PostgreSQL

El sistema funciona con dos componentes principales y ambos trabajan de forma conjunta para gestionar toda la información empresarial:

- Odoo Server → interfaz y lógica del ERP
    - Reación de base de datos
    - Configuración de usuario administrador
    - Acceso al panel principal
    - Uso de módulos (ventas, inventario, CRM…)
  
- PostgreSQL → almacenamiento de datos

Una vez desplegado Odoo mediante Docker, el siguiente paso es la creación de una base de datos, necesaria para almacenar toda la información del sistema.

Al acceder a la aplicación desde el navegador `http://localhost:8069`, Odoo muestra una pantalla inicial donde se solicita la creación de una nueva base de datos.

![BD](assets/img/base_datos.png)

Ya para terminar, Odoo se conecta automáticamente con PostgreSQL y:
- Se crea la base de datos en el servidor
- Se inicializan las tablas necesarias
- Se cargan datos básicos del sistema
- Se accede al panel principal del ERP

![ODOO](assets/img/odoo.png)

---


## 3. Administración y configuración.

## 4. Integración de módulos.

## 5. Mecanismos de acceso seguro a la información. Roles y privilegios.

## 6. Elaboración de informes.

## 7. Exportación de información.

## 8. Elaboración de documentación.
