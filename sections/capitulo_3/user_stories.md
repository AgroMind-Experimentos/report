Las user stories representan los *requisitos funcionales* de **Ecotrack** desde la perspectiva de los Agricultores y los Agrónomos. Cada historia de usuario desceribe una interaccion especifica que los usuarios necesitan realizar, como registrar cultivos o crear organizaciones. Estas historias se desglozan en tareas conceretas que guiaran el desarrollo de la plataforma, asegurando que se cumplan con las necesidades reales y expectativas de los usuarios finales, y que EcoTrack brinde una experiencia eficiente, justa y centrada en el valor de las conexiones profesionales


**USER STORIES**

<table>
    <tbody>
        <tr>
            <td>US01</td>
            <td>Crear parcela</td>
            <td>Como Agrónomo, quiero crear una parcela con sus datos específicos para gestionar las áreas de cultivo de mi organización</td>
            <td>
                <strong>Escenario 1: Creación de parcela exitosa</strong><br>
                <strong>Dado que</strong> el Agrónomo pertenece a una organización y está autenticado<br>
                <strong>Y</strong> los valores ingresados son válidos (nombre no vacío, área decimal positivo, ubicación no vacía y cultivo no vacío)<br>
                <strong>Cuando</strong> confirme la creación de la parcela<br>
                <strong>Entonces</strong> el sistema registra la parcela, asociándola a su organización<br>
                <strong>Y</strong> muestra un mensaje de confirmación<br>
                <strong>Escenario 2: Error por validación de campos</strong><br>
                <strong>Dado que</strong> el Agrónomo pertenece a una organización y está autenticado<br>
                <strong>Y</strong> se omiten datos obligatorios o se ingresan valores inválidos<br>
                <strong>Cuando</strong> confirme la creación de la parcela<br>
                <strong>Entonces</strong> el sistema rechaza el registro de la parcela<br>
                <strong>Y</strong> alerta sobre los campos incorrectos o faltantes<br>
                <strong>Escenario 3: Fallo general</strong><br>
                <strong>Dado que</strong> el Agrónomo confirmó la creación de la parcela<br>
                <strong>Cuando</strong> la operación falla por pérdida de conexión a internet, tiempo de espera agotado u otro error generalizado<br>
                <strong>Entonces</strong> el sistema no registra la parcela ni altera los datos existentes<br>
                <strong>Y</strong> muestra un mensaje alertando sobre la causa del error
            </td>
            <td>EP01</td>
        </tr>
        <tr>
            <td>US02</td>
            <td>Listado de parcelas</td>
            <td>Como Agrónomo, quiero visualizar un listado de parcelas para tener un panorama rápido de los terrenos asociados a mi organización</td>
            <td>
                <strong>Escenario 1: Visualización de parcelas con registros</strong><br>
                <strong>Dado que</strong> el Agrónomo está autenticado<br>
                <strong>Y</strong> la organización tiene parcelas registradas<br>
                <strong>Cuando</strong> solicite visualizar el listado de parcelas<br>
                <strong>Entonces</strong> el sistema retorna todas las parcelas correspondientes a su organización<br>
                <strong>Escenario 2: Visualización de listado vacío</strong><br>
                <strong>Dado que</strong> el Agrónomo está autenticado<br>
                <strong>Y</strong> la organización no tiene parcelas registradas<br>
                <strong>Cuando</strong> solicite visualizar el listado de parcelas<br>
                <strong>Entonces</strong> el sistema retorna un listado vacío<br>
                <strong>Y</strong> notifica la ausencia de registros<br>
                <strong>Escenario 3: Fallo general</strong><br>
                <strong>Dado que</strong> el Agrónomo solicitó visualizar el listado de parcelas<br>
                <strong>Cuando</strong> la operación falla por pérdida de conexión a internet, tiempo de espera agotado u otro error generalizado<br>
                <strong>Entonces</strong> el sistema no retorna el listado de parcelas ni altera los datos existentes<br>
                <strong>Y</strong> muestra un mensaje alertando sobre la causa del error
            </td>
            <td>EP01</td>
        </tr>
        <tr>
            <td>US03</td>
            <td>Modificar parcela</td>
            <td>Como Agrónomo, quiero editar los datos de una parcela existente para mantener la información de mi organización actualizada</td>
            <td>
                <strong>Escenario 1: Modificación exitosa</strong><br>
                <strong>Dado que</strong> el Agrónomo está autenticado<br>
                <strong>Y</strong> la parcela a modificar pertenece a su organización<br>
                <strong>Y</strong> los nuevos valores ingresados son válidos<br>
                <strong>Cuando</strong> confirme la actualización de la parcela<br>
                <strong>Entonces</strong> el sistema actualiza la información de la parcela<br>
                <strong>Y</strong> muestra un mensaje de éxito<br>
                <strong>Escenario 2: Error al modificar con datos inválidos</strong><br>
                <strong>Dado que</strong> el Agrónomo está autenticado<br>
                <strong>Y</strong> la parcela a modificar pertenece a su organización<br>
                <strong>Y</strong> se ingresan valores inválidos<br>
                <strong>Cuando</strong> confirme la actualización de la parcela<br>
                <strong>Entonces</strong> el sistema evita guardar los cambios<br>
                <strong>Y</strong> alerta sobre el formato incorrecto<br>
                <strong>Escenario 3: Fallo general</strong><br>
                <strong>Dado que</strong> el Agrónomo confirmó la actualización de la parcela<br>
                <strong>Cuando</strong> la operación falla por pérdida de conexión a internet, tiempo de espera agotado u otro error generalizado<br>
                <strong>Entonces</strong> el sistema no actualiza la información de la parcela ni altera los datos existentes<br>
                <strong>Y</strong> muestra un mensaje alertando sobre la causa del error
            </td>
            <td>EP01</td>
        </tr>
        <tr>
            <td>US04</td>
            <td>Eliminar parcela</td>
            <td>Como Agrónomo, quiero eliminar una parcela para remover áreas que ya no son administradas por la organización</td>
            <td>
                <strong>Escenario 1: Eliminación exitosa</strong><br>
                <strong>Dado que</strong> el Agrónomo está autenticado<br>
                <strong>Y</strong> la parcela a eliminar pertenece a su organización<br>
                <strong>Cuando</strong> confirme la eliminación de la parcela<br>
                <strong>Entonces</strong> el sistema remueve la parcela de forma permanente<br>
                <strong>Y</strong> actualiza el listado de parcelas<br>
                <strong>Escenario 2: Cancelación de la eliminación</strong><br>
                <strong>Dado que</strong> el Agrónomo está autenticado<br>
                <strong>Y</strong> se requiere confirmación para eliminar una parcela<br>
                <strong>Cuando</strong> rechace la eliminación de la parcela<br>
                <strong>Entonces</strong> el sistema conserva los datos de la parcela inalterados<br>
                <strong>Escenario 3: Fallo general</strong><br>
                <strong>Dado que</strong> el Agrónomo confirmó la eliminación de la parcela<br>
                <strong>Cuando</strong> la operación falla por pérdida de conexión a internet, tiempo de espera agotado u otro error generalizado<br>
                <strong>Entonces</strong> el sistema no remueve la parcela ni altera los datos existentes<br>
                <strong>Y</strong> muestra un mensaje alertando sobre la causa del error
            </td>
            <td>EP01</td>
        </tr>
        <tr>
            <td>US05</td>
            <td>Crear tarea</td>
            <td>Como Agrónomo, quiero crear una tarea asignando un agricultor y una parcela específicos para planificar las labores de la organización</td>
            <td>
                <strong>Escenario 1: Carga exitosa de listas de selección (Agricultores o Parcelas)</strong><br>
                <strong>Dado que</strong> el Agrónomo está autenticado en el formulario de creación de tarea<br>
                <strong>Y</strong> existen agricultores o parcelas registrados en su organización<br>
                <strong>Cuando</strong> quiera elegir un agricultor o parcela<br>
                <strong>Entonces</strong> el sistema despliega las listas de agricultores y parcelas disponibles para su selección<br>
                <strong>Escenario 2: Listas de selección vacías (Agricultores y Parcelas)</strong><br>
                <strong>Dado que</strong> el Agrónomo está autenticado en el formulario de creación de tarea<br>
                <strong>Y</strong> no existen agricultores o parcelas registrados en su organización<br>
                <strong>Cuando</strong> quiera elegir un agricultor o parcela<br>
                <strong>Entonces</strong> el sistema muestra un mensaje indicando que no hay opciones disponibles, recomendando la creación del recurso faltante<br>
                <strong>Escenario 3: Fallo general al cargar listas de selección</strong><br>
                <strong>Dado que</strong> el Agrónomo intentó seleccionar un agricultor o una parcela<br>
                <strong>Cuando</strong> la operación falle por pérdida de conexión a internet, tiempo de espera agotado u otro error generalizado<br>
                <strong>Entonces</strong> el sistema muestra un mensaje de error sobre la imposibilidad de recuperar los datos<br>
                <strong>Escenario 4: Creación de tarea exitosa</strong><br>
                <strong>Dado que</strong> el Agrónomo está autenticado y las listas de selección han cargado correctamente<br>
                <strong>Y</strong> los valores ingresados son válidos (nombre de tarea no vacío, agricultor asignado seleccionado y parcela seleccionada)<br>
                <strong>Cuando</strong> confirme la creación de la tarea<br>
                <strong>Entonces</strong> el sistema registra la tarea asociándola a la parcela y al agricultor correspondiente<br>
                <strong>Y</strong> muestra un mensaje de confirmación<br>
                <strong>Escenario 5: Error por validación de formulario</strong><br>
                <strong>Dado que</strong> el Agrónomo está autenticado en el formulario de creación de tarea<br>
                <strong>Y</strong> se omiten datos obligatorios (nombre vacío, agricultor sin seleccionar o parcela sin seleccionar)<br>
                <strong>Cuando</strong> confirme la creación de la tarea<br>
                <strong>Entonces</strong> el sistema rechaza el registro de la tarea<br>
                <strong>Y</strong> alerta sobre los campos incorrectos o faltantes<br>
                <strong>Escenario 6: Fallo general al guardar la tarea</strong><br>
                <strong>Dado que</strong> el Agrónomo confirmó la creación de la tarea<br>
                <strong>Cuando</strong> la operación falla por pérdida de conexión a internet, tiempo de espera agotado u otro error generalizado<br>
                <strong>Entonces</strong> el sistema no registra la tarea ni altera los datos existentes<br>
                <strong>Y</strong> muestra un mensaje alertando sobre la causa del error
            </td>
            <td>EP02</td>
        </tr>
