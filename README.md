# DevsuTestE2E
Pruebas E2E

# Proyecto de Automatización E2E de Demoblaze

Este proyecto contiene una prueba funcional automatizada (E2E) para el flujo de compra en la página de Demoblaze (https://www.demoblaze.com/).

## Requisitos Previos:
* Java Development Kit (JDK) 8 o superior
* Apache Maven 3.6.0 o superior 
* Google Chrome Browser (la prueba usa ChromeDriver)
* Un IDE como Eclipse o IntelliJ IDEA 

## Estructura del Proyecto:
demoblaze-automation/
├── pom.xml
├── src/
│   ├── main/java/com/demoblaze/e2e/pages/
│   │   ├── HomePage.java
│   │   ├── CartPage.java
│   │   └── CheckoutPage.java
│   └── test/java/com/demoblaze/e2e/tests/
│       └── PurchaseFlowTest.java
└── README.txt
└── conclusiones.txt

## Instrucciones de Ejecución:

1.  **Clonar o Descargar el Repositorio:**
    Si estás usando Git, clona el repositorio:
    `git clone <URL_DE_TU_REPOSITORIO>`
    Si descargaste un .zip, descomprímelo.

2.  **Navegar al Directorio del Proyecto:**
    Abre una terminal y navega a la raíz del proyecto `demoblaze-automation` donde se encuentra el `pom.xml`.

3.  **Resolver Dependencias de Maven:**
    Asegúrate de que Maven descargue todas las dependencias necesarias (WebDriverManager, Selenium, TestNG, etc.).
    `mvn clean install`
    Esto compilará el código y descargará las JARs al repositorio local de Maven.

4.  **Ejecutar las Pruebas Automatizadas:**
    Para ejecutar las pruebas, usa el siguiente comando Maven:
    `mvn clean test`

    Observarás que se abre una instancia de Google Chrome y ejecuta el flujo de prueba. Al finalizar, la terminal mostrará el resultado de la ejecución (BUILD SUCCESS si todo fue bien).




    Proyecto de Automatización de Pruebas API - Demoblaze
Introducción
Este proyecto tiene como objetivo la automatización de pruebas para los servicios REST de signup (registro de usuario) y login (inicio de sesión) de la aplicación Demoblaze. Utilizando el framework Karate DSL y Maven, se han desarrollado pruebas robustas para validar la funcionalidad de la API, asegurando la correcta interacción con los endpoints de registro y autenticación.

El ejercicio requería identificar las entradas y capturar las salidas para los siguientes casos:

Crear un nuevo usuario en signup.

Intentar crear un usuario que ya existe en signup.

Usuario y password correcto en login.

Usuario y password incorrecto en login.

Tecnologías Utilizadas
Karate DSL: Framework de automatización de pruebas API, basado en Gherkin y diseñado para pruebas de servicios web.

Maven: Herramienta de gestión de proyectos y construcción para Java.

Java 11: Lenguaje de programación utilizado para el runner de las pruebas.

JUnit 5: Framework de pruebas unitarias, integrado con Karate para la ejecución de los escenarios.

Logback: Sistema de logging utilizado por Karate para la salida de la consola.

Estructura del Proyecto
La estructura del proyecto sigue las convenciones estándar de Maven para proyectos de pruebas, con los archivos .feature ubicados en src/test/resources y el runner de JUnit en src/test/java.

demoblaze-api-karate/
├── pom.xml                     # Archivo de configuración de Maven y dependencias.
└── src/
    └── test/
        ├── java/
        │   └── com/
        │       └── demoblaze/
        │           └── api/
        │               └── tests/
        │                   └── DemoblazeTestRunner.java # Clase principal para ejecutar las pruebas con JUnit 5.
        └── resources/
            ├── demoblaze.feature   # Contiene los escenarios de prueba para signup y login.
            └── test.feature        # Un escenario de prueba adicional (ej. prueba de conectividad).

Configuración del Entorno
Para poder ejecutar este proyecto, asegúrate de tener instaladas las siguientes herramientas:

Java Development Kit (JDK) 11 o superior:

Puedes descargarlo desde el sitio oficial de Oracle o Adoptium (recomendado).

Asegúrate de que la variable de entorno JAVA_HOME esté configurada apuntando al directorio de instalación de tu JDK, y que %JAVA_HOME%\bin (Windows) o $JAVA_HOME/bin (Linux/macOS) esté añadido a tu PATH.

Apache Maven 3.6.0 o superior:

Descárgalo desde el sitio oficial de Apache Maven.

Asegúrate de que la variable de entorno M2_HOME esté configurada apuntando al directorio de instalación de Maven, y que %M2_HOME%\bin (Windows) o $M2_HOME/bin (Linux/macOS) esté añadido a tu PATH.

Cómo Ejecutar las Pruebas
Sigue estos pasos para clonar el repositorio y ejecutar las pruebas:

Clonar el Repositorio:

git clone [URL_DE_TU_REPOSITORIO_GITHUB]

(Reemplaza [URL_DE_TU_REPOSITORIO_GITHUB] con la URL real de tu repositorio).

Navegar al Directorio del Proyecto:

cd demoblaze-api-karate

Ejecutar las Pruebas:
Para ejecutar todas las pruebas definidas en los archivos .feature y generar los reportes, utiliza el siguiente comando de Maven:

mvn clean test

clean: Limpia los artefactos de compilaciones anteriores.

test: Ejecuta la fase de pruebas de Maven.

Si necesitas ver un log de depuración más detallado para solucionar problemas, puedes añadir el switch -X:

mvn clean test -X

Resultados y Reportes
Después de una ejecución exitosa de mvn clean test, Karate generará reportes HTML detallados.

Los reportes se encontrarán en el directorio:
target/cucumber-html-reports/

Para ver los resultados, abre el archivo overview-features.html en tu navegador web. Este archivo proporciona un resumen completo de todas las features y escenarios ejecutados, incluyendo los pasos, el tiempo de ejecución y cualquier fallo.
