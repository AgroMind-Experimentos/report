El diagrama representa una visión general del sistema Ecotrack, organizado en distintos bounded contexts que delimitan responsabilidades y entidades clave. En él se observa cómo los usuarios gestionan sus cuentas y perfiles, cómo las organizaciones administran parcelas, planes de suscripción y tipos de cultivos, y cómo se articulan los procesos de monitoreo y control mediante checklists, tareas, lecturas ambientales y alertas. Además, se incluyen objetos compartidos que permiten mantener coherencia en la identificación y manejo de valores comunes. En conjunto, este modelo refleja la estructura conceptual del dominio y la interacción entre sus principales componentes.

<img src="../../../img/capitulo_4/oop/class-diagram.png" width="50%">

<div style="page-break-after: always;"></div>

### IAM Bounded Context

Este diagrama corresponde al IAM Bounded Context, donde se gestiona la identidad y acceso de los usuarios. El agregado principal es User, que contiene atributos básicos como identificador, correo, contraseña cifrada, estado y rol asignado. Los roles pueden ser Agronomist o Farmer, mientras que el estado de la cuenta se define como Active, Inactive o Suspended. De esta manera, este contexto asegura el control de autenticación y autorización dentro del sistema.

<img src="../../../img/capitulo_4/oop/iam-diagram.png" width="50%">

<div style="page-break-after: always;"></div>

### Profile Bounded Context

Este diagrama representa el Profile Bounded Context, donde se gestionan los perfiles de los usuarios. El agregado principal es Profile, que contiene atributos como identificador, nombre completo, teléfono y foto de perfil. Cada perfil está asociado a un usuario específico mediante el userId. Este contexto permite almacenar y actualizar la información personal de los usuarios dentro del sistema.

<img src="../../../img/capitulo_4/oop/profile-diagram.png" width="50%">

<div style="page-break-after: always;"></div>

### Organization Bounded Context

Este diagrama corresponde al Organization Bounded Context, encargado de estructurar y administrar las organizaciones dentro del sistema. Aquí, el agregado principal Organization gestiona el nombre, estado, miembros, número máximo de parcelas y la suscripción activa. A su vez, las Plot representan las parcelas asociadas a la organización, con atributos como tamaño, ubicación y tipo de cultivo. Los cultivos se definen mediante la entidad PlantType, que puede vincularse a una lista de tipos predefinidos como papa, maíz, trigo, café, entre otros. Finalmente, el modelo incluye la entidad Subscription, que permite a la organización acceder a planes (AgroStart, AgroSmart, AgroExpert) y mantener control sobre la vigencia y estado de la suscripción. En conjunto, este contexto regula tanto la estructura organizacional como la gestión de recursos y servicios contratados.

<img src="../../../img/capitulo_4/oop/organization-diagram.png" width="50%">

<div style="page-break-after: always;"></div>

### Monitoring and Control Bounded Context

Este diagrama corresponde al Monitoring and Control Bounded Context, responsable de supervisar y gestionar las actividades y condiciones en campo. Aquí se incluyen los Checklists, que permiten organizar y dar seguimiento a las tareas (Task) asignadas a los perfiles, junto con fechas, materiales utilizados y su estado de avance. Asimismo, se registran lecturas ambientales (EnvironmentalReading) que son evaluadas frente a umbrales (Threshold) para detectar desviaciones en parámetros como temperatura, humedad o pH. Cuando se superan estos límites, se generan Alertas (Alert) con distintos niveles de severidad (INFO, WARNING, CRITICAL). Por otro lado, el contexto también incorpora sesiones de muestreo de plantas (PlantSamplingSession), que almacenan observaciones detalladas de altura, número de hojas y frutos, y permiten calcular promedios para análisis posteriores. En conjunto, este contexto asegura el control operativo mediante tareas planificadas, monitoreo en tiempo real y alertas tempranas que facilitan la toma de decisiones

<img src="../../../img/capitulo_4/oop/monitoring-diagram.png" width="50%">

<div style="page-break-after: always;"></div>

### Reports Bounded Context

Este diagrama corresponde al Reports Bounded Context, encargado de la generación y gestión de reportes dentro del sistema. El agregado principal es Report, que contiene información sobre el usuario que lo solicita, la parcela asociada, el tipo de reporte, el rango de fechas, el estado del proceso y el contenido generado. Los reportes pueden ser de tipo Parcel o General, y su ciclo de vida se refleja en el ReportStatus, que abarca estados como REQUESTED, PROCESSING, GENERATED o FAILED. A través de este contexto, los usuarios pueden solicitar reportes, generar información consolidada y manejar errores en caso de fallos durante la generación.

<img src="../../../img/capitulo_4/oop/report-diagram.png" width="50%">

<div style="page-break-after: always;"></div>
