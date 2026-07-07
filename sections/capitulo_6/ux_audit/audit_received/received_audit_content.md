Esta sección reproduce el informe de **UX Heuristics & Principles Evaluation** (Usability – Inclusive Design – Information Architecture) recibido del grupo auditor sobre EcoTrack, siguiendo el formato del Anexo D.

<table>
    <tbody>
        <tr>
            <td><strong>CARRERA</strong></td>
            <td>Ingeniería de Software</td>
        </tr>
        <tr>
            <td><strong>CURSO</strong></td>
            <td>Diseño de Experimentos de Ingeniería de Software</td>
        </tr>
        <tr>
            <td><strong>NRC</strong></td>
            <td>17820 <em>(consignado en el informe de auditoría)</em></td>
        </tr>
        <tr>
            <td><strong>PROFESOR</strong></td>
            <td>Julio Manuel Noriega Melendez</td>
        </tr>
        <tr>
            <td><strong>AUDITOR</strong> (grupo que ejecuta la sesión)</td>
            <td>AgroMind</td>
        </tr>
        <tr>
            <td><strong>CLIENTE(S)</strong> (personas que participan en la sesión)</td>
            <td>Chi Cruzatt, Kevin Jorge; Mostajo Orosco, Maria Fernanda; Orozco Torres, Alvaro Joaquin; Paucar De La Cruz, Tatiana Medalith; Ramos Aguirre, Aldair Joaquin; Reaño Delgadillo, Henry Paolo.</td>
        </tr>
    </tbody>
</table>

**SITE o APP A EVALUAR:**

<table>
    <tbody>
        <tr>
            <td><strong>Nombre de la App</strong></td>
            <td>EcoTrack</td>
        </tr>
        <tr>
            <td><strong>Enlace de despliegue evaluado</strong></td>
            <td>https://frontend-h0wa.onrender.com</td>
        </tr>
    </tbody>
</table>

**TAREAS A EVALUAR:**

El alcance de la evaluación incluyó las siguientes tareas:

1. **Autenticación y seguridad:** registro de usuarios con reglas de contraseña e inicio de sesión con control de accesos autorizados.
2. **Estructura organizacional y navegación:** gestión de organizaciones agrícolas en *My Organizations* y revisión de los menús base del dashboard.
3. **Control de roles y permisos en tareas:** verificación de las restricciones funcionales entre los roles **Farmer** y **Agronomist**.

No estuvieron incluidas en esta evaluación las siguientes tareas:

1. Conexión en tiempo real con sensores físicos de hardware IoT.
2. Pasarela de pagos para los planes AgroSmart y AgroExpert.

**ESCALA DE SEVERIDAD:**

<table>
    <thead>
        <tr>
            <th>Nivel</th>
            <th>Descripción</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>1</td>
            <td>Problema superficial que puede ser superado fácilmente por el usuario y no requiere corrección urgente.</td>
        </tr>
        <tr>
            <td>2</td>
            <td>Problema menor que genera confusión secundaria. Debe priorizarse para un siguiente release.</td>
        </tr>
        <tr>
            <td>3</td>
            <td>Problema mayor que afecta la comprensión del negocio o la eficiencia del flujo principal. Requiere prioridad alta.</td>
        </tr>
        <tr>
            <td>4</td>
            <td>Problema muy grave que bloquea el flujo o impide que el usuario complete la tarea de manera independiente.</td>
        </tr>
    </tbody>
</table>

**TABLA RESUMEN:**

<table>
    <thead>
        <tr>
            <th>#</th>
            <th>Problema</th>
            <th>Escala de severidad</th>
            <th>Heurística / Principio violado(a)</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>1</td>
            <td>La interfaz principal y los menús se muestran completamente en inglés.</td>
            <td>3</td>
            <td>Adecuación entre el sistema y el mundo real.</td>
        </tr>
        <tr>
            <td>2</td>
            <td>Se muestran datos de prueba predeterminados, como “decription” y “location”, en la tabla de organizaciones.</td>
            <td>2</td>
            <td>Estética y diseño minimalista.</td>
        </tr>
        <tr>
            <td>3</td>
            <td>No se presentan mensajes claros en pantalla ante errores 401 y 400; el error queda únicamente en la consola.</td>
            <td>3</td>
            <td>Ayuda a los usuarios a reconocer, diagnosticar y recuperarse de errores.</td>
        </tr>
        <tr>
            <td>4</td>
            <td>El registro no muestra de forma anticipada las restricciones de contraseña.</td>
            <td>2</td>
            <td>Prevención de errores.</td>
        </tr>
        <tr>
            <td>5</td>
            <td>El rol Agronomist visualiza acciones de tareas sin una indicación clara de que no cuenta con permiso para completarlas.</td>
            <td>3</td>
            <td>Flexibilidad y eficiencia de uso / Visibilidad del estado del sistema.</td>
        </tr>
        <tr>
            <td>6</td>
            <td>La eliminación de organizaciones usa un ícono genérico y no presenta una confirmación visible antes de borrar el registro.</td>
            <td>2</td>
            <td>Control y libertad del usuario / Prevención de errores.</td>
        </tr>
    </tbody>