<tr>
            <td>US06</td>
            <td>Listado de tareas general</td>
            <td>Como Agrónomo, quiero visualizar un listado de todas las tareas registradas para tener un panorama global de la planificación de labores en mi organización</td>
            <td>
                <strong>Escenario 1: Visualización de tareas con registros</strong><br>
                <strong>Dado que</strong> el Agrónomo está autenticado<br>
                <strong>Y</strong> la organización tiene tareas registradas<br>
                <strong>Cuando</strong> solicite visualizar el listado de tareas<br>
                <strong>Entonces</strong> el sistema retorna todas las tareas correspondientes a su organización<br>
                <strong>Escenario 2: Visualización de listado vacío</strong><br>
                <strong>Dado que</strong> el Agrónomo está autenticado<br>
                <strong>Y</strong> la organización no tiene tareas registradas<br>
                <strong>Cuando</strong> solicite visualizar el listado de tareas<br>
                <strong>Entonces</strong> el sistema retorna un listado vacío<br>
                <strong>Y</strong> notifica la ausencia de registros<br>
                <strong>Escenario 3: Fallo general</strong><br>
                <strong>Dado que</strong> el Agrónomo solicitó visualizar el listado de tareas<br>
                <strong>Cuando</strong> la operación falla por pérdida de conexión a internet, tiempo de espera agotado u otro error generalizado<br>
                <strong>Entonces</strong> el sistema no retorna el listado de tareas ni altera los datos existentes<br>
                <strong>Y</strong> muestra un mensaje alertando sobre la causa del error
            </td>
            <td>EP02</td>
        </tr>
        <tr>
            <td>US07</td>
            <td>Listado de tareas asignadas</td>
            <td>Como Agricultor, quiero visualizar un listado de las tareas específicas asignadas a mi usuario para conocer mis responsabilidades pendientes</td>
            <td>
                <strong>Escenario 1: Visualización de tareas asignadas</strong><br>
                <strong>Dado que</strong> el Agricultor está autenticado<br>
                <strong>Y</strong> tiene tareas asignadas dentro de la organización<br>
                <strong>Cuando</strong> solicite visualizar el listado de tareas asignadas<br>
                <strong>Entonces</strong> el sistema retorna únicamente las tareas vinculadas a su perfil de usuario<br>
                <strong>Escenario 2: Visualización de listado asignado vacío</strong><br>
                <strong>Dado que</strong> el Agricultor está autenticado<br>
                <strong>Y</strong> no tiene tareas asignadas actualmente<br>
                <strong>Cuando</strong> solicite visualizar el listado de tareas asignadas<br>
                <strong>Entonces</strong> el sistema retorna un listado vacío<br>
                <strong>Y</strong> notifica que no existen labores pendientes<br>
                <strong>Escenario 3: Fallo general</strong><br>
                <strong>Dado que</strong> el Agricultor solicitó visualizar el listado de tareas asignadas<br>
                <strong>Cuando</strong> la operación falla por pérdida de conexión a internet, tiempo de espera agotado u otro error generalizado<br>
                <strong>Entonces</strong> el sistema no retorna el listado de tareas ni altera los datos existentes<br>
                <strong>Y</strong> muestra un mensaje alertando sobre la causa del error
            </td>
            <td>EP02</td>
        </tr>
        <tr>
            <td>US08</td>
            <td>Modificar tarea</td>
            <td>Como Agrónomo, quiero editar los datos de una tarea existente para actualizar la planificación o reasignar la labor a otro agricultor</td>
            <td>
                <strong>Escenario 1: Modificación exitosa</strong><br>
                <strong>Dado que</strong> el Agrónomo está autenticado<br>
                <strong>Y</strong> la tarea a modificar pertenece a su organización<br>
                <strong>Y</strong> los nuevos valores ingresados son válidos<br>
                <strong>Cuando</strong> confirme la actualización de la tarea<br>
                <strong>Entonces</strong> el sistema actualiza la información de la tarea<br>
                <strong>Y</strong> muestra un mensaje de éxito<br>
                <strong>Escenario 2: Error al modificar con datos inválidos</strong><br>
                <strong>Dado que</strong> el Agrónomo está autenticado<br>
                <strong>Y</strong> la tarea a modificar pertenece a su organización<br>
                <strong>Y</strong> se omiten campos obligatorios o se ingresan valores inválidos<br>
                <strong>Cuando</strong> confirme la actualización de la tarea<br>
                <strong>Entonces</strong> el sistema evita guardar los cambios<br>
                <strong>Y</strong> alerta sobre el formato incorrecto o datos faltantes<br>
                <strong>Escenario 3: Fallo general</strong><br>
                <strong>Dado que</strong> el Agrónomo confirmó la actualización de la tarea<br>
                <strong>Cuando</strong> la operación falla por pérdida de conexión a internet, tiempo de espera agotado u otro error generalizado<br>
                <strong>Entonces</strong> el sistema no actualiza la información de la tarea ni altera los datos existentes<br>
                <strong>Y</strong> muestra un mensaje alertando sobre la causa del error
            </td>
            <td>EP02</td>
        </tr>
        <tr>
            <td>US09</td>
            <td>Eliminar tarea</td>
            <td>Como Agrónomo, quiero eliminar una tarea para remover de la planificación aquellas labores que ya no son necesarias o eran erradas</td>
            <td>
                <strong>Escenario 1: Eliminación exitosa</strong><br>
                <strong>Dado que</strong> el Agrónomo está autenticado<br>
                <strong>Y</strong> la tarea a eliminar pertenece a su organización<br>
                <strong>Cuando</strong> confirme la eliminación de la tarea<br>
                <strong>Entonces</strong> el sistema remueve la tarea de forma permanente<br>
                <strong>Y</strong> actualiza el listado de tareas<br>
                <strong>Escenario 2: Cancelación de la eliminación</strong><br>
                <strong>Dado que</strong> el Agrónomo está autenticado<br>
                <strong>Y</strong> se requiere confirmación para eliminar una tarea<br>
                <strong>Cuando</strong> rechace la eliminación de la tarea<br>
                <strong>Entonces</strong> el sistema conserva los datos de la tarea inalterados<br>
                <strong>Escenario 3: Fallo general</strong><br>
                <strong>Dado que</strong> el Agrónomo confirmó la eliminación de la tarea<br>
                <strong>Cuando</strong> la operación falla por pérdida de conexión a internet, tiempo de espera agotado u otro error generalizado<br>
                <strong>Entonces</strong> el sistema no remueve la tarea ni altera los datos existentes<br>
                <strong>Y</strong> muestra un mensaje alertando sobre la causa del error
            </td>
            <td>EP02</td>
        </tr>
        <tr>
            <td>US10</td>
            <td>Agregar checklist a tarea</td>
            <td>Como Agrónomo, quiero agregar un checklist de subtareas al crear o editar una tarea para detallar los pasos específicos a seguir en la labor</td>
            <td>
                <strong>Escenario 1: Intención de agregar checklist</strong><br>
                <strong>Dado que</strong> el Agrónomo está autenticado en el formulario de creación o edición de tarea<br>
                <strong>Cuando</strong> requiera agregar actividades específicas a la tarea<br>
                <strong>Entonces</strong> el sistema habilita la sección del checklist<br>
                <strong>Y</strong> solicita la lista de actividades<br>
                <strong>Escenario 2: Añadir actividad a la lista</strong><br>
                <strong>Dado que</strong> el Agrónomo se encuentra en la sección del checklist<br>
                <strong>Cuando</strong> decida añadir una nueva actividad<br>
                <strong>Entonces</strong> el sistema agrega un nuevo ítem vacío a la lista visible para su edición<br>
                <strong>Escenario 3: Quitar actividad de la lista</strong><br>
                <strong>Dado que</strong> el Agrónomo se encuentra en la sección del checklist<br>
                <strong>Y</strong> existe al menos una actividad en la lista visible<br>
                <strong>Cuando</strong> decida quitar una actividad específica<br>
                <strong>Entonces</strong> el sistema elimina dicho ítem de la lista visible<br>
                <strong>Escenario 4: Guardado exitoso del checklist</strong><br>
                <strong>Dado que</strong> el Agrónomo se encuentra creando o editando una tarea<br>
                <strong>Y</strong> la lista del checklist contiene al menos un ítem con texto válido no vacío<br>
                <strong>Cuando</strong> confirme el guardado de la tarea<br>
                <strong>Entonces</strong> el sistema registra el checklist asociado a la tarea<br>
                <strong>Y</strong> muestra un mensaje de confirmación<br>
                <strong>Escenario 5: Error por checklist sin ítems</strong><br>
                <strong>Dado que</strong> el Agrónomo se encuentra creando o editando una tarea<br>
                <strong>Y</strong> la sección del checklist fue habilitada pero no contiene ítems o estos se encuentran vacíos<br>
                <strong>Cuando</strong> confirme el guardado de la tarea<br>
                <strong>Entonces</strong> el sistema rechaza el registro de la tarea<br>
                <strong>Y</strong> alerta que se debe incluir al menos una actividad válida<br>
                <strong>Escenario 6: Fallo general al guardar</strong><br>
                <strong>Dado que</strong> el Agrónomo confirmó el guardado de la tarea con el checklist<br>
                <strong>Cuando</strong> la operación falle por pérdida de conexión a internet, tiempo de espera agotado u otro error generalizado<br>
                <strong>Entonces</strong> el sistema no registra el checklist ni altera los datos existentes<br>
                <strong>Y</strong> muestra un mensaje alertando sobre la causa del error
            </td>
            <td>EP04</td>
        </tr>
        <tr>
            <td>US11</td>
            <td>Modificar checklist de tarea</td>
            <td>Como Agrónomo, quiero modificar los textos de los ítems de un checklist durante la edición de una tarea para actualizar las indicaciones en las tareas que he asignado</td>
            <td>
                <strong>Escenario 1: Modificación exitosa</strong><br>
                <strong>Dado que</strong> el Agrónomo está autenticado en el formulario de edición de tarea<br>
                <strong>Y</strong> la tarea posee un checklist existente<br>
                <strong>Y</strong> los textos modificados de los ítems son válidos y no vacíos<br>
                <strong>Cuando</strong> confirme la actualización de la tarea<br>
                <strong>Entonces</strong> el sistema actualiza los ítems del checklist<br>
                <strong>Y</strong> muestra un mensaje de éxito<br>
                <strong>Escenario 2: Error al modificar con ítem vacío</strong><br>
                <strong>Dado que</strong> el Agrónomo está autenticado en el formulario de edición de tarea<br>
                <strong>Y</strong> la tarea posee un checklist existente<br>
                <strong>Y</strong> se modifica un ítem dejándolo sin texto<br>
                <strong>Cuando</strong> confirme la actualización de la tarea<br>
                <strong>Entonces</strong> el sistema evita guardar los cambios<br>
                <strong>Y</strong> alerta sobre el formato incorrecto<br>
                <strong>Escenario 3: Fallo general</strong><br>
                <strong>Dado que</strong> el Agrónomo confirmó la actualización de la tarea con checklist<br>
                <strong>Cuando</strong> la operación falla por pérdida de conexión a internet, tiempo de espera agotado u otro error generalizado<br>
                <strong>Entonces</strong> el sistema no actualiza la información ni altera los datos existentes<br>
                <strong>Y</strong> muestra un mensaje alertando sobre la causa del error
            </td>
            <td>EP02</td>
        </tr>
        <tr>
            <td>US12</td>
            <td>Eliminar checklist de tarea</td>
            <td>Como Agrónomo, quiero eliminar ítems específicos o la totalidad del checklist durante la edición de la tarea para mantener la tarea limpia de indicaciones que ya no sean relevantes</td>
            <td>
                <strong>Escenario 1: Eliminación directa de ítem o checklist</strong><br>
                <strong>Dado que</strong> el Agrónomo está autenticado en el formulario de edición de tarea<br>
                <strong>Y</strong> la tarea posee un checklist existente<br>
                <strong>Cuando</strong> confirme la eliminación de elementos del checklist y actualice la tarea<br>
                <strong>Entonces</strong> el sistema remueve los ítems seleccionados<br>
                <strong>Y</strong> muestra un mensaje de éxito<br>
                <strong>Escenario 2: Eliminación en cascada de checklist</strong><br>
                <strong>Dado que</strong> el Agrónomo está autenticado<br>
                <strong>Y</strong> la tarea a eliminar posee un checklist asociado<br>
                <strong>Cuando</strong> confirme la eliminación de la tarea contenedora<br>
                <strong>Entonces</strong> el sistema remueve la tarea de forma permanente<br>
                <strong>Y</strong> elimina en cascada todos los ítems del checklist asociado<br>
                <strong>Escenario 3: Fallo general</strong><br>
                <strong>Dado que</strong> el Agrónomo confirmó la eliminación de elementos o de la tarea contenedora<br>
                <strong>Cuando</strong> la operación falla por pérdida de conexión a internet, tiempo de espera agotado u otro error generalizado<br>
                <strong>Entonces</strong> el sistema no remueve los datos de los ítems ni de la tarea<br>
                <strong>Y</strong> muestra un mensaje alertando sobre la causa del error
            </td>
            <td>EP02</td>
        </tr>
        <tr>
            <td>US13</td>
            <td>Completar tarea</td>
            <td>Como Agricultor asignado, quiero marcar una tarea como completada para registrar la finalización de mi labor asignada en la parcela</td>
            <td>
                <strong>Escenario 1: Completar tarea sin checklist</strong><br>
                <strong>Dado que</strong> el Agricultor está autenticado y tiene una tarea asignada en curso<br>
                <strong>Y</strong> la tarea no posee un checklist asociado<br>
                <strong>Cuando</strong> confirme la finalización de la tarea<br>
                <strong>Entonces</strong> el sistema actualiza el estado de la tarea a "Completada"<br>
                <strong>Y</strong> muestra un mensaje de confirmación<br>
                <strong>Escenario 2: Completar tarea con checklist completo</strong><br>
                <strong>Dado que</strong> el Agricultor está autenticado y tiene una tarea asignada en curso<br>
                <strong>Y</strong> la tarea posee un checklist asociado<br>
                <strong>Y</strong> todos los ítems del checklist han sido marcados como realizados<br>
                <strong>Cuando</strong> confirme la finalización de la tarea<br>
                <strong>Entonces</strong> el sistema actualiza el estado de la tarea a "Completada"<br>
                <strong>Y</strong> muestra un mensaje de confirmación<br>
                <strong>Escenario 3: Error por checklist pendiente</strong><br>
                <strong>Dado que</strong> el Agricultor está autenticado y tiene una tarea asignada en curso<br>
                <strong>Y</strong> la tarea posee un checklist asociado<br>
                <strong>Y</strong> existen ítems del checklist sin marcar como realizados<br>
                <strong>Cuando</strong> confirme la finalización de la tarea<br>
                <strong>Entonces</strong> el sistema rechaza la actualización de estado<br>
                <strong>Y</strong> alerta que se deben completar todos los pasos antes de finalizar la labor<br>
                <strong>Escenario 4: Fallo general al guardar</strong><br>
                <strong>Dado que</strong> el Agricultor confirmó la finalización de la tarea<br>
                <strong>Cuando</strong> la operación falle por pérdida de conexión a internet, tiempo de espera agotado u otro error generalizado<br>
                <strong>Entonces</strong> el sistema no actualiza el estado de la tarea ni altera los datos existentes<br>
                <strong>Y</strong> muestra un mensaje alertando sobre la causa del error
            </td>
            <td>EP04</td>
        </tr>
        <tr>
            <td>US14</td>
            <td>Crear organización</td>
            <td>Como Agrónomo, quiero crear una organización para centralizar a mi equipo de trabajo y gestionar las parcelas de manera conjunta</td>
            <td>
                <strong>Escenario 1: Creación exitosa y asignación de dueño</strong><br>
                <strong>Dado que</strong> el Agrónomo está autenticado<br>
                <strong>Y</strong> los valores ingresados son válidos (nombre no vacío, descripción no vacía y ubicación no vacía)<br>
                <strong>Cuando</strong> confirme la creación de la organización<br>
                <strong>Entonces</strong> el sistema registra la organización<br>
                <strong>Y</strong> lo asigna automáticamente como miembro con el rol de dueño (Owner)<br>
                <strong>Y</strong> muestra un mensaje de confirmación<br>
                <strong>Escenario 2: Error por validación de campos</strong><br>
                <strong>Dado que</strong> el Agrónomo está autenticado<br>
                <strong>Y</strong> se omiten datos obligatorios o se ingresan valores inválidos<br>
                <strong>Cuando</strong> confirme la creación de la organización<br>
                <strong>Entonces</strong> el sistema rechaza el registro de la organización<br>
                <strong>Y</strong> alerta sobre los campos incorrectos o faltantes<br>
                <strong>Escenario 3: Fallo general</strong><br>
                <strong>Dado que</strong> el Agrónomo confirmó la creación de la organización<br>
                <strong>Cuando</strong> la operación falla por pérdida de conexión a internet, tiempo de espera agotado u otro error generalizado<br>
                <strong>Entonces</strong> el sistema no registra la organización ni altera los datos existentes<br>
                <strong>Y</strong> muestra un mensaje alertando sobre la causa del error
            </td>
            <td>EP03</td>
        </tr>
        <tr>
            <td>US15</td>
            <td>Listado de organizaciones</td>
            <td>Como Agrónomo, quiero visualizar el listado de mis organizaciones para acceder rápidamente a su información y gestión</td>
            <td>
                <strong>Escenario 1: Visualización con registros</strong><br>
                <strong>Dado que</strong> el Agrónomo está autenticado<br>
                <strong>Y</strong> pertenece a al menos una organización registrada<br>
                <strong>Cuando</strong> solicite visualizar el listado de organizaciones<br>
                <strong>Entonces</strong> el sistema retorna las organizaciones a las que se encuentra vinculado<br>
                <strong>Escenario 2: Visualización de listado vacío</strong><br>
                <strong>Dado que</strong> el Agrónomo está autenticado<br>
                <strong>Y</strong> no pertenece a ninguna organización registrada<br>
                <strong>Cuando</strong> solicite visualizar el listado de organizaciones<br>
                <strong>Entonces</strong> el sistema retorna un listado vacío<br>
                <strong>Y</strong> notifica la ausencia de registros<br>
                <strong>Escenario 3: Fallo general</strong><br>
                <strong>Dado que</strong> el Agrónomo solicitó visualizar el listado de organizaciones<br>
                <strong>Cuando</strong> la operación falla por pérdida de conexión a internet, tiempo de espera agotado u otro error generalizado<br>
                <strong>Entonces</strong> el sistema no retorna el listado ni altera los datos existentes<br>
                <strong>Y</strong> muestra un mensaje alertando sobre la causa del error
            </td>
            <td>EP03</td>
        </tr>
        <tr>
            <td>US16</td>
            <td>Modificar organización</td>
            <td>Como Agrónomo dueño, quiero editar los datos de mi organización para mantener la información corporativa actualizada</td>
            <td>
                <strong>Escenario 1: Modificación exitosa</strong><br>
                <strong>Dado que</strong> el Agrónomo está autenticado con rol de dueño de la organización<br>
                <strong>Y</strong> los nuevos valores ingresados son válidos<br>
                <strong>Cuando</strong> confirme la actualización de la organización<br>
                <strong>Entonces</strong> el sistema actualiza la información<br>
                <strong>Y</strong> muestra un mensaje de éxito<br>
                <strong>Escenario 2: Error por datos inválidos</strong><br>
                <strong>Dado que</strong> el Agrónomo está autenticado con rol de dueño de la organización<br>
                <strong>Y</strong> se omiten campos obligatorios o se ingresan valores inválidos<br>
                <strong>Cuando</strong> confirme la actualización de la organización<br>
                <strong>Entonces</strong> el sistema evita guardar los cambios<br>
                <strong>Y</strong> alerta sobre el formato incorrecto o faltante<br>
                <strong>Escenario 3: Error por falta de permisos</strong><br>
                <strong>Dado que</strong> el usuario está autenticado pero no posee el rol de dueño de la organización<br>
                <strong>Cuando</strong> confirme la actualización de la organización<br>
                <strong>Entonces</strong> el sistema rechaza la operación<br>
                <strong>Y</strong> alerta que no posee los permisos necesarios<br>
                <strong>Escenario 4: Fallo general</strong><br>
                <strong>Dado que</strong> el Agrónomo confirmó la actualización de la organización<br>
                <strong>Cuando</strong> la operación falla por pérdida de conexión a internet, tiempo de espera agotado u otro error generalizado<br>
                <strong>Entonces</strong> el sistema no actualiza la información ni altera los datos existentes<br>
                <strong>Y</strong> muestra un mensaje alertando sobre la causa del error
            </td>
            <td>EP03</td>
        </tr>
        <tr>
            <td>US17</td>
            <td>Eliminar organización</td>
            <td>Como Agrónomo dueño, quiero eliminar mi organización para dar de baja el espacio de trabajo de manera definitiva</td>
            <td>
                <strong>Escenario 1: Eliminación exitosa y efecto en cascada</strong><br>
                <strong>Dado que</strong> el Agrónomo está autenticado con rol de dueño de la organización<br>
                <strong>Cuando</strong> confirme la eliminación de la organización<br>
                <strong>Entonces</strong> el sistema remueve la organización de forma permanente<br>
                <strong>Y</strong> elimina en cascada todas las invitaciones pendientes y las vinculaciones de sus miembros<br>
                <strong>Y</strong> muestra un mensaje de confirmación<br>
                <strong>Y</strong> actualiza el listado de organizaciones del usuario<br>
                <strong>Escenario 2: Cancelación de la eliminación</strong><br>
                <strong>Dado que</strong> el Agrónomo está autenticado con rol de dueño de la organización<br>
                <strong>Y</strong> se requiere confirmación para eliminar la organización<br>
                <strong>Cuando</strong> rechace la eliminación de la organización<br>
                <strong>Entonces</strong> el sistema conserva los datos de la organización, invitaciones y miembros inalterados<br>
                <strong>Escenario 3: Error por falta de permisos</strong><br>
                <strong>Dado que</strong> el usuario está autenticado pero no posee el rol de dueño de la organización<br>
                <strong>Cuando</strong> confirme la eliminación de la organización<br>
                <strong>Entonces</strong> el sistema rechaza la operación<br>
                <strong>Y</strong> alerta que no posee los permisos necesarios<br>
                <strong>Escenario 4: Fallo general</strong><br>
                <strong>Dado que</strong> el Agrónomo confirmó la eliminación de la organización<br>
                <strong>Cuando</strong> la operación falla por pérdida de conexión a internet, tiempo de espera agotado u otro error generalizado<br>
                <strong>Entonces</strong> el sistema no remueve la organización ni altera los datos existentes<br>
                <strong>Y</strong> muestra un mensaje alertando sobre la causa del error
            </td>
            <td>EP03</td>
        </tr>
        <tr>
            <td>US18</td>
            <td>Crear invitación</td>
            <td>Como Agrónomo dueño, quiero enviar una invitación por correo electrónico para incorporar nuevos agricultores a la organización</td>
            <td>
                <strong>Escenario 1: Envío de invitación exitoso</strong><br>
                <strong>Dado que</strong> el Agrónomo está autenticado con rol de dueño de la organización<br>
                <strong>Y</strong> el correo electrónico ingresado tiene un formato válido y no existe una invitación previa activa para dicho usuario<br>
                <strong>Cuando</strong> confirme el envío de la invitación<br>
                <strong>Entonces</strong> el sistema registra la invitación con el estado "Pendiente"<br>
                <strong>Y</strong> muestra un mensaje de confirmación<br>
                <strong>Escenario 2: Error por correo inválido o duplicado</strong><br>
                <strong>Dado que</strong> el Agrónomo está autenticado con rol de dueño de la organización<br>
                <strong>Y</strong> el correo ingresado es inválido o ya posee una invitación pendiente en la organización<br>
                <strong>Cuando</strong> confirme el envío de la invitación<br>
                <strong>Entonces</strong> el sistema rechaza la operación<br>
                <strong>Y</strong> alerta sobre el inconveniente detectado<br>
                <strong>Escenario 3: Fallo general</strong><br>
                <strong>Dado que</strong> el Agrónomo confirmó el envío de la invitación<br>
                <strong>Cuando</strong> la operación falla por pérdida de conexión a internet, tiempo de espera agotado u otro error generalizado<br>
                <strong>Entonces</strong> el sistema no registra la invitación ni altera los datos existentes<br>
                <strong>Y</strong> muestra un mensaje alertando sobre la causa del error
            </td>
            <td>EP03</td>
        </tr>
        <tr>
            <td>US19</td>
            <td>Listado de invitaciones</td>
            <td>Como Agrónomo dueño, quiero visualizar las invitaciones enviadas filtrando por su estado para gestionar las solicitudes de ingreso pendientes y procesadas</td>
            <td>
                <strong>Escenario 1: Visualización con filtros (Pendientes / No pendientes)</strong><br>
                <strong>Dado que</strong> el Agrónomo está autenticado con rol de dueño de la organización<br>
                <strong>Y</strong> existen invitaciones registradas en el sistema para su organización<br>
                <strong>Cuando</strong> solicite el listado aplicando un filtro de estado específico (pendientes o no pendientes)<br>
                <strong>Entonces</strong> el sistema retorna exclusivamente las invitaciones que coincidan con el criterio seleccionado<br>
                <strong>Escenario 2: Visualización de listado filtrado vacío</strong><br>
                <strong>Dado que</strong> el Agrónomo está autenticado con rol de dueño de la organización<br>
                <strong>Y</strong> no existen invitaciones que correspondan al filtro de estado seleccionado<br>
                <strong>Cuando</strong> solicite el listado de invitaciones<br>
                <strong>Entonces</strong> el sistema retorna una lista vacía<br>
                <strong>Y</strong> notifica la ausencia de registros para ese criterio<br>
                <strong>Escenario 3: Fallo general</strong><br>
                <strong>Dado que</strong> el Agrónomo solicitó visualizar el listado de invitaciones<br>
                <strong>Cuando</strong> la operación falla por pérdida de conexión a internet, tiempo de espera agotado u otro error generalizado<br>
                <strong>Entonces</strong> el sistema no retorna la información ni altera los datos existentes<br>
                <strong>Y</strong> muestra un mensaje alertando sobre la causa del error
            </td>
            <td>EP03</td>
        </tr>
        <tr>
            <td>US20</td>
            <td>Eliminar invitación</td>
            <td>Como Agrónomo dueño, quiero eliminar una invitación pendiente para anular el acceso a un usuario antes de que sea aceptado</td>
            <td>
                <strong>Escenario 1: Eliminación de invitación exitosa</strong><br>
                <strong>Dado que</strong> el Agrónomo está autenticado con rol de dueño de la organización<br>
                <strong>Y</strong> la invitación seleccionada se encuentra en estado "Pendiente"<br>
                <strong>Cuando</strong> confirme la eliminación de la invitación<br>
                <strong>Entonces</strong> el sistema remueve la invitación de forma permanente<br>
                <strong>Y</strong> muestra un mensaje de confirmación<br>
                <strong>Y</strong> actualiza el listado de invitaciones de la organización<br>
                <strong>Escenario 2: Cancelación de la eliminación</strong><br>
                <strong>Dado que</strong> el Agrónomo está autenticado con rol de dueño de la organización<br>
                <strong>Y</strong> se requiere confirmación para eliminar la invitación<br>
                <strong>Cuando</strong> rechace la eliminación de la invitación<br>
                <strong>Entonces</strong> el sistema conserva el registro de la invitación inalterado<br>
                <strong>Escenario 3: Fallo general</strong><br>
                <strong>Dado que</strong> el Agrónomo confirmó la eliminación de la invitación<br>
                <strong>Cuando</strong> la operación falla por pérdida de conexión a internet, tiempo de espera agotado u otro error generalizado<br>
                <strong>Entonces</strong> el sistema no remueve la invitación ni altera los datos existentes<br>
                <strong>Y</strong> muestra un mensaje alertando sobre la causa del error
            </td>
            <td>EP03</td>
        </tr>
        <tr>
            <td>US21</td>
            <td>Listar invitaciones recibidas</td>
            <td>Como Agricultor, quiero visualizar un listado de las invitaciones que se me han enviado para conocer qué organizaciones desean incorporarme</td>
            <td>
                <strong>Escenario 1: Visualización de invitaciones recibidas</strong><br>
                <strong>Dado que</strong> el Agricultor está autenticado<br>
                <strong>Y</strong> posee invitaciones enviadas a su usuario<br>
                <strong>Cuando</strong> solicite visualizar el listado de invitaciones<br>
                <strong>Entonces</strong> el sistema retorna las invitaciones que le corresponden<br>
                <strong>Escenario 2: Visualización de listado vacío</strong><br>
                <strong>Dado que</strong> el Agricultor está autenticado<br>
                <strong>Y</strong> no posee ninguna invitación enviada a su usuario<br>
                <strong>Cuando</strong> solicite visualizar el listado de invitaciones<br>
                <strong>Entonces</strong> el sistema retorna un listado vacío<br>
                <strong>Y</strong> notifica la ausencia de solicitudes<br>
                <strong>Escenario 3: Fallo general</strong><br>
                <strong>Dado que</strong> el Agricultor solicitó visualizar el listado de invitaciones<br>
                <strong>Cuando</strong> la operación falla por pérdida de conexión a internet, tiempo de espera agotado u otro error generalizado<br>
                <strong>Entonces</strong> el sistema no retorna la información ni altera los datos existentes<br>
                <strong>Y</strong> muestra un mensaje alertando sobre la causa del error
            </td>
            <td>EP03</td>
        </tr>
        <tr>
            <td>US22</td>
            <td>Aceptar invitación</td>
            <td>Como Agricultor, quiero aceptar una invitación pendiente para ingresar como miembro activo a la organización</td>
            <td>
                <strong>Escenario 1: Aceptación exitosa</strong><br>
                <strong>Dado que</strong> el Agricultor está autenticado<br>
                <strong>Y</strong> seleccionó una invitación dirigida a él en estado "Pendiente"<br>
                <strong>Cuando</strong> confirme la aceptación de la invitación<br>
                <strong>Entonces</strong> el sistema actualiza el estado de la invitación a "Aceptada"<br>
                <strong>Y</strong> registra al Agricultor como miembro de la organización emisora<br>
                <strong>Y</strong> muestra un mensaje de éxito<br>
                <strong>Escenario 2: Fallo general</strong><br>
                <strong>Dado que</strong> el Agricultor confirmó la aceptación de la invitación<br>
                <strong>Cuando</strong> la operación falla por pérdida de conexión a internet, tiempo de espera agotado u otro error generalizado<br>
                <strong>Entonces</strong> el sistema no actualiza el estado ni altera los datos existentes<br>
                <strong>Y</strong> muestra un mensaje alertando sobre la causa del error
            </td>
            <td>EP03</td>
        </tr>
        <tr>
            <td>US23</td>
            <td>Rechazar invitación</td>
            <td>Como Agricultor, quiero declinar una invitación pendiente para notificar mi rechazo a unirme a la organización</td>
            <td>
                <strong>Escenario 1: Rechazo exitoso</strong><br>
                <strong>Dado que</strong> el Agricultor está autenticado<br>
                <strong>Y</strong> seleccionó una invitación dirigida a él en estado "Pendiente"<br>
                <strong>Cuando</strong> confirme el rechazo de la invitación<br>
                <strong>Entonces</strong> el sistema actualiza el estado de la invitación a "Rechazada"<br>
                <strong>Y</strong> muestra un mensaje de confirmación<br>
                <strong>Escenario 2: Fallo general</strong><br>
                <strong>Dado que</strong> el Agricultor confirmó el rechazo de la invitación<br>
                <strong>Cuando</strong> la operación falla por pérdida de conexión a internet, tiempo de espera agotado u otro error generalizado<br>
                <strong>Entonces</strong> el sistema no actualiza el estado ni altera los datos existentes<br>
                <strong>Y</strong> muestra un mensaje alertando sobre la causa del error
            </td>
            <td>EP03</td>
        </tr>
        <tr>
            <td>US24</td>
            <td>Listar miembros de la organización</td>
            <td>Como Agrónomo dueño, quiero visualizar un listado de los miembros vinculados a mi organización para conocer el equipo de trabajo actual</td>
            <td>
                <strong>Escenario 1: Visualización con miembros registrados</strong><br>
                <strong>Dado que</strong> el Agrónomo está autenticado con rol de dueño de la organización<br>
                <strong>Y</strong> la organización tiene miembros activos vinculados<br>
                <strong>Cuando</strong> solicite visualizar el listado de miembros<br>
                <strong>Entonces</strong> el sistema retorna los usuarios que pertenecen a la organización<br>
                <strong>Escenario 2: Visualización sin miembros adicionales</strong><br>
                <strong>Dado que</strong> el Agrónomo está autenticado con rol de dueño de la organización<br>
                <strong>Y</strong> no existen otros miembros vinculados a la organización<br>
                <strong>Cuando</strong> solicite visualizar el listado de miembros<br>
                <strong>Entonces</strong> el sistema retorna un listado únicamente con sus propios datos<br>
                <strong>Y</strong> notifica la ausencia de otros integrantes<br>
                <strong>Escenario 3: Fallo general</strong><br>
                <strong>Dado que</strong> el Agrónomo solicitó visualizar el listado de miembros<br>
                <strong>Cuando</strong> la operación falla por pérdida de conexión a internet, tiempo de espera agotado u otro error generalizado<br>
                <strong>Entonces</strong> el sistema no retorna la información ni altera los datos existentes<br>
                <strong>Y</strong> muestra un mensaje alertando sobre la causa del error
            </td>
            <td>EP03</td>
        </tr>
        <tr>
            <td>US25</td>
            <td>Eliminar miembro</td>
            <td>Como Agrónomo dueño, quiero remover a un miembro de la organización para revocar su acceso y desvincularlo del equipo de trabajo</td>
            <td>
                <strong>Escenario 1: Eliminación de miembro exitosa</strong><br>
                <strong>Dado que</strong> el Agrónomo está autenticado con rol de dueño de la organización<br>
                <strong>Y</strong> seleccionó a un miembro válido de la organización distinto a sí mismo<br>
                <strong>Cuando</strong> confirme la eliminación del miembro<br>
                <strong>Entonces</strong> el sistema remueve al usuario de la organización de forma permanente<br>
                <strong>Y</strong> actualiza el listado de miembros<br>
                <strong>Y</strong> muestra un mensaje de éxito<br>
                <strong>Escenario 2: Intento de auto-eliminación</strong><br>
                <strong>Dado que</strong> el Agrónomo está autenticado con rol de dueño de la organización<br>
                <strong>Y</strong> la organización requiere mantener a su creador<br>
                <strong>Cuando</strong> confirme la eliminación de su propio usuario<br>
                <strong>Entonces</strong> el sistema rechaza la operación<br>
                <strong>Y</strong> alerta que el dueño no puede ser removido<br>
                <strong>Escenario 3: Cancelación de la eliminación</strong><br>
                <strong>Dado que</strong> el Agrónomo está autenticado con rol de dueño de la organización<br>
                <strong>Y</strong> se requiere confirmación para eliminar a un miembro<br>
                <strong>Cuando</strong> rechace la eliminación del miembro<br>
                <strong>Entonces</strong> el sistema conserva la vinculación del usuario inalterada<br>
                <strong>Escenario 4: Fallo general</strong><br>
                <strong>Dado que</strong> el Agrónomo confirmó la eliminación del miembro<br>
                <strong>Cuando</strong> la operación falla por pérdida de conexión a internet, tiempo de espera agotado u otro error generalizado<br>
                <strong>Entonces</strong> el sistema no remueve al miembro ni altera los datos existentes<br>
                <strong>Y</strong> muestra un mensaje alertando sobre la causa del error
            </td>
            <td>EP03</td>
        </tr>
        <tr>
            <td>US26</td>
            <td>Consultar clima y recomendaciones técnicas</td>
            <td>Como usuario, quiero consultar el pronóstico del clima según mi ubicación y recibir recomendaciones de actividades para planificar mis labores de manera eficiente</td>
            <td>
                <strong>Escenario 1: Visualización exitosa de clima y recomendaciones</strong><br>
                <strong>Dado que</strong> el usuario está autenticado y ha definido una ubicación<br>
                <strong>Cuando</strong> solicite la información climática<br>
                <strong>Entonces</strong> el sistema muestra el pronóstico del tiempo actual para dicha ubicación<br>
                <strong>Y</strong> despliega una lista de recomendaciones técnicas con las actividades apropiadas para realizar bajo esas condiciones<br>
                <strong>Escenario 2: Cambio de ubicación para consulta</strong><br>
                <strong>Dado que</strong> el usuario visualiza la información climática<br>
                <strong>Cuando</strong> decida cambiar la ubicación de consulta por una nueva<br>
                <strong>Entonces</strong> el sistema actualiza el pronóstico y las recomendaciones técnicas de forma inmediata según el nuevo lugar seleccionado<br>
                <strong>Escenario 3: Fallo general</strong><br>
                <strong>Dado que</strong> el usuario solicitó la información climática o intentó cambiar la ubicación<br>
                <strong>Cuando</strong> la operación falla por pérdida de conexión a internet, tiempo de espera agotado u otro error generalizado<br>
                <strong>Entonces</strong> el sistema no actualiza la información climática ni las recomendaciones<br>
                <strong>Y</strong> muestra un mensaje alertando sobre la causa del error
            </td>
            <td>EP04</td>
        </tr>
        <tr>
            <td>US27</td>
            <td>Visualizar resumen estadístico de tareas</td>
            <td>Como Agrónomo dueño, quiero visualizar un resumen estadístico de las tareas de mi organización para analizar el desempeño y avance de las labores</td>
            <td>
                <strong>Escenario 1: Visualización de estadísticas con datos</strong><br>
                <strong>Dado que</strong> el Agrónomo está autenticado con rol de dueño de la organización<br>
                <strong>Y</strong> existen tareas registradas en el sistema para su organización<br>
                <strong>Cuando</strong> solicite visualizar el resumen estadístico<br>
                <strong>Entonces</strong> el sistema retorna indicadores métricos sobre el estado, cumplimiento y distribución de las tareas de la organización<br>
                <strong>Escenario 2: Visualización de resumen sin datos</strong><br>
                <strong>Dado que</strong> el Agrónomo está autenticado con rol de dueño de la organización<br>
                <strong>Y</strong> la organización no cuenta con tareas registradas<br>
                <strong>Cuando</strong> solicite visualizar el resumen estadístico<br>
                <strong>Entonces</strong> el sistema retorna el tablero con valores en cero<br>
                <strong>Y</strong> notifica que no existen datos suficientes para generar métricas<br>
                <strong>Escenario 3: Fallo general</strong><br>
                <strong>Dado que</strong> el Agrónomo solicitó visualizar el resumen estadístico<br>
                <strong>Cuando</strong> la operación falla por pérdida de conexión a internet, tiempo de espera agotado u otro error generalizado<br>
                <strong>Entonces</strong> el sistema no retorna la información estadística ni altera los registros<br>
                <strong>Y</strong> muestra un mensaje alertando sobre la causa del error
            </td>
            <td>EP04</td>
        </tr>
        <tr>
            <td>US28</td>
            <td>Exportar resumen estadístico a PDF</td>
            <td>Como Agrónomo dueño, quiero exportar el resumen estadístico de tareas a un archivo PDF para compartir los reportes de gestión fuera de la plataforma</td>
            <td>
                <strong>Escenario 1: Exportación exitosa</strong><br>
                <strong>Dado que</strong> el Agrónomo visualiza el resumen estadístico de su organización con datos válidos<br>
                <strong>Cuando</strong> confirme la exportación del reporte<br>
                <strong>Entonces</strong> el sistema genera un archivo en formato PDF con las métricas visualizadas y lo descarga en el dispositivo del usuario<br>
                <strong>Escenario 2: Fallo general en la generación</strong><br>
                <strong>Dado que</strong> el Agrónomo confirmó la exportación del reporte estadístico<br>
                <strong>Cuando</strong> la operación falla por pérdida de conexión a internet o un error interno al generar el documento<br>
                <strong>Entonces</strong> el sistema interrumpe la descarga<br>
                <strong>Y</strong> muestra un mensaje alertando sobre la imposibilidad de generar el archivo en ese momento
            </td>
            <td>EP04</td>
        </tr>
