¿Qué es PSR?
############

Desde sus orígenes, PHP jamás ha contado con una forma unificada de escribir
código. Algunas personas prefieren crear y seguir sus propias reglas de
codificación y de estilo. Otros bien prefieren adoptar alguna ya existente y
bien  documentada como puede ser `PEAR
<http://pear.php.net/manual/en/standards.php>`__ o `Zend Framework
<http://framework.zend.com/manual/1.12/en/coding-standard.html>`__.

PSR, son las siglas del inglés: **PHP Standards Recommendation**, al momento de
redactar esta memoria existen actualmente cuatro de estas "recomendaciones",
PSR-0 a PSR-3. A continuación se explicarán sus orígenes y en que consiste cada
una de ellas.


Framework Interoperability Group (FIG)
======================================

Durante la `conferencia PHP Tek <http://tek.phparch.com/>`__ del año 2009,
personas representantes de diversos proyectos comenzaron a debatir sobre cómo
trabajar entre proyectos, fue así como nació el FIG. La idea detrás de este
grupo es la de permitir a representares de proyectos conversar y debatir, con el
objetivo de encontrar formas de trabajar conjuntamente (**interoperabilidad**).

Las recomendaciones propuestas por FIG son gratuitas y pueden ser adoptadas por
quien así lo desee, es decir nadie esta obligado a seguir las "normas"
establecidas por FIG. Es más, ni siquiera los miembros del grupo están obligados
a seguir dichas reglas.


PSR-0, Auto-cargadores
======================

Fue el primer "estándar" introducido por FIG, y describe los requerimientos que
los proyectos han de cumplir a fin de permitir la interoperabilidad mediante el
empleo de autocargadores.

¿ Autocargadores ?
------------------

Normalmente, en la mayoría de lenguajes orientados a objetos antes de crear una
instancia de una clase esta debe ser previamente importada. En PHP el importar
una clase se realiza de forma similar a Java, utilizando las palabras
reservadas **require** o **include**. Por ejemplo:

.. code:: php

    require "Rectangle.php";
    $rect = new Rectangle(42, 25);

Al trabajar con orientación a objetos en PHP por lo general un fichero define
una única clase, por ello resulta a veces molesto tener una larga lista de
*includes* al comienzo de cada script (uno por cada clase).

La llegada de PHP 5 introdujo la función mágica `__autoload
<http://php.net/manual/es/language.oop5.autoload.php>`__ que se lanza
automáticamente al referenciar una clase que no ha sido previamente importada.
Esto permite importar en tiempo de ejecución el fichero que contiene la
definición de la clase antes que la ejecución del script falle.

PSR-0 básicamente dicta como deben organizarse físicamente los ficheros que
contienen clases para ser detectados e importados automáticamente por un
*autoloader*.


PSR-1, Codificación estándar básica
===================================

Este fue el segundo "estándar" en ser definido por FIG, y como se puede deducir
a partir de su nombre, intenta definir una serie de reglas generales a la hora
de escribir código PHP que pueden ser fácilmente implementadas
independientemente de la plataforma. Reglas como por ejemplo, escribir todos los
nombres de constantes en MAYUSCULSAS, o utilizar *camelCase* para definir
funciones y métodos, etc.


PSR-2, Normas de estilo
=======================

El tercer "estándar" definido por FIG. Extiende las normas definidas por PSR-1 y
añade algunas reglas adicionales para código escrito en PHP, reglas como por
ejemplo, utilizar 4 caracteres de espacios en lugar de tabulaciones, o que las
cada línea no debe exceder los 80 caracteres de longitud, etc.


PSR-3, Interfaz de Logger
=========================

En términos generales, PSR-3 define una interfaz de Logger que debería ser
implementada por todos aquellos softwares de logging. La idea detrás de PSR-3 es
que si se decide en algún momento cambiar de un logger a otro, no se debería
realizar ninguna tarea adicional y todo debería seguir funcionando estrictamente
igual,  los mensajes de log deberían ser escritos con los mismos niveles de
advertencias, etc.


QuickAppsCMS y PSR
==================

QuickAppsCMS ha sido desarrollado siguiendo todos los estándares descritos
anteriormente. Se ha de recordar al lector que, todas estas definiciones no son
estándares propiamente tales, sino que cada desarrollador posee la libertad
seguirlas o no. Así por ejemplo, QuickAppsCMS si bien sigue unas normas de
codificación y estilos muy estrictas, estas son en realidad variantes de PSR-1 y
PSR-2, específicamente se tratan de las normas de codificación y estilo
definidas por el proyecto CakePHP y que pueden ser `consultadas
<http://book.cakephp.org/3.0/en/contributing/cakephp-coding-conventions.html>`__
en la web oficial del mismo.
