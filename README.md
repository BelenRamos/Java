# Trabajo Practico de JAVA


## Integrantes

#### Alan Holtz
#### Marcos Martel
#### Belen Ramos
#### Manuel Velasco

## Enunciado general

Nuestro sistema/aplicación web se basa en un Foro donde los usuarios participan realizando comentarios de diversos temas. Cada tema pertenece a una categoría en concreto. Los temas son creados por usuarios logueados. 
Para hacer un comentario, un usuario debe estar logueado. Los usuarios están clasificados por tipos (Administrador, Moderador, Usuario común, Invitado). Un comentarios puede ser citado por otros usuarios, contener imágenes, y reaccionar (Me gusta, No me gusta). 
Los usuarios además, tienen un rango, que se obtiene cuando sus comentarios son likeados por los demás. Un moderador puede banear a un usuario. Si un usuario es  baneado, puede loguearse pero está restringido a la función de hacer comentarios y crear temas. Aun así puede poner likes y consultar el tiempo que le queda de penalización.
Los Administradores pueden dar de baja a una Categoría o tema, mientras que los Moderadores pueden dar de baja solo a los temas. 


## Modelo de Datos
![Der](https://user-images.githubusercontent.com/81774927/124810882-3711ad00-df38-11eb-8e13-5d27598ad98d.jpg)



## Regularidad

|Requerimiento|cant. mín.<br>1 o 2 integ|cant. máx.<br>3 o 4 integ|Detalle/Listado de casos incluidos|
|:-|-:|-:|:-|
|ABMC simple|1 x integ|1 x integ|Grupo, Categoría, Tipo_Usuario, Rango|
|ABMC dependiente|1|2| Usuario, Tema |
|CU NO-ABMC|1|2| Hacer comentario+like/dislike|
|Listado simple|1|3(*)| Listar usuarios|
|Listado complejo|0|1(*)| Listar usuarios con rango |


## Aprobación Directa

|Requerimiento|cant. mín.<br>1 o 2 integ|cant. máx.<br>3 o 4 integ|Detalle/Listado de casos incluidos|
|:-|-:|-:|:-|
|ABMC|todos|todos| 
|CU "Complejo"(nivel resumen)|1|2| Comentar+like/dislike+denuncias+baneo+descargo+rehabilitar acceso|
|Listado complejo|1|2| Listar usuarios con rango, Listar usuarios baneados|
|Nivel de acceso|2|2| Usuario, Moderador, Administrador, Invitado(no esta logueado)|
|Manejo de errores|obligatorio|obligatorio|no requiere detalle|
|requerimiento extra obligatorio (**)|0|1| Manejo de archivos, Envio de Mails|
|publicar el sitio|olbigatorio|obligatorio|no requiere detalle|
