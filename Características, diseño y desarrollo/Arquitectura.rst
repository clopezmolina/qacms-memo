Arquitectura
############

La arquitectura de QuickAppsCMS, como en todas las webs, es de tipo cliente-
servidor: los clientes hacen uso de un navegador web y realizan un intercambio
de información con el servidor, quien se encarga de recibir y atender todas las
peticiones adecuadamente. En cuanto al lado del servidor, QuickAppsCMS sigue el
paradigma MVC como base para su arquitectura, paradigma que es en realidad
definido por CakePHP, framework sobre el cual está construido QuickAppsCMS. Y
que como bien su nombre indica, MVC (Model-View-Controller), divide la lógica de
la aplicación en tres partes:

- Model: El modelo representa la parte de la aplicación que implementa la lógica
  de negocio. Ésto significa que es responsable de la recuperación de datos
  convirtiéndolos en conceptos significativos para la aplicación, así como su
  procesamiento, validación, asociación y cualquier otra tarea relativa a la
  manipulación de dichos datos.

- View: La vista hace una presentación de los datos del modelo estando separada
  de los objetos del modelo. Es responsable del uso de la información de la cual
  dispone para producir cualquier interfaz de presentación de cualquier petición
  que se presente.

- Controller: La capa del controlador gestiona las peticiones de los usuarios.
  Es responsable de responder la información solicitada con la ayuda tanto del
  modelo como de la vista. Los controladores pueden ser vistos como
  administradores cuidando de que todos los recursos necesarios para completar
  una tarea se deleguen a los trabajadores más adecuados. Espera peticiones de
  los clientes, comprueba su validez de acuerdo a las normas de autenticación o
  autorización, delega la búsqueda de datos al modelo y selecciona el tipo de
  respuesta más adecuado según las preferencias del cliente. Finalmente delega
  este proceso de presentación a la capa de la Vista.


El ciclo de una petición en QuickAppsCMS
========================================

.. figure:: /_assets/img/basic_mvc.png
   :scale: 80%
   :align: center

    Manejo de una petición típica en QuickAppsCMS.

El ciclo de una petición típica en QuickAppsCMS comienza cuando un usuario
solicita una página o un recurso. A un nivel muy alto de abstracción esta
petición pasa por las siguientes etapas para ser atendida:

1. La petición es inicialmente procesada por distintos enrutadores
   [#enrutadores]_ (Routers).

2. La petición luego de haber sido correctamente enrutada, el despachador
   (Dispatcher) busca e inicializa el controlador adecuado para atender la
   petición.

3. Se invoca la acción del controlador correspondiente para atender la petición,
   el controlador interactúa con los modelos y componentes correspondientes en
   caso de ser necesario.

4. El controlador delega en la vista la tarea de generar una presentación
   resultante de los datos proporcionada por el modelo.

5. Finalmente, cuando esta presentación se genera, se envía de inmediato al
   usuario.


Arquitectura de alto nivel
==========================

En la figura de a continuación se representan los elementos que conforman
QuickAppsCMS a más alto nivel. Como se aprecia, se divide principalmente en
cuatro grandes partes: Por un lado está el **framework CakePHP** el cual
proporciona todos aquellos elementos más básicos de la arquitectura como
despachadores, enrutadores, convenciones, etc. Proporciona además una serie de
clases y funciones de uso frecuente que pueden utilizadas por el resto de
aplicaciones que se construyan sobre esta capa; Luego se encuentra el **framwork
de QuickAppsCMS**, que consisten básicamente en una serie de añadidos al
framework de CakePHP, define por ejemplo varias funciones utilitarias que pueden
ser usadas tanto por plugins del núcleo como plugins de terceros y que permiten
realizar tareas frecuentes dentro del ámbito del CMS en cuestión; Luego se
encuentra la capa de **plugins y themes**, éstos son en definitiva los elementos
que otorgan todas las funcionalidades y características ofrecidas por
QuickAppsCMS descritas en secciones anteriores, algunos ofrecen su propia API en
forma de Componentes, Behaviors o simplemente lanzando/atendiendo eventos dentro
de la aplicación; Finalmente se encuentra el **sistema de eventos**, que a un
nivel muy alto de abstracción puede ser visto como un bus de comunicación que
permite el intercambio información tanto horizontal como verticalmente entre
los distintos elementos de la arquitectura.

.. figure:: /_assets/img/Architecture.png
   :scale: 80%
   :align: center

    Arquitectura QuickAppsCMS.

Es importante señalar que alguno de los plugins del núcleo actúan de forma
pasiva, es decir, los usuarios no interaccionan con ellos de forma directa, sino
que proporcionan sus funcionalidades extendiendo directamente el framework de
base generalmente haciendo uso del sistema de eventos. Un claro ejemplo de esto
es el plugin WYSIWYG, que simplemente convierte cualquier campo de formulario de
tipo texto largo (textarea) en un editor enriquecido si, y solo si, este usa la
clase CSS ``ckeditor``, por ejemplo:

.. code:: html

   <textarea class="ckeditor">
      Lorem ipsum dolor sit amet, consectetur adipiscing elit.
   </texarea>

Aquellos plugins con los que un usuario puede interaccionar de forma directa
quedan explicados en el manual de usuario del ``QuickBook`` adjunto a esta
memoria.

.. [#enrutadores] Los enrutadores (Routers) proporcionan herramientas para
   mapear direcciones (URLs) en acciones de controladores.