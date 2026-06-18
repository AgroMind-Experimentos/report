El componente de alertas es fundamental para la detección y respuesta temprana ante problemas de rendimiento o disponibilidad de la aplicación, permitiendo que el equipo sea notificado de inmediato cuando ocurren eventos críticos o se superan los umbrales definidos.

<div align="center">

| <img src="../../../img/logos/prometheus.svg" width="48" height="48"/><br/>Prometheus Alertmanager |
|:---:|

</div>

Para esto se emplea Prometheus Alertmanager, el componente de alertas nativo del ecosistema de Prometheus. Su funcionamiento parte de las reglas de alerta definidas en Prometheus: cuando una métrica supera un umbral establecido (por ejemplo, una latencia elevada, un consumo excesivo de memoria o la caída de un servicio), Prometheus dispara la alerta y la envía a Alertmanager. Este se encarga de gestionar dichas alertas mediante tres capacidades clave: la agrupación de alertas similares para evitar la saturación de avisos, la deduplicación para impedir notificaciones repetidas del mismo incidente, y el enrutamiento, que determina hacia qué destino debe enviarse cada alerta según su gravedad. De esta manera, Alertmanager asegura que el equipo reciba avisos relevantes y oportunos, minimizando el ruido y facilitando una respuesta ágil ante incidentes en producción.