</table>

**DESCRIPCIÓN DE PROBLEMAS Y RECOMENDACIONES:**

**PROBLEMA #1: Interfaz y menús en idioma inglés**

- **Severidad:** 3.
- **Heurística/Principio violado(a):** Adecuación entre el sistema y el mundo real.
- **Problema:** La interfaz, los menús laterales y los títulos principales están en inglés. Esta decisión representa una barrera cultural e idiomática para el público objetivo, compuesto principalmente por agricultores peruanos.
- **Recomendación:** Implementar internacionalización en el frontend y establecer el español como idioma predeterminado, utilizando términos sencillos del contexto agrícola, tales como “Mis Parcelas”, “Tareas” y “Clima”.
- **Evidencia visual:** Insertar captura del dashboard y menú lateral evaluados.

**PROBLEMA #2: Datos de prueba visibles en organizaciones**

- **Severidad:** 2.
- **Heurística/Principio violado(a):** Estética y diseño minimalista.
- **Problema:** La tabla de organizaciones muestra los valores predeterminados “decription” y “location” cuando no se ha registrado información para esos campos. Además de incluir un error ortográfico, estos textos reducen la percepción de calidad de la interfaz.
- **Recomendación:** Mostrar una celda vacía o etiquetas claras como “Sin descripción asignada” y “Organización sin ubicación” cuando la información no esté disponible.
- **Evidencia visual:** Insertar captura de la tabla de organizaciones evaluada.

**PROBLEMA #3: Errores de autenticación y registro sin retroalimentación visible**

- **Severidad:** 3.
- **Heurística/Principio violado(a):** Ayuda a los usuarios a reconocer, diagnosticar y recuperarse de errores.
- **Problema:** Ante credenciales inválidas (401) o registros fallidos (400), el backend responde correctamente, pero el frontend no muestra un mensaje comprensible para el usuario. El error se registra en consola y puede percibirse como un fallo general de la plataforma.
- **Recomendación:** Implementar manejo centralizado de errores en el cliente HTTP para convertir los códigos 401 y 400 en mensajes emergentes, por ejemplo: “Usuario o contraseña incorrectos” o “Los datos ingresados no son válidos”.
- **Evidencia visual:** Insertar captura del flujo de inicio de sesión o registro con el mensaje de error correspondiente.

**PROBLEMA #4: Restricciones de contraseña no visibles antes del registro**

- **Severidad:** 2.
- **Heurística/Principio violado(a):** Prevención de errores.
- **Problema:** El sistema bloquea correctamente las contraseñas que no cumplen los criterios de seguridad, pero no informa de manera anticipada los requisitos de longitud, mayúsculas y símbolos. Esto obliga al usuario a realizar intentos sucesivos.
- **Recomendación:** Incluir texto de ayuda dinámico o una lista de verificación visual debajo del campo de contraseña, que indique el cumplimiento progresivo de cada requisito.
- **Evidencia visual:** Insertar captura del formulario de creación de cuenta.

**PROBLEMA #5: Restricciones del rol Agronomist poco visibles en tareas**

- **Severidad:** 3.
- **Heurística/Principio violado(a):** Flexibilidad y eficiencia de uso / Visibilidad del estado del sistema.
- **Problema:** El rol Agronomist no puede completar tareas, pero la interfaz continúa mostrando acciones activas sin explicar la restricción. Esto puede provocar intentos fallidos y frustración.
- **Recomendación:** Aplicar renderizado condicional según el rol. Para Agronomist, la acción de completar tarea debe ocultarse o mostrarse deshabilitada con un tooltip como “Permiso exclusivo para agricultores”.
- **Evidencia visual:** Insertar captura de una tarea visualizada con cuenta Agronomist.

**PROBLEMA #6: Eliminación de organizaciones sin confirmación intermedia**

- **Severidad:** 2.
- **Heurística/Principio violado(a):** Control y libertad del usuario / Prevención de errores.
- **Problema:** El botón de eliminación se representa mediante un ícono de papelera y permite iniciar un borrado sin una confirmación intermedia visible en la pantalla primaria.
- **Recomendación:** Incorporar un modal de confirmación antes de eliminar una organización, indicando que la acción no puede deshacerse.
- **Evidencia visual:** Insertar captura del botón de eliminación y del modal de confirmación.

<div style="page-break-after: always;"></div>

#### 6.4.2.4. Resumen de modificaciones para subsanar hallazgos

El informe recibido contiene recomendaciones, pero no incluye evidencia de que las correcciones ya hayan sido implementadas. Por ello, las siguientes acciones deben registrarse como modificaciones pendientes de implementación o verificación, incorporando el commit y la captura correspondiente cuando se complete cada cambio.

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