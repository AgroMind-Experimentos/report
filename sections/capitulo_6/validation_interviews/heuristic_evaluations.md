**Aplicacion a evaluar: EcoTrack – Plataforma Web para Gestión Agrícola**

**TAREAS EVALUADAS**

Las tareas incluidas en la evaluación fueron:

1. Inicio de sesión y acceso a la plataforma
2. Visualización de la pantalla principal (cultivos y tareas)
3. Consulta y revisión de cultivos registrados
4. Identificación y priorización de tareas pendientes
5. Revisión de alertas asociadas a los cultivos
6. Navegación entre pantallas (regreso, cancelación, corrección de datos)

**TABLA DE ESCALA DE SEVERIDAD**

| Nivel | Descripción |
|---|---|
| **1** | Problema superficial: puede ser superado fácilmente o ocurre con poca frecuencia. No necesita ser arreglado salvo que haya tiempo disponible. |
| **2** | Problema menor: ocurre más frecuentemente o es algo más difícil para el usuario. Recomendado arreglarlo en un siguiente release con baja prioridad. |
| **3** | Problema mayor: ocurre frecuentemente o el usuario no puede resolverlo. Se debe corregir con prioridad alta. |
| **4** | Problema muy grave: impide al usuario continuar. Debe corregirse antes del lanzamiento. |

**TABLA RESUMEN DE PROBLEMAS**

| # | Problema identificado | Severidad | Heurística / Principio violado |
|---|---|---|---|
| 1 | Las alertas no indican su nivel de urgencia ni distinguen visualmente las críticas de las leves | 3 | Usability – Visibilidad del estado del sistema |
| 2 | Las tareas no muestran horarios o tiempos estimados de ejecución | 2 | Usability – Correspondencia con el mundo real |
| 3 | No existe recordatorio o notificación externa (push/celular) para tareas o alertas próximas | 2 | Usability – Visibilidad del estado del sistema |
| 4 | Las alertas no incluyen recomendaciones prácticas de qué acción tomar frente al problema detectado | 3 | Usability – Ayuda y documentación |
| 5 | No hay opción para visualizar la contraseña al iniciar sesión | 1 | Usability – Prevención de errores |
| 6 | Falta un historial de actividades o eventos por cultivo | 2 | Information Architecture – Is it understandable? |
| 7 | No se puede reasignar o delegar una tarea a otra persona desde la app | 2 | Usability – Flexibilidad y eficiencia de uso |
| 8 | No existe un módulo para registrar gastos, ventas o ganancias asociadas al cultivo | 2 | Information Architecture – Is it complete? |
| 9 | Algunos íconos carecen de etiquetas o nombres visibles, dificultando su reconocimiento | 3 | Usability – Reconocimiento mejor que recuerdo |
| 10 | No se muestra advertencia antes de salir de un formulario con datos sin guardar | 3 | Usability – Prevención de errores |

**DESCRIPCIÓN DETALLADA DE PROBLEMAS**

### Problema #1 – Alertas sin nivel de urgencia visible

**Severidad:** 3

**Heurística violada:** Usability – Visibilidad del estado del sistema

**Problema:** Los agricultores entrevistados señalaron que las alertas relacionadas con los cultivos se muestran de forma homogénea, sin distinguir entre situaciones críticas y advertencias menores, lo que dificulta priorizar la atención.

**Recomendación:** Incorporar códigos de color o iconografía diferenciada según el nivel de gravedad de la alerta (por ejemplo, verde, amarillo, rojo).

---

### Problema #2 – Falta de tiempos estimados en tareas

**Severidad:** 2

**Heurística violada:** Usability – Correspondencia con el mundo real

**Problema:** Uno de los entrevistados indicó que las tareas no muestran una referencia de tiempo estimado, lo que dificulta planificar la jornada de trabajo.

**Recomendación:** Añadir un campo opcional de duración estimada visible en cada tarjeta de tarea.

---

### Problema #3 – Ausencia de recordatorios externos

**Severidad:** 2

**Heurística violada:** Usability – Visibilidad del estado del sistema

**Problema:** Varios usuarios mencionaron que les gustaría recibir recordatorios de tareas y alertas fuera de la plataforma (por celular), ya que no siempre están revisando la aplicación activamente.

**Recomendación:** Evaluar la integración de notificaciones push o alertas vía WhatsApp/SMS para tareas próximas a vencer.

---

### Problema #4 – Alertas sin recomendación de acción

**Severidad:** 3

**Heurística violada:** Usability – Ayuda y documentación

**Problema:** Las alertas muestran el problema detectado, pero no sugieren una acción concreta que el agricultor pueda tomar para resolverlo.

**Recomendación:** Acompañar cada alerta con una recomendación breve y accionable, similar al enfoque de las recomendaciones climáticas por IA implementadas en el Capítulo VIII.

---

### Problema #5 – Sin opción de visualizar contraseña

**Severidad:** 1

**Heurística violada:** Usability – Prevención de errores

**Problema:** Al iniciar sesión, el usuario no puede verificar visualmente la contraseña ingresada, lo que puede generar errores de tipeo no detectados.

**Recomendación:** Agregar un ícono de "mostrar/ocultar contraseña" en el campo correspondiente.

---

### Problema #6 – Falta de historial por cultivo

**Severidad:** 2

**Heurística violada:** Information Architecture – Is it understandable?

**Problema:** No existe una vista que permita consultar el historial de actividades, alertas o cambios asociados a un cultivo específico a lo largo del tiempo.

**Recomendación:** Implementar una línea de tiempo o bitácora consultable por cultivo.

---

### Problema #7 – No se pueden reasignar tareas

**Severidad:** 2

**Heurística violada:** Usability – Flexibilidad y eficiencia de uso

**Problema:** Los usuarios no cuentan con una opción para delegar o reasignar una tarea previamente creada a otro miembro del equipo.

**Recomendación:** Habilitar la edición del responsable asignado desde el detalle de la tarea.

---

### Problema #8 – Ausencia de módulo financiero

**Severidad:** 2

**Heurística violada:** Information Architecture – Is it complete?

**Problema:** Dos de los tres entrevistados solicitaron poder registrar gastos, ventas o ganancias vinculadas a la producción, funcionalidad que actualmente no existe en la plataforma.

**Recomendación:** Evaluar como funcionalidad futura un módulo simple de registro financiero por parcela o campaña.

---

### Problema #9 – Íconos sin etiquetas

**Severidad:** 3

**Heurística violada:** Usability – Reconocimiento mejor que recuerdo

**Problema:** Algunos íconos de la interfaz no cuentan con texto o etiqueta visible, obligando al usuario a recordar su función en lugar de reconocerla.

**Recomendación:** Incluir etiquetas de texto junto a los íconos principales o tooltips accesibles al mantener presionado/hover.

---

### Problema #10 – Sin aviso al salir de formularios

**Severidad:** 3

**Heurística violada:** Usability – Prevención de errores

**Problema:** Si el usuario navega fuera de un formulario con información ya ingresada, no recibe ninguna advertencia y puede perder los datos sin guardar.

**Recomendación:** Mostrar un modal de confirmación ("¿Deseas salir sin guardar los cambios?") antes de abandonar formularios con datos pendientes.
