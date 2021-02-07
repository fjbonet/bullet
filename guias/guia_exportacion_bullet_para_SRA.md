# Cómo exportar reservas de aulas del Bullet para facilitar la reserva en SRA.


> + **_Versión_**: 1
> + **_Autor_**: Curro Bonet-García (fjbonet@uco.es)



Para exportar los horarios completos de un grado en Bullet:
+ Informes -> listas -> Ocupación de las Titulaciones -> Por asignatura
+ Seleccionar el grado deseado.
+ Luego pregunta por la asignatura que quieres exportar. Seleccionar el grado en cuestión y eso hace que se seleccionen todas sus asignaturas.
+ Exportar a pdf genera un pdf con todos los horarios del grado seleccionado.
+ "salvar para fichero" (segundo botón por la izquierda) genera lo siguiente:
  + **ocupacion_titulacion_[*codigo_titulacion*].html**: Es una copia en html del pdf anterior. Es decir, contiene todos los horarios
  + **ocupacion_titulacion_[*codigo_titulacion*]_M2.xls**: Archivo de excel que en realidad está vacío. Contiene un macro que se ejecuta al abrir el archivo e importa todos los archivos contenidos en la siguiente carpeta. Tiene las siguientes particularidades o errores:
    + Cuando termina la importación da un mensaje de error: "*el formato y la extensión de archivo de ....xls no coinciden. Puede que el archivo esté dañado o no sea seguro. ¿Desea abrirlo?*". Al parecer el archivo es un xlsx, pero bullet le pone extensión xls. No es un error fatal.
    + Al terminar la importanción de las hojas de la siguiente carpeta, dice: "*Errores de importación HTML*". Crea un log inaccesible. 
  + **\ocupacion_titulacion_[*codigo_titulacion*]**: Carpeta que contiene dos archivos por cada asignatura. Uno en formato html y otro en xsl:
    + **ocupacion_asignatura_[*codigo_asignatura*].html**: Archivo html con los horarios de la asignatura en cuestión.
    + **ocupacion_asignatura_[*codigo_asignatura*].xls**: Hoja de excel con los horarios de la asignatura en cuestión.
    + **ocupacion_titulacion_[*codigo_titulacion*].xls**: Hoja de excel con todos los horarios de todas las asignaturas del grado seleccionado. 
  
  
  
  
  Formatear el xls para facilitar las reservas: 
  + Seleccionar los campos que tienen celdas combinadas y "Separar celdas" en excel.
  + Seleccionar columna Evento y subir una celda para alinear el contenido de las celdas de las demás columnas.
  + Ordenar por aula....
