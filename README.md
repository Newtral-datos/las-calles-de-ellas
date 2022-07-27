# Las calles de ellas

Dataset del proyecto <a href="https://www.newtral.es/las-calles-de-ellas" target="_blank">Las Calles de Ellas</a> en el que se analiza la distribución de género en los nombres de las calles de varias ciudades españolas

<img width="100%" src="https://www.newtral.es/las-calles-de-ellas/Scrolly/img/lascalles.jpg"/>
<div style="display:flex">
<img width="330px" src="https://www.newtral.es/las-calles-de-ellas/static/media/toledo.42d80522.jpg"/>
<img width="330px" src="https://www.newtral.es/las-calles-de-ellas/static/media/tarragona.69f2673a.jpg"/>
<img width="330px" src="https://www.newtral.es/las-calles-de-ellas/static/media/dulcinea.d29c6976.jpg"/>
</div>


## Metodología

Desde Newtral.es hemos **analizado los nombres de las 39.251 calles de 69 ciudades** para comprobar cuántas de ellas recuerdan a una mujer. Para ello el equipo de técnología de Newtral.es desarrolló un algoritmo para reducir el enorme trabajo que habría conllevado identificar, revisar y anotar manualmente todas y cada una de las calles de las 69 ciudades analizadas. Hemos optado por una modalidad de trabajo híbrida en la que el algoritmo etiquetó de forma automatizada el género de las calles, y el equipo ‘humano’ supervisó y corrigió los errores del sistema automatizado. 

El equipo de tecnología ha desarrollado un *crawler* que recorre las ciudades que han sido objeto de estudio y obtiene tanto los nombres de las calles como sus geometrías para que el bot decida si hace referencia a una persona y cuál es su género. 

El proceso del bot se realiza en dos pasos: un **primer paso** basado en reglas y diccionarios, en el que se hace la asociación automática si el nombre de la calle contiene una referencia a profesiones, títulos aristocráticos y/o religiosos que permitan determinar el género (por ejemplo, calle del Padre Damián). Un **segundo paso** basado en nuestro modelo de inteligencia artificial, en el que, identificado el nombre de una calle, se determina si hace referencia a una persona y su género (por ejemplo, calle de Méndez Álvaro). 

El entrenamiento del modelo de IA se realizó en **dos fases**: la primera, a partir de un conjunto de datos no revisados con la asociación entre el nombre y el género de calles de distintas ciudades españolas y latinoamericanas. En la segunda, se reentrenó el modelo a partir de datos revisados por el equipo de periodistas de Newtral.es correspondientes a más de 20 ciudades españolas. **La precisión de este segundo algoritmo determinando el género de una calle se ha situado por encima del 93% para las ciudades analizadas**. Por último, para las calles que hacen referencia a un personaje, un nuevo proceso automatizado realizó una búsqueda en Wikidata para encontrar información de interés sobre cada uno. 


## Piezas periodísticas

A partir de estos datos hemos publicado estas dos noticias en [Newtral.es](Newtral.es)
- [Una noticia versión *scrollytelling*](https://www.newtral.es/las-calles-de-ellas/tour/)
- [Un texto con el mapa que permite buscar libremente por él](https://www.newtral.es/las-calles-de-ellas/mapa/)


## Archivos

Dentro de la carpeta *data* puedes encontrar los archivos usados en el proyecto. Uno por cada ciudad.

En cada archivo la información se estructura de la siguiente forma:
| Columna | Descripción |
|--------|---|
| Calle | Nombre completo de la calle |
| Género | Género de la persona que da nombre a la calle |
| Nombre | Nombre de la persona que da nombre a la calle |
| Religioso | Variable para declarar si la calle está concedida a una persona religiosa |
| Ficción | Variable para declarar si la calle está concedida a un personaje de ficción |
| Descripción | Información sobre la calle |
| Artículo | Link de Wikipedia de la persona que da nombre a la calle |
| Imagen | Link con una imagen de la persona que da nombre a la calle |
| Fecha de nacimiento | Fecha de nacimiento de la persona que da nombre a la calle |
| Fecha Muerte | Fecha de fallecimiento de la persona que da nombre a la calle |
| Céntrica | Variable para declarar si se trata de una calle céntrica |


## Reutilización

Puedes hacer uso de cualquiera de los datasets de este repositorio, siempre y cuando hagas la correcta atribución al equipo de Newtral.es, siguiendo las indicaciones de la licencia abajo indicada.

## Licencia

[![License: CC BY-SA 4.0](https://licensebuttons.net/l/by-sa/4.0/80x15.png)](https://creativecommons.org/licenses/by-sa/4.0/)
