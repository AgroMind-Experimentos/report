El pipeline de notificaciones se encarga de comunicar de forma automática al equipo los resultados de las pruebas y el estado del pipeline de integración y despliegue continuo. A diferencia del componente de alertas, orientado al monitoreo de la aplicación en producción, este componente notifica sobre el resultado de los procesos de construcción y despliegue.

<div align="center">

| <img src="../../../img/logos/githubactions.svg" width="48" height="48"/><br/>GitHub Actions |
|:---:|

</div>

Para ello se utiliza GitHub Actions, que gestiona los flujos de trabajo de CI/CD del proyecto. Al finalizar cada build o etapa del pipeline, GitHub Actions genera notificaciones automáticas que informan sobre el éxito o fallo de las pruebas, el tiempo de ejecución y los problemas específicos detectados. Estas notificaciones se entregan a través del correo electrónico de los responsables del proyecto, mecanismo que GitHub Actions ejecuta de forma automática al detectar la ejecución correcta o el fallo de un flujo de trabajo.

Gracias a este mecanismo, el equipo recibe retroalimentación sobre cada ciclo de integración y despliegue, lo que facilita una respuesta rápida ante cualquier incidente o fallo en el proceso.
