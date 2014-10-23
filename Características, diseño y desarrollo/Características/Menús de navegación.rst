Menús de navegación
===================

El sistema de menús proporcionado por QuickAppsCMS proporciona una forma simple
e intuitiva para la creación de árboles de navegación. Permite definir enlaces
de forma jerárquica utilizando árboles de datos MPTT [#mptt]_. Este sistema está
estrechamente ligado al sistema de bloques y regiones, pues cada menú posee un
bloque asociado es utilizado para renderizar el correspondiente menú de
navegación en un región de un theme. Es decir, el sistema de menús unicamente
define la estructura de los datos, mientras que todo el proceso de renderizado
es delegado al sistema de bloques.

.. figure:: /_assets/img/menu_tree.png
   :width: 50%
   :align: center

   Editor de árbol de navegación, los enlaces pueden ser reorganizados
   simplemente arrastrando y soltado con el ratón.

El sistema de menús permite crear árboles de enlaces de una profundidad
ilimitada, en contraste con Drupal que ofrece una profundidad máxima de 9. Por
otro lado, ofrece un solución muy simple a un problema frecuente que existe en
la mayoría de gestores de contenidos que ofrecen sistemas para la gestión de
menús: no es posible indicar cuando un enlace debe mostrarse como *activo*, y en
caso de ser posible por lo general es un proceso automático en donde el usuario
carece de un control sobre el mismo. Por ejemplo en Wordpress hay que recurrir a
la programación de código PHP para controlar cuando un enlace debe o no
mostrarse como activo. El sistema de menús proporcionado por QuickAppsCMS ofrece
opciones para controlar esta situación directamente desde el *BackEnd* de la
aplicación, por ejemplo, puede indicarse que un enlace se muestra como activo
para un conjunto determinado de direcciones o URLs, o bien se puede dejar
decidir a la aplicación decidir el estado de cada enlace.


.. [#mptt] Siglas de Modified Preorder Tree Traversal.
