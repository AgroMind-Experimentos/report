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
            <td>17820</td>
        </tr>
        <tr>
            <td><strong>PROFESORES</strong></td>
            <td>Julio Manuel Noriega Melendez</td>
        </tr>
        <tr>
            <td><strong>AUDITOR</strong> (grupo que ejecuta la sesión)</td>
            <td>Vivienda360 (Rogger Faryd, Rafael Vivanco, Raúl Tasayco, Rafael Tasayco)</td>
        </tr>
        <tr>
            <td><strong>CLIENTE(S)</strong> (personas que participan en la sesión)</td>
            <td>Chi Cruzatt, Kevin Jorge; Mostajo Orosco, Maria Fernanda; Orozco Torres, Alvaro Joaquin; Paucar De La Cruz, Tatiana Medalith; Ramos Aguirre, Aldair Joaquin; Reaño Delgadillo, Henry Paolo</td>
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
    </tbody>
</table>

**TAREAS A EVALUAR:**

El alcance de esta evaluación incluye la revisión de la usabilidad de las siguientes tareas:

1. Autenticación y Seguridad: registro de nuevos usuarios con reglas estrictas de contraseñas, e inicio de sesión con manejo de accesos autorizados.
2. Estructura Organizacional y Navegación: gestión de organizaciones agrícolas (My Organizations) y visualización de menús base en el dashboard general.
3. Control de Roles y Permisos en Tareas: verificación de las restricciones funcionales entre cuentas de tipo Farmer (Agricultor) y Agronomist (Agrónomo).

No están incluidas en esta versión de la evaluación las siguientes tareas:

1. Conexión en tiempo real con sensores físicos de hardware IoT.
2. Pasarela de pagos para planes avanzados (AgroSmart / AgroExpert).

**ESCALA DE SEVERIDAD:**

Los errores serán puntuados tomando en cuenta la siguiente escala de severidad:

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
            <td>Problema superficial: puede ser fácilmente superado por el usuario. No necesita ser arreglado con urgencia.</td>
        </tr>
        <tr>
            <td>2</td>
            <td>Problema menor: ocurre de forma secundaria o es sutilmente confuso. Asignar prioridad baja para el siguiente release.</td>
        </tr>
        <tr>
            <td>3</td>
            <td>Problema mayor: afecta directamente la comprensión del negocio o la eficiencia del flujo principal. Prioridad alta.</td>
        </tr>
        <tr>
            <td>4</td>
            <td>Problema muy grave: bloquea, confunde críticamente o impide al usuario completar su flujo de forma independiente. El lanzamiento no debe darse sin corregirlo.</td>
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
            <td>Interfaz principal y menús desarrollados completamente en idioma inglés.</td>
            <td>3</td>
            <td>Adecuación entre el sistema y el mundo real</td>
        </tr>
        <tr>
            <td>2</td>
            <td>Presencia de datos de prueba predeterminados ("decription", "location") legibles en producción.</td>
            <td>2</td>
            <td>Estética y diseño minimalista</td>
        </tr>
        <tr>
            <td>3</td>
            <td>Falta de mensajes de error explícitos en pantalla ante fallos de red 401/400 (errores silenciosos en consola).</td>
            <td>3</td>
            <td>Ayuda a los usuarios a reconocer y recuperarse de errores</td>
        </tr>
        <tr>
            <td>4</td>
            <td>Ausencia de indicadores visuales informativos sobre las restricciones de contraseña durante el registro.</td>
            <td>2</td>
            <td>Prevención de errores</td>
        </tr>
        <tr>
            <td>5</td>
            <td>Falta de feedback visual o estados inactivos (disabled) en tareas para el rol de Agronomist.</td>
            <td>3</td>
            <td>Flexibilidad y eficiencia de uso / Visibilidad del estado</td>
        </tr>
        <tr>
            <td>6</td>
            <td>Uso de iconos genéricos y falta de etiquetas de confirmación en la acción de borrado.</td>
            <td>2</td>
            <td>Prevención de errores / Control y libertad del usuario</td>
        </tr>
    </tbody>
</table>

**DESCRIPCIÓN DE PROBLEMAS:**

**PROBLEMA #1:**

