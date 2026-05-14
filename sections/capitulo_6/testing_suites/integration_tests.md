Los Core Integration Tests son esenciales para verificar que los controladores se comuniquen de manera adecuada con los distintos componentes del sistema, como los servicios y las bases de datos. Además, al analizar distintos escenarios de fallo, estas pruebas permiten comprobar que el sistema gestione correctamente situaciones inesperadas y devuelva los códigos de respuesta apropiados. De esta manera, se mejora la experiencia del usuario, se facilita la detección de errores y se contribuye al desarrollo de un software más estable y confiable.

**Monitoring and Control**

En este contexto, las pruebas de integración validan el flujo completo de los casos de uso para la gestión de las tareas. Sobresalen los `CreateTaskCommandServiceTests` y `UpdateTaskStatusCommandServiceTests`, donde no solo se prueba el escenario exitoso de creación o actualización, sino que se valida explícitamente que el servicio rechace la operación (lanzando excepciones) si la organización o la parcela especificada no existen en los repositorios.

<img src="../../../img/capitulo_6/integration_tests/monitoring.png" />
<div style="page-break-after: always;"></div>

**Organizations**

Las pruebas de integración en Organizaciones confirman el correcto registro de elementos estructurales y la gestión de permisos. Destacan comandos como `CreateOrganizationServiceTests` y `CreatePlotCommandServiceTests`, en los cuales se valida que el servicio actúe como un intermediario sólido entre las solicitudes y el almacenamiento, además de manejar adecuadamente las invitaciones mediante el `InvitationCommandServiceTests`.

<img src="../../../img/capitulo_6/integration_tests/organizations.png" />
<div style="page-break-after: always;"></div>

**Profiles**

Para Profiles, las pruebas de servicio de integración aseguran que la configuración de las cuentas de usuario se ejecute sin problemas. Pruebas como `ProfileCommandServiceTests` y `SettingsCommandServiceTests` evalúan el correcto procesamiento de la información del perfil del usuario y sus preferencias de aplicación, comprobando su persistencia a través de los mocks de los repositorios.

<img src="../../../img/capitulo_6/integration_tests/profiles.png" />
<div style="page-break-after: always;"></div>

**Report**

En el contexto Report, la validación de integración busca asegurar que la solicitud de generación o registro de datos del reporte sea atendida con precisión. A través de `ReportCommandServiceTests`, se verifica que los parámetros del reporte se inyecten correctamente en la entidad respectiva y se delegue la persistencia de forma correcta y segura.

<img src="../../../img/capitulo_6/integration_tests/report.png" />
<div style="page-break-after: always;"></div>

**Iam**

En el área de Identidad y Acceso (IAM), los test de integración garantizan los flujos de seguridad principales. Pruebas críticas como `RegisterCommandServiceTests` y `LoginCommandServiceTests` simulan el comportamiento que tendría el servicio frente a intentos válidos e inválidos de autenticación y creación de usuario, lo que representa la primera barrera de control en la plataforma.

<img src="../../../img/capitulo_6/integration_tests/iam.png" />