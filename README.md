# Vacantes Guardia Civil 2020–2024 · Dashboard

Dashboard interactivo para consultar por municipio las vacantes publicadas en el Boletín Oficial de la Guardia Civil (BOGC) entre 2020 y 2024.

**Web:** https://kd9c9zhyht-lab.github.io/guardia-civil-vacantes-dashboard/

## Fuentes

| Año | Resolución | Tipo de plaza | Concursos | Vacantes |
|---|---|---|---|---|
| 2020 | 2010026 | Libre designación | 152 | 305 |
| 2021 | 2110028 | Libre designación | 185 | 404 |
| 2022 | 2220005 | Concurso de méritos | 677 | 1.999 |
| 2023 | 2310031 | Libre designación (personal en reserva) | 143 | 217 |
| 2024 | 2430010 | Provisión por antigüedad | 708 | 1.118 |

## Datos descargables (`/datos`)

- `vacantes_guardia_civil_2020_2024.xlsx` — hojas *Vacantes*, *Municipios* (variantes originales de cada nombre) y *Validación*.
- `vacantes_guardia_civil_2020_2024.csv` — UTF-8 con BOM.
- `vacantes_guardia_civil_2020_2024.db` — SQLite, tabla `vacantes`.

## Metodología

- Cada fila es un concurso; "Nº vacantes" es el número de plazas convocadas.
- Nombres de municipio unificados entre años: mayúsculas/tildes, artículos pospuestos al principio ("Coruña (A)" → "A Coruña") y variantes cooficiales. Se conserva el texto original en una columna aparte.
- Provincia y comunidad autónoma en columnas propias.
- Validación: numeración de concursos completa y sin duplicados en cada año.
- Cada año corresponde a un único tipo de convocatoria, por lo que la evolución anual mezcla efecto año y efecto tipo.
- BQ = vacantes bloqueadas (art. 13.2 del Reglamento de Destinos), solo en 2024.
