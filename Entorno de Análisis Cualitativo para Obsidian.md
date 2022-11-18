Traducción por Mújica - Fecha: 2021-08-19 - 14:05
Leer original: [An Integrated Qualitative Analysis Environment with Obsidian](An%20Integrated%20Qualitative%20Analysis%20Environment%20with%20Obsidian.md)

# Entorno de análisis cualitativo integrado Obsidian - Axle

![Análisis de datos cualitativos con obsidiana](https://blotcdn.com/blog_a60d6a8aec4340a893fc18808f28840e/_image_cache/13c5a16a-c509-4554-ac86-293bc0eb441c.png)


MaxQDA, NVivo, Atlas.ti y una variedad de otras aplicaciones están diseñadas para ayudar a los investigadores a analizar datos cualitativos. Estas aplicaciones son sin duda poderosas, pero todas ofrecían una curva de aprendizaje demasiado empinada cuando me encargaron un pequeño proyecto de análisis en 2020 (¡además, son caras!) En cambio, \*\* diseñé un entorno de obsidiana para el análisis de datos cualitativos . \*\*

La idea central: tome cada uno de los fragmentos de texto con los que está trabajando, facilite su recorrido y agregue formas de codificarlos y escribir lo que significan los códigos.

En este ejemplo, tuve que analizar una serie de preguntas abiertas sobre la experiencia de los estudiantes durante la pandemia de COVID-19. Hubo cientos de respuestas que van desde una o dos palabras hasta cientos de palabras de estudiantes individuales. Mi objetivo era comprender los temas clave y los valores atípicos interesantes en este conjunto de datos.

Adopté un enfoque de teoría de campo fundamentado para este estudio. Leo profundamente cada respuesta, destacando los puntos clave y buscando puntos en común y rarezas. A medida que surgían esos fenómenos interesantes, los agrupaba y los describía. Una vez que los datos fueron revisados a fondo, cuantifiqué el número de respuestas atribuidas a cada uno de los temas que descubrí para tener una idea de los temas más y menos comunes. También verifiqué cada tema / conocimiento entre sí y los refiné para reducir la redundancia según fuera necesario. El informe final consistió en una lista clasificada de estos temas, ordenados por la frecuencia con la que se informaron, una descripción de cada tema y una selección de respuestas ilustrativas de los estudiantes.

## Cómo hacer esto con Obsidian

He creado un kit para este entorno de análisis cualitativo para que lo descargue y lo utilice en cualquier nuevo proyecto de análisis que emprenda. Para configurarlo, consulte las instrucciones que se encuentran a continuación. A lo largo del resto de esta guía, sin embargo, explico cómo hacer esto desde cero (mientras hago referencia al kit).

### Configurar el entorno

1.  Instale Obsidian, si aún no lo ha hecho. Consulte [https://obsidian.md](https://obsidian.md/) para conocer las últimas versiones.
2.  [Descargue el kit de inicio del entorno de análisis cualitativo de GitHub](https://github.com/ryanjamurphy/obsidian-qualitative-analysis-environment) .
3.  Extraiga el kit descargado donde desee en su computadora.
4.  Abra Obsidian, abra el Selector de bóveda (el pequeño icono de bóveda en la parte inferior izquierda) y abra las carpetas recién extraídas.
5.  Para usar toda la funcionalidad del entorno, debe deshabilitar el Modo seguro en la bóveda (porque usa algunos complementos de la comunidad). Para hacer esto, vaya a Preferencias → Complementos de la comunidad y desactive el Modo seguro.

### Preparando los datos

Primero, haga que cada punto de datos tenga su propio `.md` archivo markdown ( ), nombrándolos secuencialmente comenzando en 1. Cree una carpeta en su computadora titulada “Entorno de análisis cualitativo integrado” (o lo que desee). Crea una subcarpeta en esa carpeta llamada **"data ponits"** (_para datos de registrados_ o lo que quieras). Luego, abra Obsidian, vaya al Selector de bóvedas (el icono de la bóveda en la parte inferior izquierda de la aplicación) y cree una nueva bóveda. Seleccione la carpeta de nivel superior "Entorno de análisis cualitativo integrado" que creó hace un momento. Esto creará una bóveda de análisis de datos para que la personalice en el entorno perfecto para esta tarea.

Poner los puntos de datos en cada uno de sus propios archivos y numerarlos secuencialmente es un truco: nos permite usar los comandos "Nota diaria siguiente" y "Nota diaria anterior" del complemento básico Daily Note para recorrer rápidamente las respuestas. Por lo tanto, habilite ese complemento y configure esos dos comandos en una tecla de acceso rápido de fácil acceso (usé cmd\+ alt\+ →/←. ¡Usará estos comandos al menos una vez por cada dato que esté analizando!

En segundo lugar, cree una _carpeta en su "Proyecto de análisis"_ llamada **"codes"**. Luego, en su nueva bóveda de obsidiana, vaya a `Preferences → Files & Links → Default Location for New Notes`y cambie esto a su nueva carpeta **codes**. Esto significará que cada nueva nota que cree desde los enlaces o desde el comando "Nueva nota" aparecerá en esta carpeta (donde se agruparán los _códigos_).

### Codificando los datos

Abra el primer punto de datos: el archivo en la carpeta **data point** llamado "1".

Debajo de los datos de texto, agregue un pie de página. Podría usar un encabezado (por ejemplo, `## Coding`). Acabo de dejar un par de líneas nuevas entre los datos en sí y donde estaba poniendo los códigos (vea la captura de pantalla). En este pie de página, simplemente enumerará cada uno de los **codigos** que identifique en el _punto de datos_.

_Revise los datos_. ¿Qué dice? ¿Qué tiene de interesante? ¿Cómo podría ayudarlo a responder sus preguntas de investigación? Piense en las respuestas a estas preguntas como _códigos_: son las conclusiones interesantes que son relevantes para este _dato_. En el pie de página, escriba estos _códigos_.

Aquí está el secreto _para hacer que toda esta configuración funcione_: agregue cada _código_ como un `[[`enlace interno `]]`. Eso nos brinda varias cosas:
- Los códigos se sugieren cuando inicia un nuevo enlace interno `[[`, para que podamos elegir entre las opciones en lugar de intentar recuperarlas.
- Las respuestas individuales se relacionarán estructuralmente con los códigos a través de vínculos de retroceso (y se vincularán visualmente a los códigos a través de la vista de gráfico).
- La edición de un código cambiando el nombre propagará el cambio en ese código a lo largo de los datos.
- Finalmente, convierte a los _códigos en sí mismos en un objeto al que podemos agregar información_. Puede abrir un código como vínculo como una nota y describirlo, incrustar instancias ejemplares de la codificación de las respuestas, etc.

Es posible que desee mantener un _índice de códigos_ [[01 Report]], solo para proporcionar un lugar fácil para organizar y ver todos los códigos que ha identificado a la vez. En el índice de códigos, enumere cada código que agregue a sus datos. ¡No dude en pedirlos bajo los títulos o como desee!

Una vez que haya terminado de leer un _punto de datos_ y agregar _códigos_, pase al siguiente usando el comando _Siguiente nota diaria_ (o tocando la tecla de acceso rápido que asignó anteriormente).

### Analizando los datos

Cuando utilice la teoría de campo fundamentada, debe actualizar, revisar y refinar gradualmente su teoría (su codificación) a medida que revisa los datos. El objetivo es hacer visibles todos los conocimientos interesantes que se encuentran dentro de sus datos, explicar claramente cuáles son esos hallazgos y verificarlos y volver a verificarlos continuamente a medida que continúa revisando sus datos.

Eso significa que a medida que revisa más y más datos, está haciendo cuatro cosas:
1. Etiquetar los _puntos de datos_ con los _códigos_ que ya ha identificado;
2. Crear nuevos _códigos_ para resaltar cualquier cosa nueva en el _punto de datos_ que aún no haya capturado/identificado;
3. Refinando los _códigos_ existentes (a) resumiendo y agregándoles detalles (comúnmente conocido como escribir *memorandos* sobre los _códigos_), (b) incorporando ejemplos particularmente ilustrativos de ellos en los _datos_, (c) dividiendo los _códigos_ si realmente contienen diferentes elementos importantes ideas, y (d) combinar _códigos_ si se superponen significativamente; y
4. Según sea necesario, busque _códigos_ de _códigos_: agrupar y estructurar las ideas que ha encontrado en la medida en que la agrupación hace que sus conclusiones sean más claras o más impactantes.

### Informar sobre los datos

Una vez que haya revisado todos los datos al menos una vez, debe tener un conjunto de _códigos_ que agrupen los diferentes _puntos de datos_ por las ideas interesantes que contienen. Es posible que desee volver a revisar los _datos_, o los _códigos_, o los subconjuntos específicos de los datos, más de una vez para refinar aún más su análisis (consulte los pasos de análisis 1-4 anteriores). Una vez que se sienta satisfecho con las conclusiones, es hora de escribirlo.

### Cuantificando tus códigos

Una cosa fácil de hacer es _cuantificar_ el número de _puntos de datos_ asociados con cada _códigos_. Esto le brinda una estimación rápida de la _frecuencia_ o la frecuencia con que se encuentran estas conclusiones en sus datos. 

Hay muchas formas de cuantificar el número de puntos de datos por códigos. La más simple es usar las funciones básicas de búsqueda de Obsidian. Para cada códigos, ingrese `"[[`seguido del nombre exacto en su búsqueda, luego finalice la consulta de búsqueda con `]]"`. Esto buscará menciones exactas del código vinculado. Una vez que la búsqueda haya finalizado, toque el botón _Copiar resultados de búsqueda_ sobre el cuadro de texto de la consulta de búsqueda. Por último, en las opciones que se le presentan, cambie el Prefijo de lista a "Numerado". Esto le da un recuento del número de resultados para cada tema.

Sin embargo, eso podría ser tedioso si tiene muchos temas para contar. En su lugar, puede utilizar Dataview de la siguiente manera:
1.  Instale y habilite el complemento Dataview.
2.  Cree una página de "Estadísticas" [[03 Statistics]] en la carpeta de nivel superior de su bóveda.
3.  Coloque el siguiente bloque de código en la nueva página de estadísticas, asegurándose de inicializar y darle al bloque de código el tipo "vista de datos". (Es decir, escriba "dataview" inmediatamente después de las tres primeras comillas inversas del código de cercado). Tenga en cuenta que si le asignó un nombre diferente a la carpeta "códigos", tendrá que cambiar el nombre especificado en la segunda línea del bloque de código.

(Nota: esto ya está hecho en el kit de inicio del entorno de Análisis cualitativo. ¡Simplemente visite la nota de Estadísticas para ver esta información!)

```
TABLE length(file.inlinks) as "Data Points", length(file.outlinks) as "Related Themes"
FROM "codes"
SORT length(file.inlinks) DESC
```

Esto genera una _tabla que enumera cada código_, la cantidad de _puntos de datos asociados con ese código_ y la cantidad de _otros códigos que ha vinculado a ese código_ (si es que lo ha hecho).

Al informar sobre sus _códigos_, estos recuentos le brindan algunos puntos de partida. ¿Por qué los códigos principales aparecen con tanta frecuencia? ¿Por qué son raros los de abajo? ¡Especula, teoriza, debate y discute!

### Redactar cada código

Es su trabajo informar sobre la relevancia de los códigos que ha descubierto para sus preguntas de investigación. Las _notas_ que ya ha desarrollado sobre cada código le brindan un punto de partida para los comentarios. Construya sobre ellos y use cualquier caso ejemplar que haya incorporado para ilustrar sus puntos. Si necesita _mirar hacia atrás en sus datos_, los vínculos de retroceso de sus códigos apuntarán a todos los _puntos de datos_ que codificó con un código determinado.

También es posible que desee examinar _códigos que parecen tener puntos de datos comunes_ en mente. ¿Por qué ocurrieron estas superposiciones? ¿Qué podrían significar?

A medida que revisa sus datos para desarrollar sus ideas y argumentos, puede ser útil abrir muchas _notas_ a la vez para que pueda consultar rápidamente cada una.

### Conclusión

¡Eso es todo! Incluiré este artículo en el kit.

-   11 de agosto de 2021: He abierto el medio ambiente. [¡Búscalo y colabora en él en GitHub!](https://github.com/ryanjamurphy/obsidian-qualitative-analysis-environment)
