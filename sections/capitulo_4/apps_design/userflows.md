- User Flow – Agricultor Juan Carlos
  
        User goal: "Juan Carlos quiere organizar y dar seguimiento a sus cultivos de manera sencilla para mejorar el control de su producción y reducir pérdidas."

<img src="../../../img/capitulo_4/apps_design/userflow-1.png" width="80%">

- Explicación de los flujos y condiciones

  - Inicio de sesión / acceso

        Ingresa con usuario y contraseña.

        Happy path: Accede correctamente al Dashboard.

        Unhappy path: Credenciales erróneas o error de conexión → mensaje de error con opción de reintentar.

  - Visualización de tareas del cultivo

        Ve una lista organizada de tareas pendientes: riego, fertilización, control de plagas, cosecha.

        Cada tarea incluye estado (pendiente, en proceso, completada).

        Happy path: Puede consultar y entender fácilmente las tareas.

        Unhappy path: No tiene tareas, pide crear tarea".

- User Flow – Ingeniera Agrónoma (Ana Morales)


    - User Goal: Ana quiere gestionar y consultar información confiable de los agricultores y sus cultivos para garantizar la trazabilidad y brindar asesorías técnicas precisas.

<img src="../../../img/capitulo_4/apps_design/userflow-2.png" width="80%">


- Explicación de los flujos y condiciones

  - Inicio de sesión / acceso

        Ana ingresa a la aplicación con sus credenciales.

        Happy path: Accede correctamente a su Dashboard.

        Unhappy path: Error en credenciales o conexión → mensaje de error con opción de reintentar.

  - Dashboard de agrónoma

        Visualiza las organizaciones creadas y la lista de agricultores a su cargo o que asesora.

        Desde aquí puede crear una nueva organización o seleccionar una existente para acceder a la información.

        Happy path: Accede al detalle de la organización seleccionada.

        Unhappy path: Error de carga de organizaciones → mensaje de reintento.

  - Creación de organización

        Ana puede registrar una organización y asociar agricultores.

        Happy path: Organización creada correctamente y agricultores vinculados.

        Unhappy path: Datos incompletos (ej. falta nombre) → mensaje de validación para corregir.

  - Creación de parcelas

        Dentro de la organización, Ana puede crear una parcela con nombre, área, ubicación y cultivo.

        Happy path: Parcela registrada y disponible en la lista de parcelas.

        Unhappy path: Datos incompletos o error de red → advertencia "No se pudo registrar la parcela".

  - Visualización de parcelas y tareas

        Ana accede a la lista de parcelas creadas y selecciona una para visualizar sus tareas (riego, fertilización, control de plagas, etc.).

        Happy path: Visualiza las tareas organizadas por estado (pendiente, en proceso, completada).

        Unhappy path: Error de conexión o falta de datos → mensaje "No se pudieron cargar las tareas".

  - Gestión de tareas

        Ana puede crear nuevas tareas dentro de la parcela o consultar las ya registradas.

        Happy path: La tarea se guarda correctamente y se actualiza la lista.

        Unhappy path: Datos faltantes (ej. sin fecha asignada) o error de carga → mensaje de advertencia.