Soporte para múltiples SGBD
===========================

Como se analizó en capítulos anteriores, uno de los inconvenientes con Joomla y
Wordpress es que ofrecen soporte unicamente para MySQL. Si bien es cierto que
este SGBD es quizás el más utilizado y extendido en entornos web, en algunas
ocasiones, ya sea por cuestiones técnicas o de fuerza mayor, es necesario
emplear otras plataformas como MSSQL o PostgreSQL.

Gracias a la capa de modelo proporcionada por CakePHP, QuickAppsCMS es capaz de
funcionar con múltiples SGBD, en concreto, *QuickAppsCMS* acepta:

- MySQL (5.1.10 or greater)
- PostgreSQL
- Microsoft SQL Server (2008 or higher)
- SQLite 3

Además es posible funcionar con múltiples conexiones a BD a la vez. Por ejemplo,
un plugin de tercero puede utilizar su propia base de datos para funcionar,
mientras que el núcleo de QuickAppsCMS puede haber sido instalado en otra base
de datos completamente distinta.
