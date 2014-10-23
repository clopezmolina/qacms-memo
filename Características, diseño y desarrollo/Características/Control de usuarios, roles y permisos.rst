Control de usuarios, roles y permisos
=====================================

QuickAppsCMS permite crear un número ilimitado de cuentas de usuario. Cada uno
de estos usuarios puede pertenecer a ``uno o más`` *roles*. El pertenecer a un
rol u otro proporciona acceso a distintas secciones de la plataforma, por
defecto, QuickAppsCMS define tres roles que son descritos lineas más abajo. Por
otro lado, QuickAppsCMS ofrece mecanismos para el alta, modificación y baja de
cuentas de usuarios integrados con un sistema de envío de mensajes automáticos,
así por ejemplo, cada vez que un usuario se registra recibe en su cuenta email
instrucciones de activación.


**Administrator**

Los usuarios que pertenezcan a este rol son aquellos que más privilegios poseen
dentro del sistema. Pueden existir múltiples usuarios con este rol, pero debe al
menos siempre existir uno. Ninguna restricción es aplicada a estos usuarios y
pueden moverse libremente por el sistema. Algunas de las cosas que estos
usuarios pueden realizar son por ejemplo:

- Acceso completo al *BackEnd* del sitio web, crear nuevos contenidos, gestionar
  otros usuarios, instalar nuevos plugins, etc.

- Visualizar contenidos restringidos a roles concretos.

- Gestionar otros usuarios de roles inferiores.

Este rol es generalmente asignado a personas encargadas de mantener el sitio
web, por ejemplo diseñadores o programadores. Durante el último paso del proceso
de instalación de QuickAppsCMS éste crea automáticamente una nueva cuenta de
usuario, dicha cuenta es asignada por defecto a este rol.


**Authenticated**

Todo visitante del sitio web que se ha identificado es automáticamente asignado
a este rol. Así por ejemplo, un administrador del sistema pertenece a la vez a
dos grupos: "Administrator" y "Authenticated". Los usuarios pertenecientes a
este rol pueden por defecto:

- Acceder el sitio web


**Anonymous**

Todo visitante del sitio web que no se ha identificado es automáticamente
asignado a este rol. Estos usuarios pueden por defecto:

- Acceder el sitio web


Control de accesos (ACL)
------------------------

Los usuarios que posean los privilegios adecuados pueden fácilmente crear nuevas
reglas de acceso a las diversas secciones que conforman un sitio web. Estas
reglas son creadas en función de una combinación de "plugin", "controlador" y
"acción". Por ejemplo, es posible restringir por roles el acceso a la acción
"login" del controlador "Gateway" perteneciente el plugin "User"
(User/Gateway/login), es decir, la página de login de usuarios.

QuickAppsCMS hace uso del sistema ACL (Access Control Lists) proporcionado por
CakePHP para gestionar estos permisos, este sistema permite gestionar los
permisos de toda la aplicación de una manera simple y granular. Dicho sistema se
basa en la definición de dos estructuras que son utilizadas internamente:

- ACO (Access Control Object): Representan recursos deseados por algo o alguien.
- ARO (Access Request Object): Representa a alguien o algo que requiere otra cosa.

En el ejemplo anterior: un usuario intentando acceder a la página de login; los
distintos roles a los que el usuario pertenece son considerados AROs, mientras
que la página de login a la que intenta acceder sería un ACO. Como un usuario
puede pertenecer a múltiples roles, el acceso se concede si, y solo si, alguno
de sus roles (AROs) posee permisos sobre el ACO solicitado.

Adicionalmente, QuickAppsCMS permite definir reglas de acceso a contenidos de
forma granular. Los usuarios con privilegios suficientes para crear nuevos
contenidos o editar los ya existentes pueden, por ejemplo, permitir que una
determinada publicación sea accesible únicamente por usuarios pertenecientes a
un rol en concreto. Lo mismo es aplicable al sistema de bloques, pudiendo crear
bloques de contenido visibles únicamente a un conjunto de roles de usuario en
particular.


Autenticación y Autorización
----------------------------

Tanto la acreditación de permisos como la identificación de cada ARO son
procesos existentes y bien diferenciados en cualquier aplicación basada en
permisos. En QuickAppsCMS ambas tareas son "extendibles" por plugins de
terceros gracias al API proporcionada, gracias a ésta es posible identificar y
conceder permisos a grupos de usuarios de una forma flexible y transparente.

Autenticación
~~~~~~~~~~~~~

Es el proceso de identificar a un usuario (persona o cosa) mediante el uso de
credenciales y asegurar que cada usuario es quien dice ser. Con frecuencia estas
credenciales son proporcionadas mediante el uso del clásico formulario de
identificación basado en usuario/contraseña, formulario presente por defecto en
toda instalación de QuickAppsCMS. Aunque QuickAppsCMS ofrece una robusta API que
permite a cualquier plugin definir nuevos métodos de autenticación, así por
ejemplo un plugin podría añadir un formulario de identificación basado en `OAuth
<http://oauth.net/>`__, o por ejemplo, permitir la identificación mediante
`Facebook <http://facebook.com>`__. Otra característica interesante del sistema
de autenticación proporcionado por QuickAppsCMS es que permite bloquear usuarios
que alcancen un numero determinado de intentos de login fallidos, por ejemplo,
es posible bloquear a un usuario durante 60 minutos si realiza 10 intentos
fallidos de autenticación. Tanto el tiempo de bloque como el el umbral de fallos
son ambos parámetros configurables por los administradores del sitio web.


Autorización
~~~~~~~~~~~~

La autorización es el proceso de asegurar que un usuario (previamente
identificado) posee permisos sobre los recursos que desea acceder. Nuevamente,
QuickAppsCMS ofrece una API para permitir a otros plugins de terceros definir
nuevos mecanismos de autorización (adaptadores). Un problema común con los
sistemas de autorización es que deben estar constantemente comprobando
privilegios contra normalmente una BD, esta tarea es realizada siempre al menos
una vez por cada página solicitada lo que puede producir un mal rendimiento de
la aplicación en su conjunto en casos de alta demanda. Para solucionar este
inconveniente, QuickAppsCMS emplea un sistema de autorización basado en cache
denominado "CachedAutorize", gracias a esto se reduce de forma considerable el
número de consultas hacia la BD por cada petición.