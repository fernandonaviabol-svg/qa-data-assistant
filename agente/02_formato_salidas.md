# Formatos de salida (v1.0)

## 1. Tabla de hallazgos
Columnas, en este orden:
ID | Regla | Severidad | Fila Excel | Campo | Valor actual | Propuesta | Motivo | Acción | Estado | Aprobado (S/N)

- ID: H001, H002, ... (consecutivo).
- Valor actual: entre corchetes, por ejemplo [ Panamá ].
- Acción: Corregir / Eliminar / Decidir (requiere decisión humana).
- Estado: Detectado -> Propuesto -> Aprobado -> Aplicado (o Rechazado).
Si hay muchos casos iguales, agrupalos en un solo hallazgo con la lista de filas.

## 2. Resumen por regla
Tabla: Regla | Descripción | Casos | Severidad.
Al final: total de hallazgos y conteo por severidad (Alta / Media / Baja).

## 3. Caso de prueba
ID (CP-001) | Título | Historia o regla asociada | Tipo (funcional, negativa, límite,
seguridad, regresión, humo) | Técnica ISTQB | Precondición | Datos de entrada | Pasos |
Resultado esperado | Prioridad (Alta/Media/Baja) | Automatizable (S/N)

Reglas: un caso = una sola verificación; datos explicitos; resultado esperado verificable;
sin ambigüedades.

## 4. Matriz de cobertura
Tabla: Historia / Regla | Casos que la cubren | Técnicas usadas | Riesgo no cubierto.
Declara siempre el alcance: que se cubre y que NO se cubre.

## 5. Reporte de ejecución
1) Resumen ejecutivo  2) Alcance y archivo (nombre y versión)  3) Reglas aplicadas
4) Resultados por severidad  5) Hallazgos principales  6) Cobertura  7) Riesgos y supuestos
8) Recomendaciones  9) Decisiones pendientes del usuario.

## 6. Log de cambios (hoja Log_Cambios)
ID cambio | Fecha | Hallazgo | Fila | Campo | Antes | Despues | Aprobado por | Versión resultante

## 7. Revisión de requerimientos
Tabla: Historia | Problema (ambigüedad, vacío, contradicción, no verificable) | Cita del texto |
Pregunta para el analista | Sugerencia de redacción.
