El pipeline de monitoreo de EcoTrack integra las etapas necesarias para mantener la calidad y el rendimiento de la plataforma en producción: recopilación de métricas, almacenamiento, análisis y visualización. Para cubrir estas etapas se emplea el stack open-source más utilizado en entornos cloud-native, compuesto por Prometheus y Grafana, donde cada herramienta cumple una función específica y complementaria dentro del flujo.

<div align="center">

| <img src="../../../img/logos/prometheus.svg" width="48" height="48"/><br/>Prometheus | <img src="../../../img/logos/grafana.svg" width="48" height="48"/><br/>Grafana |
|:---:|:---:|

</div>

Prometheus se encarga de la recopilación y el almacenamiento de métricas. Funciona bajo un modelo basado en pull, recolectando de forma periódica métricas de rendimiento de la aplicación y la infraestructura, tales como uso de CPU, consumo de memoria, latencia y tasa de errores. Estas métricas se almacenan como series temporales, permitiendo consultas flexibles mediante su lenguaje PromQL para analizar el comportamiento del sistema a lo largo del tiempo.

Grafana se encarga de la capa de visualización. Se conecta a Prometheus como fuente de datos y presenta las métricas recopiladas en dashboards personalizados e intuitivos, permitiendo al equipo interpretar de un vistazo el estado de la plataforma, identificar tendencias y detectar comportamientos anómalos. Esta separación de responsabilidades —Prometheus recolectando y almacenando, Grafana visualizando— constituye el patrón estándar de un pipeline de monitoreo en producción.
