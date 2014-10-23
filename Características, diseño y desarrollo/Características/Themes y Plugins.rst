Themes y Plugins
================

Plugins
-------

QuickAppsCMS ha ido diseñado para ser completamente modular. El núcleo de
QuickAppsCMS podría considerarse como una caja de piezas Lego™: una plataforma y
algunos cuantos ladrillos (plugins) para comenzar. Estos ladrillos permiten
realizar diversas cosas, pero usualmente algunos ladrillos adicionales pueden
ser necesarios.

Estos plugins adicionales son denominados plugins de terceros. Son paquetes de
código capaces de extender o mejorar el núcleo QuickAppsCMS para añadir (o
modificar) sus características y funcionalidades.

Similar a Composer, QuickAppsCMS proporciona una API para manejar dependencias,
aunque mucho más limitado en cuanto a funcionalidades. Este sistema está
enfocado principalmente en resolver dependencias entre plugins y así asegurar
que por ejemplo, un plugin no pueda ser desinstalado si este es utilizado por un
segundo plugin. Esta API proporciona diversas utilidades para manejar todo el
ciclo de vida de un plugin, instalación, actualizaciones, etc de una manera
transparente al desarrollador. Se invita al lector a consultar la documentación
adicional para conocer detalles sobre el mismo.


Themes
------

Los themes o "temas visuales" son un conjunto unificado de elementos de diseño y
esquemas de color que pueden ser aplicados sobre cualquier página web para
otorgarles una apariencia profesional. Utilizar un theme es una forma rápida y
simple de asegurar que todas las páginas web son visualmente consistentes y
atractivas. En QuickAppCMS todos los themes son más que una mera colección de
hojas de estilo, imágenes u otros elementos estrictamente estéticos. Estos son
en realidad tratados internamente como *plugins*, gracias a lo cual es posible
añadir cierta lógica a todo el proceso de renderizado de cada pagina web. Por
ejemplo, cada theme puede definir un conjunto de parámetros que pueden ser
configurados por los usuarios y enfocados en manipular aspectos del diseño de
una manera simple y transparente, aspectos como por ejemplo color de fondo,
tamaño de fuente etc.

A diferencia de Drupal, como se vio en capítulos anteriores, QuickAppsCMS trata
de forma independiente los themes de *FrontEnd* y *BackEnd*. Gracias a esto se
logran principalmente dos cosas:

- Es posible tener aspectos visuales completamente distintos para al área de
  administración y la parte pública de cada sitio web.
- El desarrollar nuevos aspectos visuales es extremadamente simple.

Por otro lado, todo el código HTML generado de forma automática por el núcleo de
QuickAppsCMS sigue las normas establecidas por *Twitter Bootstrap*. Por ejemplo,
tablas, botones o formularios, todos utilizan las clases CSS pre-establecidas
por el framework Twitter Bootstrap para establecer su aspecto visual.

De igual forma, y aunque no estrictamente ligado al ámbito del diseño, todo el
código JavaScript automáticamente generado por el núcleo de QuickAppsCMS fue
diseñado para ser compatible con jQuery. Por ejemplo, efectos "drag & drop",
ventanas emergentes, tooltips, todas ellos asumen que el theme hace uso de la
librería jQuery.
