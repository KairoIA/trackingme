# TrackingMe 🏆

App personal para seguir actividades (objetivos anuales, rachas) y peso. Un solo `index.html` sin dependencias (salvo Google Fonts) + `logo.svg`.

**En vivo:** https://kairoia.github.io/trackingme/

## Páginas
- **Track:** objetivos del año con progreso, marca de ritmo (dónde deberías ir hoy) y rachas 🔥 días seguidos · 🏆 semanas con ≥1 · 💣 semanas con ≥3.
- **Calendar:** toca un día para apuntar actividades y peso; resumen del mes.
- **Weight:** peso actual, zonas (<71 óptimo · 71–77 normal · 77–78 atención · >78 alerta), gráfica y lista (toca un registro para editarlo).
- **History:** objetivos por año y copia de seguridad (guardar / restaurar JSON).

## Datos
Solo en el `localStorage` del dispositivo:
- `mytracker_days`: `{ "AAAA-MM-DD": ["workout", "running", …] }`
- `mytracker_weight`: `[{ "date": "AAAA-MM-DD", "kg": 74.5 }, …]`
- `mytracker_lastbackup`: fecha de la última copia.

Objetivos (`GOALS`), históricos anteriores a 2026 (`HIST`) y actividades (`ACTIVITIES`) están al principio del `<script>` de `index.html`. Un año sin objetivos propios usa los del último año que los tiene.

**Kegel y Cinta son actividades distintas.** Kegel existe en 2024-2025 (objetivos e históricos) y ya no se apunta (`retired`). En 2026 no hay Kegel: los días de 2026 marcados `kegel` pierden esa marca al abrir la app, y las fechas afectadas se guardan en `mytracker_kegel2026_removed`.
