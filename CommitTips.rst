=====================
Tips para los commits
=====================

* Empezar por el mensaje
========================
En lugar de considerar al **commit** como un corte, como un guardado para evitar perder cosas, pienso en el **commit**
como una unidad de trabajo con un **objetivo**. Ese **objetivo** lo voy a expresar en el **mensaje**, y voy a escribir
(o al menos pensar) ese mensaje antes de efectuar las modificaciones (por ejemplo, escribir una función en Python).
El mensaje tiene que ser una oración simple, básicamente compuesta de sujeto y predicado. Comparado con un **Caso de Uso**
que representa la relación entre **actores** y **acciones**, el sujeto es un actor y el predicado es la acción.

.. snipet::
    Actor ----- Acción

Si el actor es una función y la acción es el agregado en el código:
.. snipet::
    :filename: mensaje

    "agregar función"

Una vez pensado ese mensaje, empezamos a trabajar en la tarea. Puede ser que el desarrollo de esa tarea impliqe cambios
en ese mensaje, no importa, lo importante es el enfoque: pensar el objetivo y al logralo confirmar los cambios con el
commit.

* Analizar el mensaje del commit
================================
* El mensaje es una oración simple:
    Eso es un **commit**.

* El mensaje tiene varios predicados es decir varias acciones diferenciadas:
    Es momento de dividir el mensaje. Una forma de resolver esto es abrir otra rama de trabajo o **branch**, y antes de
    de comenzar a trabajar, elaborar cada oración correspondiente al mensaje de cada uno de los **commits** resultantes.

* El mensaje tiene varios sujetos es decir varios elementos sobre los que se va a aplicar una acción:
    Acá hay dos opciones:
    * Si esos sujetos representan entidades bien diferenciadas, por ejemplo clases de un modelo de
    arquitectura en la que cada una tiene métodos con propósitos bien diferenciados, es probable que dependiendo de la
    complejidad de la tarea también sea recomendable dividir el mensaje u objetivo.
    * Si esos sujetos representan un mismo tipo de entidad por ejemplo objetos o instancias de una misma clase, sobre
    los que se va a ejecutar la misma acción o tarea y además sus métodos de clase asociados son los mismos, podemos
    pensar en un objetivo único con una tarea repetitiva, y se puede mantener todo en el mismo commit salvo que
    implique un desarrollo complejo.
    Estos ejemplos son muy generales. En la práctica, vamos aplicar nuestro criterio o sentido común (pensando como
    equipo u organización) para en cada caso saber como dividir el problema en commits.

* Tengo varios objetivos y los mensajes que elaboré para cada uno son muy similares:
    Puede darse la situación en la que tenga varios objetivos de trabajo y los mensajes en los que pensé para cada uno
    sean muy parecidos. Esto puede ser que represente una tarea repetitiva aplicada a distintos elementos. En este caso
    aplicaría los criterios del punto anterior, con la diferencia de que en este caso tenía planificado de antemano
    trabajar en varios commits y existe la posibilidad de desarrollarlos en el mismo **commit**, valga la redundancia,
    aplicando los criterios y el sentido común citados en el caso de un mensaje con varios sujetos.

Ejemplos
========

...