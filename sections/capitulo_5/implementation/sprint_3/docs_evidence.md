<table>
  <thead>
    <tr>
      <th>Endpoint</th>
      <th>Operaciones</th>
      <th>Parámetros</th>
      <th>URL</th>
      <th>Response</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Auth</td>
      <td>POST</td>
      <td>No tiene</td>
      <td>/auth/login</td>
      <td>Inicia sesión y retorna token</td>
    </tr>
    <tr>
      <td>Auth</td>
      <td>POST</td>
      <td>No tiene</td>
      <td>/auth/logout</td>
      <td>Cierra sesión del usuario actual</td>
    </tr>
    <tr>
      <td>Checklists</td>
      <td>POST</td>
      <td>No tiene</td>
      <td>/api/checklists</td>
      <td>Crea un nuevo checklist</td>
    </tr>
    <tr>
      <td>Checklists</td>
      <td>GET</td>
      <td>taskId</td>
      <td>/api/checklists</td>
      <td>Obtiene checklists por Task Id</td>
    </tr>
    <tr>
      <td>Config</td>
      <td>GET</td>
      <td>No tiene</td>
      <td>/config/public</td>
      <td>Obtiene configuración pública para el front</td>
    </tr>
    <tr>
      <td>Logbooks</td>
      <td>POST</td>
      <td>No tiene</td>
      <td>/api/logbooks</td>
      <td>Crea un nuevo logbook</td>
    </tr>
    <tr>
      <td>Logbooks</td>
      <td>GET</td>
      <td>No tiene</td>
      <td>/api/logbooks</td>
      <td>Obtiene todos los logbooks</td>
    </tr>
    <tr>
      <td>Logbooks</td>
      <td>GET</td>
      <td>{logbookId}</td>
      <td>/api/logbooks/{logbookId}</td>
      <td>Obtiene un logbook por id</td>
    </tr>
    <tr>
      <td>Users</td>
      <td>GET</td>
      <td>No tiene</td>
      <td>/users</td>
      <td>Lista todos los usuarios</td>
    </tr>
    <tr>
      <td>Users</td>
      <td>POST</td>
      <td>No tiene</td>
      <td>/users</td>
      <td>Crea un nuevo usuario</td>
    </tr>
    <tr>
      <td>Users</td>
      <td>GET</td>
      <td>{id}</td>
      <td>/users/{id}</td>
      <td>Obtiene un usuario por id</td>
    </tr>
    <tr>
      <td>Users</td>
      <td>PATCH</td>
      <td>{id}</td>
      <td>/users/{id}</td>
      <td>Actualiza un usuario</td>
    </tr>
    <tr>
      <td>Users</td>
      <td>DELETE</td>
      <td>{id}</td>
      <td>/users/{id}</td>
      <td>Elimina un usuario</td>
    </tr>
    <tr>
      <td>Users</td>
      <td>GET</td>
      <td>No tiene</td>
      <td>/users/me</td>
      <td>Obtiene el usuario actual (requiere sesión)</td>
    </tr>
    <tr>
      <td>Reports</td>
      <td>POST</td>
      <td>No tiene</td>
      <td>/api/reports/tasks</td>
      <td>Solicita un nuevo reporte de tareas</td>
    </tr>
    <tr>
      <td>Reports</td>
      <td>POST</td>
      <td>{reportId}</td>
      <td>/api/reports/{reportId}/generate</td>
      <td>Genera el contenido de un reporte</td>
    </tr>
    <tr>
      <td>Reports</td>
      <td>GET</td>
      <td>{reportId}</td>
      <td>/api/reports/{reportId}</td>
      <td>Obtiene un reporte por id</td>
    </tr>
    <tr>
      <td>Reports</td>
      <td>GET</td>
      <td>{profileId}</td>
      <td>/api/reports/profile/{profileId}</td>
      <td>Obtiene todos los reportes de un perfil</td>
    </tr>
    <tr>
      <td>Settings</td>
      <td>GET</td>
      <td>No tiene</td>
      <td>/settings</td>
      <td>Obtiene ajustes del usuario actual</td>
    </tr>
    <tr>
      <td>Settings</td>
      <td>PATCH</td>
      <td>No tiene</td>
      <td>/settings</td>
      <td>Actualiza los ajustes del usuario actual</td>
    </tr>
    <tr>
      <td>Settings</td>
      <td>POST</td>
      <td>No tiene</td>
      <td>/settings/password</td>
      <td>Cambia la contraseña del usuario</td>
    </tr>
    <tr>
      <td>Tasks</td>
      <td>POST</td>
      <td>No tiene</td>
      <td>/api/tasks</td>
      <td>Crea una nueva tarea</td>
    </tr>
    <tr>
      <td>Tasks</td>
      <td>GET</td>
      <td>status</td>
      <td>/api/tasks</td>
      <td>Obtiene tareas por estado</td>
    </tr>
    <tr>
      <td>Tasks</td>
      <td>PATCH</td>
      <td>{taskId}</td>
      <td>/api/tasks/{taskId}/status</td>
      <td>Actualiza el estado de una tarea</td>
    </tr>
    <tr>
      <td>Tasks</td>
      <td>GET</td>
      <td>{taskId}</td>
      <td>/api/tasks/{taskId}</td>
      <td>Obtiene una tarea por id</td>
    </tr>
  </tbody>
</table>