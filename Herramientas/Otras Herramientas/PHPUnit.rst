PHPUnit
#######

Las pruebas son un aspecto fundamental en todo proceso de desarrollo sea cual
sea el lenguaje de programación. Pues es la única forma de asegurar que nuestros
programas funcionan correctamente. Las pruebas manuales pueden funcionar, pero
solo pueden ser realizadas de forma irregular y por lo general son muy
limitadas. Por ello, la forma de realizar pruebas en profundidad y de forma
regular es utilizar herramientas automatizadas para esta tarea. En PHP, estas
pruebas son generadas utilizando un framework especializado, que permite
realizar pruebas sobre trozos aislados de código como funciones o métodos de una
clase en particular. Las pruebas unitarias en PHP se han convertido en
prácticamente un estándar al ser utilizado por grandes aplicaciones como Zend
Framework, Symfony o CakePHP.

.. figure:: /_assets/img/travis-ci_buid_details.png
   :align: center

   Pruebas unitarias de QuickAppsCMS.

PHPUnit es uno de estos frameworks comentados en lineas anteriores, provee
diversas librerías para crear pruebas unitarias y *test suites* para automatizar
las pruebas de funciones y clases escritas en PHP. PHpUnit se inspira en JUnit,
el cual fue creado por *Kent Beck* y *Erich Gamma* como una herramienta para
eXtreme Programming (XP). Una de las reglas de XP es la ir probando trozos
pequeños del software con cierta regularidad y lo antes posible. Mientras que
las pruebas unitarias son una regla fundamental de XP, no es necesario adoptar
XP para poder utilizar PHPUnit. PHPUnit es una genial herramienta para realizar
pruebas sobre clases o sobre un conjunto de funciones, y de este modo agilizar
los ciclos de desarrollo y evitando realizar sesiones de depuración
interminables. [about-phpunit]_

.. [about-phpunit] PHPUnit Documentation. A short introduction to the test framework, 2014.
   http://pear.php.net/manual/en/package.php.phpunit.intro.php
