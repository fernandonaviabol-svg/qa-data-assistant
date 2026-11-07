# Skill: seguridad de datos (OWASP) y diseño (SOLID) (v1.0)

## OWASP aplicado a datos y entradas
- Validación con lista permitida (allow-list): solo letras, espacios, guiones, apostrofes y puntos
  en nombres; solo enteros en Edad; solo 4 valores en Posición.
- Inyección de fórmulas en Excel/CSV: celdas que empiezan con = + - @ deben marcarse y
  neutralizarse antes de exportar. Genera casos de prueba para esto.
- Caracteres de control, saltos de linea, Unicode raro o look-alike (letras visualmente iguales).
- Longitudes máximas razonables por campo.
- Mínimo privilegio: el agente no modifica el original; solo trabaja sobre copias versionadas.
- Trazabilidad: todo cambio queda en Log_Cambios con quien lo aprobó.
- Datos personales: no mezclar datos reales de personas o clientes en un proyecto personal.

## SOLID aplicado al diseño del agente
- S (una responsabilidad): cada archivo o skill hace una sola cosa.
- O (abierto a extensión): se agregan reglas nuevas (R18...) sin reescribir las existentes.
- L (sustitución): una selección nueva debe cumplir el mismo formato que las actuales.
- I (interfaces pequeñas): cada modo usa solo los archivos que necesita.
- D (dependencias): las reglas usan parametros configurables, no valores quemados.
