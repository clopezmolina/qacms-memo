¿Qué es Composer?
#################

.. image:: /_assets/img/composer_logo.png
   :scale: 40%
   :align: center

Antes de hablar sobre Composer, conviene introducir brevemente el concepto de
*paquete*: Trozos reutilizables de código que pueden ser usados en cualquier
proyecto para añadir funcionalidades adicionales. El concepto es muy similar al
utilizado en Java y sus paquetes *.jar*, en donde no es necesario conocer
detalles sobre su contenido, sino que basta conocer lo que su API ofrece. En
ocasiones un paquete puede utilizar otro paquete para su correcto
funcionamiento, esta situación se conoce como **dependencia**.

La mayoría de sistemas de paquetes cuentan con mecanismos para controlar
dependencias de forma transparente, así por ejemplo se pueden construir
paquetes reutilizando otros ya existentes sin mayores complicaciones. La mayoría
de lenguajes de programación modernos cuentan con herramientas para trabajar con
paquetes, por ejemplo *Gems* utilizado por `Ruby <http://rubygems.org/>`__.

PHP cuenta con su propio sistema de paquetes, denominado PEAR, o PHP
Extension and Application Repository, un entorno de desarrollo y sistema de
distribución para componentes de código PHP. El proyecto PEAR fue fundado por
Stig S. Bakken en 1999 para promover la reutilización de código que realizan
tareas comunes. [about-pear]_

Si bien PEAR ha acompañado a PHP durante ya más de una década, sus múltiples
desventajas han provocado un serio decaimiento y abandono por parte de la
comunidad de desarrolladores PHP durante los últimos años. Las principales
desventajas que han llevado a esta situación son:

- Para publicar código en los repositorios oficiales de PEAR es necesario conseguir
  un número de votos positivos, de lo contrario la solicitud es automáticamente
  rechazada. Mecanismo originalmente destinado a garantizar cierto nivel de
  calidad en las publicaciones, pero que al final han producido un bajo nivel de
  contribuciones y han simplemente fomentado el elitismo entre desarrolladores.

- Actualmente gran parte del código publicado en los repositorios de PEAR está
  desactualizado y obsoleto. Muchos paquetes llevan años sin ser actualizados,
  lo que indica un abandono por parte de sus creadores. Esto no es mas que
  consecuencia del abandono masivo por parte de la comunidad como se comentó en
  lineas anteriores.

- PEAR obliga a instalar los paquetes y librerías de forma global en lugar de
  para cada proyecto, lo que produce grandes problemas en situaciones en la
  que por ejemplo, se tienen dos aplicaciones utilizando la misma librería pero
  en versiones diferentes.

En lugar de utilizar PEAR y paquetes para desarrollar, la comunidad comenzó
entonces a utilizar frameworks, pues estos cubrían gran parte de las necesidades
para la mayoría de proyectos. Con esto vuelve a surgir un problema ya comentado
en secciones anteriores, la *interoperabilidad*. Cada framework posee ciertas
peculiaridades y convenciones acerca de como realizar las cosas, por ello una
librería escrita en, por ejemplo, `CodeIgniter
<https://ellislab.com/codeigniter>`__ no pude ser utilizada en `Symfony
<http://symfony.com/>`__ al tener ciertas dependencias propias del framework
para el cual fue diseñada inicialmente. Así la solución de emplear un framework
como plataforma de desarrollo en lugar de paquetes independientes de código nos
lleva nuevamente al problema inicial: La reutilización de código.

Y es aquí donde `Composer <https://getcomposer.org/>`__ entra en escena.
Composer, es un **gestor de dependencias para PHP**. Composer no es un gestor
de paquetes. Bien es cierto que trabaja con paquetes o librerías, pero las
gestiona en  función de cada proyecto, instalándolos en un único directorio
dentro del proyecto. Por defecto nunca instalará nada de forma global. Por lo
tanto, es un gestor de dependencias. [about-composer]_

.. [about-pear] Wikipedia. PEAR, 2014
   http://es.wikipedia.org/wiki/PEAR

.. [about-composer] Composer. Dependency management, 2014
   https://getcomposer.org/doc/00-intro.md

.. [php-packages] Packages: The Way Forward for PHP, Phil Sturgeon, 2012
   http://philsturgeon.uk/blog/2012/03/packages-the-way-forward-for-php   