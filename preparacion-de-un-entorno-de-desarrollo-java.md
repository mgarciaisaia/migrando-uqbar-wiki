| | \_\_TOC\_\_ |
|---------------|

Para realizar aplicaciones de complejidad mediana-grande en Java, es recomendable contar con un entorno de trabajo que contemple al menos:

-   Una herramienta de versionado de fuentes
-   Una herramienta de manejo de dependencias
-   Un mecanismo para automatizar los procesos administrativos del desarrollo (test, release, deploy, etc)
-   Un entorno de programación que permita:
    -   Ayudas a la detección temprana de errores, autocompleción, herramientas para navegar y buscar ágilmente dentro del código, etc.
    -   Soporte para la realización de refactors automatizados
    -   Integración con la mayor cantidad posible de las demás herramientas que utilizamos.

En este artículo se propone una configuración de entorno de trabajo que intenta cumplir con los anteriores objetivos. Las herramientas seleccionadas para eso son:

-   **Java Development Kit**
-   **Eclipse** como entorno integrado de desarrollo
-   **Svn** como repositorio de fuentes y herramienta de versionado
-   **Maven** como herramienta para manejar dependencias y automatizar diversos procesos administrativos.

Adicionalmente se instalarán extensiones al entorno de desarrollo eclipse para integrarlo con svn y maven.

JDK (Java Development Kit)
--------------------------

Contiene un compilador y una máquina virtual (el runtime) que traduce a código de máquina el código intermedio que genera el compilador (.java → COMPILADOR (javac.exe) → .class → VM (java.exe) → ejecutable final).

Al tiempo de escribir este artículo la última versión estable es 1.7. Para el propósito aquí descripto es recomendable instalar la *Standard Edition*.

### Download e instalación base

A continuación se detallan los pasos básicos de instalación según el sistema operativo que se esté utilizando. Luego de realizar este paso inicial se deberá pasar a la configuración del entorno.

Este es el link de [downloads](http://www.oracle.com/technetwork/java/javase/downloads/index.html).

Desde ahí buscan el Latest Release y se descargan el JDK del sistema operativo que esté instalado en sus máquinas.

Para más detalles adicionales a los que se encuentran en esta página, se puede consultar el [manual de instalación de sun](http://java.sun.com/javase/6/webnotes/install/index.html).

##### Ubuntu

Para instalarlo en Ubuntu se puede hacer:

`sudo apt-get install default-jdk`

Eso instalará el jdk default (para Ubuntu es *OpenJDK de la versión que se bajaron*), si se desea instalar en cambio el JDK de Sun se puede hacer:

`sudo apt-get install sun-java6-jdk sun-java6-jre`

##### Otros sistemas operativos

Para otros sistemas operativos se puede bajar el instalable de: <http://java.sun.com/javase/downloads/> .

[Este tutorial](http://www.it.uc3m.es/tlp/guia/guiaWinXP.html) indica cómo instalarlo en Windows XP (en especial pasos 1 a 3).

### Documentación

-   [Java Tutorials](http://java.sun.com/docs/books/tutorial/)
-   [Javadoc reference guide](http://java.sun.com/j2se/1.4.2/docs/tooldocs/windows/javadoc.html)
-   [Writing comment tips](http://java.sun.com/j2se/javadoc/writingdoccomments/index.html)

Eclipse
-------

La instalación del eclipse es muy sencilla: hay que bajar el que corresponda a su sistema operativo desde <http://www.eclipse.org/downloads/> y descomprimirlo en su disco rígido. Posiblemente deseen crear un acceso directo para apuntar al ejecutable.

A los efectos de los objetivos planteados en este artículo, se recomienda elegir la versión denominada "Eclipse IDE for Java EE Developers".

  
Esa versión pesa bastante. Si no van a utilizar las herramientas de programación web es posible utilizar la versión más liviana "Eclipse IDE for Java Developers".

### Configuraciones adicionales

Chequeá las [Configuraciones generales para cualquier Eclipse](configuraciones-generales-para-cualquier-eclipse.md)

### Configurar un JDK en eclipse

Si se bajaron una versión especifica de Java, un JDK, van a querer que el eclipse lo use para compilar, etc. Para eso, desde el eclipse deben ir a - Window -&gt; Preferences - En el arbol de la izquierda, "Java -&gt; Installed JRE". - En el panel de la derecha, agregan un nuevo JDK, con el botón "Add" - Ahí siguen los pasos default, y en el primer campo "JRE Home", apuntan al directorio del JDK que descomprimieron. - Luego se aseguran de checkearlo como el "default" en la tabla.

### Documentación

-   [Página principal de Eclipse](http://www.eclipse.org/)

Svn
---

Pueden instalar el plugin de svn para eclipse basándose en [este tutorial](http://subclipse.tigris.org/servlets/ProjectProcess?pageID=p4wYuA).

Maven
-----

Instalar según la [Guía de Instalación de Maven](guia-de-instalacion-de-maven.md) (configurando el settings como se explica [aquí](http://uqbar-wiki.org/index.php?title=Configuraci%C3%B3n_de_Maven_para_poder_utilizar_las_herramientas_de_Uqbar))

Links útiles
------------

-   [Amigandonos con el entorno de desarrollo](amigandonos-con-el-entorno-de-desarrollo.md)

