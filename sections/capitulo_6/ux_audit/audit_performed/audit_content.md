Esta sección aplica el formato de **UX Heuristics & Principles Evaluation** (Usability – Inclusive Design – Information Architecture) indicado en el Anexo D, para registrar la evaluación heurística realizada por el equipo sobre el producto del grupo auditado.

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
            <td><strong>AUDITOR</strong></td>
            <td>Agromind</td>
        </tr>
        <tr>
            <td><strong>CLIENTE(S)</strong> (personas que participan en la sesión)</td>
            <td>Cacho Seminario, Diego Alonso<br>Ruiz Huisa, Daniel Elias<br>Palacin Lazo, Gerardo Valentin<br>Villugas Jeronimo, Liam Anderson</td>
        </tr>
    </tbody>
</table>

**SITE o APP A EVALUAR:**

<table>
    <tbody>
        <tr>
            <td><strong>Nombre de la App</strong></td>
            <td>SafeWork</td>
        </tr>
    </tbody>
</table>

**TAREAS A EVALUAR:**

El alcance de esta evaluación incluye la revisión de la usabilidad de las siguientes tareas:

1. Autenticación de usuario (inicio de sesión y recuperación/cambio de contraseña).
2. Gestión y seguimiento de casos/reportes (historial, línea de tiempo, notas internas, búsqueda y filtrado por estado).
3. Gestión del perfil de usuario (foto de perfil, actualización de área/departamento) y soporte al usuario (chat de soporte, búsqueda de preguntas frecuentes).

No están incluidas en esta versión de la evaluación las siguientes tareas:

1. Panel administrativo y gestión de roles/permisos avanzados.
2. Registro de nuevos usuarios.
3. Rendimiento, seguridad de backend y pruebas de carga.

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
            <td>Problema superficial: puede ser fácilmente superado por el usuario o ocurre con muy poca frecuencia. No necesita ser arreglado a no ser que exista disponibilidad de tiempo.</td>
        </tr>
        <tr>
            <td>2</td>
            <td>Problema menor: puede ocurrir un poco más frecuentemente o es un poco más difícil de superar para el usuario. Se le debería asignar una prioridad baja de cara al siguiente release.</td>
        </tr>
        <tr>
            <td>3</td>
            <td>Problema mayor: ocurre frecuentemente o los usuarios no son capaces de resolverlo. Es importante que sea corregido y se le debe asignar una prioridad alta.</td>
        </tr>
        <tr>
            <td>4</td>
            <td>Problema muy grave: un error de gran impacto que impide al usuario continuar con el uso de la herramienta. Es imperativo que sea corregido antes del lanzamiento.</td>
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
            <td>El botón "Forgot your password?" no funciona.</td>
            <td>4</td>
            <td>Prevención de errores / Ayuda a reconocer y recuperarse de errores</td>
        </tr>
        <tr>
            <td>2</td>
            <td>No está implementada la función "Historial de reportes" (US16).</td>
            <td>3</td>
            <td>Visibilidad del estado del sistema</td>
        </tr>
        <tr>
            <td>3</td>
            <td>No está implementada la función de "Chat de soporte" (US18).</td>
            <td>3</td>
            <td>Ayuda y documentación</td>
        </tr>
        <tr>
            <td>4</td>
            <td>No está implementada la función de "Foto de perfil" (US16).</td>
            <td>2</td>
            <td>Reconocimiento antes que recuerdo / Diseño inclusivo</td>
        </tr>
        <tr>
            <td>5</td>
            <td>No está implementada la función de "Notas internas" en el caso (US25).</td>
            <td>3</td>
            <td>Flexibilidad y eficiencia de uso</td>
        </tr>
        <tr>
            <td>6</td>
            <td>No está implementada la función de "Línea de tiempo del caso" (US26).</td>
            <td>3</td>
            <td>Visibilidad del estado del sistema</td>
        </tr>
        <tr>
            <td>7</td>
            <td>No está implementada la actualización de área/departamento en el perfil (US32).</td>
            <td>2</td>
            <td>Control y libertad del usuario</td>
        </tr>
        <tr>
            <td>8</td>
            <td>No está implementada la búsqueda de reportes (US35).</td>
            <td>3</td>
            <td>Flexibilidad y eficiencia de uso / Arquitectura de información</td>
        </tr>
        <tr>
            <td>9</td>
            <td>No está implementada la búsqueda de preguntas frecuentes por palabras clave (US37).</td>
            <td>2</td>
            <td>Ayuda y documentación</td>
        </tr>
        <tr>
            <td>10</td>
            <td>No está implementado el cambio de contraseña desde el perfil (US30).</td>
            <td>4</td>
            <td>Control y libertad del usuario</td>
        </tr>
    </tbody>
</table>

**DESCRIPCIÓN DE PROBLEMAS:**

**PROBLEMA #1:**

