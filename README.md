# Seguimiento Ambiental

Panel de seguimiento ambiental de GH Consultora: habilitaciones, vencimientos y auditorías,
publicado con GitHub Pages.

## Cómo está armado

Mismo patrón que `gh-calibraciones` y `gh-seguimiento-mediciones`:

- `index.html` — shell público. **No contiene ningún dato de las empresas.**
- Login con Google (GIS) + fetch a un Web App de Apps Script que valida el email
  contra la lista de casillas autorizadas antes de devolver nada.
- Los datos viven en Google Sheets, en la cuenta `info.ghconsultora@gmail.com`.

## Fuentes de datos

| Planilla | Para qué |
|---|---|
| `Seguimiento y control GH CONSULTORA` | habilitaciones, expedientes, vencimientos |
| `Seguimiento Visitas a empresas` | auditorías ambientales por empresa |

## Qué muestra

- Habilitaciones por empresa, separadas en Ambiente (predio / transporte) e Hidráulica.
- Semáforo de vencimientos: rojo vencida · naranja ≤ 3 meses · amarillo 3 meses + 1 semana · verde el resto.
- Avisos por mail: a los 3 meses + 1 semana se define responsable, a los 3 meses se le avisa solo a esa persona.
- Franja de auditoría ambiental por empresa, con su frecuencia (mensual / semestral / a confirmar).
- Lista de auditorías pendientes lista para copiar y pegar en WhatsApp.

## Pendiente de configurar

En `index.html`:

- `CLIENT_ID` — OAuth Client ID creado en Google Cloud bajo `info.ghconsultora@gmail.com`.
- `BACKEND_URL` — URL `/exec` del Web App de Apps Script.
