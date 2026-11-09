# biblioteca

La librería propia de la Forja. **Nada entra aquí sin estar comprobado** contra la hoja de datos e impreso a 1:1 con la pieza real encima (la lista está en [COMPROBACION.md](COMPROBACION.md)).

| Archivo | Qué es |
|---|---|
| `forja.pretty/` | Huellas: `LOGO_FORJA` (6, 8 y 10 mm, serigrafía y dorada) y las piezas del mes |
| `forja.kicad_sym` | Símbolos propios (los crea KiCad al guardar el primero) |

Se usa siempre a través de la variable de ruta `${AKMON}`, nunca con una ruta absoluta: así funciona en cualquier PC.
