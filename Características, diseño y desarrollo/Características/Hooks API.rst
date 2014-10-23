Hooks API
=========

Junto con la flexibilidad de una arquitectura basada en plugins surge siempre la
necesidad de un mecanismo basado en eventos para "unir" a todos estos plugins.
Este mecanismo reduce enormemente las dependencias entre plugins al no existir
las invocaciones directas de métodos entre plugins.

Cualquier plugin puede hacer uso de esta API y registrarse a sí mismo en el
denominado *EventManager* para ser notificado cuando un nuevo evento es
accionado. De esta forma, por ejemplo, un plugin A puede accionar un método de
otro plugin B (y/o C, D, etc) sin tener conocimiento alguno sobre la existencia
del plugin B.

Los *hooks* son funciones o métodos escritos en PHP que son automáticamente
invocados por el núcleo de QuickAppsCMS o alguno de sus plugins con el fin de
modificar el comportamiento del sistema. Los *hooks* son más que meras
"notificaciones" sobre la ocurrencia de algún evento, sino que son capaces de
transportar cualquier tipo de información relevante para el contexto en el que
éstos son invocados.

.. figure:: /_assets/img/EDA.png
   :scale: 100%
   :align: center

   Ejemplo de funcionamiento. Durante el proceso de persistencia o recuperación
   de entidades (Usuarios) diversos eventos son accionados y atendidos por
   distintos plugins.

