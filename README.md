🧾 NORMALIZACIÓN DE DB — Guía Visual
🎯 Propósito del sitio

El contenido presenta de forma gráfica y simplificada cómo pasa una tabla desordenada y redundante a una estructura normalizada siguiendo las formas normales (principalmente de 1FN a 3FN).


**[Ver en vivo](https://bellmojica.github.io/NORMALIZACI-NDB/)**


📌 Secciones clave de la guía
📍 Estado: Sin Normalizar

Ejemplo de tabla con datos redundantes y errores:

Nombre País Médico
J. Carlos España Perez, J.
Carlos A. México Perez, J.
Juan S. México Lopez, M.

⚠️ Problema: valores repetidos (“Perez, J.” aparece varias veces), lo cual causa inconsistencias si hay cambios de datos.

📍 1FN: Definir Identidad

Transformación inicial:

ID_PACIENTE | Nombre | País | Médico
101         | J. Carlos España Perez, J.
102         | Carlos A. México Perez, J.

✅ Regla de la 1FN:

Cada celda debe tener un único valor atómico.

Debe definirse una clave primaria identificadora única.

📍 3FN: El Esquema Perfecto

Se propone un diseño final en tercera forma normal (3FN) con tres tablas separadas:

TABLA PACIENTES

ID_PACIENTE (PK)

Nombre

ID_PAIS (FK)

TABLA MÉDICOS

ID_MEDICO (PK)

Nombre_Med

TABLA PAÍSES

ID_PAIS (PK)

Nombre_Pais

📌 Regla de la 3FN:

“Todo depende de la clave, solo de la clave, y de nada más que de la clave.”

Esto elimina redundancias, favorece la integridad y hace que los cambios solo se hagan en un lugar lógico.

🧠 ¿Qué estás viendo en esencia?

La página muestra un resumen visual básico del proceso de normalización:

Sin normalizar: Redundancias e inconsistencias.

Primera Forma Normal (1FN): Valores atómicos y clave primaria.

Tercera Forma Normal (3FN): Separación lógica de entidades para evitar dependencias inadecuadas.
