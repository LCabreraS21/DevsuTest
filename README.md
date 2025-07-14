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





Si necesitas ver un log de depuración más detallado para solucionar problemas, puedes añadir el switch -X:

Bash

mvn clean test -X
Resultados y Reportes
Después de una ejecución exitosa de mvn clean test, Karate generará reportes HTML detallados que te permitirán analizar los resultados de tus pruebas.

Los reportes se encontrarán en el directorio:

target/cucumber-html-reports/
Para ver los resultados, abre el archivo overview-features.html en tu navegador web. Este archivo proporciona un resumen completo de todas las features y escenarios ejecutados, incluyendo los pasos, el tiempo de ejecución y cualquier fallo.
Los reportes se encontrarán en el directorio:
target/cucumber-html-reports/

Para ver los resultados, abre el archivo overview-features.html en tu navegador web. Este archivo proporciona un resumen completo de todas las features y escenarios ejecutados, incluyendo los pasos, el tiempo de ejecución y cualquier fallo.
