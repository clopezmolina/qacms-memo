PHPDocumentor
#############

phpDocumentor es una herramienta escrita en PHP diseñada para generar
documentación completa directamente desde código PHP o desde documentación
externa. La verdad es que, el código PHP es tan legible que puede funcionar
prácticamente como su propia documentación. phpDocumentor hace uso de este hecho
analizando todas las estructuras lógicas que pueden ser encontradas en PHP, como
ficheros, clases, funciones, constantes, variables globales, y variables/métodos
de clases; organizándolos en formato de manual técnico.

phpDocumentor genera estos manuales leyendo documentación desde unos comentarios
PHP especiales denominados *DocBlocks*. Los DocBlocks son el lugar donde los
desarrolladores deben documentar cualquier información relevante que pueda ser
utilizada por terceros (o por sí mismos) y así facilitar la interoperabilidad
entre paquetes de software. [what-is-phpdocumentor]_

phpDocumentor se puede utilizar desde línea de comandos o mediante una interfaz
web. Tiene soporte para la vinculación entre la documentación, la incorporación
de documentos a nivel de usuario como tutoriales, y la creación de código fuente
resaltado con referencias cruzadas a la documentación en general de PHP.
phpDocumentor es capaz de analizar toda la sintaxis de PHP y soporta tanto PHP4
como PHP5. Se trata de un proyecto de código abierto y se distribuye bajo la
licencia LGPL. [wiki-phpdocumentor]_

.. figure:: /_assets/img/api_demo.png
   :align: center

   API de QuickAppsCMS generada utilizando PHPDcumentor.

Durante el proceso de desarrollo de QuickAppsCMS v2, la documentación ha ocupado
siempre los primeros lugares en cuanto a prioridades. Procurando siempre
documentar absolutamente todo y proporcionar ejemplos de utilidad para un
desarrollador. La API de QuickAppsCMS (en todas sus versiones) ha sido
generada utilizando esta herramienta y puede ser consultada en los anexos de
esta memoria o en su versión online disponible desde la web oficial del
proyecto.

.. [what-is-phpdocumentor] phpDocumentor Quickstart. What is phpDocumentor? What can it do?, 2014.
   http://manual.phpdoc.org/HTMLSmartyConverter/HandS/phpDocumentor/tutorial_phpDocumentor.quickstart.pkg.html

.. [wiki-phpdocumentor] Wikipedia. PhpDocumentor, 2014.
   http://es.wikipedia.org/wiki/PhpDocumentor   