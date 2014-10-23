Motor de búsqueda integrado
===========================

QuickAppsCMS proporciona una poderosa API para la indexación y localización de
contenidos. Gracias a esto, es posible ofrecer a los visitantes de un sitio web
un motor de búsqueda integrado para la búsqueda de contenidos. Esta API es
proporcionada en forma de *Behavior* y cualquier tabla puede utilizarla, al
hacerlo todas sus entidades son automáticamente indexadas al ser creadas o
modificadas. Este proceso busca y extrae palabras para generar un índice de
palabras, gracias a este índice una una entidad puede ser localizada utilizando
utilizando un formulario de búsqueda.

Por defecto esta API es utilizada para indexar todos los contenidos y todos
usuarios. Así por ejemplo es posible buscar publicaciones cuyo título contengan
alguna palabra en particular, o en el caso de los usuarios, es posible localizar
usuarios cuyos nombres coincidan con algún patrón de búsqueda.

El proceso de búsqueda propiamente tal se realiza haciendo uso de la misma API,
ésta permite localizar entidades cuyo indice de palabras coincida con alguna
sentencia de búsqueda. Las sentencias de búsqueda son cadenas de texto que
siguen un lenguaje de consulta propio, aunque muy similar a utilizado por
motores de búsqueda como Google, éstas tienen un aspecto similar a:

    "esta frase si" palabra_suelta -"pero no esta frase" created:2014..2015

Se trata de un sistema con muchas posibilidades, como se puede apreciar en el
ejemplo anterior es posible incluso crear comandos u operadores de filtrado
(created). QuickAppsCMS incorpora de serie un conjunto de estos comandos
especiales (y cuyos detalles se encuentran en los anexos de este documento),
aunque la API es lo suficientemente flexible como para permitir que otros
plugins definan sus propios comandos o modifiquen el comportamiento de los ya
existentes. Para mayor detalles, se invita al lector a consultar los anexos a
este documento.
