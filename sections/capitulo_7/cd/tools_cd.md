### Tools

- **GitHub Actions / GitHub CI-CD Apps**  
  Se utilizan para automatizar el flujo de integración y despliegue continuo (CI/CD). En nuestro caso, GitHub Actions gestiona el pipeline que permite ejecutar pruebas, validar cambios y desplegar automáticamente cuando el código cumple con los requisitos establecidos.  
  Este proceso se integra con plataformas como Railway y Vercel, permitiendo una entrega continua del software tanto en backend como en frontend.

- **Railway (Backend Deployment)**  
  Se utiliza como plataforma de despliegue del backend. Permite automatizar la publicación de la API directamente desde el repositorio conectado a GitHub, facilitando el despliegue continuo sin necesidad de configuración manual de servidores.

- **Vercel (Frontend / Landing Page Deployment)**  
  Se encarga del despliegue del frontend y la landing page. Está integrado con GitHub, lo que permite que cada cambio en el repositorio se despliegue automáticamente, asegurando rapidez en la entrega y consistencia entre versiones.

- **Trello**  
  Se utiliza para la gestión del flujo de trabajo y seguimiento del proyecto. Permite organizar tareas, asignar responsabilidades y controlar el avance del desarrollo dentro del equipo, facilitando la coordinación durante todo el ciclo de CI/CD.

### Practices 

**Feature Branching y Pull Requests:** Las nuevas funcionalidades o correcciones se desarrollan en ramas separadas siguiendo el flujo de GitFlow. Una vez lista la funcionalidad, se crea un Pull Request hacia la rama principal. GitHub Actions ejecuta automáticamente las pruebas y validaciones antes de permitir la fusión, asegurando que solo el código aprobado llegue a producción.

**Pipeline Automatizado con GitHub Actions:** Cada push o merge a las ramas principales activa un pipeline en GitHub Actions que ejecuta las pruebas, valida el build y coordina el despliegue automático hacia Railway (backend) y Vercel (frontend/landing). Esto garantiza que el software esté siempre en un estado desplegable.

**Despliegue Continuo por Plataforma:** El despliegue se realiza de forma separada según la capa de la aplicación. Railway gestiona el despliegue automático del backend al detectar cambios en el repositorio conectado, mientras que Vercel hace lo propio con el frontend y la landing page, asegurando consistencia y rapidez en cada entrega.

**Integración con Repositorio GitHub:** Tanto Railway como Vercel están directamente conectados al repositorio de GitHub, lo que elimina pasos manuales en el proceso de entrega. Cada cambio validado se refleja automáticamente en los entornos de producción correspondientes.

**Rollback y Control de Versiones:** En caso de errores tras un despliegue, tanto Railway como Vercel permiten revertir rápidamente a una versión anterior desde sus paneles de control, reduciendo el tiempo de inactividad y minimizando el impacto en los usuarios finales.