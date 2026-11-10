# ENGLISH MGM — Auditoría inicial

Este documento registra una revisión estática preliminar de `index.html` y `config.js`.

## Hallazgos
- La aplicación concentra interfaz, estilos y lógica en `index.html`.
- El panel del estudiante consulta datos periódicamente cada ocho segundos.
- Hay acciones de eliminación de salones, estudiantes y actividades que requieren protección del historial.
- El panel de resultados presenta mejores intentos; falta una vista completa del historial.
- La seguridad depende de las funciones RPC de Supabase; revisar permisos antes de ampliar operaciones.

## Plan seguro
1. Mantener `main` intacta.
2. Realizar rediseño Playful Neon en `desarrollo`.
3. Probar cambios visuales con datos ficticios sin escrituras en Supabase.
4. Auditar RPC, respaldos y restauración antes de migraciones de datos.
