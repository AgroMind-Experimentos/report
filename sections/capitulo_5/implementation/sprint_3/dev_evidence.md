**Avances en la Implementación del Back-End**

En esta sección se presentan los avances del desarrollo del Back-End de la solución Ecotrack, completando la lógica interna del sistema. Se consolidó la arquitectura utilizando Clean Architecture y Domain Driven Design, configurando la infraestructura base, el acceso a datos, la documentación con Swagger y la estructura de servicios e interfaces. Además, se implementaron los módulos principales del dominio, incluyendo la gestión de tareas y checklists, la gestión de bitácoras, al igual que la gestión de parcelas y usuarios, habilitando endpoints funcionales y estables para su integración con el Front-End. Estos avances fortalecen la mantenibilidad del proyecto y dejan el Back-End en un estado completo para las siguientes etapas del desarrollo.

A continuación, se detallan los commits realizados en el repositorio vinculado a la implementación del servidor:

<table>
    <thead>
        <tr>
            <th><strong>Repositorio</strong></th>
            <th><strong>Rama</strong></th>
            <th><strong>ID de Commit</strong></th>
            <th><strong>Mensaje de Commit</strong></th>
            <th><strong>Descripción del Commit</strong></th>
            <th><strong>Fecha de Commit</strong></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>ecotrack-backend</td>
            <td>feature/user-management</td>
            <td>48912f6</td>
            <td>feat(profile): add profile, configuration, iam</td>
            <td>-</td>
            <td>13/11/2025</td>
        </tr>
        <tr>
            <td>ecotrack-backend</td>
            <td>feature/user-management</td>
            <td>aee4ce8</td>
            <td>feat(database): update connection strings to use environment variables</td>
            <td>-</td>
            <td>13/11/2025</td>
        </tr>
        <tr>
            <td>ecotrack-backend</td>
            <td>feature/task-management</td>
            <td>f7eb91b</td>
            <td>feat(monitoringandcontrol): add tasks and checklists management</td>
            <td>-</td>
            <td>13/11/2025</td>
        </tr>
        <tr>
            <td>ecotrack-backend</td>
            <td>feature/task-management</td>
            <td>5a3a7f7</td>
            <td>feat: add logbooks and improve code</td>
            <td>-</td>
            <td>13/11/2025</td>
        </tr>
        <tr>
            <td>ecotrack-backend</td>
            <td>feature/initial-structure</td>
            <td>6a9d0e6</td>
            <td>feat(shared): add IEvent interface and configure dependency injection for shared context and Cortex mediator</td>
            <td>-</td>
            <td>12/11/2025</td>
        </tr>
        <tr>
            <td>ecotrack-backend</td>
            <td>feature/initial-structure</td>
            <td>bfb42fd</td>
            <td>build: add database connection settings and update package references</td>
            <td>-</td>
            <td>22/10/2025</td>
        </tr>
        <tr>
            <td>ecotrack-backend</td>
            <td>feature/initial-structure</td>
            <td>72e6b2a</td>
            <td>feat(shared): implement AppDbContext and repository pattern with snake_case naming convention</td>
            <td>-</td>
            <td>22/10/2025</td>
        </tr>
    </tbody>
</table>