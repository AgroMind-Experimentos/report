La documentación completa de la RESTful API es accesible a través de swagger en el siguiente enlace:

- [Swagger UI – EcoTrack API](https://backend-production-fc468.up.railway.app/swagger/index.html)

<table>
    <thead>
        <tr>
            <th>Endpoint</th>
            <th>Operación</th>
            <th>Parámetros</th>
            <th>URL</th>
            <th>Response</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><strong>Auth – Register</strong></td>
            <td>POST</td>
            <td>Body: <code>RegisterResource</code></td>
            <td>/api/v1/auth/register</td>
            <td>200 OK</td>
        </tr>
        <tr>
            <td><strong>Auth – Login</strong></td>
            <td>POST</td>
            <td>Body: <code>LoginResource</code></td>
            <td>/api/v1/auth/login</td>
            <td>200 OK</td>
        </tr>
        <tr>
            <td><strong>Auth – Logout</strong></td>
            <td>POST</td>
            <td>Ninguno</td>
            <td>/api/v1/auth/logout</td>
            <td>200 OK</td>
        </tr>
        <tr>
            <td><strong>Auth – Cambiar contraseña del usuario actual</strong></td>
            <td>POST</td>
            <td>Body: <code>ChangePasswordResource</code></td>
            <td>/api/v1/auth/password</td>
            <td>200 OK</td>
        </tr>
        <tr>
            <td><strong>Checklists – Create a new Checklist</strong></td>
            <td>POST</td>
            <td>Body: <code>CreateChecklistRequest</code></td>
            <td>/api/v1/checklists</td>
            <td>200 OK</td>
        </tr>
        <tr>
            <td><strong>Checklists – Get checklists by Task Id</strong></td>
            <td>GET</td>
            <td>Query: <code>taskId</code></td>
            <td>/api/v1/checklists</td>
            <td>200 OK</td>
        </tr>
        <tr>
            <td><strong>Checklists – Mark or unmark a checklist item as completed</strong></td>
            <td>PATCH</td>
            <td>Path: <code>itemId</code><br>Body: <code>UpdateChecklistItemRequest</code></td>
            <td>/api/v1/checklists/items/{itemId}</td>
            <td>200 OK</td>
        </tr>
        <tr>
            <td><strong>Checklists – Update checklist items</strong></td>
            <td>PUT</td>
            <td>Path: <code>id</code><br>Body: <code>UpdateChecklistRequest</code></td>
            <td>/api/v1/checklists/{id}</td>
            <td>200 OK</td>
        </tr>
        <tr>
            <td><strong>Config – Obtener configuración pública para el front</strong></td>
            <td>GET</td>
            <td>Ninguno</td>
            <td>/api/v1/config</td>
            <td>200 OK</td>
        </tr>
        <tr>
            <td><strong>Invitations – Invite</strong></td>
            <td>POST</td>
            <td>Path: <code>orgId</code><br>Body: <code>InviteByEmailResource</code></td>
            <td>/api/v1/organizations/{orgId}/invite</td>
            <td>200 OK</td>
        </tr>
        <tr>
            <td><strong>Invitations – Invitations</strong></td>
            <td>GET</td>
            <td>Query: <code>profileId</code></td>
            <td>/api/v1/invitations</td>
            <td>200 OK</td>
        </tr>
        <tr>
            <td><strong>Invitations – Accept</strong></td>
            <td>POST</td>
            <td>Path: <code>id</code><br>Body: <code>RespondInvitationResource</code></td>
            <td>/api/v1/invitations/{id}/accept</td>
            <td>200 OK</td>
        </tr>
        <tr>
            <td><strong>Invitations – Reject</strong></td>
            <td>POST</td>
            <td>Path: <code>id</code><br>Body: <code>RespondInvitationResource</code></td>
            <td>/api/v1/invitations/{id}/reject</td>
            <td>200 OK</td>
        </tr>
        <tr>
            <td><strong>Logbooks – Creates a new logbook</strong></td>
            <td>POST</td>
            <td>Body: <code>CreateLogbookRequest</code></td>
            <td>/api/v1/logbooks</td>
            <td>200 OK</td>
        </tr>
        <tr>
            <td><strong>Logbooks – Get all logbooks</strong></td>
            <td>GET</td>
            <td>Ninguno</td>
            <td>/api/v1/logbooks</td>
            <td>200 OK</td>
        </tr>
        <tr>
            <td><strong>Logbooks – Get logbook by id</strong></td>
            <td>GET</td>
            <td>Path: <code>logbookId</code></td>
            <td>/api/v1/logbooks/{logbookId}</td>
            <td>200 OK</td>
        </tr>
        <tr>
            <td><strong>Organizations – Organizations</strong></td>
            <td>POST</td>
            <td>Body: <code>CreateOrganizationResource</code></td>
            <td>/api/v1/organizations</td>
            <td>200 OK</td>
        </tr>
        <tr>
            <td><strong>Organizations – Organizations</strong></td>
            <td>GET</td>
            <td>Query: <code>profileId</code></td>
            <td>/api/v1/organizations</td>
            <td>200 OK</td>
        </tr>
        <tr>
            <td><strong>Organizations – {id}</strong></td>
            <td>PATCH</td>
            <td>Path: <code>id</code><br>Body: <code>UpdateOrganizationResource</code></td>
            <td>/api/v1/organizations/{id}</td>
            <td>200 OK</td>
        </tr>
        <tr>
            <td><strong>Organizations – {id}</strong></td>
            <td>GET</td>
            <td>Path: <code>id</code></td>
            <td>/api/v1/organizations/{id}</td>
            <td>200 OK</td>
        </tr>
        <tr>
            <td><strong>Organizations – {id}</strong></td>
            <td>DELETE</td>
            <td>Path: <code>id</code></td>
            <td>/api/v1/organizations/{id}</td>
            <td>200 OK</td>
        </tr>
        <tr>
            <td><strong>Plots – Plots</strong></td>
            <td>POST</td>
            <td>Body: <code>CreatePlotResource</code></td>
            <td>/api/v1/plots</td>
            <td>200 OK</td>
        </tr>
        <tr>
            <td><strong>Plots – Plots</strong></td>
            <td>GET</td>
            <td>Ninguno</td>
            <td>/api/v1/plots</td>
            <td>200 OK</td>
        </tr>
        <tr>
            <td><strong>Plots – {id}</strong></td>
            <td>PATCH</td>
            <td>Path: <code>id</code><br>Body: <code>UpdatePlotResource</code></td>
            <td>/api/v1/plots/{id}</td>
            <td>200 OK</td>
        </tr>
        <tr>
            <td><strong>Plots – {id}</strong></td>
            <td>GET</td>
            <td>Path: <code>id</code></td>
            <td>/api/v1/plots/{id}</td>
            <td>200 OK</td>
        </tr>
        <tr>
            <td><strong>Plots – {id}</strong></td>
            <td>DELETE</td>
            <td>Path: <code>id</code></td>
            <td>/api/v1/plots/{id}</td>
            <td>200 OK</td>
        </tr>
        <tr>
            <td><strong>Plots – {organizationid}</strong></td>
            <td>GET</td>
            <td>Path: <code>organizationId</code></td>
            <td>/api/v1/plots/organization/{organizationId}</td>
            <td>200 OK</td>
        </tr>
        <tr>
            <td><strong>Profiles – Listar todos los usuarios, opcionalmente filtrados por rol</strong></td>
            <td>GET</td>
            <td>Query: <code>role</code></td>
            <td>/api/v1/profiles</td>
            <td>200 OK</td>
        </tr>
        <tr>
            <td><strong>Profiles – Crear un nuevo usuario</strong></td>
            <td>POST</td>
            <td>Body: <code>CreateProfileResource</code></td>
            <td>/api/v1/profiles</td>
            <td>200 OK</td>
        </tr>
        <tr>
            <td><strong>Profiles – Obtener un usuario por id</strong></td>
            <td>GET</td>
            <td>Path: <code>id</code></td>
            <td>/api/v1/profiles/{id}</td>
            <td>200 OK</td>
        </tr>
        <tr>
            <td><strong>Profiles – Actualizar un usuario</strong></td>
            <td>PATCH</td>
            <td>Path: <code>id</code><br>Body: <code>UpdateProfileResource</code></td>
            <td>/api/v1/profiles/{id}</td>
            <td>200 OK</td>
        </tr>
        <tr>
            <td><strong>Profiles – Eliminar un usuario</strong></td>
            <td>DELETE</td>
            <td>Path: <code>id</code></td>
            <td>/api/v1/profiles/{id}</td>
            <td>200 OK</td>
        </tr>
        <tr>
            <td><strong>Profiles – Obtener el usuario actual (requiere sesión)</strong></td>
            <td>GET</td>
            <td>Ninguno</td>
            <td>/api/v1/profiles/me</td>
            <td>200 OK</td>
        </tr>
        <tr>
            <td><strong>Reports – Generar reporte del estado de todas las tareas (JSON)</strong></td>
            <td>GET</td>
            <td>Query: <code>organizationId</code></td>
            <td>/api/v1/reports</td>
            <td>200 Reporte generado exitosamente</td>
        </tr>
        <tr>
            <td><strong>Reports – Generar reporte del estado de todas las tareas (PDF)</strong></td>
            <td>GET</td>
            <td>Query: <code>organizationId</code></td>
            <td>/api/v1/reports/pdf</td>
            <td>200 Reporte PDF generado exitosamente</td>
        </tr>
        <tr>
            <td><strong>Settings – Obtener settings del usuario actual</strong></td>
            <td>GET</td>
            <td>Ninguno</td>
            <td>/api/v1/settings</td>
            <td>200 OK</td>
        </tr>
        <tr>
            <td><strong>Settings – Actualizar settings del usuario actual</strong></td>
            <td>PATCH</td>
            <td>Body: <code>SettingsResource</code></td>
            <td>/api/v1/settings</td>
            <td>200 OK</td>
        </tr>
        <tr>
            <td><strong>Tasks – Create a new task</strong></td>
            <td>POST</td>
            <td>Body: <code>CreateTaskRequest</code></td>
            <td>/api/v1/tasks</td>
            <td>200 OK</td>
        </tr>
        <tr>
            <td><strong>Tasks – Get tasks filtered by status, organizationId or responsibleId</strong></td>
            <td>GET</td>
            <td>Query: <code>status</code><br>Query: <code>organizationId</code><br>Query: <code>responsibleId</code></td>
            <td>/api/v1/tasks</td>
            <td>200 OK</td>
        </tr>
        <tr>
            <td><strong>Tasks – Update a task's status</strong></td>
            <td>PATCH</td>
            <td>Path: <code>taskId</code><br>Body: <code>UpdateStatusRequest</code></td>
            <td>/api/v1/tasks/{taskId}/status</td>
            <td>200 OK</td>
        </tr>
        <tr>
            <td><strong>Tasks – Get task by id</strong></td>
            <td>GET</td>
            <td>Path: <code>taskId</code></td>
            <td>/api/v1/tasks/{taskId}</td>
            <td>200 OK</td>
        </tr>
        <tr>
            <td><strong>Tasks – Update task title and description</strong></td>
            <td>PUT</td>
            <td>Path: <code>taskId</code><br>Body: <code>UpdateTaskRequest</code></td>
            <td>/api/v1/tasks/{taskId}</td>
            <td>200 OK</td>
        </tr>
        <tr>
            <td><strong>Tasks – Delete a task by id</strong></td>
            <td>DELETE</td>
            <td>Path: <code>taskId</code></td>
            <td>/api/v1/tasks/{taskId}</td>
            <td>200 OK</td>
        </tr>
    </tbody>
</table>
