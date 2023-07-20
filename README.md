# cea_api
API Rest para crear un Centro de Enseñanza Automovilístico público y accesible para todos.

EndPoint http://my-json-server.typicode.com/macorreag/cea_api/

Tecnología json-server

https://youtu.be/OAOCa2qYq2Y

Despliegue [https://my-json-server.typicode.com/](https://my-json-server.typicode.com/)

# Examenes
Un examen de conducción usualmente tiene 40 preguntas y se pasa con un 90% es decir 36 respuestas correctas, el tiempo permitido es de 1 hora lo nque quiere decir que tiene 1:30 por pregunta

## Dificultades de las preguntas

 - **Alta:** Cada pregunta equivale a 3.75%
 - **Media:** Cada pregunta equivale a 2.5%
 - **Baje:** Cada pregunta equivale a 1.25%

## Resultados Examenes
 - **Aprobado:** Supero el examen con mas del 90% de las las respuestas correctas.
 - **Reprobado:** Su puntaje es inferior al 90%.



## Ejemplo de una pregunta

  1. ¿El combustible para el Motor OTTO es?
  - [ ] A.C.P.M.
  - [ ] Gas
  - [x] Gasolina
  - [ ] Hidrogeno

  # API Rest
  
  # Limitaciones
  El archivo db.json no puede superar los 10kb

  # Preguntas

  Se colocan en el archivo _db.json_

  ## Formato de una pregunta 
  ```json
  { 
			"id": 1, /*Identificador de la pregunta*/
			"categories": ["marco legal"], /*A que categoría pertenece esta pregunta*/
			"authors": ["macorreag"], /*Quienes redactaron la pregunta*/
			"Title": "Los tipos de sanciones por infracciones al Código son",
			"description": "",
			"help_text": "", /*Explicación detallada de la pregunta*/
			"options": [
				{
					"text": "Amonestación",
					"answer": "false", /*Permite verificar si la opcion es la correcta si este parametro no se envía se considera que esta no corresponde a la solucion es decir estara en falso, pero si se envia uno en true se considera prergunat de una opción y si se envian multiples si se considera de opcion multiple*/
					"help_text": "", /*Permite explicar porque es correcta ó incorrecta.*/
				},
				{
					"text": "Multas",
					"help_text": ""
				},
				{
					"text": "Suspención de la licencia de conducción",
					"answer": "false",
					"help_text": ""
				},
				{
					"text": "Todas las anteriores",
					"answer": "true",
					"help_text": ""
				}
			]
		}
  ```
