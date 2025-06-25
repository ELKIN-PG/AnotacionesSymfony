## Configuración Inicial.

1. **Instalación de Requisitos Previos:**
   - **PHP**: Asegúrate de tener PHP instalado en tu sistema. Symfony requiere PHP 8.0 o superior.
   - **Composer**: Es un gestor de dependencias para PHP. Necesitarás Composer para instalar Symfony y gestionar las dependencias de tu proyecto.
   - **Servidor Web**: Puedes usar el servidor web integrado de Symfony para desarrollo, pero también puedes configurar Apache o Nginx.
   - **Base de Datos**: Dependiendo de tu elección, necesitarás tener acceso a una base de datos como MySQL, PostgreSQL, etc.

2. **Instalación de Symfony CLI:**
   - Symfony CLI es una herramienta que proporciona un entorno de desarrollo local para aplicaciones Symfony. Puedes descargarlo desde [symfony.com](https://symfony.com/download).

3. **Crear un Nuevo Proyecto Symfony:**
   - Abre tu terminal y ejecuta el siguiente comando para crear un nuevo proyecto Symfony:
     ```bash
     symfony new mi_proyecto --webapp
     ```
   - Este comando creará un nuevo directorio llamado `mi_proyecto` con una estructura básica de Symfony.

4. **Estructura del Proyecto:**
   - Una vez creado el proyecto, familiarízate con la estructura de directorios. Algunos de los más importantes son:
     - `bin/`: Contiene el archivo console, que es la línea de comandos de Symfony.
     - `config/`: Aquí es donde se encuentran los archivos de configuración.
     - `src/`: Contiene el código fuente de tu aplicación, como controladores, entidades, etc.
     - `templates/`: Aquí es donde se almacenan las plantillas Twig.
     - `var/`: Contiene archivos generados automáticamente, como caché y logs.
     - `vendor/`: Contiene las dependencias de Composer.
     - `public/`: Es el directorio raíz web y contiene el archivo `index.php`.

5. **Ejecutar el Servidor de Desarrollo:**
   - Navega al directorio de tu proyecto y ejecuta el siguiente comando para iniciar el servidor de desarrollo:
     ```bash
     symfony serve
     ```
   - Esto iniciará un servidor web local y podrás acceder a tu aplicación Symfony en `http://localhost:8000`.

6. **Verificar la Instalación:**
   - Abre tu navegador y ve a `http://localhost:8000`. Deberías ver la página de bienvenida de Symfony, lo que indica que tu proyecto se ha configurado correctamente.

El `MakerBundle` es un paquete que proporciona una serie de comandos útiles para generar código en Symfony, como controladores, entidades, formularios, etc. Este paquete es muy útil durante el desarrollo, pero no es necesario en un entorno de producción.

Para resolver este error, necesitas instalar el `MakerBundle`. Puedes hacerlo ejecutando el siguiente comando en tu terminal, dentro del directorio de tu proyecto Symfony:

`composer require symfony/maker-bundle --dev`

Este comando instalará el `MakerBundle` como una dependencia de desarrollo en tu proyecto.


El error que estás viendo se debe a que el `MakerBundle` está intentando generar pruebas PHPUnit para tu controlador, pero PHPUnit no está instalado en tu proyecto. Esto ocurre porque respondiste "y" (sí) a la pregunta sobre si deseas generar pruebas PHPUnit, pero no tienes PHPUnit instalado.

Para resolver este problema, tienes dos opciones:

### Opción 1: Instalar PHPUnit

Si deseas generar pruebas PHPUnit para tus controladores, puedes instalar PHPUnit ejecutando el siguiente comando:

Copy

`composer require --dev phpunit/phpunit`

Una vez instalado PHPUnit, puedes volver a ejecutar el comando `make:controller` y responder "yes" a la pregunta sobre generar pruebas PHPUnit.

Despues de esto, generamos nuevamente el controlador

