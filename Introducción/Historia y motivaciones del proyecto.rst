Historia y Motivaciones del Proyecto
####################################

El principal motivo que me ha llevado a crear *QuickAppsCMS* es originado
a partir de mi experiencia personal durante mis años como desarrollador PHP
[#php]_, años durante los cuales he tenido oportunidad de participar en
proyectos de diversa índole y envergadura.

Si bien es cierto que hoy en día existen cientos de aplicaciones similares a
*QuickAppsCMS* escritas en PHP, son en realidad escasas aquellas que ofrecen
soluciones completas y de calidad, y desde el punto de vista de un programador o
desarrollador, son prácticamente inexistentes aquellas que ofrezcan una API
consistente, bien construida y sobre todo guiada por estándares.

Algunos de los CMS más populares son también los más antiguos y primeros en
aparecer en la red. Quizás sea esto uno de los motivos por el cual (como se verá
en capítulos posteriores) poseen unas arquitecturas un tanto obsoletas,
engorrosas, difíciles de escalar y de mantener. Por ello fue que decidí comenzar
a construir un CMS cuya arquitectura fuera simple, eficiente y amigable para
desarrolladores. La forma de conseguir esto fue utilizar como base `CakePHP v2
<http://cakephp.org/>`__, uno de los frameworks MVC más populares y robustos que
existen actualmente para PHP, de esta forma la arquitectura de *QuickAppsCMS* se
convierte en cierta forma en una "extensión" del propio framework dando como
resultado un CMS con unas bases tecnológicas y cualidades únicas de alto valor
para un desarrollador.

Además de contar con unas bases tecnológicas sólidas debía también ofrecer un
conjunto de funcionalidades lo suficientemente grande para cubrir una amplia
gama de necesidad, por ello *QuickAppsCMS* hereda algunas de las mejores ideas
de los CMS más populares en la actualidad. A día de hoy, los dos CMS más
populares son indiscutiblemente `Drupal <https://www.drupal.org/>`__ y
`Wordpress <http://wordpress.org/>`__, el primero orientado a ser un gestor de
contenidos multipropósito y muy configurable, el segundo enfocado principalmente
en la creación de blogs y configurable mediante plugins.

Así, con Drupal y Wordpress como referencias, y con CakePHP v2 como base
tecnológica, surge en el año 2011 la primera versión de *QuickAppsCMS*. Aunque,
si bien aquella primera versión cumplía con todos los objetivos que en un inicio
me propuse alcanzar, lamentablemente por limitaciones del propio framework
CakePHP algunos aspectos de *QuickAppsCMS* no resultaron de mi completo agrado,
como por ejemplo acoplamientos en partes del sistema que impedían a otras sacar
provecho de algunas funcionalidades. O por ejemplo, el mapeo ORM de CakePHP v2,
que utiliza estructuras de tipo arrays para representar datos y consultas, que
hacen muy difícil o imposible realizar tareas como sub-consultas o formateo de
resultados. Limitaciones que al final repercuten en una complejidad añadida a la
arquitectura de *QuickAppsCMS*. La mayoría de estas limitaciones surgen del
hecho de que CakePHP está diseñado para ofrecer compatibilidad para versiones
antiguas de PHP, perdiendo así algunas de las ventajas de sus versiones más
modernas como por ejemplo la reutilización de código mediante `Traits
<http://php.net/manual/en/language.oop5.traits.php>`__ o el encapsulamiento
mediante `Namespaces
<http://php.net/manual/en/language.namespaces.rationale.php>`__.

Otra situación que repercute en mis motivaciones fue que, cuatro meses después
de haber liberado la primera versión de *QuickAppsCMS*, CakePHP libera una
revisión de su última versión disponible (versión sobre la que se construyó
*QuickAppsCMS*) añadiendo un nuevo sistema de eventos a dicho framework. Como se
verá más adelante una de las piezas clave en la arquitectura de *QuickAppsCMS*
es precisamente su sistema de eventos, y que en aquella primera versión de
*QuickAppsCMS* fue desarrollado desde cero y a medida, pues en ese entonces
CakePHP no ofrecía nada similar. Hubiera sido interesante aprovechar el sistema
de eventos ofrecido por CakePHP y lograr así una comunicación a todos los
niveles de la aplicación de forma consistente y sin necesidad de añadir nuevas
convenciones a la plataforma.

Actualmente, al momento de redactar esta memoria, CakePHP v3 está en activo
desarrollo, desarrollo del cual participio activamente implementando nuevas
funcionalidades del framework o importando funcionalidades existentes en
versiones anteriores. Así, la presente memoria se centra en **QuickAppsCMS v2**,
la segunda versión de este CMS. Esta vez utilizando CakePHP v3 como base
tecnológica; he reconstruido desde cero el CMS en su totalidad eliminando por
completo todos los aspectos negativos surgidos en la primera versión y
aprovechando al máximo las nuevas características introducidas por el framework
y por las últimas versiones de PHP. Para mayor información se invita al lector a
consultar en la  `web oficial del proyecto <http://quickappscms.org>`__ la hoja
de rutas seguida para el desarrollo de esta nueva versión, así mismo, las
políticas de versionado  que se encuentran en el repositorio oficial de `GitHub
<https://github.com/quickapps/docs/blob/1.x/eng/developers/versioning-
policy.md>`__.

.. [#php] Lenguaje de programación de uso general de código del lado del
   servidor originalmente diseñado para el desarrollo web de contenido dinámico.