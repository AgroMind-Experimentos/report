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
            <td><strong>Auth – Register</strong></td>
            <td>POST</td>
            <td>Body: <code>{ email, password, fullName }</code></td>
            <td>/auth/register</td>
            <td>201 Created – Usuario registrado, retorna usuario + token</td>
        </tr>
        <tr>
            <td><strong>Auth – Login</strong></td>
            <td>POST</td>
            <td>Body: <code>{ email, password }</code></td>
            <td>/auth/login</td>
            <td>200 OK – Retorna token JWT + datos del usuario</td>
        </tr>
        <tr>
            <td><strong>Auth – Logout</strong></td>
            <td>POST</td>
            <td>Header: <code>Authorization: Bearer token</code></td>
            <td>/auth/logout</td>
            <td>200 OK – Sesión cerrada correctamente</td>
        </tr>
        <tr>
            <td><strong>Crops – Crear cultivo</strong></td>
            <td>POST</td>
            <td>Body: <code>{ name, type, organizationId, ... }</code></td>
            <td>/api/v1/crops</td>
            <td>201 Created – Cultivo registrado</td>
        </tr>
        <tr>
            <td><strong>Crops – Listar cultivos</strong></td>
            <td>GET</td>
            <td>Ninguno</td>
            <td>/api/v1/crops</td>
            <td>200 OK – Lista de cultivos</td>
        </tr>
        <tr>
            <td><strong>Crops – Obtener cultivo por ID</strong></td>
            <td>GET</td>
            <td>Path: <code>{id}</code></td>
            <td>/api/v1/crops/{id}</td>
            <td>200 OK – Detalles del cultivo</td>
        </tr>
        <tr>
            <td><strong>Crops – Cultivos por organización</strong></td>
            <td>GET</td>
            <td>Path: <code>{organizationId}</code></td>
            <td>/api/v1/crops/organization/{organizationId}</td>
            <td>200 OK – Lista de cultivos filtrados</td>
        </tr>
        <tr>
            <td><strong>Organizations – Crear organización</strong></td>
            <td>POST</td>
            <td>Body: <code>{ name, address, ownerId }</code></td>
            <td>/api/v1/organizations</td>
            <td>201 Created – Organización registrada</td>
        </tr>
        <tr>
            <td><strong>Organizations – Listar organizaciones</strong></td>
            <td>GET</td>
            <td>Ninguno</td>
            <td>/api/v1/organizations</td>
            <td>200 OK – Lista de organizaciones</td>
        </tr>
        <tr>
            <td><strong>Organizations – Obtener organización por ID</strong></td>
            <td>GET</td>
            <td>Path: <code>{id}</code></td>
            <td>/api/v1/organizations/{id}</td>
            <td>200 OK – Datos de la organización</td>
        </tr>
    </tbody>
</table>