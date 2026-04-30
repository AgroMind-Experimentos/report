**CARRERA:** Ingeniería de Software

**CURSO:** Aplicaciones Web

**CLIENTE:** Usuarios agrícolas (Agricultores y Agrónomos)

**AUDITOR:** Equipo del proyecto EcoTrack

**APP A EVALUAR: EcoTrack – Plataforma Web para Gestión Agrícola**

**TAREAS EVALUADAS**

Las tareas incluidas en la evaluación fueron:

1. Registro e inicio de sesión
2. Visualización del dashboard
3. Selección de cultivos
4. Creación de parcelas
5. Visualización y gestión de tareas
6. Revisión de alertas del cultivo
7. Generación y consulta de reportes
8. Uso de la landing page para conocer el producto

**TABLA DE ESCALA DE SEVERIDAD**

<table>
    <thead>
        <tr>
            <th>Nivel</th>
            <th>Descripción</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><strong>1</strong></td>
            <td>Problema superficial: puede ser superado fácilmente o ocurre con poca frecuencia. No necesita ser arreglado salvo que haya tiempo disponible.</td>
        </tr>
        <tr>
            <td><strong>2</strong></td>
            <td>Problema menor: ocurre más frecuentemente o es algo más difícil para el usuario. Recomendado arreglarlo en un siguiente release con baja prioridad.</td>
        </tr>
        <tr>
            <td><strong>3</strong></td>
            <td>Problema mayor: ocurre frecuentemente o el usuario no puede resolverlo. Se debe corregir con prioridad alta.</td>
        </tr>
        <tr>
            <td><strong>4</strong></td>
            <td>Problema muy grave: impide al usuario continuar. Debe corregirse antes del lanzamiento.</td>
        </tr>
    </tbody>
</table>


**TABLA RESUMEN DE PROBLEMAS**

<table>
    <thead>
        <tr>
            <th>#</th>
            <th>Problema identificado</th>
            <th>Severidad</th>
            <th>Heurística / Principio violado</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>1</td>
            <td>Falta opción de inicio de sesión alternativo (Google, celular)</td>
            <td>2</td>
            <td>Usability – Flexibilidad y eficiencia</td>
        </tr>
        <tr>
            <td>2</td>
            <td>Landing page sin imágenes reales del campo</td>
            <td>2</td>
            <td>Inclusive Design – Experiencias comparables</td>
        </tr>
        <tr>
            <td>3</td>
            <td>Selección de cultivos sin apoyo visual (iconos/fotos)</td>
            <td>3</td>
            <td>Usability – Reconocimiento mejor que recuerdo</td>
        </tr>
        <tr>
            <td>4</td>
            <td>Alertas poco visibles; falta diferenciación por criticidad</td>
            <td>3</td>
            <td>Usability – Visibilidad del estado del sistema</td>
        </tr>
        <tr>
            <td>5</td>
            <td>Tareas urgentes no tienen color o jerarquía destacada</td>
            <td>3</td>
            <td>Usability – Señalización y prioridades</td>
        </tr>
        <tr>
            <td>6</td>
            <td>Dashboard con pocos gráficos o indicadores visuales</td>
            <td>2</td>
            <td>Information Architecture – Is it understandable?</td>
        </tr>
        <tr>
            <td>7</td>
            <td>Crear parcelas sin mapa o soporte geográfico visual</td>
            <td>3</td>
            <td>Usability – Correspondencia con el mundo real</td>
        </tr>
        <tr>
            <td>8</td>
            <td>Falta opción “Recordar sesión”</td>
            <td>1</td>
            <td>Usability – Minimizar carga del usuario</td>
        </tr>
        <tr>
            <td>9</td>
            <td>Falta calendario para ver tareas</td>
            <td>2</td>
            <td>Usability – Control del usuario</td>
        </tr>
        <tr>
            <td>10</td>
            <td>Alertas importantes no enviadas por WhatsApp</td>
            <td>2</td>
            <td>Inclusive Design – Ajuste al contexto real</td>
        </tr>
    </tbody>
</table>

**DESCRIPCIÓN DETALLADA DE PROBLEMAS**

## **Problema #1 – Falta opción de inicio de sesión alternativo**

**Severidad:** 2

**Heurística violada:** Usability – Flexibilidad y eficiencia del uso

**Problema:**

Los usuarios prefieren iniciar sesión con Google, correo institucional o número de celular, lo cual no está disponible y genera fricción.

**Recomendación:**

Agregar login con Google, instituciones y celular.


## **Problema #2 – Falta de imágenes reales en la landing page**

**Severidad:** 2

**Heurística violada:** Inclusive Design – Experiencias comparables

**Problema:**

Las imágenes no representan el contexto real agrícola, lo que reduce conexión emocional.

**Recomendación:**

Incluir fotografías reales del campo, cooperativas o agrónomos.


## **Problema #3 – Selección de cultivos sin apoyo visual**

**Severidad:** 3

**Heurística violada:** Usability – Reconocimiento mejor que recuerdo

**Problema:**

Los cultivos con nombres similares generan confusión sin iconos o fotos de referencia.

**Recomendación:**

Añadir iconografía o imágenes pequeñas para cada cultivo.


## **Problema #4 – Alertas poco visibles**

**Severidad:** 3

**Heurística violada:** Usability – Visibilidad del estado del sistema

**Problema:**

Las alertas no destacan ni indican su severidad.

**Recomendación:**

Usar colores por nivel, banners y señales visuales fuertes para alertas críticas.


## **Problema #5 – Tareas urgentes sin jerarquía visual**

**Severidad:** 3

**Heurística violada:** Usability – Señalización y prioridades

**Problema:**
Las tareas urgentes se ven idénticas a las normales.

**Recomendación:**
Colores, etiquetas o iconos para urgencia.


## **Problema #6 – Dashboard con poca visualización gráfica**

**Severidad:** 2

**Heurística violada:** Information Architecture – Is it understandable?

**Problema:**

La vista inicial carece de indicadores gráficos que permitan interpretar rápidamente el estado de la organización.

**Recomendación:**

Añadir KPIs, gráficos de barras, indicadores de cultivo y alertas activas.


## **Problema #7 – Crear parcelas sin soporte geográfico**

**Severidad:** 3

**Heurística violada:** Usability – Correspondencia con el mundo real

**Problema:**

Los usuarios necesitan ubicar parcelas en un mapa, no solo datos textuales.

**Recomendación:**

Integrar mapas interactivos para delimitar la parcela.


## **Problema #8 – Falta opción “Recordar sesión”**

**Severidad:** 1

**Heurística violada:** Usability – Minimizar carga del usuario

**Problema:**
El usuario debe loguearse siempre, poco ideal en campo.

**Recomendación:**
Implementar “Mantener sesión iniciada”.

## **Problema #9 – Falta calendario para visualizar tareas**

**Severidad:** 2

**Heurística violada:** Usability – Control y eficiencia del usuario

**Problema:**

No existe vista de calendario para planificar semanal o mensualmente.

**Recomendación:**

Añadir calendario con vista semanal, mensual y por responsable.


## **Problema #10 – Alertas no enviadas por WhatsApp**

**Severidad:** 2

**Heurística violada:** Inclusive Design – Adaptación al contexto

**Problema:**
Los usuarios agrícolas dependen más de WhatsApp que del correo.

**Recomendación:**
Integrar notificaciones vía WhatsApp API.