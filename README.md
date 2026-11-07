# QA Data Assistant

Agente de IA, sin código y sin costo, que apoya tareas de QA sobre un archivo Excel de nominas de
selecciones de futbol: consultar datos, validar calidad, diseñar casos de prueba, revisar
requerimientos y generar reportes.

## Qué hace
- Consultas sobre selecciones, jugadores y clubes (con calculos verificables).
- Validación de datos con 17 reglas (espacios, tildes, duplicados, variantes de equipos, etc.).
- Cambios solo con aprobación humana y registro en un log.
- Diseño de casos de prueba con técnicas ISTQB y cobertura declarada.
- Revisión de historias de usuario y reportes de resultados.

## Estructura del repositorio
- agente/ : instrucciones, reglas, formatos y skills del agente (archivos Markdown).
- datos/ : archivo Excel original (solo lectura) y versiones de trabajo.
- resultados/ : hallazgos, casos de prueba y reportes generados.

## Cómo usarlo
1. Crear un proyecto en un asistente de IA que acepte archivos e instrucciones.
2. Pegar agente/00_instrucciones_agente.md como instrucciones del proyecto.
3. Cargar los demás archivos de agente/ y el Excel de trabajo.
4. Escribir el modo de trabajo (CONSULTAR, VALIDAR, MODIFICAR, DISEÑAR PRUEBAS, REPORTAR,
   REVISAR REQUERIMIENTOS) y la tarea.

## Principios
El agente no reemplaza al QA: asiste. No modifica originales, no inventa datos y no aplica
cambios sin aprobación.

## Versión
v1.0
