Utilizar la misma base de datos de películas e insertar varias
películas con distinto contenido.
'''
db.movies.insertMany ([
    {
        title: "Emma",
        year: 2020,
        rating: 3.5,
        genre: "Drama",
        description: "Emma Woodhouse es una joven inglesa que se ocupa de las relaciones de quienes la rodean, aunque a veces de una manera un tanto entrometida.",
        actors : ["Anya Taylor‑Joy","Johnny Flynn","Mia Goth"],
        country: "Emiratos Árabes Unidos",
        income: 2600000,
        duration: "1h 46m"
    },
    {
        title: "Mas alla de la luna",
        year: 2020,
        rating: 4.5,
        genre: "Animacion",
        description: "El joven y aventurero Fei Fei construye un cohete y lo lleva a la luna para encontrarse con la mítica diosa Chang'e.",
        actors : ["Phillipa Soo","Ken Jeong","Sandra Oh","Kimiko Glenn"],
        country: "EEUU",
        income: 4500000,
        duration: "1h 55m"
    },
    {
        title: "Greenland: El último refugio",
        year: 2020,
        rating: 3.8,
        genre: "Accion, Drama",
        description: "Un objeto del espacio está a punto de colisionar con la Tierra y una familia ha sido escogida para entrar en un búnker subterráneo en el que poder sobrevivir. Sin embargo, tienen poco tiempo. Tan solo cuentan con 48 horas antes de que el mundo que conocen se destruya para siempre.",
        actors : ["Gerard Butler", "Morena Baccarin", "David Denman"],
        country: "EEUU",
        income: 2600000,
        duration: "2h"
    },
    {
        title: "Sentimental",
        year: 2020,
        rating: 3.2,
        genre: "Comedia Dramatica",
        description: "Sentimental habla de las relaciones sentimentales cotidianas de dos parejas que viven en el mismo bloque de pisos. La cordialidad entre los dos hogares se ve interrumpida cuando la pareja del bajo invita a la otra a una cena, durante la cual les proponen practicar sexo en grupo",
        actors : ["Alberto San Juan", "Belén Cuesta", "Javier Cámara"],
        country: "España",
        income: 2600000,
        duration: "1h 56m"
    },
    {
        title: "Eso que tú me das",
        year: 2018,
        rating: 4.5,
        genre: "Documental",
        description: "En 2015, el cantante de Jarabe de Palo, Pau Donés, es diagnosticado de cáncer. Durante cinco años, el artista convive con esta terrible enfermedad y, veinte días antes de morir, decide llamar a Jordi Évole desde el hospital para grabar este documental",
        actors : ["Jordi Évole", "Pau Donés"],
        country: "España",
        income: 3600000,
        duration: "1h 5m"
    },
    {
        title: "LAS BRUJAS (DE ROALD DAHL)",
        year: 2020,
        rating: 4.0,
        genre: "Fantasía, Comedia, Familia",
        description: "Las Brujas (de Roald Dahl), basada en el libro del mismo nombre del también autor de Matilda y Charlie y la fábrica de chocolate, presenta un mundo en el que las brujas son de verdad, existen y viven entre nosotros.",
        actors : ["Anne Hathaway", "Octavia Spencer", "Stanley Tucci"],
        country: "EEUU",
        income: 2600000,
        duration: "1h 45m"
    },
    {
        title: "ESTE CUERPO ME SIENTA DE MUERTE",
        year: 2020,
        rating: 4.5,
        genre: "Suspenso, Terror, Comedia",
        description: "Baker Dill es un capitán de barco pesquero cuya tranquila existencia se ve alterada cuando su exmujer le pide que asesine a su violento marido.",
        actors : ["Vince Vaughn", "Kathryn Newton", "Alan Ruck"],
        country: "EEUU",
        income: 2600000,
        duration: "1h 46m"
    },
    {
        title: "Pinocho",
        year: 2018,
        rating: 3.0,
        genre: "Drama, Fantasia",
        description: "Película basada en el libro de Carlo Collodi Las aventuras de Pinocho (1883) sobre una marioneta de madera que se convierte en un niño de verdad y tiene como padre a Geppetto (Roberto Benigni)",
        actors : ["Roberto Benigni", "Federico Ielapi", "Rocco Papaleo"],
        country: "España",
        income: 3200000,
        duration: "2h 5m"
    }
])
'''
Listar todas las películas del año 2018.
'''
db.movies.find({year: 2018})
'''
Listar las 10 primeras películas de Hollywood.
'''
db.movies.find({country: "EEUU"}).limit(10)
'''
Listar las 5 películas más taquilleras.
'''
db.movies.find().sort({ income: -1}).limit(5)
'''
Listar el 2do conjunto de 5 películas más taquilleras.
'''
db.movies.find().sort({ income: -1}).skip(5).limit(5)
'''
Repetir query 3 y 4 pero retornando sólo el título y genre.
'''
db.movies.find({country: "EEUU"}, {title:1,genre:1}).sort({ year: 1}).limit(10)
'''
'''
db.movies.find({}, {title:1,genre:1}).sort({ income: -1}).limit(5)
'''
Mostrar los distintos países que existen en la base de datos.
'''
db.movies.distinct("country")
'''
