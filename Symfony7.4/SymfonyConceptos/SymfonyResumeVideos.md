## Vendor Symfony

Aunque la búsqueda no arrojó un resultado directo y conciso para "Vendor Symfony", en el contexto de PHP y Composer, el directorio `vendor/` en un proyecto Symfony (o cualquier proyecto PHP que use Composer) es donde se instalan todas las dependencias y bibliotecas de terceros. Composer es el administrador de dependencias que descarga y organiza estas bibliotecas en la carpeta `vendor/`. Este directorio es crucial para el funcionamiento de la aplicación, ya que contiene todo el código externo del que depende tu proyecto.

## DataSystem Symfony

No se encontró una definición directa para "DataSystem Symfony". Sin embargo, Symfony es un framework de desarrollo web en PHP que ofrece una estructura robusta para construir aplicaciones empresariales escalables y personalizables. Permite a las organizaciones desarrollar soluciones web de alto rendimiento.

## Namespace en PHP

Los `namespaces` en PHP son una forma de encapsular y agrupar clases, interfaces, funciones y constantes relacionadas. Su propósito principal es resolver problemas de colisión de nombres entre el código que creas y las clases/funciones/constantes internas de PHP o de terceros. Permiten acortar nombres largos y mejorar la legibilidad del código. En Symfony, los `namespaces` se utilizan ampliamente para organizar el código del framework y de las aplicaciones, siguiendo estándares como PSR-0 y PSR-4 para mapear los nombres de clase completamente calificados (Fully Qualified Class Names - FQCN) a rutas de archivo.

## Package load Symfony

Symfony se compone de numerosos componentes individuales que se pueden instalar y cargar como "paquetes" a través de Composer. Estos paquetes proporcionan funcionalidades específicas, como el componente `Finder` para encontrar archivos, `Console` para interfaces de línea de comandos, `String` para manipulación de cadenas orientada a objetos, y `EventDispatcher` para la comunicación entre componentes. La gestión de paquetes en Symfony se simplifica con Symfony Flex.

## ORM Doctrine

Doctrine es el sistema de mapeo objeto-relacional (ORM) que Symfony integra. Un ORM simplifica las interacciones con la base de datos permitiendo a los desarrolladores trabajar con objetos PHP en lugar de escribir consultas SQL directas. Doctrine permite definir entidades (clases PHP que representan tablas de base de datos) y mapear sus propiedades a columnas de tabla. Soporta diferentes tipos de relaciones entre entidades (OneToOne, OneToMany, ManyToOne, ManyToMany) y proporciona `lifecycle callbacks` para ejecutar lógica personalizada durante el ciclo de vida de una entidad. Su objetivo es hacer más fácil la construcción, consulta y mantenimiento de bases de datos en aplicaciones Symfony.

## Bundle Symfony -> Plugins

Los `Bundles` en Symfony son una forma de organizar y distribuir código Symfony reutilizable entre diferentes proyectos. Son una parte fundamental del ecosistema de Symfony y extienden el framework a nivel de framework.

Por otro lado, un `plugin system` permite definir puntos de extensión en tu aplicación para que los desarrolladores puedan añadir funcionalidades específicas. Mientras que los `bundles` están diseñados para ser reutilizables en múltiples proyectos, los `plugins` suelen ser específicos de una sola aplicación. Los `plugins` pueden ser útiles para integrar servicios de terceros, añadir nuevas características o tipos de contenido.

## Overhead Symfony

Aunque Symfony es un framework completo, los desarrolladores han optimizado cada clase y método para ser lo más rápido posible, minimizando el "overhead" (sobrecarga de rendimiento). La sobrecarga básica (tiempo para mostrar un "hola mundo" con y sin Symfony) es mínima. El framework es escalable y reacciona bien a las pruebas de estrés. Se recomienda desactivar utilidades de depuración como Xdebug en entornos de producción para optimizar el rendimiento.

## Deprecaciones, funcionalidades que ya no se usan

Las "deprecaciones" en Symfony se refieren a funcionalidades o métodos que se marcan como obsoletos y que serán eliminados en futuras versiones. Symfony proporciona un componente `symfony/deprecation-contracts` con una función global `trigger_deprecation()` que activa avisos de deprecación. Estos avisos pueden ser capturados y registrados para su posterior descubrimiento en entornos de desarrollo y producción, ayudando a los desarrolladores a adaptar su código a las nuevas versiones.

## Versiones LTS

Las versiones LTS (Long-Term Support) de Symfony son aquellas que reciben soporte extendido para corrección de errores y problemas de seguridad. Estas versiones son recomendadas para la mayoría de los usuarios, ya que ofrecen mayor estabilidad y un ciclo de vida más largo. Las versiones menores (no LTS) se lanzan cada seis meses, mientras que las versiones mayores (también LTS) se lanzan cada dos años. Por ejemplo, Symfony 6.4 y 5.4 son versiones LTS actuales o recientemente LTS.

## SymfonyFlex, se sobreponer sobre composer, administra las dependencias.

Symfony Flex es un plugin de Composer que actúa como una herramienta de gestión de paquetes y dependencias para proyectos Symfony. Simplifica el proceso de mantenimiento de aplicaciones Symfony, permitiendo añadir, eliminar y configurar `bundles` y librerías de manera eficiente. Flex automatiza tareas comunes y optimiza el flujo de trabajo de desarrollo, liberando a los desarrolladores de tareas de configuración que consumen mucho tiempo.

## Componentes de inyección de dependencias, composición de clases

El componente `DependencyInjection` de Symfony es una herramienta poderosa que simplifica la gestión de dependencias, objetos y atributos dentro de tu aplicación. Promueve el desacoplamiento de componentes, haciendo el código más modular y fácil de mantener. Symfony soporta tres tipos de inyección:

