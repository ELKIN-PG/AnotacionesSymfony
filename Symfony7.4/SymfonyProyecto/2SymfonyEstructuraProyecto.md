# Estructura de un Proyecto Symfony

A continuación, una explicación técnica y resumida de la estructura de directorios de un proyecto Symfony, optimizada para formato Markdown compatible con Obsidian.

---

## Estructura de Directorios

```plaintext
/proyecto-symfony
├── bin/                # Ejecutables
├── config/             # Configuración
├── public/             # Archivos públicos
├── src/                # Código fuente
├── templates/          # Plantillas Twig
├── tests/              # Tests unitarios/funcionales
├── var/                # Archivos generados (caché, logs)
├── vendor/             # Dependencias de Composer
├── .env                # Variables de entorno
├── composer.json       # Dependencias y configuración
├── symfony.lock        # Bloqueo de versiones
```

### Descripción de Directorios y Archivos

- **bin/**  
  Contiene ejecutables, como `bin/console`, para comandos CLI (crear entidades, migraciones, etc.).  
  **Ejemplo**: `php bin/console make:controller`

- **config/**  
  Archivos de configuración YAML, PHP o XML para bundles, servicios, rutas, etc.  
  **Archivos clave**:  
  - `config/packages/*`: Configuración de bundles.  
  - `config/services.yaml`: Definición de servicios.  
  - `config/routes.yaml`: Rutas de la aplicación.

- **public/**  
  Punto de entrada público. Contiene `index.php` (front controller) y recursos estáticos (CSS, JS, imágenes).  
  **Uso**: Configura el servidor web para apuntar aquí.

- **src/**  
  Código fuente de la aplicación.  
  - `src/Controller/`: Controladores para manejar solicitudes HTTP.  
  - `src/Entity/`: Entidades Doctrine (modelos de base de datos).  
  - `src/Repository/`: Repositorios para consultas a la base de datos.  
  - `src/Service/`: Lógica de negocio reusable.

- **templates/**  
  Plantillas Twig para renderizar vistas.  
  **Ejemplo**: `templates/base.html.twig` (plantilla base).

- **tests/**  
  Tests unitarios y funcionales (usando PHPUnit).  
  **Ejemplo**: `tests/Controller/HomeControllerTest.php`.

- **var/**  
  Archivos generados:  
  - `var/cache/`: Caché de la aplicación.  
  - `var/log/`: Logs (e.g., `dev.log`).  
  **Nota**: Borrar caché con `php bin/console cache:clear`.

- **vendor/**  
  Dependencias instaladas por Composer. No modificar manualmente.

- **.env**  
  Variables de entorno (base de datos, claves API, etc.).  
  **Ejemplo**:
  ```env
  DATABASE_URL="mysql://user:pass@127.0.0.1:3306/db"
  ```

- **composer.json**  
  Define dependencias y scripts de Composer.

- **symfony.lock**  
  Bloquea versiones de dependencias para consistencia.
