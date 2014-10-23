SEO-friendly
============

En QuickAppsCMS todas las URLs o contenido automáticamente generado han sido
cuidadosamente diseñados y optimizados para ofrecer compatibilidad con motores
de búsqueda y sus arañas [#spiders]_, es decir, QuickAppsCMS ofrece de serie
optimizaciones SEO [#SEO]_ básicas. Por ejemplo, todos los contenidos publicados
poseen un slug [#slug]_ que es posteriormente utilizado en cada URL que apunte
hacia el contenido. QuickAppsCMS ofrece también cierto nivel de control sobre
aspectos como meta-descripciones o sobre los propios slugs, pues en la mayoría
de gestores de contenidos estas propiedades son automáticamente generadas a
partir del contenido publicado, situación que limita enormemente el grado de
optimización SEO que un usuario puede realizar, teniendo que recurrir en muchos
casos a la instalación de plugins adicionales a fin de conseguir un mayor
control sobre estos elementos. En QuickAppsCMS todas las URLs hacia los
contenidos publicados siguen el siguiente patrón:

   http://example.com/slude-del-tipo-de-contenido/slug-del-contenido.html

Así por ejemplo a un artículo titulado "Los delfines abandonan la tierra" le
será asignado el siguiente enlace:

  http://example.com/article/los-delfines-abandonan-la-tierra.html

Todo esto es posible gracias el poderoso sistema de enrutamiento (Router)
proporcionado por CakePHP. Otros plugins pueden hacer uso de este sistema y
crear sus propias reglas de enrutamiento, como por ejemplo URLs personalizadas a
ciertos contenidos.

.. [#spiders] Es un software que recorre Internet siguiendo cada enlace que
   encuentra, y cogiendo el contenido de cada sitio web que visita para añadirlo
   a las bases de datos de su motor de búsqueda.

.. [#SEO] SEO (Search Engine Optimization), es el proceso de mejorar la
   visibilidad de un sitio web en los resultados orgánicos de los diferentes
   buscadores.

.. [#slug] En la edición de periódicos, un slug es un nombre corto dada a un
   artículo que está en producción.