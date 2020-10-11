# Censo de población y vivienda Chile 2017 - Bases de datos

En el repositorio se encontrará a disposición los datos
cartográficos divididos en la siguiente estructura:

#### Polígonos cartográficos
1. Región
	2. Comuna
		3. Distrito Censal
			4. Zona o Localidad
				-Zona cuando es urbano
				-Localidad cuando es rural

Técnicamente el nivel de mayor desagregación es el de nivel de manzana, pero tiene el problema
que por ley de transparencia no se permite llegar a ese nivel. Entonces toda agregación
que se quiera hacer desde la base de microdatos solo puede llegar a nivel de zona o localidad.

#### Microdatos

La base de microdatos se divide en 3 tablas:

1. Personas: Datos a nivel de individuo
2. Hogar: Datos a nivel del hogar 
3. Vivienda: datos particulares de la misma vivienda

La presente estructura obviamente debe presentarse como una estructura relacional jerárquica
donde cada persona está asociada a un hogar, dicho hogar a una vivienda y la vivienda a una zona
o localidad.

Para descagar la base de datos con las tres tablas en formado .db del censo hacer [click aquí](https://drive.google.com/file/d/1ROtWwX4J4fWwnfj7QFe9iStDdAf9jF4p/view?usp=sharing). 
La gracia de este formato
de entrega, es que no solo se campan las 3 tablas, sino que la tabla de hogar y vivienda vienen con un 
un geocódigo el cual sirve como identificador para cruzar con las agregaciones espaciales.

Para ver la función que se implementó para crear el geocódigo, [hacer click aquí](https://github.com/demcortillas/methods/blob/main/GEOCODIGO.py).

Para mayor detalle o consultas, puedes escribirme a diegmedina@udec.cl