Wordpress
#########

.. image:: /_assets/img/wordpress_logo.jpg
   :scale: 50%
   :align: center

Wordpress posee unas interfaces muy amigables por lo que resulta fácil para
nuevos usuarios adaptarse al esquema de trabajo propuesto por la aplicación.
Cuenta además con una gran cantidad de plugins y themes gratuitos de gran
calidad. El inconveniente es que Wordpress está demasiado enfocado en gestionar
plataformas de tipo Blog y realizar sitios webs que se salgan de este marco
resulta una tarea de una complejidad no despreciable.

.. figure:: /_assets/img/uso_cms_pie.png
   :scale: 80%
   :align: center

   Porcentajes de uso global. Wordpress es utilizado por un 23% de las webs a
   nivel mundial. Datos proporcionados por [w3techs-cms]_.



Aspectos positivos
==================

- Interfaces: Sus interfaces son muy amigables, fáciles de utilizar y de una
  estética muy cuidada. Ofrece "tips" o ayuda en forma de "tooltips" en todo
  momento lo que facilita enormemente la utilización y configuración de la
  herramienta por parte de usuarios con poca experiencia.

- Shortcodes API: Los shortcodes de WordPress son pequeños códigos que puedes
  añadir en el editor de WordPress. Se usan para añadir funciones al contenido de
  tus entradas y páginas sin tener que escribir un script cada vez que necesites
  hacer esa tarea. [wordpress-shortcodes]_

- Plugins y Themes: Posee una enorme cantidad de aspectos visuales y plugins
  gratuitos. Incorpora además un buscador integrado que permite instalar nuevas
  funcionalidades o cambiar el aspecto visual del sitio web con solo un par de
  clics.

- Blogging: Como plataforma de blogging, Wordpress sea quizás la mejor
  herramienta disponible a día de hoy, incorpora múltiples utilidades enfocadas
  a la publicación de entradas tipo blogs, como por ejemplo su sistema de
  categorización y etiquetado de contenidos.

- Fácil de instalar y actualizar: Todo el proceso de instalación, en media, no
  lleva más de cinco minutos en completarse. Y como es habitual en Wordpress, la
  interfaz de instalación es muy intuitiva y fácil de utilizar.

- Editor WYSIWYG [#wysiwyg]_: Incorpora por defecto un editor enriquecido con
  guardado automático y posibilidad de publicar contenidos vía e-mail.  

- Comunicación entre blogs: Trackback [#trackback]_, Pingback [#pingback]_, etc.


Aspectos negativos
==================

- Rendimiento: Wordpress funciona de forma fluida a la hora de gestionar sitios
  web pequeños, pero para sitios web que reciban una cantidad importante de
  visitantes por día puede que sea necesario migrar la aplicación a un servidor
  de mayores capacidades.

- Seguridad: En comparación con otras aplicaciones similares, la seguridad en
  Wordpress no es tan elevada como cabría de esperarse. Quizás sea por el nivel
  de popularidad del cual goza, pero los sitios webs creados con Wordpress son
  de los que más ataques reciben a diario en Internet.

- Bases de datos: Unicamente ofrece soporte para bases de datos MySQL. Tampoco
  cuenta con una capa de abstracción de datos, lo ha hace imposible implementar
  correctamente mecanismos de acceso para otros SGBD. 

- PSR: Wordpress no implementa ninguno de los PSR propuestos por FIG. Es mas,
  algunas de ellas van directamente en contra de la filosofía de Wordpress. Por
  ejemplo *PSR-1* y *PSR-2*; Wordpress sigue unas normas de estilo y codificación,
  que en mi opinión personal, dejan bastante que desear, como por ejemplo la
  utilización de `Yoda conditions <http://en.wikipedia.org/wiki/Yoda_conditions>`__
  o el empleo casi indiscriminado de caracteres de espacio. Lamentablemente
  los autores del proyecto se muestran
  `completamente cerrados <https://core.trac.wordpress.org/ticket/23357#comment:3>`__
  a la posibilidad de adoptar estos estándares en un futuro.

- Difícil de escalar: La API sobre el cual está construido Wordpress es
  difícil de modificar y escalar, así que no es la herramienta idónea para
  personas que buscan un alto grado de personalización. Su arquitectura está
  altamente acoplada, quizás debido al empleo del paradigma basada en
  procedimientos (o *programación funcional*), y que en definitiva dan como 
  resultado un código de muy mala calidad y difícil de mantener.

- Themes y plugins: Para crear plugins y themes se requiere un alto grado de
  conocimiento del lenguaje PHP, además de las convenciones establecidas por la
  propia API de Wordpress, API que como se comentó líneas arriba, no sigue
  ningún tipo de estándar.

- Multilenguaje: No permite crear contenidos en múltiples idiomas, aunque
  existen algunos plugins que otorgan dicha funcionalidad.

- Actualizaciones: Un problema bien conocido en Wordpress es su sistema de
  actualizaciones; cada vez que una nueva versión es publicada se ofrece la
  posibilidad de actualizar la plataforma con un simple clic desde el *BackEnd*,
  acción que en muchos casos puede detener el correcto funcionamiento del sitio
  web, teniendo que recurrir a diversas peripecias para restaurar los daños.


.. figure:: /_assets/img/wordpress_architecture.jpg
   :align: center

   Arquitectura de Wordpress.



Conclusiones
============

Wordpress es ideal para personas noveles o con conocimientos técnicos limitados
y que buscan de una forma rápida montar un pequeño blog o web sencilla. Es en la
actualidad el CMS más popular y más utilizado a nivel mundial; alrededor del 20% de
las webs en Internet utilizan esta herramienta. Cuenta además con una enorme
comunidad a sus espaldas por lo que resulta fácil encontrar ayuda en cualquier
momento.

.. [w3techs-cms] W3Techs. Usage of content management systems for websites, 2014
   http://w3techs.com/technologies/overview/content_management/all

.. [wordpress-shortcodes] Ayuda Wordpress. Qué son los shortcodes y cómo crearlos, 2014
   http://ayudawp.com/que-son-los-shortcodes-y-como-crearlos/

.. [#wysiwyg] WYSIWYG es el acrónimo de What You See Is What You Get (en español,
   "lo que ves es lo que obtienes"). Se aplica a los procesadores de texto y
   otros editores de texto con formato (como los editores de HTML) que permiten
   escribir un documento viendo directamente el resultado final, frecuentemente
   el resultado impreso.

.. [#trackback] Se trata de un enlace inverso que permite conocer qué enlaces
   apuntan hacia un determinado artículo; de ese modo, avisa a otro weblog que
   se está citando uno de sus artículos.

.. [#pingback] Método para que los autores de la web soliciten una notificación
   cuando alguien enlaza uno de sus documentos. El envío y la recepción de esta
   información es transparente al usuario. Esto permite a autores no perder de
   vista quién los está enlazando.