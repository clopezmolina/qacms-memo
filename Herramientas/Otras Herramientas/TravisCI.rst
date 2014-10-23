Travis CI
#########

Travis CI es un herramienta de integración continua [#ci]_ alojada y gratuita para
todos los proyectos de código libre alojados en GitHub. Travis CI se configura
de manera muy simple añadiendo un fichero con extensión *.yaml* a la raíz de los
repositorios GIT.

Travis CI detecta auténticamente nuevos *commits* realizados sobre los
repositorios de GitHub, y cada vez que esto ocurre, intentara compilar el
proyecto y ejecutar todas las pruebas registradas. Una vez que todo el proceso
ha concluido, opcionalmente se puede configurar Travis CI para que envíe
notificaciones e-mail a los correos personales de los miembros del proyecto.

.. figure:: /_assets/img/travis-ci_buid.png
   :align: center

   Pruebas de integración de QuickAppsCMS con Travis CI.

Soporta integraciones para una gran cantidad de lenguajes de programación, como
C, C++ Java, Perl, Ruby y por supuesto PHP. Esta herramienta es utilizada por
inportantes proyectos de código libre, como por ejemplo Ruby, Node.js o Plone
entre otros.

Una de las principales características de Travis CI es que permite ejecutar
integraciones sobre diversos entornos a la vez. Así por ejemplo, tras realizar
un *commit*, es posible realizar compilaciones y ejecutar pruebas para múltiples
versiones de PHP.

QuickAppsCMS hace uso de esta herramienta para garantizar un correcto
funcionamiento de la aplicación sobre distintas versiones de PHP y distintos
SGBD. Además, es utilizado para realizar comprobaciones de sintaxis y normas de
estilo (PSR-1 y PSR-2).


.. [#ci] Modelo informático propuesto inicialmente por Martin Fowler que consiste
   en hacer integraciones automáticas de un proyecto lo más a menudo posible
   para así poder detectar fallos cuanto antes.