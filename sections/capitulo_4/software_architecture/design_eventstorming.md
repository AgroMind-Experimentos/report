En esta sección se explica y evidencia el proceso de Design-Level EventStorming, que sirvió para plantear una aproximación revisada y mejorada al modelado de nivel general para el dominio del problema.

**Step 1: Unstructured Exploration**  
<img src="../../../img/capitulo_4/software_architecture/design-level-eventstorming-step-1.png" width="80%">  
En este paso el equipo comenzó con una lluvia de ideas de los eventos del dominio.

**Step 2: Timelines**  
<img src="../../../img/capitulo_4/software_architecture/design-level-eventstorming-step-2.png" width="80%">  
En este segundo paso, el equipo ordeno los eventos de dominio en el orden que ocurren en el dominio empresarial.  
Se tuvo en cuenta los happy path y luego se agregaron los escenarios alternativos.

**Step 3: Pain Points**  
<img src="../../../img/capitulo_4/software_architecture/design-level-eventstorming-step-3.png" width="80%">  
En este tercer paso, el equipo colocó dudas sobre el dominio o documentación faltante en algunas partes del flujo que ya había sido ordenado anteriormente.

**Step 4: Pivotal Points**  
<img src="../../../img/capitulo_4/software_architecture/design-level-eventstorming-step-4.png" width="80%">  
En este cuarto paso, el equipo buscó eventos comerciales importantes que indiquen un cambio en el contexto y los marcó con una línea.

**Step 5: Commands**  
<img src="../../../img/capitulo_4/software_architecture/design-level-eventstorming-step-5.png" width="80%">  
En este quinto paso, el equipo añadió comandos que desencadenen eventos o el flujo de eventos, junto a sus actores.

**Step 6: Policies**  
<img src="../../../img/capitulo_4/software_architecture/design-level-eventstorming-step-6.png" width="80%">  
En este sexto paso, el equipo añadió policies, que son reglas de negocio que hace que se ejecuten comandos sin la necesidad de un actor.

**Step 7: Read Models**  
<img src="../../../img/capitulo_4/software_architecture/design-level-eventstorming-step-7.png" width="80%">  
En este séptimo paso, el equipo añadió read models, que son como la vista de datos que el usuario usa para tomar la decisión de ejecutar un comando.

**Step 8: External Systems**  
<img src="../../../img/capitulo_4/software_architecture/design-level-eventstorming-step-8.png" width="80%">  
En este octavo paso, el equipo identifico sistemas externos, en este caso solo se tiene uno que es la API que usaremos para el consumo de datos climáticos.

**Step 9: Aggregates**  
<img src="../../../img/capitulo_4/software_architecture/design-level-eventstorming-step-9.png" width="80%">  
En este noveno paso, el equipo antes de agregar los agregados, discutió bastantes cosas sobre pasos anteriores y se decidió hacer algunos cambios en los read models, policies, eventos y commands.


**Step 10: Bounded Contexts**  
<img src="../../../img/capitulo_4/software_architecture/design-level-eventstorming-step-10.png" width="80%">  
En este último paso, el equipo buscó agregados que estén relacionados entre sí mediante policies para luego identificar bounded contexts.  
[Ver en Miro](https://miro.com/welcomeonboard/Tkt0b0FqK3BGdThsbmVRKytveUdDdTBMeHZtNW52aTcvaHBHQ3dKYTlCS2FzMlhLYVZhNnAwaHpkRHNhOTlTSzFLRVhFeW5JQlZJck5hUzNBSlMrbVpqbVB1M3ErOFNsY0hQTDNXbStrSXZ0WnFBK2I3dlk0YXl0OFJwamdhcXB0R2lncW1vRmFBVnlLcVJzTmdFdlNRPT0hdjE=?share_link_id=129166886960)
