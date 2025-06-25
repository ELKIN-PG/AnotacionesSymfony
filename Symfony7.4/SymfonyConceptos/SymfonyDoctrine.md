![[Pasted image 20250616215602.png]]

### DoctrineMongoDBBundle

**DoctrineMongoDBBundle** **ODM** *Object Document Manager*, tratas con objetos PHP simples, que despues son persistidos hacia y desde **MongoDB**

Al parecer, **Doctrine** Es un mapeador objeto-relacional *ORM* escrito en *PHP* que proporciona una capa de persistencia para objetos PHP, es una capa de abstraccion que se sitúa encima de un *Sistema de gestion de bases de datos* (SGBD)

Las **Entidades** , que en este caso son los objetos que son representados como entidades tienen propiedades persistibles, instancias que puede ser guardada y obtenida en base de datos por la capacidad de mapear los datos a travez de **Entity Manager**, una implementacino del [Patron data mapper](https://www.martinfowler.com/eaaCatalog/dataMapper.html)

![[Pasted image 20250616223020.png]]
*Guardado y persistencia de los datos*

Una de las caracteristicas de **Doctrine** es que se basa en [Active record pattern](https://es.wikipedia.org/wiki/Active_record) para trabajar con datos, si necesitamos crear un nuevo objeto `Usuario` en la base de datos, no tendremos que escribir ninguna sentencia SQl, simplemente hariamos.

![[Pasted image 20250616223429.png]]

Ahora, cuando se trata de hacer las consultas a las bases de datos, se usa un tipo de dialecto SQL denominado [DQL](https://blacksmithgu.github.io/obsidian-dataview/queries/differences-to-sql/)

### La diferencia de SQL, DQL

Una consulta DQL se ejecuta de arriba a abajo, línea por línea. Se parece más a un programa de ordenador que a una típica consulta SQL.

Cuando se evalúa una línea, produce un conjunto de resultados y pasa todo el conjunto a la siguiente línea DQL, que manipulará el conjunto que recibió de la línea anterior.

*Más caracteristicas de Doctrine*

- Soporte para datos jerárquicos;
- Soporte para hooks (métodos que pueden validar o modificar las escrituras y lecturas de la base de datos) y eventos para manejar la lógica de negocio relacionada;
- Herencia;
- Un framework de caché que utiliza diversos motores como memcached, SQLite o APC;
- Transacciones [ACID](https://es.wikipedia.org/wiki/ACID "ACID");
- Diversos comportamientos del modelo (conjuntos anidados, internacionalización, log, índice de búsqueda);
- Una función "compilar" que combina varios archivos PHP del framework en uno solo para evitar el descenso de rendimiento que provoca incluir varios archivos PHP.