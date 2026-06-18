Todo cambio de código en EcoTrack pasa por un proceso de revisión antes de integrarse a las ramas estables. Esto se gestiona mediante Pull Requests en GitHub:


**Tipos de Revisiones:**

- **Revisión por Pares:** Un miembro del equipo distinto al autor revisa el PR para verificar que el código sea claro y cumpla con los estándares definidos en 6.2.1.1.
- **Revisión Formal:** Para cambios de mayor impacto, el equipo evalúa el código en conjunto usando un checklist, lo que permite detectar problemas que una sola persona podría pasar por alto.
- **Revisión Automática:** ESLint y SonarLint corren en cada PR vía GitHub Actions. Si alguna verificación falla, el PR no puede fusionarse.

**Proceso de Revisión:**

- El autor abre un PR con una descripción de qué cambió y cómo probarlo, usando mensajes en formato Conventional Commits.
- Los revisores dejan comentarios en las líneas específicas del diff. Los comentarios deben ser concretos y orientados a soluciones.
- El autor responde cada comentario y aplica los cambios necesarios.
- El PR se aprueba solo cuando todos los comentarios están resueltos y las verificaciones automáticas pasan.

**Criterios de Aceptación:**

- El código no debe introducir vulnerabilidades de seguridad ni romper los estándares de calidad definidos.
- La cobertura de pruebas debe mantenerse en al menos un 80%.

**Frecuencia:**

Las revisiones ocurren de forma continua durante el sprint. Ningún PR debe quedar sin respuesta más de 48 horas. Al cierre de cada sprint se revisa si quedaron PRs pendientes.
