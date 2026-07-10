
**UA01 – Exportar reportes a Excel (Experiment Card 01)**

El endpoint `GET /api/v1/reports/excel` genera y descarga el reporte del estado de las tareas en formato `.xlsx`.

<img src="../../../../img/capitulo_8/experimentation/ua01_api_reports_excel.png" alt="Endpoint GET /api/v1/reports/excel en Swagger" />

</br>

**UA03 – Registrar geolocalización de parcela (Experiment Card 03)**

Se agregaron los campos de latitud y longitud a las parcelas (`/api/v1/plots`), de modo que las coordenadas se guardan y se consultan junto con cada parcela.

<img src="../../../../img/capitulo_8/experimentation/ua03_api_plots.png" alt="Endpoint PATCH /api/v1/plots/{id} con los campos de latitud y longitud en Swagger" />

</br>

Los experimentos UA02, UA04 y UA05 no cambiaron el backend. El tablero Kanban usa el endpoint de estado que ya existía (`PATCH /api/v1/tasks/{taskId}/status`), y el catálogo de cultivos y las recomendaciones climáticas funcionan en el lado del cliente.
