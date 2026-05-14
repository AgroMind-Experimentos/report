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

## 1. Feature Branching y Merge Requests
Es una forma de trabajar con ramas en Git. Cada nueva funcionalidad se desarrolla en una rama separada (feature branch), sin afectar el código principal. Cuando ya está lista, se crea un Merge Request (o Pull Request) para revisar el código antes de integrarlo a la rama principal. Normalmente pasa revisiones y pruebas automáticas antes de aprobarse.

## 2. Despliegue semiautomático
El sistema de CI/CD prepara todo automáticamente (build, tests, empaquetado), pero el paso de ponerlo en producción no ocurre solo. Se necesita una acción humana para ejecutar el despliegue final. Es un punto intermedio entre automático y manual.

## 3. Aprobación manual
Es un “filtro de seguridad” antes de lanzar a producción. Una persona responsable revisa los resultados de las pruebas, logs o reportes del pipeline y decide si se puede desplegar o no. Esto reduce riesgos de errores en producción.