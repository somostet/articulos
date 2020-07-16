---

layout: default
title: UCanAccess
description: UCanAccess es una implementación de controlador Java JDBC de código abierto que permite a los desarrolladores...
fecha: 12/12/2018
images: /assets/images/Articulos/UCA.png
image: /assets/images/Articulos/UCA.png
thumbnail: /assets/images/Articulos/UCA.png
author: Isaac Quinzada
categories: Programación
lang: es
comments: true

---
Autor: **Isaac Quinzada** 

Fecha: *26/10/2018*
<br>
<br>

***
# Uso de Access en JDK 1.8 o superior
***
<br>
<center><img src="{{site.baseurl}}/assets/images/Articulos/UCA.png" alt="UCanAccess" class="img-fluid"/></center>
<br>
# ¿Qué es UCanAccess?
<br>
<center><img src="{{site.baseurl}}/assets/images/UCanAccess/UCanAccess.png" alt="UCanAccess" class="img-fluid"/></center>
<br>
El driver JDBC/ODBC está obsoleto a partir de la versión 8 de **java**.  UCanAccess es una implementación de controlador Java JDBC de código abierto que permite a los desarrolladores de Java y programas cliente JDBC (por ejemplo, DBeaver, NetBeans, SQLeo, OpenOffice Base, LibreOffice Base, Squirrel SQL) leer / escribir bases de datos de Microsoft Access.
<br><br>
Debido a que es una implementación pura de Java, se ejecuta en sistemas operativos Windows y no Windows (por ejemplo, Linux / Unix). No se necesita ODBC. UCanAccess utiliza:
<br>
* Jackcess como biblioteca de entrada / salida de MS Access (sitio web: http://jackcess.sourceforge.net/ ).
* HSQLDB como DBMS sincronizado (sitio web: http://hsqldb.org/ ).

# Instalación de la librería UCanAccess
Primero es necesario descargar la librería desde su sitio oficial:
<br>
http://ucanaccess.sourceforge.net/site.html <br>
<center><img src="{{site.baseurl}}/assets/images/UCanAccess/1.png" alt="UCanAccess" class="img-fluid"/></center>
<br>
Una vez clicada la opción correspondiente, elegiremos la versión que necesitamos y descargaremos el archivo -bin.zip de la correspondiente versión.
En esta guía será utilizada la versión 4.0.3.
<br><br>
Nos aseguraremos de descomprimir el archivo .zip que descargamos:
<br>
<center><img src="{{site.baseurl}}/assets/images/UCanAccess/2.png" alt="UCanAccess"  class="img-fluid"/></center>
<br>
Tomaremos todos los archivos .jar tanto de la carpeta principal como de la carpeta lib y los pasaremos a una carpeta para mantenerlos todos a mano.
<br>
Para añadir la librería a nuestro proyecto:<br><br>
Desde **NetBeans**:<br>
Desde la carpeta ___Libraries___ y le damos botón derecho y pinchamos en ___Add JAR/Folder.___
<center><img src="{{site.baseurl}}/assets/images/UCanAccess/3.png" alt="UCanAccess"  class="img-fluid"/></center>
<br>
Seleccionamos nuestra carpeta donde nos hemos descargado y copiado las librerías anteriores, marcamos todas y le damos a  ___Abrir___.
<br>
<center><img src="{{site.baseurl}}/assets/images/UCanAccess/4.png" alt="UCanAccess"  class="img-fluid"/></center>
<br><br><br>
**En JCreator**<br>
[Descargar](http://www.jcreator.org/download.htm "Descargar") JCreator versión 4.5 LE
<br><br>
Seleccionaremos la opción para crear un nuevo proyecto.<br>
<center><img src="{{site.baseurl}}/assets/images/UCanAccess/5.png" alt="UCanAccess"  class="img-fluid"/></center>
<br><br>
Seleccionaremos “Basic Java Application”<br>
<center><img src="{{site.baseurl}}/assets/images/UCanAccess/6.png" alt="UCanAccess"  class="img-fluid"/></center>
<br><br>
Estableceremos un nombre para el proyecto<br>
<center><img src="{{site.baseurl}}/assets/images/UCanAccess/7.png" alt="UCanAccess"  class="img-fluid"/></center>
<br><br>
Una vez establecido el nombre y demás especificaciones, Se nos desplegará la ventana de Project ClassPath, aquí elegiremos la versión del JDK a utilizar:
<br>
<center><img src="{{site.baseurl}}/assets/images/UCanAccess/8.png" alt="UCanAccess"  class="img-fluid"/></center>
<br><br>
Pasaremos a la Pestaña de “Required Libraries”<br>
<center><img src="{{site.baseurl}}/assets/images/UCanAccess/9.png" alt="UCanAccess"  class="img-fluid"/></center>
<br><br>
Clicaremos en “New” <br>
<center><img src="{{site.baseurl}}/assets/images/UCanAccess/10.png" alt="UCanAccess" class="img-fluid"/></center>
<br><br>
Posteriormente en Add > Add archive<br>
<center><img src="{{site.baseurl}}/assets/images/UCanAccess/11.png" alt="UCanAccess" class="img-fluid"/></center>
<br><br>
Seleccionaremos las 5 jars de ucanacces y clicaremos en abrir.<br>
<center><img src="{{site.baseurl}}/assets/images/UCanAccess/12.png" alt="UCanAccess" class="img-fluid"/></center>
<br><br>
<center><img src="{{site.baseurl}}/assets/images/UCanAccess/13.png" alt="UCanAccess" class="img-fluid"/></center>
<br><br>
Ahora le daremos un nombre y clicaremos en aceptar<br>
<center><img src="{{site.baseurl}}/assets/images/UCanAccess/14.png" alt="UCanAccess" class="img-fluid"/></center>
<br><br>
Por último, activaremos las librerías que agregamos y seleccionaremos finish.<br>
<center><img src="{{site.baseurl}}/assets/images/UCanAccess/15.png" alt="UCanAccess" class="img-fluid"/></center>
<br><br><br>
**En Eclipse**
<br>
Para efectos de esta guía será utilizado el entorno de desarrollo Eclipse en su versión Oxygen.
Enlace de descarga	
<br>
Daremos clic derecho sobre el proyecto y seleccionaremos properties:
<br>
<center><img src="{{site.baseurl}}/assets/images/UCanAccess/16.png" alt="UCanAccess" class="img-fluid"/></center>
<br><br>
<center><img src="{{site.baseurl}}/assets/images/UCanAccess/17.png" alt="UCanAccess" class="img-fluid"/></center>
<br>
Dentro de properties buscaremos la sección Java Build Path, dentro en Libraries > Add External JARS buscaremos la carpeta donde tenemos los .jar descargados y los vincularemos.
<br><br>
Ya tendríamos las librerías vinculadas a nuestro proyecto.

<br><br><br>
# Uso de UCanAccess en un Proyecto Java
<br>
Conexión:<br>
Dentro de nuestra clase conexión deberemos importar lo siguiente: <br>

```java
import java.sql.*; 
```

<br><br>

1. Crearemos tres variables de tipo string para almacenar la ruta de la base de datos, el usuario y la contraseña (estos últimos, de existir). 
<br><br>

```java
private String nombre_bd = "C:\\Users\\Usuario\\Desktop\\Empleados.mdb";
private String usuarioBD="";
private String passwordBD="";

Utilizaremos además los siguientes objetos:
private Connection cnn; //objeto que permite la conexión a la BD
private Statement stmt; // objeto que permite la manipulaciòn de sentencias SQL
private ResultSet recordset; // objeto que permite obtener resultados de la BD
```

Dentro del constructor de la clase es donde crearemos nuestra conexión:
<br><br>

```java
public Conexion() throws Exception {
    	try {
    		Class.forName("net.ucanaccess.jdbc.UcanaccessDriver");
    		cnn=DriverManager.getConnection("jdbc:ucanaccess://"+this.nombre_bd,this.usuarioBD,this.passwordBD);
    		stmt = cnn.createStatement();
    	}
    	catch (ClassNotFoundException e){ 
    		throw new Exception ("Error No se pudo cargar el driver puente Jdbc_Odbc");
       	 }
    	catch (SQLException e){ 
    		throw new Exception (e+"Error No se pudo establecer la conexion con la base de dato");
    	}
    	catch (Exception e) {
    		throw new Exception (e);
    	}
    }
```

<br><br>
Con esto, ya podremos conectarnos a la base de datos sin ningún problema y realizar todas sentencias sql y operaciones que necesitemos mediante JDBC.
<br><br><br>
<div id="disqus_thread"></div>
<script>
/**
*  RECOMMENDED CONFIGURATION VARIABLES: EDIT AND UNCOMMENT THE SECTION BELOW TO INSERT DYNAMIC VALUES FROM YOUR PLATFORM OR CMS.
*  LEARN WHY DEFINING THESE VARIABLES IS IMPORTANT: https://disqus.com/admin/universalcode/#configuration-variables*/
/*
var disqus_config = function () {
this.page.url = PAGE_URL;  // Replace PAGE_URL with your page's canonical URL variable
this.page.identifier = PAGE_IDENTIFIER; // Replace PAGE_IDENTIFIER with your page's unique identifier variable
};
*/
(function() { // DON'T EDIT BELOW THIS LINE
var d = document, s = d.createElement('script');
s.src = 'https://https-t-e-t-github-io-index-html.disqus.com/embed.js';
s.setAttribute('data-timestamp', +new Date());
(d.head || d.body).appendChild(s);
})();
</script>
<noscript>Please enable JavaScript to view the <a href="https://disqus.com/?ref_noscript">comments powered by Disqus.</a></noscript>
<script id="dsq-count-scr" src="//https-t-e-t-github-io-index-html.disqus.com/count.js" async></script>

{% if page.comments %} {% endif %}
