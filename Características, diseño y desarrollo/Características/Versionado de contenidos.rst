Versionado de contenidos
========================

El versionado de contenidos es una funcionalidad que permite crear y gestionar
históricos sobre los contenidos de un sitio web. En QuickAppsCMS cada vez que un
contenido es modificado su estado previo a los cambios es almacenado de forma
que en un futuro pueda ser restaurado a su estado anterior. En QuickAppsCMS
todos los contenidos son tratados como objetos-entidades portadores de
información, por ello los respaldos consisten básicamente en una serialización
de dichos objetos. Las ventajas de esto último es que permite crear históricos
de contenidos con estructuras complejas de información, pues en la mayoría de
gestores de contenidos esta funcionalidad está limitada a contenidos de tipo
texto plano, como por ejemplo en Wordpress.

.. figure:: /_assets/img/revisions.png
   :scale: 60%
   :align: center

   Interfaz de gestión para versionado de contenidos.