- **Inyección por Constructor:** Las dependencias se inyectan a través del constructor de una clase.
- **Inyección por Setter:** Las dependencias se establecen utilizando métodos `setter`.
- **Inyección por Propiedad:** Las dependencias se asignan directamente a propiedades públicas de la clase.

## dotenv, administrador de variables de entorno

El componente `symfony/dotenv` se encarga de registrar variables de entorno desde un archivo `.env`. Este archivo se utiliza para almacenar configuraciones específicas del entorno (como credenciales de base de datos, claves API, etc.) que no deben ser parte del control de versiones. El componente `Dotenv` parsea estos archivos y hace que las variables estén accesibles a través de `$_SERVER` o `$_ENV`.

## Symfony como full stack, templates y plantilas twig

Symfony puede funcionar como un framework full-stack, lo que significa que cubre tanto el backend como el frontend. Para la parte del frontend, utiliza Twig como su motor de plantillas por defecto. Twig es un lenguaje de plantillas flexible, rápido y seguro que permite a los desarrolladores organizar y renderizar HTML de manera eficiente. Proporciona una sintaxis concisa y es fácil de usar para diseñadores web. Twig compila las plantillas a PHP y las cachea automáticamente en entornos de producción para un rendimiento óptimo.

## AbstractKernel MicroKernelTrait comportamientos del kernel

El `MicroKernelTrait` en Symfony se utiliza para construir frameworks propios o aplicaciones de una sola clase Kernel. El `Kernel` por defecto de las aplicaciones Symfony utiliza este `trait` para configurar los `bundles`, las rutas y el contenedor de servicios en la misma clase. Este enfoque de micro-kernel ofrece flexibilidad, permitiendo controlar la estructura y las características de tu aplicación de forma concisa. Requiere la implementación de métodos como `registerBundles()`, `configureContainer()` y `configureRoutes()`.

## EventDispatcher, componente, patron observer notificador, lanzado de colas y procesos

El componente `EventDispatcher` en Symfony implementa el patrón Observer. Proporciona herramientas que permiten a los componentes de tu aplicación comunicarse entre sí mediante el envío de "eventos" y la escucha de los mismos. Esto facilita la creación de aplicaciones modulares y extensibles. Cuando ocurre una acción específica (por ejemplo, un usuario que se registra), un "emisor de eventos" dispara un evento, y los "listeners de eventos" o "suscriptores de eventos" responden a estas notificaciones ejecutando un código determinado. Este sistema es fundamental para la integración continua de nuevas funcionalidades, como el procesamiento de datos en tiempo real y las notificaciones a usuarios.

## Patrones de diseño que usa symfony

Symfony utiliza varios patrones de diseño para construir su arquitectura robusta y modular. Algunos ejemplos incluyen:

- **Observer (Observador):** Implementado por el componente `EventDispatcher` para la comunicación entre componentes.
- **Factory (Fábrica):** Para la creación de objetos.
- **Builder (Constructor):** Para construir objetos complejos paso a paso.
- **Singleton (Singletón):** Aunque no es tan prominente en el desarrollo moderno de Symfony, se puede encontrar en ciertos contextos.
- **Structural Patterns:** Patrones que se ocupan de la composición de clases y objetos.

## Componente Mailer

El componente `Mailer` de Symfony, junto con el componente `Mime`, proporciona un sistema potente para crear y enviar correos electrónicos. Soporta mensajes multiparte, integración con Twig para plantillas de correo, incrustación de CSS, adjuntos y más. Permite configurar diferentes "transportes" (servicios de envío de correo como SendGrid o Mailgun) y ofrece características de alta disponibilidad como `failover` y `load balancing` para asegurar que los correos se envíen incluso si un servidor de correo falla.

## Envíos push notificador (Componente Notifier)

El componente `Notifier`, introducido en Symfony 5.0, es una abstracción para enviar notificaciones a los usuarios a través de diferentes canales (SMS, Slack, correo electrónico, notificaciones push, etc.). Permite gestionar dinámicamente cómo se envían los mensajes. Para notificaciones push, se integra con servicios de terceros como Expo y OneSignal a través de sus respectivos paquetes `notifier`.

## Componente String orientado a objetos

El componente `symfony/string` proporciona una API orientada a objetos para la manipulación de cadenas de texto. Aborda de manera unificada bytes, puntos de código UTF-8 y clústeres de grafemas, facilitando el trabajo con cadenas multilingües y complejas de una manera más segura y predecible que las funciones de cadena tradicionales de PHP.

## EventListeners

Los `EventListeners` (oyentes de eventos) son clases o métodos que "escuchan" eventos específicos disparados por la aplicación y responden a ellos ejecutando un código. En Symfony, cuando un evento es disparado, el `EventDispatcher` decide qué método ejecutar dentro de la clase del oyente. Alternativamente, se pueden usar `EventSubscribers`, que son clases que definen uno o más métodos que escuchan varios eventos, manteniendo el conocimiento de los eventos dentro de la clase, lo que los hace más fáciles de reutilizar.

## Política de releases

Las versiones de Symfony siguen un modelo basado en el tiempo: las versiones menores se lanzan cada seis meses (en mayo y noviembre), y las versiones mayores se lanzan cada dos años. Existen versiones LTS (Long-Term Support) que reciben soporte para corrección de errores y seguridad durante un período más prolongado (generalmente 3 años para errores y más para seguridad). Las versiones LTS son las recomendadas para la mayoría de los proyectos debido a su estabilidad y soporte extendido.

---

Espero que este reporte te sea de gran utilidad para tu aplicación Obsidian. Si necesitas más información sobre algún tema en particular, no dudes en preguntar.