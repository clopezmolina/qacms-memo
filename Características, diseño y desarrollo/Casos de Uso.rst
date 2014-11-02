Casos de Uso
############

En el diagrama de a continuación se observan los casos de usos y actores
que por defecto vienen en toda instalación inicial de QuickAppsCMS. Nuevos
casos de uso, actores o asociaciones puede ser definidos por personal con
privilegios suficientes.

Como podrá deducir el lector, cada uno de los casos de uso correspondientes al
BackEnd son ofrecidos por los plugins del núcleo del sistema, y cuyos detalles
han sido ampliamente descrito en secciones anteriores o en el QuickBook adjunto.

.. figure:: /_assets/img/use-cases/Global.png
   :align: center

   Caso de uso CMS general.

En esencia, cada uno de los casos de uso que se aprecian en el diagrama ofrecen
un CRUD [#crud]_ completo sobre generalmente una única estructura de información
concreta. Por ejemplo ejemplo, el caso de uso `Manage Users` permite crear
nuevos usuarios en el sistema, eliminar uno ya existente, buscar un usuario en
particular o modificar su información personal. Por esta razón y a fin de evitar
la redundancia, se ofrece a continuación únicamente el detalle de uno de ellos,
quizás el más interesante e importante dentro del sistema:

.. figure:: /_assets/img/use-cases/Contents-System.png
   :align: center

   Caso de uso gestión de contenidos.


Caso de Uso: Create Contents
============================

Escenario típico
----------------

1. El usuario escoge qué tipo de contenido va a crear haciendo uso de una GUI,
   estos tipos de contenidos han sido previamente definidos en el caso de uso
   `Define Content Types`.	

3. El sistema genera de forma dinámica una interfaz apropiada al tipo de
   contenido escogido.

2. El usuario ingresa la información que definen al contenido, título, idioma,
   etc.

3. El usuario envía los datos y el sistema crea el nuevo contenido.

4. Termina con éxito.


Escenario alternativo
---------------------

1a. No existen tipos de contenidos definidos con anterioridad.

  1a1. Abortar operación.

2a. La información introducida por el usuario no cumple con las reglas de validación definidas por el tipo de contenido.

  2a1. Recargar interfaz con los datos introducidos por el usuario.

  2a2. Mostrar un mensaje detallando los errores.

  2a3. Abortar la operación de guardado.


Caso de Uso: Translate Contents
===============================

Escenario típico
----------------

1. El usuario busca un "contenido padre" para un idioma en concreto.

2. El sistema pregunta al usuario a qué idioma desea traducir el contenido.

3. El usuario escoge uno de los idiomas a los que el contenido no ha sido aún
   traducido.

4. El sistema inicia el caso de uso `Create Content`.

5. Termina con éxito.


Escenario alternativo
---------------------

2a. El contenido padre ya ha sido traducido a todos los idiomas disponibles activos en el sistema.

   2a1. Abortar operación.


**NOTA**: Un `contenido padre` es aquél contenido que no es traducción de ningún
otro y que además a sido marcado para ser visualizado en un idioma en
particular.


Caso de Uso: Modify Contents
============================

Escenario típico
----------------

1. El usuario escoge un contenido existente para modificar.

2. El sistema genera de forma dinámica una interfaz apropiada al tipo de
   contenido que pertenece el contenido escogido.

3. El sistema completa la información de la interfaz de forma automática con
   los datos actuales del contenido.

4. El usuario modifica esta información.

5. El usuario envía los datos y el sistema actualiza el nuevo contenido.

6. El sistema realiza una copia de seguridad de la información anterior a los
   cambios.

7. Termina con éxito.


Escenario alternativo
---------------------

2a. La definición del tipo de contenido al que pertenece el contenido escogido ya no existe (ha sido eliminado).

   2a1. Mostrar mensaje de error explicando la situación.

   2a2. Abortar la operación.


Caso de Uso: Delete Contents
============================

Escenario típico
----------------

1. El usuario busca y escoge un contenido existente para eliminar.

2. El sistema elimina el contenido.

3. Termina con éxito.


Escenario alternativo
---------------------

2a. El contenido a eliminar posee traducciones en otros idiomas:

   2a1. Eliminar traducciones.

2b. El contenido a eliminar posee históricos (copias de seguridad) generados por por el caso de uso `Modify Content`:

   2b1. Eliminar copias de seguridad.


.. [#crud] Acrónimo de Crear, Obtener, Actualizar y Borrar (del original en
   inglés: Create, Read, Update and Delete)
