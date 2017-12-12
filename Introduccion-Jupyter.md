# Jupyter Notebook

## Qué es  Jupyter  Notebook?

[Jupyter Notebooks](https://jupyter-notebook.readthedocs.org/en/latest/notebook.html) (antes IPython Notebooks), son documentos web  que combinan  texto con el formato markdown,  expresiones matemáticas escritas en Latex con MathJax y  sentencias ejecutables  de Python.

## Lanzamiento del servidor de Jupyter notebook

Para lanzar la aplicación, primero abrimos el terminal e escribimos lo siguiente

```Bash
jupyter notebook
```

Esto iniciará el servidor de Jupyter de manera automática en un navegador web predeterminado, pero si no se consigue esto de manera correcta, simplemente abrimos un   navegador web cualquiera e escribimos  en la barra de direcciones.


```
http://localhost:8888/tree
```

Esto mostrará un simple navegador de archivos que muestra  el contenido del directorio desde el que se ha lanzado el terminal. Debes hacer  clic en el botón `New Notebook` y luego seleccionar ** Python 3 ** u otro lenguaje,  en la parte inferior para crear tu primer cuaderno o notebook.

![nnotebook](Imagenes/nnotebook.gif)

## Executando una celda de código

Debajo de las barras de herramientas, verás una celda de código, prefijada con `In []:`. Esta celda puede contener  segmentos de código arbitrariamente largo, pero se puede comenzar con una simple expresión. En esa celda de código escribimos

```Python
x = 5
```

y entonces pulsamos  *Shift+Enter*.  Si  hacemos click en Enter, te darás con la sorpresa de que simple agregarás otra linea a la celda en la cual te encuentras trabajando. Siempre pulsamos  *Shift+Enter* para realizar operaciones en la celda de código.

¿Entonces qué pasó? Hemos asignado  a x el número 5 con la observación que  la etiqueta de esa celda ahora leerá `In [1]:` porque esa es la primera instrucción que hemos ejecutado con este kernel de Python. También notarás que el cuaderno ha creado una nueva celda, ya que  hemos utilizamos la única celda existente.

En esta nueva celda, inprimimos  el valor que asignamos a x, usando una función de Python

```Python
print(x)
```

pulsamos  **Shift+Enter** y tenemos  la salida que esperamos!.
La celda recibe la etiqueta `In [2]:` con la respuesta  de ese comando impresa  inmediatamente debajo de la celda. Todo el procedimiento debe ser algo como esto:


![corre-imprime](Imagenes/correr-imprimir.gif)

## Kernels en Jupyter Notebook

Un *kernel*  es un programa que ejecuta e introspecta el código de un usuario. Jupyter incluye un kernel para código Python en sus dos versiones 2 y 3, además de que existen  otros kernels para otros lenguajes.

* [Making kernels for Jupyter](http://jupyter-client.readthedocs.io/en/latest/kernels.html)

## Sobreescribiendo  variables

Puesto que cada celda está interactuando con la misma instancia de Python, si le damos a `x` un nuevo valor y escribimos  ` print (x) `obtendremos ese nuevo valor. Eso es bastante sencillo, pero ¿qué pasa si eliminamos la celda donde le dimos a `x` un nuevo valor?. Veamos


![sobreescribir-variables](Imagenes/sobreescribir.gif)

Aunque eliminamos la celda donde asignamos `x = 7`, la asignación sigue siendo válida. De hecho, la asignación permanecerá válida hasta que explícitamente ejecutemos una celda que establece x igual a un nuevo valor, o hasta que se reinicie completamente esta instancia de Jupyter notebook .

## Markdown

Markdown es un lenguaje de marcado ligero parecido al que se emplea en muchas wikis y basado originalmente en convenciones existentes en el marcado de los los correos electronicos. Emplea texto plano, procurando que sea legible pero consiguiendo que se convierta en XHTML correctamente formateado.

Es realmente impresionante. Las celdas en  dJupyter se pueden utilizar para muchas cosas: ejecutar código Python, escribir texto en Markdown, etc. Esto nos permite escribir notas sobre lo que estamos haciendo, el código que estamos trabajando utilizando inclusive diferentes librerias, lo que estamos * tratando * de hacer, lo que queramos!.

Para crear una celda de Markdown en Jupyter, hacemos clic en una celda vacía, luego haga clic en la lista desplegable (por defecto, dirá "Código") y seleccione "Markdown", como se muestra a continuación.

Markdown es también (tipo de) código, así que después de escribir algún texto, también se pulsa * Mayús + Enter * para ejecutar la celda y renderizar el texto de Markdown. Por ejemplo simplemente escribe una oración o dos en una celda de márgenes, luego pulse * Mayús + Intro * para procesar el texto.

*  [Markdown tutorial](http://www.markdowntutorial.com/)

![markdown](Imagenes/rmarkdown.gif)

## MathJax

Markdown puede hacer más que solo renderizar simple texto, puede renderizar texto y ecuciones  en Latex usando **MathJax**!

* Para ecuaciones matemáticas en una sola línea, rodea el código LaTeX dentro de signos `$` individuales
`$...$`

* Para la representación de entornos de matématicas, rodea el código de LaTeX dentro de los signos `$$`
`$$...$$`

![mathjax](Imagenes/mathjax.gif)

**Notas:**


Tenga en cuenta que la composición matemática es manejada por MathJax y no por LaTeX. Aunque la gran mayoría de la sintaxis de MathJax es idéntica a LaTeX, hay algunas pequeñas diferencias.

* [What is the relation between Latex and MathJax?](http://meta.math.stackexchange.com/questions/6177/what-is-the-relation-between-latex-and-mathjax).

## Más sintaxis de Markdown

Hay varias referencias para aprender Markdown, una de las mejores referencias es la [John Gruber](http://daringfireball.net/projects/markdown/syntax).  Algunas características que pueden ser útiles, se listan a continuación:

Para escribir en cursiva, ajuste el texto con `*`: `*letras en cursiva*`
Para escribir en negrita, ajuste el texto con `**`: `**letras en negrita**`

Para una lista con viñetas, inicie la línea con  `*`, luego escribe en el espacio seguido por el elemento de viñeta
```
* item
* otro item
* adicional item
```

Se pueden crear bloques de código para albergar extractos de código fuente de un lenguaje de programación o para reproducir literalmente cualquier tipo de texto sin que sea interpretado por markdown.  Una opción para resaltar pequeños trozos de código dentro de párrafos de texto normal. Para lograr esto debemos encerrar el código entre dos acentos graves .

## Moviendo las celdas alrededor

A menudo se desea agregar o eliminar celdas, o simplemente moverlos alrededor. Para mover una celda, simplemente haga clic en ella para seleccionarla, luego use las flechas Arriba y Abajo en la barra de herramientas para cambiar la posición de la celda.

![mov-celdas](Imagenes/mov-celdas.gif)

Para agregar una celda, puede hacer clic en el botón + en la barra de herramientas. Una vez que conozcas  el diseño de notebook de Jupyter, también puedes hacer clic en  *Help -> Keyboard Shortcuts*  para encontrar varios accesos directos para agregar, eliminar y administrar la posición y el tipo de celda.

