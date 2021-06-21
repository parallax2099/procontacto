# procontacto
Examén de Introducción

EJERCICIO 2

Las siguientes preguntas están orientadas a la comprensión del protocolo HTTP. Son agnósticas al lenguaje de programación, la idea es comprender los conceptos del estándar:
1.	¿Qué es un servidor HTTP? 
Es una aplicación que procesa peticiones en un servidor creando una comunicación bidireccional, que puede ser asíncrona o síncrona, generando una respuesta que se envía al cliente bajo el protocolo de hipertexto. El servidor puede generar estas respuestas en algún lenguaje de programación.
2.	¿Qué son los verbos HTTP? Mencionar los más conocidos
GET, POST, HEADER, PUT, DELETE, CONNECT
3.	¿Qué es un request y un response en una comunicación HTTP? ¿Qué son los headers? 
Request es una solicitud o petición que se hace desde un cliente, por ejemplo un navegador web, hacía un servidor solicitando algún dato en especifico. Y el response, es la respuesta que da el servidor en formato http. En el header vienen datos del lenguaje de programación, codificación del texto de respuesta, el tipo de datos (JSON, XML, Texto, Hipertexto), idioma.
4.	¿Qué es un queryString? (En el contexto de una url)
Es una parte de la URL que contiene los datos que deben pasar a las aplicaciones web, esto es los parámetros que requiere o espera recibir.
5.	¿Qué es el responseCode? ¿Qué significado tiene los posibles valores devueltos?
Es una convención de respuesta del protocolo HTTP para indicar el estado de la respuesta del servidor hacia un cliente.
Los códigos de respuestas esta agrupadas de la siguiente forma:
Respuestas informativas (100–199),
Respuestas satisfactorias (200–299),
Redirecciones (300–399),
Errores de los clientes (400–499),
y errores de los servidores (500–599).

6.	¿Cómo se envía data en un Get y cómo en un POST? 
En el método GET se envían los datos como parte de la URL en el formato variable=valor separadas por el carácter &.
En el método POST se envian de manera “oculta”, no son parte de la URL a través del header de la petición.
7.	¿Qué verbo http utiliza el navegador cuando accedemos a una página?
Se utiliza el verbo CONNECT.
8.	Explicar brevemente qué son las estructuras de datos JSON y XML dando ejemplo de estructuras posibles.
JSON (JavaScript Object Notation - Notación de Objetos de JavaScript) , es un formato ligero de intercambio de información. Un ejemplo es:
{
“Personas”: [
	{
	“Nombre”: “Roberto Mendez”,
	“Edad”: “34”
	},
	{
	“Nombre”: “María Candelaria”,
	“Edad”: “42”
	}
]
}

XML (Extensible Markup Language), es un formato de intercambio de información y meta lenguaje para definir reglas basadas en etiquetas, las cuales pueden tener atributos y definir categorias. Un ejemplo es:
<Personas>
	<Persona>
		<Nombre> Roberto Mendez </Nombre>
		<Edad>34</Edad>
	</Persona>
	<Persona>
		<Nombre> María Candelaria </Nombre>
		<Edad>42</Edad>
	</Persona>
</Personas>


9.	Explicar brevemente el estándar SOAP
SOAP (Simple Object Access Protocol), es un protocolo que permite comunicar dos entidades en diferentes procesos a través del uso de XML. 

10.	Explicar brevemente el estándar REST Full
REST es un conjunto de principios arquitectónicos que se ajusta a las necesidades de los servicios web y las aplicaciones móviles ligeros. Cuando se envía una solicitud de datos a una API de REST, se suele hacer a través de un protocolo de transferencia de hipertexto, comúnmente denominado HTTP. Una vez que reciben la solicitud, las API diseñadas para REST pueden devolver mensajes en distintos formatos: HTML, XML, texto sin formato y JSON. Por lo que RestFul son estas API’s.

11.	¿Qué son los headers en un request? ¿Para qué se utiliza el key Content-type en un header?
Los header se usan para enviar información entre el cliente y servidor adicional al contenido solicitado o enviado. Una cabecera esta compuesta por su nombre, seguida de dos puntos y su valor.
La cabecera Content-type es usada para definir el tipo de contenido que se sera devuelto al cliente. Un ejemplo puede ser text/html; charset=utf-8

EJERCICIO 3
Recomendamos previamente entender los conceptos de la sintaxis “json” antes de arrancar con los ejercicios.
Descargar el POSTMAN (aplicación para realizar request como cliente), adjuntando un screen de resolución para cada ítem:

1.	Realizar un request GET a la URL: https://procontacto-reclutamiento-default-rtdb.firebaseio.com/contacts.json
2.	Realizar un request POST a la URL anterior, y con body:
{
"name":"Tu nombre",
"email":tunombre.tuapellido@procontacto.com.mx
}
Tip: (Marcar la opción “raw” como body)
3.	Realizar nuevamente un request GET a la URL: https://procontacto-reclutamiento-default-rtdb.firebaseio.com/contacts.json
¿Qué diferencias se observan entre las llamadas el punto 1 y 3?
En el punto 1 se envío la petición sin parametros y devolvío un JSON con varios datos de contactos. Devolvió un estatus 200.
El el punto 3, en la URL se envian parámetros en la URL, y devolvío un JSON con varios datos de contactos. Devolvió un estatus 200.
El punto 2 devolvió un JSON con error: No data supplied. Y un estatus 400.
