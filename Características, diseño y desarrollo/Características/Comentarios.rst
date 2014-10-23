Comentarios
===========

QuickAppsCMS ofrece de serie un plugin para la gestión de comentarios que ofrece
su propia API y que permite a cualquier otro plugin hacer uso de ella para
ofrecer así la publicación de comentarios sobre cualquier Entidad. Gracias este
plugin es posible crear sitios webs estilo Blog muy similares a los ofrecidos
por Wordpress.

Esta API permite a cualquier entidad del sistema ser *comentable*. Su
funcionamiento consiste, en esencia, en realiza asociaciones *1:N* de forma
dinámica entre una tabla cualquiera y un repositorio unificado de comentarios.
Ofrece en forma de *Componente* una pequeña interfaz para la publicación y
listado de comentarios en *FrontEnd*, junto con una completa interfaz
empaquetada en forma de *Trait* destinada a ofrecer un CRUD completo para
*BackEnd*.

.. figure:: /_assets/img/comments_gui.png
   :width: 70%
   :align: center

   Interfaz de gestión para comentarios en BackEnd.

Entre otras de sus características se encuentra la posibilidad de habilitar
mecanismos de protección contra contenido indeseado o SPAM: sistema CAPTCHA
[#CAPTCHA]_ para verificar que quien publica un comentario es en efecto un
humano y no un software automatizado. Por otro lado se ofrece la integración con
AKISMET [#AKISMET]_, para asegurar que los comentarios publicados no contienen
mensajes que pudieran ser clasificados como SPAM como publicidad engañosa y/o
enlaces a sitios peligrosos.

.. [#CAPTCHA] Son las siglas de Completely Automated Public Turing test to tell
  Computers and Humans Apart. Este test es controlado por una máquina, en lugar
  de por un humano como en la prueba de Turing. Por ello, consiste en una prueba
  de Turing inversa.

.. [#AKISMET] Servicio de filtrado SPAM.
