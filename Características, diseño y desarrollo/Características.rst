Características
###############

Antes de continuar es conveniente aclarar algunos conceptos y palabras clave que
se utilizarán tanto en esta sección como en posteriores. La mayoría de éstos son
elementos definidos por el framework sobre el cual QuickAppsCMS fue
construido, por ello, y si el lector así lo desea, puede consultar detalles
sobre los mismos en la documentación oficial del proyecto `CakePHP
<http://book.cakephp.org/3.0/en/index.html>`__ disponible en versión online.

- Behaviors: Los Behaviors o *Comportamientos* son una manera de organizar y 
  permitir la reutilización de lógica horizontal en la capa de Modelo del
  paradigma MVC. Conceptualmente son similares de los Traits de PHP.
  [about-behaviors]_

- Components: Los Components o *Componentes* son paquetes de lógica compartida
  entre controladores. La utilización de componentes mantiene el código de los
  controladores más limpia y permite la reutilización entre los mismos.
  [about-components]_

- Helper: Los Helpers o *Ayudantes* son el equivalente a los componentes para la
  capa de presentación del paradigma MVC. Contienen lógica de presentación que
  puede ser compartida entre múltiples vistas o diseños. [about-helpers]_

- Trait: Desde PHP 5.4.0, PHP implementa una metodología de reutilización de
  código llamada Traits. Los traits (rasgos) son un mecanismo de reutilización
  de código en lenguajes de herencia simple, como PHP. El objetivo de un trait
  es el de reducir las limitaciones propias de la herencia simple permitiendo
  que los desarrolladores reutilicen a voluntad conjuntos de métodos sobre
  varias clases independientes y pertenecientes a clases jerárquicas distintas.
  [about-traits]_

- Router: Routing o *Enrutamiento* es una funcionalidad que permite realizar
  mapeos entre URLs y acciones de controladores. Esta funcionalidad fue
  incorporada a CakePHP con el fin de poder crear URLs amigables de forma simple
  y flexible. [about-routes]_

- Entity: Entities o *Entidades* son estructuras pertenecientes al mapeo
  relacional de CakePHP. Mientras que las `Tablas
  <http://book.cakephp.org/3.0/en/orm/table-objects.html>`__ representan y
  proveen acceso a colecciones de objetos, las Entidades representan filas
  independientes u objetos de dominio de una aplicación. [about-entities]_


.. toctree::
   :maxdepth: 1

   Características/Hooks API
   Características/Hooktags
   Características/Soporte para múltiples SGBD
   Características/Tipos de contenidos
   Características/Versionado de contenidos
   Características/Multilenguaje
   Características/Comentarios
   Características/Control de usuarios, roles y permisos
   Características/Themes y Plugins
   Características/Motor de búsqueda integrado
   Características/Editor enriquecido
   Características/Gestor de ficheros
   Características/SEO-friendly
   Características/Clasificación de contenidos
   Características/Bloques y Regiones
   Características/Menús de navegación



.. [about-behaviors] CookBook 3.0. Behaviors, 2014.
   http://book.cakephp.org/3.0/en/orm/behaviors.html

.. [about-components] CookBook 3.0. Components, 2014.
   http://book.cakephp.org/3.0/en/controllers/components.html

.. [about-helpers] CookBook 3.0. Helpers, 2014
   http://book.cakephp.org/3.0/en/views/helpers.html

.. [about-traits] Manual de PHP. Traits, 2014.
   http://php.net/manual/es/language.oop5.traits.php

.. [about-routes] CookBook. Routes, 2014.
   http://book.cakephp.org/3.0/en/development/routing.html

.. [about-entities] BookBook. Entities, 2014.
   http://book.cakephp.org/3.0/en/orm/entities.html