- **Severidad:** 4
- **Heurística/Principio violado(a):** Prevención de errores / Ayuda a reconocer, diagnosticar y recuperarse de errores.
- **Problema:** Al hacer clic en "Forgot your password?" en la pantalla de login, la aplicación arroja un error no controlado en consola (`ERROR N: NG04002: 'forgot-password'`) que indica que la ruta no coincide con ninguna definida (`NoMatchError`). El usuario no recibe ninguna retroalimentación visual y queda sin poder recuperar su contraseña.

<img src="../../../../img/capitulo_6/ux_audit/problem-1.png" />

- **Recomendación:** Corregir el ruteo/handler asociado al botón de recuperación de contraseña para que resuelva correctamente el flujo, evitando el error de ruta inexistente, y mostrar al usuario retroalimentación clara (mensaje de confirmación o de error) en lugar de fallar silenciosamente.

**PROBLEMA #2:**

- **Severidad:** 3
- **Heurística/Principio violado(a):** Visibilidad del estado del sistema.
- **Problema:** No se encontró en la interfaz la función "Historial de reportes", como se menciona en la US16.

<img src="../../../../img/capitulo_6/ux_audit/problem-2.png" />

- **Recomendación:** Implementar la función de "Historial de reportes", conforme al alcance mencionado en la US16.

**PROBLEMA #3:**

- **Severidad:** 3
- **Heurística/Principio violado(a):** Ayuda y documentación.
- **Problema:** No se encontró en la interfaz la función "Chat de soporte", como se menciona en la US18.
- **Recomendación:** Implementar la función de "Chat de soporte", conforme al alcance mencionado en la US18.

**PROBLEMA #4:**

- **Severidad:** 2
- **Heurística/Principio violado(a):** Reconocimiento antes que recuerdo / Diseño inclusivo (personalización de identidad).
- **Problema:** No se encontró en la interfaz la función "Foto de perfil", como se menciona en la US16.

<img src="../../../../img/capitulo_6/ux_audit/problem-4.png" />

- **Recomendación:** Implementar la función de "Foto de perfil", conforme al alcance mencionado en la US16.

**PROBLEMA #5:**

- **Severidad:** 3
- **Heurística/Principio violado(a):** Flexibilidad y eficiencia de uso.
- **Problema:** No se encontró en la interfaz la función "Notas internas", como se menciona en la US25.

<img src="../../../../img/capitulo_6/ux_audit/problem-5.png" />

- **Recomendación:** Implementar la función de "Notas internas", conforme al alcance mencionado en la US25.

**PROBLEMA #6:**

- **Severidad:** 3
- **Heurística/Principio violado(a):** Visibilidad del estado del sistema.
- **Problema:** No se encontró en la interfaz la función "Línea de tiempo del caso", como se menciona en la US26.

<img src="../../../../img/capitulo_6/ux_audit/problem-6.png" />

- **Recomendación:** Implementar la función de "Línea de tiempo del caso", conforme al alcance mencionado en la US26.

**PROBLEMA #7:**

- **Severidad:** 2
- **Heurística/Principio violado(a):** Control y libertad del usuario.
- **Problema:** No se encontró en la interfaz la función "Actualización de área/departamento en el perfil", como se menciona en la US32.

<img src="../../../../img/capitulo_6/ux_audit/problem-7.png" />

- **Recomendación:** Implementar la función de "Actualización de área/departamento en el perfil", conforme al alcance mencionado en la US32.

**PROBLEMA #8:**

- **Severidad:** 3
- **Heurística/Principio violado(a):** Flexibilidad y eficiencia de uso / Arquitectura de información (findability).
- **Problema:** No se encontró en la interfaz la función "Búsqueda de reportes", como se menciona en la US35.

<img src="../../../../img/capitulo_6/ux_audit/problem-8.png" />

- **Recomendación:** Implementar la función de "Búsqueda de reportes", conforme al alcance mencionado en la US35.

**PROBLEMA #9:**

- **Severidad:** 2
- **Heurística/Principio violado(a):** Ayuda y documentación.
- **Problema:** No se encontró en la interfaz la función "Búsqueda de preguntas frecuentes", como se menciona en la US37.

<img src="../../../../img/capitulo_6/ux_audit/problem-9.png" />

- **Recomendación:** Implementar la función de "Búsqueda de preguntas frecuentes", conforme al alcance mencionado en la US37.

**PROBLEMA #10:**

- **Severidad:** 4
- **Heurística/Principio violado(a):** Control y libertad del usuario.
- **Problema:** No se encontró en la interfaz la función "Cambio de contraseña desde el perfil", como se menciona en la US30.

<img src="../../../../img/capitulo_6/ux_audit/problem-10.png" />

- **Recomendación:** Implementar la función de "Cambio de contraseña desde el perfil", conforme al alcance mencionado en la US30.
