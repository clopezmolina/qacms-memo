Frameworks PHP
##############

PHP es una plataforma de desarrollo muy sólida y con grandes posibilidades.
Proporciona herramientas para interactuar con diversos motores de bases de
datos, con servicios de email, con información en diversos lenguajes de marcado
y muchísimo más. Gracias a la facilidad y flexibilidad para desarrollar
utilizando PHP, es realmente simple comenzar a codificar un proyecto escribiendo
directamente en PHP, aunque hacer esto puede resultar efectivo y sencillo, lo
cierto es que se debe ser muy cuidadoso para no terminar creando aplicación
engorrosas y rodeadas de `codigo spaghetti
<http://es.wikipedia.org/wiki/C%C3%B3digo_espagueti>`__: Múltiples lineas de
código con un alto grado de interacción entre ellas y mezcladas con código HTML
y/o JavaScript.

Al codificar utilizando PHP directamente, muchas cosas pueden salir mal o no
como inicialmente se esperaban. Un efecto común en este tipo de desarrollos es
la redundancia: múltiples ficheros que realizan tareas muy similares o bien
directamente las mismas, problema bien conocido en informática y que afecta,
entre otras cosas, labores mantenimiento al tener que realizar un mismo cambio
en múltiples partes de la aplicación a la vez. Cambios que de no hacerse con el
debido cuidado puede producir múltiples fallos, por ello se ha de asegurar
cubrir de forma intensiva con "tests" cada porción de código, tarea que puede
resultar compleja, o imposible en algunos casos al tener multitud de código
entrelazado.

Como se mencionó en el apartado anterior, en los inicios de PHP la falta de
estándares provocaba que cada desarrollador codificara sus proyectos utilizando
sus propias normas o como mejor que pareciese. En este proceso, algunas personas
se dieron cuenta de que esto resultaba poco efectivo al producir proyectos
difíciles de mantener y de escalar. Así fue como algunos comenzaron a crear sus
propios "frameworks" para usar en sus proyectos personales. Aunque, distaban
enormemente de ser algo formalizado y bien organizado como los frameworks que se
conocen hoy en día, pues básicamente consistían en una serie de reglas para
organizar ficheros y tareas de uso frecuentes.

Con el surgimiento de PHP 5 grandes avances en la orientación a objetos  fueron
introducidos, fue recién entonces cuando se podría afirmar que el  desarrollo
formal de frameworks comenzó. Los frameworks, surgen para solventar algunas de
las complicaciones mencionadas en párrafos anteriores. Y en esencia se basan en
el refrán "divide y vencerás", proporcionando una forma de organizar y
distribuir el código de nuestras aplicaciones escritas en PHP. Al gozar de una
alta granularidad es fácil testear cada una de estas piezas de código, y en
consecuencia, es fácil reutilizar código en otras partes del proyecto (o incluso
en otros proyectos).

Organizar nuestro código no tiene por qué necesariamente ser beneficioso, por
ello es necesario discernir correctamente cuándo utilizar un framework o no. Por
ejemplo, para aplicaciones pequeñas seguramente no hay necesidad de fragmentar
el código en múltiples piezas y la utilización de un framework resultaría
unicamente en una perdida evitable de rendimiento. Algunas ventajas de utilizar
un framework pueden ser las siguientes:

1. Organización de código y ficheros: Cada framework utiliza su propia estructura
   de directorios, ficheros y convenciones que han de ser seguidas a la hora de
   codificar nuestras aplicaciones.

2. Utilidades y librerías: Aunque PHP de por sí ofrece un amplio abanico de
   librerías y herramientas, los frameworks suelen ofrecer un conjunto de librerías
   para agilizar tareas como:

   a) Generación de código HTML
   b) Validación de información
   c) Abstracciones para diversos motores de bases de datos
   d) Manejo de Sesiones y Cookies
   e) Envío de e-mails

3. Paradigma MVC: La mayoría de frameworks PHP siguen este paradigma, ayuda  a
   separar la lógica del proyecto en diversas capas con el objetivo
   de mantener las cosas ordenadas y facilitar el mantenimiento. En PHP, el
   patrón MVC por lo general sigue la siguiente estructura:

   a) Modelo: Representación de estructuras de información, generalmente 
      interactuando directamente una base de datos.
   b) Vista: Plantillas de cada página, generalmente escritas en HTML
   c) Controlador: Generalmente manejan las peticiones HTTP y se encargan
      de renderizar y devolver las respuestas apoyándose en las otras dos capas.

4. Seguridad: A pesar de que diversas técnicas pueden ser utilizadas manualmente
   para garantizar cierto grado de seguridad en nuestras aplicaciones, esta tarea
   resulta muchas veces compleja y laboriosa. La mayoría de frameworks
   proporcionan una capa de seguridad de forma automática, por ejemplo en
   CakePHP podemos encontrar:

   a) Seguridad contra inyecciones SQL
   b) Protección ante ataques `XSS <http://es.wikipedia.org/wiki/Cross-site_scripting>`__
   c) Protección ante ataques `Path Traversal <https://www.owasp.org/index.php/Path_Traversal>`__
   d) Protección ante ataques `Web tampering <https://www.owasp.org/index.php/Web_Parameter_Tampering>`__
   e) Encriptación de Cookies

5. Desarrollo ágil y ligero: Escribir menos y con calidad, uno de los grandes
   beneficios de utilizar un framework. Al trabajar de forma organizada, tareas
   como testeo, mantenimiento o cambios se realizan de una manera muchos más
   simple y rápida.

6. Soporte: Todos los frameworks más populares lo son gracias a las comunidades
   detrás de ellos. Cada uno posee sus propias plataformas en donde
   desarrolladores pueden solicitar ayuda o intercambiar opiniones.


En definitiva, los frameworks PHP ayudan a organizar el código de nuestros
proyectos, permitiendo así la reutilización y facilitando tareas como
mantenimiento o la colaboración entre miembros de un proyecto. Es decir, existen
para facilitar la vida de los desarrolladores PHP.
