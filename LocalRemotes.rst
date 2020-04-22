====================================================================
Guia para practicar con repositorios remotos sin miedo a romper nada
====================================================================

1. Crear carpetas
=================
En una carpeta raiz, por ejemplo **remotes/**, creamos cuatro carpetas:

.. code-block:: bash

    cd remotes
    mkdir server
    mkdir client-1
    mkdir client-2
    mkdir client-3

2. Inicializar proyecto
=======================
En la recientemente creada server, creamos un proyecto nuevo, por ejemplo, **my-files**:

.. code-block:: bash

    cd server
    mkdir my-files
    cd my-files
    git init

3. Incluir archivos y/o carpetas iniciales
==========================================
Tomamos los archivos y subcarpetas con que trabajajemos habitualmente y los copiamos en el proyecto inicializado:

.. code-block:: bash

    cp ruta/carpetas/archivos remotes/server/carpetas/archivos
    cd remotes/server/my-files
    git add .
    git commit -m "first commit"

4. Clonar proyecto
==================
Clonamos el repositorio del server en cada cliente

.. code-block:: bash

    cd ../client-1
    git clone ../server/my-files
    cd ../client-2
    etc.

5. Trabajar en los clientes
===========================
Continuar trabajando alternativamente en cada **client** creando previamente un branch para cada tarea específica,
dividiendo cada tarea en commits acotados para aplicar cada cambio.
