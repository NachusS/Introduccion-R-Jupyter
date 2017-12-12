# Introduccion-R-Jupyter
Utilización de Jupyter Notebook con R. (Herramienta didáctica)
# Seminario utilización Jupyter Notebook con R, en clase.

## Esta documentación ha sido clonada del (Sitio web del curso de R)
Autor: (Cesar Lara)
* http://c-lara.github.io/Curso-R/ 

## Introducción

En este seminario se pretende mostrar la facilidad de manejo y las múltiples posibilidades que tenemos al utilizar
Jupyter notebook, con R o Python, tanto en clase, pŕácticas o entrega de Informes finales.

Se usará un [kernel nativo de R](https://github.com/IRkernel/IRkernel), sobre [Jupyter](http://jupyter.org/) descargado a traves de [Anaconda](https://www.continuum.io/anaconda-overview), además de otras herramientas mencionadas abajo.

R como lenguaje de programación y multiparadigma, plantea un modo distinto de escribir código, por lo que  precisa de ciertos requisitos, que se enumeran a continuación:


## Elementos Clave

* Manejo de línea de comandos y Markdown.
* Uso de Git y Github.
* El lenguage de programación R.
* R básico.
* Gráficos.


## Software

### Anaconda 

[Anaconda](https://www.continuum.io/downloads) es una distribución completa  libre de [Python](https://www.python.org/) incluye [paquetes de Python ](http://docs.continuum.io/anaconda/pkg-docs).

Anaconda incluye los instaladores de Python 2.7 y 3.5.  La instalación en **Linux**, se encuentra en la página de Anaconda y es 
más o menos así,

  * Descargar el instalador de Anaconda para Linux.

  * Después de descargar el instalar, en el terminal, ejecuta para 3.5.

```bash
bash Anaconda3-2.4.1-Linux-x86_64.sh

```
Instalando Anaconda con su navegador, en l aúltima versión ya viene preparado la descarga del lenguaje R, para que se pueda utilizar con los notebooks. De todas formas aqui explico, como se puede instalar desde la linea de comandos, si ya se tuvieviera instalado Anaconda.

Es recomendable leer, alguna de las característica de Anaconda en el siguiente material [conda 30-minutes test drive](http://conda.pydata.org/docs/test-drive.html).

**Otros proyectos y librerias interesantes para utilizar con este entorno:**

 * La instalación de paquetes como [seaborn](http://stanford.edu/~mwaskom/software/seaborn/) o [bokeh](http://bokeh.pydata.org/en/latest/) se pueden realizar a través de Anaconda, de la siguiente manera:



``` bash
 conda install bokeh
```
Alternativamente podemos desde PyPI usando **pip**:

```bash
pip install bokeh
``` 

El proyecto [Anaconda](https://www.continuum.io/downloads) ha creado [R Essentials](http://anaconda.org/r/r-essentials), que incluye el IRKernel y alrededor de 80 paquetes para análisis de datos, incluyendo `dplyr`, `shiny`, `ggplot2`,`caret`, etc. Para instalar **R Essentials** en un entorno de trabajo, hacemos

```bash
 conda install -c r r-essentials
``` 

### Proyecto Jupyter y el Jupyter Nbviewer

El [Proyecto Jupyter](http://jupyter.org/)  es una aplicación web que te permite crear y compartir documentos que contienen código de diversos lenguajes de programación, ecuaciones,  visualizaciones y texto en diversos formatos. El uso de Jupyter incluye la ciencia de datos, simulación numérica, la modelización en estadística, Machine Learning, etc.


[Jupyter nbviewer](https://nbviewer.jupyter.org/)  es un servicio web gratuito que te permite compartir las versiones de archivos realizados por Jupyter, permitiendo el renderizado de diversos fórmatos incluyendo, código latex.

- [Jupyter Documentation](https://jupyter.readthedocs.io/en/latest/).

[Unofficial Jupyter Notebook Extensions](http://jupyter-contrib-nbextensions.readthedocs.io/en/latest/) contiene una colección de extensiones no oficiales de la comunidad que añaden funcionalidad a Jupyter notebook. Estas extensiones están escritas principalmente en Javascript y se cargarán localmente en su navegador.

```bash
 pip install jupyter_contrib_nbextensions
```

O utilizando conda

```bash
conda install -c conda-forge jupyter_contrib_nbextensions
```

#### Kernel de bash en Jupyter 
- Las notas sobre comandos Linux (clase1)  se usado el kernel de Bash de Jupyter:

    ```
    pip install bash_kernel
    python -m bash_kernel.install
    ```
### Git y Github

[Git](https://git-scm.com/) es un sistema de control de versiones de gran potencia y versatilidad en el manejo de un gran número de archivos de  código fuente a a través del desarrollo no lineal, es decir vía la gestión rápida de ramas y mezclado de diferentes versiones.

Para poder revisar y aprender los comandos necesarios de Git, puedes darle una ojeada al excelente [tutorial de CodeSchool](https://try.github.io/levels/1/challenges/1) o a la [guía](http://rogerdudler.github.io/git-guide/index.es.html) de Roger Dudle para aprender  Git.

[Github](https://github.com/) es una plataforma de desarrollo colaborativo de software utilizado para alojar proyectos (muchos proyectos importantes como paquetes de R, Django, el Kernel de Linux, se encuentran alojados ahí) utilizando Git y el framework Ruby on Rails.

Podemos instalar Git en Ubuntu utilizando el administrador de paquetes `Apt`:

```bash
c-lara@Lara:~$sudo apt-get update
c-lara@Lara:~$sudo apt-get install git
```

Referencias y Lecturas

- [Usando el GIT](http://www.cs.swarthmore.edu/~newhall/unixhelp/git.php).
- [Practical Git Introduction](http://marc.helbling.fr/2014/09/practical-git-introduction).
- [Visual Git Guide](http://marklodato.github.io/visual-git-guide/index-es.html).

Existe un versión de git para Windows, que se puede descargar [aquí](https://git-scm.com/download/win), así como también  una lista de GUI, que podemos usar en Windows: [Lista de GUI para git](https://git-scm.com/downloads/guis).

### R y Rstudio

[R](https://www.cran.r-project.org/) y [RStudio](https://www.rstudio.com/) . RStudio es un IDE para R. Es software libre con licencia GPLv3 y se puede ejecutar sobre distintas plataformas  o incluso desde la web usando [RStudio Server](https://support.rstudio.com/hc/en-us/articles/200552306-Getting-Started).


```bash
wget https://download1.rstudio.org/rstudio-0.99.893-amd64.deb
sudo dpkg -i *.deb
rm *.deb
``` 
- [Programming Part 1 (Writing code in RStudio)](https://www.rstudio.com/resources/webinars/rstudio-essentials-webinar-series-part-1/).
- Using R and Rstudio for Data Management, Statistical and Graphics, Nicholas J. Horton and Ken Kleinman, CRC Press, 2015.

Para actualizar [R](https://www.cran.r-project.org/) se podría escribir en el terminal

```
sudo echo "deb http://cran.rstudio.com/bin/linux/ubuntu precise/" | sudo tee -a /etc/
```

### R Presentations

[R presentations](https://support.rstudio.com/hc/en-us/sections/200130218-R-Presentations) son una característica de RStudio que permiten la creación fácil de presentaciones HTML5 utilizando una combinación de Markdown y R.

El objetivo de R Presentations es crear diapositivas  que hagan uso de código R y de  ecuaciones de LaTeX tan sencillas como sea posible. Son especialmente útiles para el uso en el aula o en la enseñanza, ya que se puede presentar mostrar  código durante la presentación.

### ggplot2

[ggplot2](http://ggplot2.org/) es un paquete pata gráficos de R, basado en basado en *Grammar on Graphics* de Wilkonson y está formado  de un conjunto de componentes independientes que pueden ser usadas de muchas maneras diferentes. La forma de instalar este paquete es de la forma habitual

```r
install.package('ggplot2')
```

La sintaxis es un poco distinta, como indica el siguiente ejemplo


```r
geom_lm <- function(formula = y ~ x, colour = alpha("steelblue", 0.5), 
                    size = 2, ...)  {
  geom_smooth(formula = formula, se = FALSE, method = "lm", colour = colour,
    size = size, ...)
}
ggplot(mpg, aes(displ, 1 / hwy)) + 
  geom_point() + 
  geom_lm()
ggplot(mpg, aes(displ, 1 / hwy)) + 
  geom_point() + 
  geom_lm(y ~ poly(x, 2), size = 1, colour = "red")
```

Mayor información en la [documentación de ggplot2](http://docs.ggplot2.org/current/). 

El paquete gglot2, tiene una lista de [extensiones](http://www.ggplot2-exts.org/gallery/), para aumentar la funcionalidad y la interacción en los gráficos.

### R Markdown 

[R Markdown](http://rmarkdown.rstudio.com/index.html) es un framework para ciencia de datos de manera que puede crear reportes dinámicos con R, además de ejecutar y guardar código. Por ejemplo sea un tabla en markdown con R.

```r
cat("x | y", "--- | ---", sep="\n")
cat(apply(df, 1, function(X) paste(X, collapse=" | ")), sep = "\n")
```

R Markdown soporta formatos de salida estáticos y dinámicos que incluye  hTML, pdf,  beamer-latex, html5T, shiny,etc.

Más información:


* [Lecciones de R Markdown ](http://rmarkdown.rstudio.com/lesson-1.html).



### R Notebooks


Un R Notebooks es un documento R Markdown, que permite mostrar independientemente e interactivamente , código R y sintaxis de  otros lenguajes. Es una manera fácil de generar reportes, análisis estadísticos, visualización de datos.

Más información en  la página de  [R Notebooks](http://rmarkdown.rstudio.com/r_notebooks.html).


### Shiny 

[Shiny](http://shiny.rstudio.com/)  es una herramienta para crear fácilmente aplicaciones web interactivas **(apps)** que permiten a los usuarios interactuar con sus datos sin tener que manipular el código, usando un paradigma conocido como [programación reactiva](https://en.wikipedia.org/wiki/Reactive_programming)  que enfatiza  valores que cambian en el tiempo
 y expresiones que registran esos cambios.  Para sacar el máximo partido de Shiny, se debe  entender el modelo de [programación reactiva](http://shiny.rstudio.com/articles/reactivity-overview.html) que se utiliza. 

Más información en el [tutorial de Shiny](http://shiny.rstudio.com/tutorial/)


### Knitr 

[knitr](http://yihui.name/knitr/)  fue diseñado para ser una máquina de generación dinámica de reportes o documentos que son  una mezcla de texto y código que se procesa y devuelve respuestas válidas para la ciencia de datos. 

El diseño de knitr permite no permite sólo código R, sino de otros lenguajes como Python, Java Script o Awk, además de producir resultados en formatos como LaTeX, HTML5, Markdown, AsciiDoc, etc, como se muestran en los [ejemplos de knitr](https://github.com/yihui/knitr-examples).

El paquete [**Knitr**](http://yihui.name/knitr/) se instala en R


```r
install.packages("knitr")
library("knitr")
```


Knitr es libre, además de poseer muchos [ejemplos](https://github.com/yihui/knitr-examples) y [demostraciones](http://yihui.name/knitr/demos/).

### SQL y PostgreSQL

El SQL es el lenguaje estándar ANSI/ISO de definición, manipulación y control de bases de datos relacionales.

[PostgreSQL](https://www.postgresql.org/ ) es un sistema de administración de bases de datos relacionales (RDBMS). Significa que es un sistema para administrar datos guardados en relaciones. Una relación es esencialmente un término matemático para referirse a una tabla aunque  existen otras maneras de organizar las bases de datos. 

Una buena referencia de SQL es el libro de Thomas Nield [Getting Started with SQL A Hands-On Approach for Beginners](http://shop.oreilly.com/product/0636920044994.do ). 

La instalación de PostgreSQL en Linux, se da en la siguiente [página](https://launchschool.com/blog/how-to-install-postgres-for-linux).

- **Lectura Recomendable: [Introduction to SQL](https://launchschool.com/books/sql)**.
- [Started with Postgresql and R](https://datashenanigan.wordpress.com/2015/05/18/getting-started-with-postgresql-in-r/).
- [Mastering SQL for data science ](http://www.kdnuggets.com/2016/06/seven-steps-mastering-sql-data-science.html).

### Roxygen 

[Roxygen](http://roxygen.org/) es un sistema para escribir documentación de  paquetes y si estás familiarizado con Javadoc, reconocerás su sintaxis de manera casi natural. Pero Roxygen, hace algunas cosas más, como la de incluir  el manejo de espacio de nombres de importación y exportación. Para usar este paquete , primero debemos  instalarlo, así que debes ejecutar lo siguiente:

```
install.packages("roxygen2")
```
### Explicacióń y partes del Seminario con ejemplos de Notebooks en R

1. **Introducción a Jupyter Notebook** [introducción](https://github.com/NachusS/Introduccion-R-Jupyter/blob/master/Introduccion-Jupyter.md)

2. **Ejemplo de Notebook en R**

