# Reglas de validación de datos (v1.0)

Parámetros configurables (el usuario puede cambiarlos al pedir la validación):
- Edad mínima válida: 15. Edad máxima válida: 45.
- Posiciones válidas: Portero, Defensa, Volante, Delantero.
- Jugadores esperados por selección: 42 (6 Portero, 12 Defensa, 12 Volante, 12 Delantero).

Orden de ejecución: R01, R02, R03 ... R17. Para cada regla reporta: cuántos casos, severidad y
ejemplos con fila de Excel. Las reglas SOLO detectan y proponen; nunca corrigen por si solas.

### R01 - Filas de encabezado repetidas (Alta)
Busca filas dentro de los datos cuyo contenido sea igual a los nombres de las columnas.
Propuesta: eliminar la fila (requiere aprobación).

### R02 - Encabezado corrupto o mal escrito (Media)
Busca encabezados repetidos que no coincidan exactamente con los de la fila 1.

### R03 - Espacios al inicio o al final, incluidos tabuladores (Media)
Aplica a todas las columnas. Propuesta: recortar espacios (trim).

### R04 - Espacios dobles dentro del texto (Baja)
Propuesta: dejar un solo espacio.

### R05 - Nombres de selección mal escritos o sin tilde (Media)
Compara los nombres de selección contra su forma esperada en español. Si hay duda, marca
"Requiere decisión humana". No asumas el nombre correcto sin evidencia.

### R06 - Cantidad de jugadores por selección distinta de lo esperado (Alta)
Cuenta registros reales (sin encabezados repetidos) por selección.

### R07 - Distribución por posición inesperada (Media)
Cuenta por posición dentro de cada selección y compara con lo esperado.

### R08 - Posición fuera del catálogo (Alta)
Cualquier valor que no sea una posición válida (considera mayúsculas, tildes y espacios).

### R09 - Edad inválida (Alta)
Vacía, no numérica, decimal o fuera del rango configurado.

### R10 - Celdas vacías (Alta)
En cualquiera de las 5 columnas de datos.

### R11 - Duplicados (Alta / Media)
- Filas exactamente iguales: Alta.
- Mismo Selección + Jugador con datos distintos: Media, "posible homonimo o duplicado".
  Nunca elimines: requiere decisión humana.

### R12 - Tildes inconsistentes en apellidos (Media)
Mismo apellido escrito con y sin tilde en distintas filas. Marca como SOSPECHA. No corrijas:
no puedes saber la ortografía correcta sin una fuente.

### R13 - Formato inconsistente del campo Jugador (Baja)
Mezcla de solo apellido y nombre + apellido. Informa el porcentaje de cada formato.

### R14 - Variantes y erratas en nombres de equipos (Media)
Agrupa nombres que difieran solo por tildes, mayúsculas, puntuación, "FC / F.C. / F. C." o por
errores de tecleo (similitud alta). Para cada grupo propone un nombre canónico y pide aprobación.
Primero agrupa con reglas exactas; usa tu criterio solo para los casos dudosos.

### R15 - Sufijos o abreviaturas de país en equipos (Media)
Detecta marcas como (KSA), (Qat), -Br, (Urug). Lista todas las variantes. NO las elimines por
defecto: a veces distinguen clubes con el mismo nombre. Propone una regla única por equipo y
espera la decisión humana.

### R16 - Caracteres no permitidos y fórmulas (Alta)
- Celdas que empiezan con = + - @ (riesgo de inyección de fórmulas).
- Caracteres de control, saltos de linea dentro de la celda, o simbolos extranos.

### R17 - Estructura (Baja)
Columnas no declaradas, hojas vacías, filas completamente vacías.

## Qué NO debes hacer
- No corregir sin aprobación. No borrar filas. No unificar nombres ambiguos por tu cuenta.
- No dar por "correcto" lo que no verificaste con código.
