El equipo revisa la calidad y seguridad del código antes de que llegue a revisión o producción:

- **Calidad del Código:** Se mide con métricas como cobertura de pruebas y complejidad ciclomática. En el frontend Vue 3 se usa **ESLint** con `eslint-plugin-vue`, que detecta imports mal usados, variables sin usar y violaciones de la Vue Style Guide. En el backend .NET 9 se usa **SonarLint** en el IDE, que avisa en tiempo real sobre code smells, duplicación de lógica y métodos demasiado complejos.

- **Seguridad del Código:** Las vulnerabilidades más comunes se mitigan desde el diseño: la inyección SQL se previene usando Entity Framework Core con queries parametrizadas; el XSS se evita con el escape automático del template de Vue 3, sin usar `v-html` con datos del usuario; y la validación de entradas se hace con Data Annotations en ASP.NET Core, que rechaza los requests malformados antes de que lleguen a la lógica del sistema.

<div align="center">

| <img src="../../../../img/logos/eslint.svg" width="48" height="48"/><br/>ESLint |
|:---:|

</div>

ESLint corre automáticamente en el pipeline de CI en cada Pull Request, bloqueando la fusión si hay errores de linting. SonarLint actúa en el IDE del desarrollador, por lo que los problemas se detectan antes incluso de hacer commit.
