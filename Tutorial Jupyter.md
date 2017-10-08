# Tutorial

## 0. Links

Video Principal: https://www.youtube.com/watch?v=b7CbZPwEjVw <br>

Jupyter: 

1. http://jupyter.readthedocs.io/en/latest/install.html
2. https://stackoverflow.com/questions/31989995/how-can-i-safely-install-jupyter-ipython-4-over-a-conda-installation 

Instalando matplotlib: https://stackoverflow.com/questions/43437884/jupyter-notebook-import-error-no-module-named-matplotlib <br>

mini-conda: https://conda.io/miniconda.html <br>

latex: 

1. https://stackoverflow.com/questions/13208286/how-to-write-latex-in-ipython-notebook
2. http://reu.dimacs.rutgers.edu/Symbols.pdf
3. http://nbviewer.jupyter.org/github/ipython/ipython/blob/1.x/examples/notebooks/Part%205%20-%20Rich%20Display%20System.ipynb

markdown:

1. https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet
2. https://www.tablesgenerator.com/markdown_tables

## 1. Instalar mini-conda y Python 3

CloudNine incluye Python 2.7 por defecto, pero es necesario instalar Python 3

<pre>
$ wget https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh
$ chmod a+x Miniconda3-latest-Linux-x86_64.sh
$ ./Miniconda3-latest-Linux-x86_64.sh
</pre>

Aceptar todo y abrir una nueva terminal

## 1.1 Creando un environment

No probar esto todavía.

<pre> 
$ conda create -n py3 python=3 jupyter
$ source activate py3
</pre>

## 2. Instalar y ejecutar Jupyter Notebook

Saltarse la primera línea en caso de haber creado el environment.

<pre>
$ conda install jupyter
$ jupyter notebook --ip=0.0.0.0 --port=8080 --no-browser
</pre>

### Notas

* Abrir el link que sale al final. 
* Se debe escribir el último comando cada vez que se inicia el workspace en C9.
* En caso de haber creado un environment en Python es necesario acceder a este primero.

## 2.1 Crear un alias

1. Dar click al engranaje situado en la esquina superior derecha del árbol de directorios
2. Seleccionar 'Show Home in Favorites' y 'Show Hidden Files'
3. Agregar al final del archivo '.bash_aliases':

<pre>$ alias jnmb='jupyter notebook --ip=0.0.0.0 --port=8080 --no-browser' </pre>

Abrir una nueva terminal. Ahora para ejecutar Jupyter solo es necesario escribir jnmb en la consola.

### Notas

Jupyter a veces presenta problemas de conexión, aumentar la RAM a 1 gb y actualizar donde se pueda.

## 3. Instalar matplotlib

<pre>
$ pip install matplotlib
</pre>