<tr>
            <td>US29</td>
            <td>Registrar cuenta de usuario</td>
            <td>Como usuario visitante, quiero registrar una cuenta con mi nombre, apellido, correo y contraseña para acceder a las funcionalidades de la plataforma</td>
            <td>
                <strong>Escenario 1: Registro exitoso con consentimiento</strong><br>
                <strong>Dado que</strong> el usuario no posee una cuenta registrada<br>
                <strong>Y</strong> los datos ingresados son válidos (nombre, apellido, correo y contraseña)<br>
                <strong>Y</strong> marca explícitamente la casilla de consentimiento de uso de datos personales<br>
                <strong>Cuando</strong> confirme el registro de la cuenta<br>
                <strong>Entonces</strong> el sistema registra la cuenta de usuario<br>
                <strong>Y</strong> muestra un mensaje de confirmación<br>
                <strong>Escenario 2: Error por falta de consentimiento o datos inválidos</strong><br>
                <strong>Dado que</strong> el usuario intenta registrar una cuenta<br>
                <strong>Y</strong> se omiten datos obligatorios, se ingresan valores inválidos o no se marca la casilla de consentimiento de uso de datos personales<br>
                <strong>Cuando</strong> confirme el registro de la cuenta<br>
                <strong>Entonces</strong> el sistema rechaza la operación<br>
                <strong>Y</strong> alerta sobre los campos incorrectos o la falta de consentimiento<br>
                <strong>Escenario 3: Fallo general</strong><br>
                <strong>Dado que</strong> el usuario confirmó el registro de la cuenta<br>
                <strong>Cuando</strong> la operación falla por pérdida de conexión a internet, tiempo de espera agotado u otro error generalizado<br>
                <strong>Entonces</strong> el sistema no registra la cuenta ni altera los datos existentes<br>
                <strong>Y</strong> muestra un mensaje alertando sobre la causa del error<br>
                <br>
                * <strong>Consideración legal:</strong> La marcación de la casilla de consentimiento de uso de datos personales es un requerimiento estrictamente obligatorio para finalizar la transacción, en cumplimiento directo con la Ley de Protección de Datos Personales.
            </td>
            <td>EP05</td>
        </tr>
        <tr>
            <td>US30</td>
            <td>Iniciar sesión</td>
            <td>Como usuario registrado, quiero iniciar sesión con mi correo y contraseña para acceder a las funcionalidades de la plataforma</td>
            <td>
                <strong>Escenario 1: Inicio de sesión exitoso</strong><br>
                <strong>Dado que</strong> el usuario posee una cuenta activa<br>
                <strong>Y</strong> las credenciales ingresadas son válidas (correo y contraseña)<br>
                <strong>Cuando</strong> confirme el inicio de sesión<br>
                <strong>Entonces</strong> el sistema autentica al usuario<br>
                <strong>Y</strong> concede acceso a la plataforma<br>
                <strong>Escenario 2: Error por credenciales inválidas</strong><br>
                <strong>Dado que</strong> el usuario intenta iniciar sesión<br>
                <strong>Y</strong> el correo o la contraseña ingresados son incorrectos<br>
                <strong>Cuando</strong> confirme el inicio de sesión<br>
                <strong>Entonces</strong> el sistema rechaza la autenticación<br>
                <strong>Y</strong> alerta sobre el error en las credenciales proporcionadas<br>
                <strong>Escenario 3: Fallo general</strong><br>
                <strong>Dado que</strong> el usuario confirmó el inicio de sesión<br>
                <strong>Cuando</strong> la operación falla por pérdida de conexión a internet, tiempo de espera agotado u otro error generalizado<br>
                <strong>Entonces</strong> el sistema no autentica al usuario<br>
                <strong>Y</strong> muestra un mensaje alertando sobre la causa del error
            </td>
            <td>EP05</td>
        </tr>
        <tr>
            <td>US31</td>
            <td>Información de la Landing Page</td>
            <td>Como visitante, quiero interactuar con una página del startup para entender cómo ayudará para la productividad del campo</td>
            <td>
                <strong>Escenario 1: Acceso inicial</strong><br>
                <strong>Dado que</strong> el visitante ingresa a la landing page<br>
                <strong>Cuando</strong> visualice la cabecera<br>
                <strong>Entonces</strong> el sistema muestra un encabezado con la propuesta de valor clara<br>
                <strong>Y</strong> un subtítulo explicando los beneficios clave<br>
                <strong>Escenario 2: Información adicional</strong><br>
                <strong>Dado que</strong> el visitante navega en la landing page<br>
                <strong>Cuando</strong> llegue a la sección informativa<br>
                <strong>Entonces</strong> el sistema visualiza un resumen del startup con sus objetivos propuestos
            </td>
            <td>EP06</td>
        </tr>
        <tr>
            <td>US32</td>
            <td>Visualizar información de la página</td>
            <td>Como visitante, quiero ver una explicación breve sobre la plataforma, para comprender el producto y su propósito</td>
            <td>
                <strong>Escenario 1: Mostrar explicación del producto</strong><br>
                <strong>Dado que</strong> el visitante interactúa con el menú de navegación<br>
                <strong>Cuando</strong> seleccione la sección "About"<br>
                <strong>Entonces</strong> el sistema despliega esa parte de la página<br>
                <strong>Y</strong> describe brevemente la plataforma incluyendo gráficos o imágenes ilustrativas<br>
                <strong>Escenario 2: Métricas clave</strong><br>
                <strong>Dado que</strong> el visitante navega dentro de la sección "About"<br>
                <strong>Cuando</strong> avance en la lectura<br>
                <strong>Entonces</strong> el sistema muestra métricas clave que refuerzan la propuesta de valor
            </td>
            <td>EP06</td>
        </tr>
        <tr>
            <td>US33</td>
            <td>Visualización de beneficios y características</td>
            <td>Como visitante, quiero conocer los beneficios y características principales del producto, para evaluar si es útil para mis necesidades</td>
            <td>
                <strong>Escenario 1: Visualización de beneficios y características</strong><br>
                <strong>Dado que</strong> el visitante interactúa con el menú de navegación<br>
                <strong>Cuando</strong> seleccione la sección "Servicios"<br>
                <strong>Entonces</strong> el sistema muestra una lista de beneficios<br>
                <strong>Y</strong> acompaña cada uno con un ícono o imagen ilustrativa<br>
                <strong>Escenario 2: Detalle expandido</strong><br>
                <strong>Dado que</strong> el visitante visualiza la lista de beneficios<br>
                <strong>Cuando</strong> seleccione un beneficio específico<br>
                <strong>Entonces</strong> el sistema despliega información adicional con una explicación breve
            </td>
            <td>EP06</td>
        </tr>
        <tr>
            <td>US34</td>
            <td>Sección de testimonios</td>
            <td>Como visitante, quiero poder ver testimonios de agricultores y agrónomos que utilizan EcoTrack para poder confiar más en la solución</td>
            <td>
                <strong>Escenario 1: Visualización de testimonios</strong><br>
                <strong>Dado que</strong> el visitante navega por la landing page<br>
                <strong>Cuando</strong> llegue a la sección de testimonios<br>
                <strong>Entonces</strong> el sistema muestra experiencias incluyendo nombres, fotografías y comentarios de usuarios reales<br>
                <strong>Escenario 2: Ampliar testimonio</strong><br>
                <strong>Dado que</strong> el visitante interactúa con la sección de testimonios<br>
                <strong>Cuando</strong> seleccione un testimonio específico<br>
                <strong>Entonces</strong> el sistema despliega información ampliada con el comentario completo del usuario
            </td>
            <td>EP06</td>
        </tr>
    </tbody>
