El equipo empleará GitHub como repositorio de alojamiento y Git como sistema de control de versiones para todos los entregables del proyecto Demy. Se aplicará la estrategia de ramificación GitFlow Workflow, con el uso de Semantic Versioning y mensajes estructurados bajo la convención de Conventional Commits.

**Repositorios del Proyecto**

<table>
    <thead>
        <tr>
            <th><strong>Producto</strong></th>
            <th><strong>Repositorio GitHub</strong></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><strong>Landing Page</strong></td>
            <td><a href="https://github.com/AgroMind-Experimentos/landing">https://github.com/AgroMind-Experimentos/landing</a></td>
        </tr>
        <tr>
            <td><strong>Report</strong></td>
            <td><a href="https://github.com/AgroMind-Experimentos/report">https://github.com/AgroMind-Experimentos/report</a></td>
        </tr>
        <tr>
            <td><strong>Frontend</strong></td>
            <td><a href="https://github.com/AgroMind-Experimentos/frontend">https://github.com/AgroMind-Experimentos/frontend</a></td>
        </tr>
        <tr>
            <td><strong>Backend</strong></td>
            <td><a href="https://github.com/AgroMind-Experimentos/backend">https://github.com/AgroMind-Experimentos/backend</a></td>
        </tr>
    </tbody>
</table>

**Modelo GitFlow**

Se seguirá el enfoque planteado por Vincent Driessen, el cual define dos ramas principales:

* **main**: contiene las versiones estables listas para producción.
* **develop**: integra nuevas funcionalidades antes de pasar al entorno de producción.

<table>
    <thead>
        <tr>
            <th><strong>Tipo de rama</strong></th>
            <th><strong>Uso principal</strong></th>
            <th><strong>Convención de nombres</strong></th>
            <th><strong>Ejemplo</strong></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><strong>feature</strong></td>
            <td>Desarrollo de funcionalidades nuevas.</td>
            <td><code>feature/&lt;nombre-descriptivo&gt;</code></td>
            <td><code>feature/sprint1-salim</code></td>
        </tr>
        <tr>
            <td><strong>release</strong></td>
            <td>Preparación de una versión previa al despliegue.</td>
            <td><code>release/vX.Y.Z</code></td>
            <td><code>release/v1.0.0</code></td>
        </tr>
        <tr>
            <td><strong>hotfix</strong></td>
            <td>Corrección rápida de errores en producción.</td>
            <td><code>hotfix/&lt;problema&gt;</code></td>
            <td><code>hotfix/fix-crash-navbar</code></td>
        </tr>
    </tbody>
</table>

**Versionado Semántico**

Se implementará el esquema Semantic Versioning 2.0.0, con el formato:

**MAJOR.MINOR.PATCH**

* **MAJOR**: cambios incompatibles con versiones anteriores.
* **MINOR**: incorporación de nuevas funciones compatibles.
* **PATCH**: corrección de errores o mejoras menores.

**Conventional Commits**

Los mensajes de commit seguirán el estándar Conventional Commits para asegurar trazabilidad y generar changelogs automáticos.

**Formato general:**
`<tipo>(opcional-scope): descripción breve`

* **Tipos de commit definidos:**
    * **feat**: nueva funcionalidad
    * **fix**: corrección de errores
    * **docs**: cambios en documentación
    * **style**: ajustes de formato (espacios, comas, etc.)
    * **refactor**: modificaciones de código sin impacto en funciones o errores
    * **test**: adición o modificación de pruebas
    * **chore**: tareas de mantenimiento o generales

**Permisos**

Los roles y niveles de acceso detallados a continuación se mantienen de manera íntegra y consistente en la totalidad de los repositorios que conforman el ecosistema de la organización.

<table>
    <thead>
        <tr>
            <th><strong>Persona</strong></th>
            <th><strong>Permiso</strong></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Orozco Torres, Alvaro Joaquin</td>
            <td>Admin</td>
        </tr>
        <tr>
            <td>Reaño Delgadillo, Henry Paolo</td>
            <td>Admin</td>
        </tr>
        <tr>
            <td>Chi Cruzatt, Kevin Jorge</td>
            <td>Write</td>
        </tr>
        <tr>
            <td>Mostajo Orosco, Maria Fernanda</td>
            <td>Write</td>
        </tr>
        <tr>
            <td>Paucar De La Cruz, Tatiana Medalith</td>
            <td>Write</td>
        </tr>
        <tr>
            <td>Ramos Aguirre, Aldair Joaquin</td>
            <td>Write</td>
        </tr>
    </tbody>
</table>