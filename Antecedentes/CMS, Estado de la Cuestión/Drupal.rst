Drupal
######

.. image:: /_assets/img/drupal_logo.png
   :scale: 50%
   :align: center

Es una herramienta extremadamente versátil y configurable, y al igual que
Wordpress, posee gran cantidad de plugins (o módulos como los llama Drupal),
pero no dispone de tantos aspectos visuales gratuitos. Además, la gran mayoría
de éstos, inclusive los themes de pago, son de baja calidad y vistosidad. Está
enfocado en gestionar sitios web de virtualmente cualquier naturaleza gracias a
su sistema de Nodos. El principal inconveniente con Drupal es que posee una
curva de aprendizaje extremadamente elevada tanto para desarrolladores como para
*webmasters*, situación que lo ha convertido en el blanco de diversas burlas en
Internet.

.. figure:: /_assets/img/drupal_learning_curve.jpg
   :scale: 50%
   :align: center

   Curva de aprendizaje de Drupal, objetivo de continuas mofas en Internet.


Aspectos positivos
==================

- Sistema de nodos: Todo los contenidos de un sitio web Drupal son almacenados
  y tratados bajo el concepto de nodos. Un nodo puede ser cualquier tipo
  publicación, como por ejemplo una "página", un "artículo", un "nuevo tema"
  de foro, etc. El tratar todos los contenidos como nodos otorga la flexibilidad
  de definir nuevos tipos de contenidos. [drupal-nodes]_

- Sistema de bloques: Similar a los módulos de Joomla, son cajas de contenido 
  que pueden ser posicionados en las distintas regiones o áreas de un tema
  visual. Pueden ser utilizados para presentar cualquier tipo de información,
  por ejemplo, menús de navegación, breadcrumbs [#breadcrumbs]_, etc.

- Drush: Es una interfaz de línea de comando para gestionar sitios web creados
  con Drupal de una forma rápida y sencilla (similar a apt-get). Permite
  realizar tareas como por ejemplo: instalar nuevos módulos o temas visuales,
  gestionar tareas programadas, gestionar la base de datos, etc.

- Display modes: Permite a Drupal renderizar un mismo contenido de forma
  diferente según el contexto en el que se halle. Es un poderoso sistema que
  permite personalizar al detalle cómo un contenido debería ser mostrado bajo
  distintas situaciones, por ejemplo, para un artículo de un Blog sólo se
  debería mostrar un texto "resumen" cuando dicho artículo se muestra en un
  listado de un resultado de búsqueda.

- Field API: Una de las piezas fundamentales de Drupal es la capacidad que
  posee para definir multitud de contenidos distintos de forma simple, esto es
  posible a su "Field API", cuyo funcionamiento es muy similar al de un
  modelador de datos tipo `EAV 
  <http://en.wikipedia.org/wiki/Entity%E2%80%93attribute%E2%80%93value_model>`__.

- Hooks API: Los *hooks* son funciones escritas en PHP que son invocadas
  automáticamente por Drupal y sus módulos en momentos concretos de la ejecución
  del script, y que permiten modificar el comportamiento de la aplicación.

- Motor de búsqueda: Similar a Joomla, Drupal incorpora un potente motor de
  búsqueda que permite localizar contenidos y usuarios utilizando criterios de
  búsqueda. Los criterios de búsqueda aceptan una gran variedad de palabras
  claves que permiten construir búsquedas legibles por humanos, por ejemplo
  *dogs OR cats*. Su funcionamiento se basa en la indexación de palabras para
  cada contenido o usuario creado.

- Bases de datos: Ofrece soporte múltiples SGBD. Concretamente, la versión 7 de
  Drupal puede funcionar con MySQL, PostgreSQL o SQLite.



Aspectos negativos
==================

- Themes, Front y BackEnd: En Drupal, *BackEnd* y *FrontEnd* están embebidos
  lo que produce serias dificultades al tener todo combinado en una misma página.
  Por otro lado, los *themes* disponibles, ya sean gratuitos o de pago son en 
  general poco vistosos, aunque se dispone de una gran cantidad de ellos.

- Rendimiento: Su rendimiento comienza a caer de forma considerable una vez se
  han instalado algunos *plugins* para añadir funcionalidades específicas.
  Además, Drupal hace un uso intensivo del almacenamiento en BD; almacena todo
  tipo de información como por ejemplo, parámetros de configuración, plantillas
  HTML, logs, incluso llega a almacenar código PHP directamente en BD.
  En media, Drupal realiza unas 100 consultas a la BD por cada respuesta.

- Editor WYSIWYG: No cuenta por defecto con un editor enriquecido. Una de las
  tareas más habituales tras instalar Drupal es buscar e instalar un *plugin*
  para añadir esta funcionalidad.

- Curva de aprendizaje: Uno de los aspectos más criticado por la comunidad de
  desarrolladores es la complejidad de su estructura interna. La falta de
  estándares junto con una codificación en general de muy mala calidad y poco
  documentada simplemente hacen aún mas difícil el aprendizaje de la
  herramienta. La programación en Drupal, al igual que Wordpress, sigue el
  paradigma basada en procedimientos. Su API está llena de inconsistencias y
  resulta casi imposible conocer la totalidad de funciones que ésta provee; en
  especial sus *hooks*, pues Drupal provee `varios cientos 
  <https://api.drupal.org/api/drupal/includes%21module.inc/group/hooks/7>`__ de
  estas funciones que los desarrolladores han de conocer.

- Multilenguaje: No permite crear contenidos en múltiples idiomas, aunque
  existen algunos módulos que otorgan dicha funcionalidad.

- PSR: Drupal no implementa ninguno de los PSR propuestos por FIG. Aunque en
  su última versión (aún en desarrollo al momento de redactar esta memoria)
  posiblemente adopte al menos PSR-0.

- Seguridad: Drupal cuenta con un enorme historial de `vulnerabilidades 
  <http://secunia.com/community/advisories/search/?search=drupal>`__, historial
  que por desgracia se hace cada vez más extensa con las liberaciones de nuevas
  versiones.



.. figure:: /_assets/img/drupal_architecture.png
   :width: 70%
   :align: center

   Arquitectura de Drupal.



Conclusiones
============

De los tres CMS analizados en esta sección, Drupal es posiblemente el que más
posibilidades posee de las tres gracias a su sistema de Nodos, con el que es
posible crear contenidos de virtualmente cualquier tipo: Blogs, Galerías de
imágenes, Wikis, etc. Además, gracias a su sistema de *hooks* es posible alterar
casi cualquier aspecto en la ejecución de cada petición. Por desgracia, su
elevada complejidad tanto en términos de usabilidad como técnicos, hacen que la
herramienta sea muy difícil de escalar y mantener. Está más bien orientada a
personas con unos conocimientos técnicos avanzados.


.. [drupal-nodes] Drupal. About nodes, 2014
   https://www.drupal.org/documentation/modules/node

.. [#breadcrumbs] Consiste en una línea de texto en la que se indica el
   recorrido seguido y la forma de regresar. Permite que el usuario conozca la
   ruta de su ubicación en directorios y subdirectorios, y navegue a través de
   ella.
