=====================================================================
Guia para practicar con repositorios remotos sin miedo a romper nada:
=====================================================================

*#. Crear carpetas
    En una carpeta raiz, por ejemplo **remotes/**, creamos cuatro carpetas:
    .. code-block:: bash
    	cd remotes
	    mkdir server
	    mkdir client-1
	    mkdir client-2
        mkdir client-3

*#. Inicializar proyecto
    En la recientemente creada server, creamos un proyecto nuevo, por ejemplo, **my-files**:
	.. code-block:: terminal
	    cd server
	    mkdir my-files
	    cd my-files
	    git init

*#. Incluir archivos y/o carpetas iniciales
    Tomamos los archivos y subcarpetas con que trabajajemos habitualmente y los copiamos en el proyecto inicializado:
	.. code-block:: terminal
    	cp ruta/carpetas/archivos remotes/server/carpetas/archivos
	    cd remotes/server/my-files
	    git add .
	    git commit -m "first commit"

*#. Clonar proyecto
    Clonamos el repositorio del server en cada cliente
	.. code-block:: terminal
    	cd ../client-1
	    git clone ../server/my-files
	    cd ../client-2
	    etc.

5. Continuar trabajando alternativamente en cada client creando previamente un branch para cada tarea específica, dividiendo cada tarea en commits acotados para aplicar cada cambio.

Tips para los commits:
	Diferenciar los cambios que voy a aplicar:
		a. Los cambios implican una tarea que requiere planificación en varios pasos:
			dividir cada paso en commits
		b. Los cambios implican una actividad relativamente extensa pero repetitiva, por ejemplo escribir la misma palabra cincuenta veces.
			hacer un solo commit
	Una forma de diferenciar qué tipo de cambios son los que voy a aplicar, en ambos casos, es escribir los mensajes de los commits antes de ejecutar las tareas:
		a. El mensaje es una oración simple (sujeto, predicado y algún modificador) representa un commit.
		b. La oración tiene sólo un verbo pero repite mucho la palabra y en el sujeto o en un modificador (y esto, y lo otro, etc.) dividir en más commits.
		c. La oración se va a repetir en varios commits, unir esos commits en uno.
	El objetivo es que cuando me encuentre en una situación donde las cosas no salen como esperaba o no encuentro parte del trabajo, puedo buscar a traves de los commits como estaba todo en determinado punto e identificar el problema.