</table>

**EPICS**

<table>
    <thead>
        <tr>
            <th>Epic ID</th>
            <th>Titulo</th>
            <th>Descripción</th>
        </tr>
    </thead>
    <tbody>
        <tr>
        <tr>
            <td>EP01</td>
            <td>Gestión de parcelas</td>
            <td>Brindar a los Agronomos herramientas para crear, modificar y eliminar parcelas propiedad de sus organizaciones</td>
        </tr>
        <tr>
            <td>EP02</td>
            <td>Gestión de tareas</td>
            <td>Permitir la planificación y gestión de tareas y checklists en parcelas y ejecución</td>
        </tr>
        <tr>
            <td>EP03</td>
            <td>Gestión de organizaciones y miembros</td>
            <td>Facilitar a los Agrónomos la creación de organizaciones, la gestión de agricultores mediante invitaciones y eliminaciones, y el acceso a reportes generales de la organización</td>
        </tr>
        <tr>
            <td>EP04</td>
            <td>Recomendaciones y análisis de datos</td>
            <td>Proporcionar asesoría a los agricultores a través de recomendaciones técnicas usando datos del clima y métricas de trabajo a partir de las tareas creadas en la organización</td>
        </tr>
        <tr>
            <td>EP05</td>
            <td>IAM y Cuentas de usuario</td>
            <td>Permitir que los usuarios puedan registrarse, iniciar sesión, completar y editar su perfil, además de adquirir planes de suscripción para acceder a funcionalidades según su rol</td>
        </tr>
        <tr>
            <td>EP06</td>
            <td>Landing Page</td>
            <td>Dar visibilidad a la propuesta de valor de la plataforma mediante la landing page, incluyendo secciones de información, beneficios, planes, testimonios y formularios de contacto</td>
        </tr>
    </tbody>
</table>