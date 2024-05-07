<section id="inicio" align="center">
  <h1>Proyecto final</h1>
  <h2>Ingesta de datos de ligas de fútbol</h2>
  <img src="./img/img-bootcamp-ing-datos.png"/>
</section>

<h3>Proyecto para el Bootcamp de Ingeniería de datos en <a href="https://codigofacilito.com">Código Facilito</a></h3>

<h3>Líder del bootcamp: <a href="https://talkingpts.org/our-team/sergio-sanchez/">Sergio Sánchez, Ingeniero de Datos Sr. en TalkingPoints</a></h3>

<h3>Tabla de Contenidos:</h3>

- [**Información del proyecto**](#información-del-proyecto) 📁
- [**Version 1.0.0:**](#version-100) ✅
- [**Fuentes de datos**](#fuentes-de-datos) 🗄️
- [**Prerrequisitos**](#prerrequisitos) 📝
- [**Herramientas y tecnologías**](#herramientas-y-tecnologías) 🛠️
- [**Instalación y configuración del Entorno**](#instalación-y-configuración-del-entorno) 💻
- [**Documentación Técnica**](#documentación-técnica) ⚙️
- [**Screenshots**](#screenshots) 📸
- [**Información adicional**](#información-adicional) 🪧
- [**Agradecimientos**](#agradecimientos) 👋🏽
- [**Autor**](#autor) ⚡🪪

### **Información del proyecto**

Proyecto final para el bootcamp de Ingeniería de Datos de [Código Facilito](https://codigofacilito.com), donde se va a construir un sistema de ETL para ingestar datos de distintas ligas de fútbol de Europa, aplicando lo aprendido durante la cursada y utilizando varias de las herramientas vistas en el curso.

- Objetivo General:
  
  Construir un sistema de ETL donde se ingesta en una tabla de Snowflake la información de las 7 ligas de fútbol más importantes de Europa

- Requisitos Específicos:
  - Extraer datos de múltiples fuentes (páginas web) con python.
  - Transformar estos datos con Python para obtener un dataset limpio.
  - Crear un DAG en Airflow, desplegado de manera local con Astro CLI, para que dos veces por semana vaya a la página web, extraiga la información, la transforme, y luego se cargue en una tabla en Snowflake.
  - Una vez hecho esto, se podrá hacer todo tipo de trabajos de analítica de datos, ya sea top five de los equipos con más goles, con menos goles, con mayor partidos ganados, etc.

- Alcance:
  
  Para el público en general, no se busca resolver una problemática en particular, sino practicar algunas de las herramientas vistas en el bootcamp y mostrar un ETL sencillo que capture la esencia de un proceso básico y fundamental en Ingeniería de datos, mostrando el paso a paso de la extracción, la transformación y la carga de distintas ligas de Europa, con actualización automática periódica.


### **Version 1.0.0:**

[![Demo](https://img.shields.io/badge/Demo_(En_proceso)-informational?style=for-the-badge&logo=vercel&logoColor=fff&color=23272d)](https://...)

### **Fuentes de datos**

- df_ligas.csv
- team_table.csv

### **Prerrequisitos**

Lista de software y herramientas, que necesitas para instalar y ejecutar este proyecto:

- Git
- GitHub
- Docker
- Python 3.2 en adelante
- Pandas
- Snowflake
- Airflow
- Astro CLI

### **Herramientas y tecnologías**

Tecnologías utilizadas para construir el proyecto:

- [Git](https://git-scm.com/) - El controlador de versiones utilizado
- [GitHub](https://github.com/) - La plataforma de desarrollo colaborativo, donde se aloja este proyecto.
- [Docker](https://www.docker.com/) - La tecnología de contenedores utilizada para manejar una imagen de airflow.
- [Python](https://www.python.org/) - El lenguaje de programación utilizado.
- [Pandas](https://pandas.pydata.org/) - Una librería  de Python para la manipulación y el análisis de los datos.
- [SQL](https://www.postgresql.org) - El lenguaje de consulta utilizado para bases de datos relacionales.
- [Snowflake](https://www.snowflake.com/es/) - La plataforma de almacenamiento de datos basada en la nube que fue utilizada. 
- [Airflow](https://airflow.apache.org/) - La plataforma de gestión de flujo (un orquestador) utilizada.
- [Astronomer](https://docs.astronomer.io/) - Aplicación de software como servicio (SaaS) que posee y ejecuta recursos de Astro. En este caso se utiliza Astro CLI para desplegar y correr la UI de Airflow.

### **Instalación y configuración del Entorno** 

Una guía paso a paso sobre cómo configurar el entorno de desarrollo e instalar todas las dependencias.

`Astro CLI`

```bash
# Instalar Astro CLI por medio de WSL
curl -sSL install.astronomer.io | sudo bash -s

# En el Visual Studio Code o el editor de tu preferencia, inicializar Astro y todos los paquetes necesarios
astro dev init

# Levantar la UI de Airflow
astro dev start o bien sudo astro dev start en caso de acceso denegado  
```



`Docker`

```bash
# paso 1
```

`Snowflake`

```python
# paso 2
```


`Snowflake`
Crear una cuenta y un nuevo warehouse.
Establecer roles y permisos para el acceso seguro.
Documentar el proceso de configuración para futuras referencias.

`DBT`
Instalar DBT localmente o usar DBT Cloud.
Configurar el perfil de DBT para conectar con Snowflake.
Crear un proyecto DBT inicial.

`Python`
Configurar un entorno virtual.
Instalar bibliotecas necesarias (requests, pandas, snowflake-connector-python).
Configurar herramientas de desarrollo (IDE, control de versiones).

`Diseño del Modelo de Datos`
Esquema de Snowflake:
Definir tablas para ventas, clientes, y datos de marketing.
Documentar el esquema y las relaciones entre tablas.

`Modelos de DBT`
Crear modelos de transformación.
Definir cómo las tablas serán transformadas (agregaciones, joins, limpieza de datos).
Documentar cada modelo con descripciones en el código.

`Extracción de Datos`
Scripts de Python:
Escribir scripts para extraer datos de APIs o bases de datos.
Utilizar pandas para manipular datos si es necesario.
Automatizar la extracción de datos mediante cron jobs o Airflow.
Documentar los scripts, incluyendo parámetros, formatos de datos y frecuencia de extracción.
 
`Carga de Datos`
Carga inicial a Snowflake:
Usar snowflake-connector-python para cargar datos.
Crear tablas en Snowflake usando scripts SQL o desde Python.
Documentar el proceso de carga, incluyendo mapeo de datos y configuración de carga.

`Transformación de Datos`
DBT para transformación:
Configurar y ejecutar modelos DBT.
Utilizar pruebas DBT para asegurar la calidad de los datos.
Documentar transformaciones, incluyendo lógica de negocio y optimizaciones.

`Análisis y Reporting`
SQL y Herramientas de BI:
Crear consultas SQL para análisis.
Configurar dashboards en herramientas de BI conectadas a Snowflake.
Documentar consultas y dashboards, incluyendo KPIs y métricas visualizadas.

---

### **Documentación Técnica**


`Procesos`

1. Ingesta
   
   - dfafaf
   - fdasf
   - dfafa
   - dfafadf
   - dfafafd
   - dfafd
   - 
   
2. Carga
    
   - dfafaf
   - dfadf
   - dfadfa
   - dfdfaf
   - dfadf
 
3. Transformación

   - dfafaf
   - dfadf
   - dfadfa
   - dfdfaf
   - dfadf


---
### **Screenshots**




### **Información adicional**




### **Agradecimientos**

- En especial, agradecimiento a Código Facilito por la excelente experiencia del bootcamp, la entrega y el compromiso permanente con toda su comunidad, que se extiende más allá del ámbito académico y son un ejemplo de plataforma educativa a nivel internacional.
- Agradecimientos al líder del bootcamp Sergio Sánchez por diseñar los contenidos, y a todos los profesores y el equipo que conforman Código facilito, brindando su apoyo y conocimiento para lograr la mejor experiencia educativa.


---

### **Autor**

<p align="center">
  <a href="https://git.io/typing-svg"><img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=21&pause=1000&color=C2D9F8&width=435&lines=Hello+World!+I+am+Nahuel;A+passionate+Data+Engineer;and+Full+Stack+Developer⚡." alt="Typing SVG" /></a>
</p>

<h3>¡Hola, mi nombre es <b>Nahuel</b> 👋🏽!</h3>

- Soy de Buenos Aires (Argentina).
- Estudio Ingeniería en sistemas.
- Me gusta leer y estudiar sobre diversos temas, explorar nuevas tecnologías y resolver problemas.
- Me desempeño como Data Engineer en NTT Data, pero en mi trabajo diario hago tanto ingeniería de datos como ciencia de datos y machine learning.
- Tengo formación en desarrollo full Stack con JavaScript y Python, pero por mi trabajo utilizo diariamente tecnologías para data como Python, numpy, pandas, Scikit learn, SQL, tecnologías de Big Data como PySpark y Microsoft Azure para trabajar en la nube, entre otras.

💬 Siéntete libre de ponerte en contacto conmigo.

[![Contact Me](https://img.shields.io/badge/Gmail-informational?style=for-the-badge&logo=Mail.Ru&logoColor=fff&color=c6362c)](mailto:nahue.developer1@gmail.com)
[![LinkedId](https://img.shields.io/badge/LinkedIn-informational?style=for-the-badge&logo=linkedin&logoColor=fff&color=0274b3)](https://www.linkedin.com/in/nahuel-developer/)
[![GitHub Profile](https://img.shields.io/badge/GitHub-informational?style=for-the-badge&logo=GitHub&logoColor=fff&color=343941)](https://github.com/Nahuel-DevOne)
[![Linktree](https://img.shields.io/badge/-Linktree-323330?style=for-the-badge&logo=linktree&logoColor=#41e45f)](https://linktr.ee/nahuel.lopez)

Desarrollado con 💙 por [**Nahuel DevOne⚡**](https://linktr.ee/nahuel.lopez)

[**⚡Volver al inicio⚡**](#inicio)

---