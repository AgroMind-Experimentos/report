## 8.2.6. Methods Selection

Para validar las hipótesis planteadas, cada experimento combina métodos cuantitativos y cualitativos según la naturaleza de las métricas definidas en las secciones anteriores. Adicionalmente, se seleccionaron herramientas de análisis de rendimiento y experiencia de usuario para verificar que las nuevas funcionalidades no degraden la calidad técnica de la plataforma.

### Herramientas seleccionadas

| Herramienta | Google Analytics | Catchpoint | RedLine13 | Lighthouse |
|---|---|---|---|---|
| **Precio** | Plan gratuito/créditos gratis | Basado en suscripción, con pruebas gratuitas | Gratuito con limitaciones | Plan gratuito, disponible para ejecución local |
| **Capacidad de Análisis** | Análisis exhaustivo de métricas y datos de usuario | Monitoreo exhaustivo de rendimiento y experiencia de usuario desde múltiples ubicaciones | Análisis orientado a pruebas de carga y rendimiento de aplicaciones | Análisis orientado a la experiencia de usuario, con métricas clave de rendimiento y accesibilidad |
| **Sencillez** | Aprendizaje sencillo de las métricas | Interfaz avanzada pero detallada y completa | Información detallada y resumida sobre rendimiento | Información resumida en valores clave que puntúan aspectos de la aplicación |
| **Ventajas** | Excelente capacidad de generación de reportes y amplia integración con otros servicios | Análisis en tiempo real desde diversas ubicaciones y dispositivos, ideal para empresas con usuarios globales | Simulación de tráfico y pruebas de rendimiento bajo condiciones de carga | Evaluación de accesibilidad, rendimiento y diseño con métricas claras para optimizar la experiencia del usuario |

### Métodos cuantitativos

**Pruebas A/B con grupos de control**

Cada experimento se ejecuta con dos grupos: uno que accede a la funcionalidad nueva (condición experimental) y otro que continúa usando la versión actual (condición de control). La comparación entre ambos grupos permite atribuir los cambios observados en las métricas a la funcionalidad implementada y no a variaciones naturales de uso.

**Análisis de logs del backend**

Las acciones registradas en el servidor —como el guardado de coordenadas GPS o el registro de acciones preventivas— se extraen de los logs del backend para calcular métricas de adopción y frecuencia de uso que no son visibles desde el frontend.

**Consultas a la base de datos**

Las métricas relacionadas con calidad de datos —como duplicidades o errores ortográficos en el registro de cultivos— se obtienen mediante consultas directas a la base de datos al cierre del periodo de prueba, comparando los registros previos y posteriores a la implementación.

**Auditoría de rendimiento y accesibilidad con Lighthouse**

Se utiliza Lighthouse para evaluar el rendimiento, accesibilidad y buenas prácticas de EcoTrack en las principales vistas de la aplicación. Esta auditoría se ejecuta antes y después de incorporar las funcionalidades experimentales para verificar que los cambios no degraden la experiencia técnica del usuario. Los resultados obtenidos se presentan en la sección 8.2.7.

### Métodos cualitativos

**Encuestas in-app**

Se muestra una encuesta breve (escala 1–5) dentro de la plataforma tras el uso de cada funcionalidad experimental. Este método permite medir la satisfacción UX y el valor percibido directamente en el contexto de uso, sin depender de entrevistas externas.

**Satisfacción del usuario en pruebas A/B**

Adicionalmente, dentro de las pruebas A/B se captura la recepción del usuario mediante esta misma escala, permitiendo comparar la valoración entre el grupo experimental y el de control.

### Resumen por experimento

| Experimento | Método principal | Método de soporte |
|---|---|---|
| Exportar a Excel | Google Analytics (eventos de descarga) | Encuesta in-app |
| Vista Kanban | Consulta a BD (estado de tareas) | Encuesta in-app |
| Geolocalización | Logs del backend (coordenadas guardadas) | Encuesta in-app |
| Crops dropdown | Consulta a BD (duplicados/errores) + timestamps frontend | — |
| Recomendaciones IA | Encuesta in-app | Logs del backend (acciones preventivas) |