- **Severidad:** 3
- **Heurística/Principio violado(a):** Adecuación entre el sistema y el mundo real.
- **Problema:** Al inspeccionar el panel principal se constata que toda la interfaz, los menús laterales (Home, Tasks, Weather, Reports, Profile, Settings) y los títulos (My Organizations, Create New Organization) se encuentran en idioma inglés. Dado que el público objetivo principal del proyecto son los agricultores peruanos, el uso del inglés representa una barrera cultural e idiomática severa que afectará negativamente la adopción del sistema.
- **Recomendación:** Implementar la internacionalización (i18n) en el frontend para asegurar que el idioma nativo por defecto sea el español, utilizando términos sencillos del entorno agrícola ("Mis Parcelas", "Tareas", "Clima").

**PROBLEMA #2:**

- **Severidad:** 2
- **Heurística/Principio violado(a):** Estética y diseño minimalista.
- **Problema:** En la tabla de organizaciones creada, los campos correspondientes a la columna Description muestran el texto "decription" (con un error ortográfico en inglés) y la columna Location muestra "location". Esto denota que el sistema está renderizando los valores por defecto que se envían desde la base de datos o el backend cuando el usuario no completa la información.
- **Recomendación:** Modificar el componente de la tabla para que, en caso de campos vacíos o por defecto, muestre un espacio limpio o una leyenda elegante como "Sin descripción asignada" u "Organización sin ubicación".

**PROBLEMA #3:**

- **Severidad:** 3
- **Heurística/Principio violado(a):** Ayuda a los usuarios a reconocer, diagnosticar y recuperarse de errores.
- **Problema:** Los logs de la consola demuestran que ante credenciales inválidas (Error 401 Unauthorized) o registros fallidos (Error 400 Bad Request), el backend responde correctamente, pero el frontend no está capturando de manera clara el mensaje para mostrar una alerta amigable en la interfaz gráfica. Si el sistema falla de manera silenciosa para el usuario común, este asumirá que la aplicación no funciona.
- **Recomendación:** Implementar un interceptor de errores en el cliente HTTP del frontend (ej. Axios o Fetch) para capturar los códigos de estado 401 y 400, transformándolos en mensajes emergentes (Toasts o Modales) como "Usuario o contraseña incorrectos" o "Los datos ingresados no son válidos".

**PROBLEMA #4:**

- **Severidad:** 2
- **Heurística/Principio violado(a):** Prevención de errores.
- **Problema:** El sistema bloquea correctamente el registro si la contraseña no cumple con los criterios de seguridad avanzados (mínimo 8 dígitos, mayúsculas y un símbolo). Sin embargo, el formulario no advierte explícitamente estas condiciones al usuario de manera anticipada, obligándolo a adivinar la estructura mediante un proceso de "ensayo y error".
- **Recomendación:** Añadir un texto de ayuda dinámico debajo del campo de contraseña o una lista de verificación visual que cambie a color verde a medida que el usuario cumpla con cada uno de los requisitos técnicos de seguridad exigidos por el backend.

**PROBLEMA #5:**

- **Severidad:** 3
- **Heurística/Principio violado(a):** Flexibilidad y eficiencia de uso / Visibilidad del estado del sistema.
- **Problema:** Por diseño del negocio, los usuarios con rol de Agronomist no pueden completar tareas (facultad exclusiva del rol Farmer). No obstante, si un agrónomo inicia sesión, la interfaz le sigue mostrando las opciones de interacción de las tareas activas sin distinguir visualmente que no posee permisos de edición para completarlas, lo que provoca clics inútiles y frustración.
- **Recomendación:** Aplicar un renderizado condicional en la interfaz basado en los claims del token de usuario. Si el usuario logueado es un Agronomist, el botón o casilla para "Completar Tarea" debe ocultarse por completo o aparecer opaco (en estado disabled) acompañado de un tooltip que aclare: "Permiso exclusivo para agricultores".

**PROBLEMA #6:**

- **Severidad:** 2
- **Heurística/Principio violado(a):** Control y libertad del usuario / Prevención de errores.
- **Problema:** En la columna Actions del panel organizacional, aparece un botón rojo con un icono de papelera para eliminar registros. Si el usuario presiona este botón por accidente, el registro se expone a un borrado inmediato sin intermediarios directos visibles en la pantalla primaria.
- **Recomendación:** Asegurar que el botón de eliminación gatille siempre un cuadro de diálogo de confirmación intermedia (Modal) preguntando al usuario: "¿Está seguro de que desea eliminar esta organización? Esta acción no se puede deshacer", previniendo pérdidas accidentales de datos en el entorno agrícola.
