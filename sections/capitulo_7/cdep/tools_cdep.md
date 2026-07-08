### Tools (Herramientas)

- GitHub Actions o GitLab CI:  
  Se utilizan para automatizar el pipeline de CI/CD. Permiten ejecutar pruebas automáticas, validaciones y despliegues a diferentes entornos como desarrollo, staging y producción mediante workflows configurables.

- Railway:  
  Se utiliza para el despliegue del backend y la gestión de la base de datos. Facilita la automatización de despliegues, variables de entorno y administración de servicios en la nube.

- Render:  
  Se encarga del despliegue del frontend y la landing page. Permite integración directa con repositorios Git, automatizando despliegues en cada push y ofreciendo alta disponibilidad y rendimiento global.

### Practices (Prácticas)

- Feature Branching:  
  Utilizamos una estrategia de ramas en Git donde los desarrolladores trabajan en nuevas funcionalidades dentro de ramas separadas. Una vez completadas y probadas, estas ramas se fusionan a la rama develop, la cual gestiona la integración de cambios y el despliegue del sistema.

- Commit-based deployment (Despliegue basado en commits):  
  Cada vez que se realiza un commit en la rama develop, el pipeline de CI/CD se activa automáticamente para ejecutar los procesos de construcción, pruebas y despliegue. Esto permite mantener un flujo de entrega continuo y automatizado.

- Rollback automático:  
  En caso de detectar fallos en producción después del despliegue, el pipeline puede restaurar automáticamente la versión anterior estable del sistema y notificar al equipo de desarrollo. Esto garantiza estabilidad y rápida recuperación ante errores.