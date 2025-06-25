En Symfony, el directorio `templates` se crea automáticamente cuando instalas el paquete necesario para manejar las vistas con Twig. Si no tienes el directorio `templates`, es probable que necesites instalar el paquete `twig-bundle`, que es el responsable de manejar las plantillas Twig en Symfony.

Puedes instalar el `twig-bundle` ejecutando el siguiente comando en tu terminal:

Copy

`composer require twig`

Este comando instalará el paquete Twig y configurará automáticamente tu proyecto para usar Twig como motor de plantillas. Después de instalar Twig, el directorio `templates` debería crearse automáticamente en la raíz de tu proyecto.