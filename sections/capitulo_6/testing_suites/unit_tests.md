Los Core Entities Unit Tests cumplen un papel fundamental en el desarrollo de software, ya que permiten asegurar la confiabilidad y el correcto comportamiento de las entidades principales del sistema. Estas pruebas ayudan a detectar errores de manera temprana, mejorar la estabilidad del código y facilitar el mantenimiento y futuras actualizaciones de la aplicación, aislando el comportamiento de las dependencias.

**Monitoring and Control**

En este contexto, las pruebas unitarias se enfocan en validar la correcta inicialización y los comportamientos intrínsecos de las entidades principales como Task y Checklist. Por ejemplo, en pruebas como `TaskAggregateTests` y `ChecklistsTests` se asegura de que al crear una tarea o lista de chequeo, se asignen correctamente a una organización, lote y responsable, reflejando el estado inicial esperado para el seguimiento adecuado de las actividades agrícolas.

<img src="../../../img/capitulo_6/unit_tests/monitoring.png" />
<div style="page-break-after: always;"></div>

**Organizations**

Las pruebas unitarias del contexto de Organizaciones se centran en verificar que las entidades que agrupan a los usuarios y recursos estén bien definidas en su estado base. Aquí destacan pruebas como `OrganizationTests`, `PlotTests` e `InvitationTests`, donde se valida que al instanciar una organización o una parcela, los atributos descriptivos y las asociaciones de ubicación se configuren correctamente de acuerdo a las reglas de negocio.

<img src="../../../img/capitulo_6/unit_tests/organizations.png" />
<div style="page-break-after: always;"></div>

**Profiles**

Para el contexto de Profiles, las pruebas unitarias validan la creación de los perfiles de usuario. Por ejemplo, a través de los `ProfileTests` se comprueba que un perfil recién creado incluya de forma íntegra los datos personales del usuario y su identificador en el sistema, asegurando la consistencia en el manejo de la identidad pública dentro de la plataforma.

<img src="../../../img/capitulo_6/unit_tests/profiles.png" />
<div style="page-break-after: always;"></div>

**Report**

En el contexto de Report, las pruebas unitarias se aseguran de que el modelo principal de reporte esté estructuralmente correcto al instanciarse. Con los `ReportTests` se valida que entidades destinadas al análisis de datos, como los reportes de rendimiento o de métricas de lotes, almacenen correctamente la información básica antes de ser procesados o exportados.

<img src="../../../img/capitulo_6/unit_tests/report.png" />
