# Dashboard MELI

Dashboard web para monitoreo de efectividad de preventivos MELI.

## Fuente maestra
La única fuente de datos del dashboard es la hoja **Prueba Pilot MELI** del archivo `Formato Piloto.xlsx`.

`Sheet1` no se utiliza.

## Columnas esperadas
- Taller
- Fecha
- Derivada Preventivo
- Preventivo
- MELI Programados
- MELI Entregadas
- Mismo Día
- Correctivos
- Correctivos Autorizados
- Descripción Correctivos
- Efectividad %

## Funcionalidades
- Carga manual XLSX/XLS/CSV.
- Filtro por taller y fechas.
- KPIs de efectividad, entregas, servicios y correctivos.
- Gráficas de efectividad, distribución de mantenimiento y programados vs entregados.
- Bitácora agrupada por taller y fecha.
- Exportación de la vista filtrada.

## OneDrive
La integración de OneDrive debe realizarse mediante Microsoft Graph + Microsoft Entra ID. No se deben colocar secretos de Microsoft ni claves de OpenAI en `index.html`.

La integración recomendada es:

OneDrive/SharePoint → Microsoft Graph → backend seguro → dashboard.

## OpenAI
OpenAI es opcional y se reserva para una capa de análisis ejecutivo sobre los datos ya cargados. La clave debe vivir en el backend/secret manager, nunca en el frontend.
