## Integración Continua (CI)

Cada vez que se realiza un commit en una rama de desarrollo, el pipeline se encarga de ejecutar pruebas automáticas y validar que la aplicación pueda seguir siendo desplegada sin errores. Esto ayuda a mantener el código en un estado listo para producción en todo momento.

## Despliegue Manual

Aunque el sistema puede estar configurado para desplegar automáticamente, la publicación final se realiza solo cuando existe una aprobación previa. Esto agrega una capa de control antes de impactar a los usuarios finales.

## Monitoreo y Feedback

El proceso de CD incorpora herramientas de monitoreo que permiten evaluar el comportamiento del sistema después de integrar nuevos cambios, observando rendimiento, errores y estabilidad general.

## Aprobación del Despliegue

En esta etapa, el pipeline se detiene temporalmente hasta recibir la validación de un desarrollador, administrador o equipo de operaciones, quienes confirman que el despliegue puede realizarse de forma segura en producción.