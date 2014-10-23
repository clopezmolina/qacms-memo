Tipos de contenidos
===================

Como se analizó en capítulos anteriores, Drupal posee una enorme flexibilidad
gracias a la capacidad para definir nuevos tipos de contenidos de forma
simplificada. Por ejemplo, una entrada de Blog se compone generalmente por un
título y un cuerpo; mientras que una noticia cuente quizás, con un titular, una
entradilla y un cuerpo. Tanto Artículo como Noticia son contenidos, pero de
distinto tipo, diferenciándose entre ellos por los "campos" que definen sus
estructuras.

QuickAppsCMS provee una sofisticada API denominada *Field API* la cual
permite, entre otras cosas, añadir propiedades (o atributos) virtuales a
cualquier Entidad. Haciendo uso de está API QuickAppsCMS es capaz de
proporcionar un mecanismo muy similar al empleado por Drupal para definir nuevos
tipos de contenidos de forma simple y eficiente.


Field API (EAV)
---------------

La *Field API* de QuickAppsCMS permite a cualquier tabla definir columnas
adicionales sin necesidad de alterar físicamente su esquema. Esta API es
proporcionada en forma de Behavior y cualquier tabla puede hacer uso de ella
para añadir esta funcionalidad.

Proporciona además una interfaz gráfica de usuario (GUI) encapsulada en forma de
Trait, de manera que otros plugins del sistema puede hacer uso de ella y así
ofrecer a los usuarios una forma simple y amigable de gestionar todas estas
columnas virtuales.

.. figure:: /_assets/img/EAV.png
   :scale: 75%
   :align: center

   Field API es un modelador de datos EAV.

Estas "columnas virtuales" reciben internamente el nombre de "Fields", pues son
más que meras celdas contenedoras de información atómica, sino que se tratan en
realidad de complejas mini-aplicaciones encargadas de gestionar las operaciones
relacionadas con el procesamiento de datos (CRUD). Así por ejemplo, podemos
tener columnas capaces de gestionar complejas estructuras de información como
una "galería de imágenes" o un "listado".

Otra característica de esta API es que permite utilizar estas columnas virtuales
como parte de cláusulas WHERE de una consulta SQL, como si de una columna real
se tratase. Característica que al ser combinada con el motor de búsqueda
integrado de QuickAppsCMS es capaz de ofrecer sorprendentes resultados.


View Modes
----------

QuickAppsCMS proporciona un sistema para definir *contextos de renderizado*,
así por ejemplo, un mismo contenido puede ser mostrado de diversas formas según
el contexto en el que se halle. Por ejemplo, para un artículo de un Blog sólo se
debería mostrar un texto "resumen" cuando dicho artículo se muestra como parte
de un resultado de búsqueda.

Por defecto QuickAppsCMS trae consigo un conjunto predefinido de estos
contextos, aunque otros plugins poseen plena libertad para añadir nuevos
contextos o redefinir los ya existentes. Los contextos predefinidos incluidos en
toda instalación de QuickAppsCMS son:

- Default: Es utilizado como contexto por defecto si no se ha detectado ningún
  contexto coincidente.

- Teaser: Es un formato muy corto que es comúnmente utilizado en la página
  principal de los sitios web en forma de, por ejemplo, "ultimas noticias", etc.

- Search Result: Es un formato corto utilizado generalmente al listar múltiples
  contenidos a la vez como por ejemplo un resultado de búsqueda.

- RSS: Muy similar a *Search Result*, pero destinado a mostrar listados de
  contenidos de un feed RSS.

- Full: Utilizado por lo general cuando un contenido de mostrado en su propia
  página, por ejemplo el detalle de una noticia.

Estos contexto son automáticamente establecidos por QuickAppsCMS durante la
ejecución del script, aunque cualquier plugins de la plataforma pueden cambiar
de un contexto a otro con total libertad.