Las siguientes métricas de negocio de EcoTrack son las que guían la medición de todos los experimentos del capítulo.

| Métrica | Descripción | Fórmula | Técnica de Recolección | Meta |
|---|---|---|---|---|
| Tasa de exportación de reportes | % de usuarios activos que descargaron al menos un reporte en el periodo | (Usuarios con ≥1 descarga / Total usuarios activos) × 100 | Evento de Google Analytics al pulsar "Exportar a Excel" | ≥ 40% |
| Puntuación de satisfacción UX | Promedio de valoraciones de usuarios tras probar una funcionalidad | Promedio de puntuaciones en encuesta in-app (escala 1–5) | Encuesta in-app que aparece al terminar de usar la función | ≥ 4.0 / 5.0 |
| Tasa de completitud de tareas | % de tareas registradas que alcanzan estado "completada" | (Tareas completadas / Tareas registradas) × 100 | Consulta en BD filtrando tareas por estado | +12% sobre línea base |
| Tasa de adopción de geolocalización | % de usuarios activos que registraron al menos una ubicación | (Usuarios con ≥1 ubicación registrada / Total usuarios activos) × 100 | Logs del backend al guardar coordenadas en un registro | ≥ 35% |
| Tiempo promedio de registro de cultivo | Tiempo que tarda un usuario en completar el formulario de cultivo | Promedio(timestamp_fin − timestamp_inicio) en segundos | Timestamps del frontend al abrir y cerrar el formulario de cultivo | −10% vs. línea base |
| Tasa de error en registro de cultivos | % de registros con nombre duplicado o variación ortográfica de un cultivo ya existente | (Registros duplicados o con error / Total registros de cultivo) × 100 | Revisión de registros en BD al cierre del periodo | −25% vs. línea base |
| Valor percibido de la sección de clima | % de usuarios que valoran positivamente la sección de clima con IA | (Usuarios con respuesta ≥4/5 en encuesta / Total encuestados) × 100 | Encuesta in-app al salir de la sección de clima | ≥ 45% |
| Acciones preventivas registradas | Promedio de acciones preventivas por usuario activo en el periodo | Total acciones preventivas / Total usuarios activos | Logs del backend con acciones de tipo preventivo | +15% vs. línea base |
