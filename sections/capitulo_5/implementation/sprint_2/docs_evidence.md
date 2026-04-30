Para este segundo sprint, el enfoque se centró exclusivamente en el desarrollo del frontend de la aplicación, utilizando una herramienta para la simulación de un backend.

Se realizó el despliegue de un JSON Server en la plataforma de Azure para simular los servicios de servidor y permitir el consumo de datos desde el frontend.

Link del JSON Server: [agrotrack-mockapi.azurewebsites.net](http://agrotrack-mockapi.azurewebsites.net)

**Endpoints de la API Simulada**

<table>
    <thead>
        <tr>
            <th><strong>Endpoint</strong></th>
            <th><strong>Descripción</strong></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><code>/users</code></td>
            <td>Gestión de usuarios (registro, autenticación, perfil).</td>
        </tr>
        <tr>
            <td><code>/organizations</code></td>
            <td>Gestión de organizaciones agrícolas.</td>
        </tr>
        <tr>
            <td><code>/plots</code></td>
            <td>Gestión de parcelas (creación, edición, eliminación).</td>
        </tr>
        <tr>
            <td><code>/tasks</code></td>
            <td>Gestión de tareas agrícolas (asignación, seguimiento, recordatorios).</td>
        </tr>
        <tr>
            <td><code>/reports</code></td>
            <td>Generación y visualización de reportes agrícolas.</td>
        </tr>
    </tbody>
</table>