Bloques y Regiones
==================

En QuickAppsCMS los bloques son objetos contenedores de información y son
utilizados para organizar los contenidos de un sitio web. Pueden ser utilizados
para proporcionar contenidos o funcionalidades especificas de un sitio web (por
ejemplo, un formulario de búsqueda o un listado de categorías), y pueden ser
ubicadas en las distintas regiones que un theme proporciona.

.. figure:: /_assets/img/blocks.png
   :width: 50%
   :align: center

   Ejemplo, bloques disponibles en una página web.

QuickappsCMS define dos tipos de bloques:

- Estáticos: Estos pueden ser creados desde el *BackEnd* de QuickAppsCMS por
  cualquier usuario con los privilegios adecuados. Éstos bloques contienen
  generalmente HTML plano, como texto, imágenes o material embebido de otras web
  como vídeos de YouTube o mapas de GoogleMaps.

- Dinámicos: Son aquellos bloques que son registrados por plugins de terceros y
  son capaces de ofrecer parámetros configurables a fin de modificar su
  comportamiento. El núcleo de QuickAppsCMS trae consigo unos cuantos de estos
  bloques, como por ejemplo "Language Switcher", el cual proporciona enlaces
  para que los usuarios puedan cambiar de un lenguaje a otro. Los lenguajes que
  este bloque mostrará dependerá de los administradores del sitio web hayan
  marcado como *activos*, es decir este bloque renderiza su contenido de
  forma dinámica. Estos bloques son muy similar al concepto de **widget**
  utilizado por Wordpress.

Los bloques dentro de una misma región pueden ser reordenados con un simple
"arrastrar y soltar". Además, se puede restringir su visibilidad a un conjunto
determinado de páginas o bien un conjunto de roles de usuarios, por ejemplo, un
bloque en particular puede ser mostrado únicamente a usuarios con rol de
administrador.

.. figure:: /_assets/img/regions.png
   :width: 50%
   :align: center

   Ejemplo, regiones definidas por un theme en particular.

En cuanto a las regiones, como el lector podrá ya deducir, se tratan de áreas
contenedoras de bloques definidas por cada theme. Es decir, cada theme puede
definir todas las regiones que su diseñador estime oportunas. QuickAppsCMS no
obliga a los diseñadores a implementar un conjunto predefinido de regiones como
ocurre con Drupal, sino que cada diseñador posee plena libertar para definir o
no las regiones que mejor se adapten a su diseño. Cuando se decide cambiar de un
theme a otro desde el *BackEnd* QuickAppsCMS es capaz de detectar las regiones
en común entre dos themes y mover los bloques asignados desde un theme a otro.
