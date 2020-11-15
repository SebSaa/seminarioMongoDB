Utilizar la misma base de datos de películas e insertar varias películas (al menos 30) con distinto contenido.  
```
> db.movies.insertMany ([
...     {
...         title: "Biutiful",
...         year: 2010,
...         rating: 3.5,
...         genre: "Drama",
...         description: "El eje central de esta película es lo que le sucede a su protagonista – Uxbal- en su vida personal y familiar. ",
...         actors : ["Javier Bardem", "Maricel Álvarez", "Diaryatou Daff"],
...         country: "Emiratos Árabes Unidos",
...         income: 2600000,
...         duration: "145m"
...     },
...     {
...         title: "El jardinero fiel",
...         year: 2005,
...         rating: 3.5,
...         genre: "Animacion",
...         description: "La temática abordada en este film es la experimentación, por parte de una industria farmacéutica, con una medicación contra la tuberculosis en poblaciones de Kenia, poniendo en riesgo su salud. ",
...         actors : ["Ralph Fiennes", "Rachel Weisz"],
...         country: "Reino Unido",
...         income: 3500000,
...         duration: "128m"
...     },
...     {
...         title: "El sindrome de China",
...         year: 1978,
...         rating: 3.8,
...         genre: "Intriga - Catástrofe",
...         description: "Esta película trata sobre los riesgos de la energía nuclear. El tema está inserto en una trama de suspenso y, por ello, resulta un recurso muy interesante para captar la atención",
...         actors : ["Michael Douglas", "Jane Fonda", "Jack Lemmon"],
...         country: "EEUU",
...         income: 1500000,
...         duration: "123m"
...     },
...     {
...         title: "Una temporada de incendios",
...         year: 1995,
...         rating: 3.8,
...         genre: "Testimonial",
...         description: "Con esta película es posible trabajar las diversas problemáticas que sufren campesinos y grupos aborígenes cuando ciertos sectores se apropian de los recursos naturales existentes en las tierras históricamente ocupadas por ellos.",
...         actors : ["Sonia Braga", "Luis Guzman", "Raul Julia", "Edward James Olmos"],
...         country: "EEUU",
...         income: 2300000,
...         duration: "122m"
...     },
...     {
...         title: "Un lugar en el mundo ",
...         year: 1992,
...         rating: 4.5,
...         genre: "Drama",
...         description: "Esta película permite realizar varias lecturas y descubrir en ella diversas historias.",
...         actors : ["Federico Luppi", "José Sacristán", "Cecilia Roth"],
...         country: "Argentina",
...         income: 3800000,
...         duration: "120m"
...     },
...     {
...         title: "Diamante de Sangre ",
...         year: 2006,
...         rating: 4.0,
...         genre: "Thriller",
...         description: "La historia que se narra en esta película se desarrolla durante la guerra civil desatada en territorios de Sierra Leona, África, durante la década de los ’90.",
...         actors : ["Leonardo DiCaprio", "Jennifer Connelly", "Djimon Hounsou"],
...         country: "EEUU",
...         income: 4600000,
...         duration: "138m"
...     },
...     {
...         title: "Tocando el viento",
...         year: 1997,
...         rating: 3.5,
...         genre: "Suspenso, Terror, Comedia",
...         description: "Un grupo de mineros alterna su trabajo con la música, tocando en una banda que forma parte de la identidad del pueblo.",
...         actors : ["Ewan McGregor", "Tara Fitzgerald", "Pete Postlethwaite"],
...         country: "Reuno Unido",
...         income: 2600000,
...         duration: "107m"
...     },
...     {
...         title: "Erin Brockovich",
...         year: 2000,
...         rating: 3.0,
...         genre: "Drama",
...         description: "La protagonista de esta película está atravesando problemas personales y consigue trabajo en un pequeño estudio de abogados en donde se ocupará de investigar las causas de una enfermedad sufrida por algunas personas.",
...         actors : ["Julia Roberts", "Albert Finney", "Aaron Eckhart"],
...         country: "España",
...         income: 4200000,
...         duration: "131m"
...     },
...     {
...         title: "Babel",
...         year: 2006,
...         rating: 4.0,
...         genre: "Drama",
...         description: "La película cuenta las historias de cuatro familias que viven muy lejanas unas de otras, en otros países, otros continentes y que, de algún modo, se entrecruzarán hacia el final. ",
...         actors : ["Brad Pitt", "Cate Blanchett", "Gael Garcia Bernal", "Koji Yakusho"],
...         country: "EEUU",
...         income: 4500000,
...         duration: "142m"
...     },
...     {
...         title: "Jugando en los campos del señor",
...         year: 1991,
...         rating: 3.3,
...         genre: "Drama",
...         description: "A la selva amazónica llega un grupo de misioneros con el propósito de evangelizar a los indios niaruna.",
...         actors : ["Tom Berenger", "John Lightgow", "Daryl Hannah", "Kathy Bates"],
...         country: "EEUU",
...         income: 2300000,
...         duration: "186m"
...     },
...     {
...         title: "El día después de mañana",
...         year: 2004,
...         rating: 5.3,
...         genre: "Drama, Accion",
...         description: "El cambio climático forma parte de la agenda científica, política y, también, de los contenidos a enseñar en la escuela.",
...         actors : ["Dennis Quaid", "Jake Gyllenhaal", "Emmy Rossum"],
...         country: "EEUU",
...         income: 2300000,
...         duration: "124m"
...     },
...     {
...         title: "Los lunes al sol",
...         year: 2002,
...         rating: 3.3,
...         genre: "Drama",
...         description: "El cambio climático forma parte de la agenda científica, política y, también, de los contenidos a enseñar en la escuela.",
...         actors : ["Javier Bardem", "Luis Tosar", "José Ángel Egido", "Nieve de Medina", "Enrique Villén", "Celso Bugallo", "Joaquín Climent"],
...         country: "España, Italia, Francia",
...         income: 4300000,
...         duration: "113m"
...     },
...     {
...         title: "Quebracho",
...         year: 1974,
...         rating: 4.3,
...         genre: "Drama",
...         description: "Esta película es un clásico del cine nacional. Es recordada por mostrar cómo una empresa llamada “La Forestal”, a fines del siglo XIX y principios del siglo XX, arrasó con buena parte del monte de quebracho en el norte argentino",
...         actors : ["Juan Carlos Gené", "Héctor Alterio", "Luis Aranda", "Diana Arias"],
...         country: "Argentina",
...         income: 5300000,
...         duration: "95m"
...     },
...     {
...         title: "Ciudad de Dios",
...         year: 2002,
...         rating: 2.3,
...         genre: "Drama",
...         description: "Ciudad de Dios narra la vida de varias personas que habitan una favela en Río de Janeiro a lo largo de casi treinta años.",
...         actors : ["Alexandre Rodrigues", "Leandro Firmino"],
...         country: "Brasil",
...         income: 3300000,
...         duration: "130m"
...     },
...     {
...         title: "Los educadores",
...         year: 2005,
...         rating: 2.3,
...         genre: "Drama",
...         description: "Dos jóvenes deciden luchar contra la sociedad del consumismo y la explotación de trabajadores de los países del Tercer Mundo.",
...         actors : ["Julia Jentsch", "Daniel Brühl", "Stipe Erceg", "Burghart Klaussner"],
...         country: "Alemania",
...         income: 2750000,
...         duration: "127m"
...     }
... ])
```
Crear índice en field rating y luego hacer búsquedas usando este campo.  
```
db.movies.createIndex({rating: 1})
```
  Obtengo los index 
```
> db.movies.getIndexes()
[
        {
                "v" : 2,
                "key" : {
                        "_id" : 1
                },
                "name" : "_id_"
        },
        {
                "v" : 2,
                "key" : {
                        "rating" : 1
                },
                "name" : "rating_1"
        }
]
```
  Consulta 
```

```
  Elimino el index creado  
```
db.movies.dropIndex({rating: 1})
```
Crear índice en title y description, y después hacer búsquedas de texto en estos campos.  
```
db.movies.createIndex({title: 1,descripcion:1})
```
