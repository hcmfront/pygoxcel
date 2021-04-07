# pygoxcel
Excel generator for Python based on Go

La API esta integramente desarrollada en GO lang, utiliza una base de postgres para realizar una consulta a una tabla cualquiera a eleccion del desarrollador.

Para realizar una prueba se debe:

1   configurar el acceso a la BD de postgres utilizando el archivo .env 

2   modificar las estructuras de la tabla a utilizar en el archivo "employees_emailnotification.go" del directorio models. O crear el propio.

3   la ejecucion es  "go run src/main.go". Esto genera una salida por consola con "Server running at port 8080"

4   la consulta se realiza a traves de postman u otra herramienta, haciendo:

GET a http://localhost:8080/api/todos o 

GET http://localhost:8080/api/todos/1 ,donde el /1 significa q buscara el id 1 en la tabla.

5   la primera consulta GET genera como respuesta un archivo excel con nombre "test_employees_emailnotification.xlsx".

6   la segunda, un json con los datos de la tupla.


El objetivo original del desarrollo era validar la performance de GO, realizando una consulta a una tabla con 100K registros, 
extraerlos y generar un archivo excel con los datos.

a modo de informacion la prueba demoro 49 segundos.

salu2
