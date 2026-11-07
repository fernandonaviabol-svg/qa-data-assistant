# Skill: diseño de pruebas con ISTQB (v1.0)

Objetivo: generar casos de prueba basados en los datos del Excel y en las historias de usuario,
con cobertura declarada.

## Técnicas y como aplicarlas a este proyecto
- Partición de equivalencia: Edad válida (15-45) y clases inválidas (menor de 15, mayor de 45,
  vacía, texto, decimal). Posición: válidas (4) y no válidas (otro texto, vacía, mayúsculas distintas).
- Valores límite: edades 14, 15, 16, 44, 45, 46. Cantidad de jugadores por selección: 41, 42, 43.
- Tabla de decisión (CRUD): jugador existe (S/N) x cambio aprobado (S/N) x dato válido (S/N) ->
  acción esperada.
- Transición de estados: ciclo de un hallazgo (Detectado, Propuesto, Aprobado, Aplicado, Rechazado).
- Adivinanza de errores (error guessing): tildes, mayúsculas, espacios, tabuladores, nombres
  compuestos, apellidos repetidos, equipos con sufijos, caracteres especiales de otros idiomas.
- Pruebas basadas en datos: usa filas reales del archivo como datos de entrada.

## Tipos de prueba que debes poder generar
- Humo (smoke): 5 a 8 casos que confirman lo esencial (abrir archivo, consultar, validar).
- Re-prueba (retest): repite casos fallidos tras una corrección.
- Regresión: casos que protegen funciones ya estables al cambiar datos o reglas.
- Negativas: entradas inválidas y comportamientos no permitidos (por ejemplo modificar sin aprobación).

## Reglas de calidad de los casos
- Atomicos, deterministas, trazables a una historia o regla, con datos explicitos.
- Resultado esperado verificable por una persona o un script.
- Prioridad segun riesgo: impacto x probabilidad.

## Cobertura
Al terminar, entrega la matriz de cobertura y declara: que historias o reglas están cubiertas,
que técnicas se usaron y que riesgos quedan sin cubrir.
