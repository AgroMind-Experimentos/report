Esta sección resume las modificaciones realizadas sobre EcoTrack para atender los hallazgos reportados por el grupo auditor.

<table>
    <thead>
        <tr>
            <th>#</th>
            <th>Hallazgo / Problema reportado</th>
            <th>Severidad</th>
            <th>Modificación a implementar o verificar</th>
            <th>Evidencia (commit / pantalla)</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>1</td>
            <td>Interfaz principal y menús en inglés.</td>
            <td>3</td>
            <td>Incorporar internacionalización y establecer español como idioma predeterminado. Traducir menús, títulos, botones, mensajes y etiquetas con vocabulario agrícola sencillo.</td>
            <td>Pendiente: commit de i18n y captura del dashboard en español.</td>
        </tr>
        <tr>
            <td>2</td>
            <td>Valores de prueba visibles en campos de descripción y ubicación.</td>
            <td>2</td>
            <td>Eliminar valores por defecto de prueba y aplicar textos alternativos cuando los campos estén vacíos, por ejemplo “Sin descripción asignada” y “Sin ubicación registrada”.</td>
            <td>Pendiente: commit del componente de organizaciones y captura de la tabla corregida.</td>
        </tr>
        <tr>
            <td>3</td>
            <td>Errores 401 y 400 sin mensaje visible para el usuario.</td>
            <td>3</td>
            <td>Implementar manejo centralizado de errores en el cliente HTTP y mostrar mensajes amigables mediante toast, alerta o modal para errores de autenticación y validación.</td>
            <td>Pendiente: commit del interceptor o servicio HTTP y capturas de los mensajes 401/400.</td>
        </tr>
        <tr>
            <td>4</td>
            <td>Requisitos de contraseña no visibles antes de enviar el formulario.</td>
            <td>2</td>
            <td>Agregar ayuda contextual y lista de verificación dinámica para longitud mínima, mayúscula y símbolo requerido.</td>
            <td>Pendiente: commit del formulario de registro y captura del checklist de contraseña.</td>
        </tr>
        <tr>
            <td>5</td>
            <td>Acciones de tareas sin restricción visual para el rol Agronomist.</td>
            <td>3</td>
            <td>Aplicar renderizado condicional por rol para ocultar o deshabilitar la acción “Completar tarea” e informar el motivo mediante tooltip o mensaje contextual.</td>
            <td>Pendiente: commit de control de permisos y captura de tarea desde una cuenta Agronomist.</td>
        </tr>
        <tr>
            <td>6</td>
            <td>Eliminación de organizaciones sin confirmación explícita.</td>
            <td>2</td>
            <td>Agregar modal de confirmación con opciones de cancelar y confirmar antes de ejecutar la eliminación.</td>
            <td>Pendiente: commit del modal de eliminación y captura del diálogo de confirmación.</td>
        </tr>
    </tbody>
</table>