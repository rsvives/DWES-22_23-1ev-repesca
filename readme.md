# Desarrollo web en entorno servidor | Subida de nota 1ª Ev.

## Instrucciones:

- Leer todo el enunciado antes de empezar
- Clonar el repositorio alojado en la siguiente URL `https://github.com/rodri-afa/DWES-22_23-1ev-repesca.git`
- Realizar los programas de PHP en los ficheros que han sido clonados.
- Se valorará positivamente con hasta un punto sobre 10, la legibilidad del código, los comentarios y el uso debido de elementos HTML y CSS

## Entrega

Una vez terminado, es necesario:

- Comprimir la carpeta del repositorio en .zip y subirla al campus virtual
- `Recomendable:` Por otra parte, se recomienda hacer commit con todos los cambios, y crear una bifurcación (fork). Para ello, simplemente bastaría con subir los archivos (hacer push) al repositorio de partida (origin / master). Como no se tienen credenciales para poder subir archivos sobre ese repositorio, el propio VSCode nos sugiere crear una bifurcación, a lo que se aceptará.

## Enunciado

El examen consta de 4 ficheros:

- index.php (formulario con filtros)
- controlador.php (procesar filtros)
- resultados.php (vista con los resultados en html)
- datos.json (json con los datos que tiene que mostrar resultados.php)

Se trata de una aplicación que hace una petición a la [API de Rick y Morty](https://rickandmortyapi.com/api/character) filtrando los datos en base a los campos introducidos en el fichero `index.php`. Los filtros son recogidos en `controlador.php`, quien hace la llamada a la API, filtra los datos, genera un json con los datos a mostrar (`datos.json`) y redirije a `resultados.php`, donde se muestran un conjunto de tarjetas HTML con la imagen, el nombre, el estado y el nombre del origen.

### (3pt) index.php

Crear un formulario que permita:

- seleccionar género (Male, Female, Unknown) **[1pt]**
- seleccionar el estado (Dead, Alive, Unknown) **[1pt]**

Extra: **[1pt]**
En vez de crear el método de selección de "estado" de forma estática (a pelo), hacerlo de forma dinámica en base a los valores que se encuentran en la API. Para ello tendrás que hacer una llamada a la API en este mismo fichero, iterar el campo "status" de los resultados, añadir cada elemento nuevo a un array y, a la hora de crear el select o el conjunto de radio buttons, iterar dicho array para darles los distintos valores.

> en caso de no seleccionar ningún filtro, mostrar todos los resultados (los 20 primeros personajes)

### (2pt) controlador.php

Fichero encargado de:

- recibir los filtros. En caso de no recibir ningún filtro, mostrar todos los resultados **[1pt]**
- hacer la petición a la API, crear un array con los datos que cumplan los criterios de los filtros y finalmente parsearlo en un json y guardarlo como fichero(`datos.json`) **[1pt]**

### (2pt) resultados.php

Fichero encargado de:

- parsear e iterar los datos contenidos en `datos.json`. **[1pt]**
- representar los datos como un conjunto de tarjetas HTML con la imagen, el nombre, el estado y el nombre del origen de cada personaje. **[1pt]**
- incluir un botón que permita borrar los datos de `datos.json` y, al mismo tiempo, volver a cargar la página del formulario `index.php`. **[1pt]**

### (1pt) datos.json

Fichero json con los datos a iterar en resultados.php

### (1pt) Comentarios, CSS y formato de código

Se valorará con 1 punto el formato del código (tabulaciones, variables descriptivas, comentarios, etc) y el uso de CSS que mejore visualmente los interfaces mostrados.

- comentarios, formato, y naming de variables: **[0,5pt]**
- CSS **[0,5pt]**
