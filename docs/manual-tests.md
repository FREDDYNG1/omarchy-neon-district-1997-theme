# Checklist manual

Estado de referencia: activación real exitosa el 2026-10-20. Confirmados por el usuario: apariencia general del escritorio, colores y ocho fondos. El informe histórico registró 12 comprobaciones automáticas satisfactorias. No equivale a aprobar las siguientes pruebas específicas.

Anota fecha, versión, resultado y evidencia redactada junto a cada casilla. Conserva los informes originales con información personal fuera del repositorio. No marques una casilla solo porque exista un archivo generado.

- [ ] Bloqueo/desbloqueo: probar desde la sesión con acceso de recuperación disponible; verificar texto, foco, error de contraseña y desbloqueo correcto. No automatizar el bloqueo ni publicar contraseñas.
- [ ] Kitty: abrir el perfil independiente, revisar ANSI, cursor, selección, pestañas y lectura de código. Confirmar que la configuración principal no se escribió.
- [ ] Menús y launcher: abrir, buscar, navegar con teclado y comprobar selección y texto secundario.
- [ ] Notificaciones: revisar una notificación real de prueba, contraste, cierre y acciones cuando proceda.
- [ ] `litotep.taskbar`: comprobar ventanas, foco, selección y comportamiento visual si está instalado.
- [ ] `litotep.music-wave`: reproducir audio y comprobar actualización, animación y contraste si está instalado.
- [ ] VS Code: abrir un archivo de código, comprobar tema local, búsqueda y selección; no cambiar extensiones ajenas.
- [ ] Neovim: comprobar sintaxis, cursor, selección y ventanas flotantes con la configuración habitual.
- [ ] Obsidian: comprobar notas y paneles en un vault propio sin exponer contenido privado.
- [ ] btop: comprobar métricas, gráficos y alertas durante uso normal.

Las dos pantallas Full HD y ausencia de errores nuevos de configuración Hyprland se registraron automáticamente en la activación de referencia. La revisión actual no repite pruebas IPC ni asegura ausencia de errores en todos los diarios de aplicaciones.

## Registro de nuevas pruebas

| Fecha | Prueba | Resultado | Evidencia revisada |
|---|---|---|---|
| — | Pendientes anteriores | Sin ejecutar o sin confirmación específica | No disponible |

## Clasificación explícita

| Grupo | Estado | Evidencia / límite |
|---|---|---|
| Apariencia general, colores y ocho wallpapers | Aprobadas por el usuario | Confirmación de revisión visual |
| Doce comprobaciones automáticas de activación | Aprobadas históricamente | Informe conservado fuera del paquete; no repetidas ahora |
| Bloqueo/desbloqueo, Kitty visual, menús, notificaciones, cada complemento y cada editor/btop | Pendientes | Sin evidencia específica de ejecución completa |
| Pruebas fallidas | Ninguna confirmada en la evidencia revisada | No equivale a ausencia de todo posible fallo |
| Comprobación visual e interacción de la sesión desde Codex | No verificables en este entorno | Sin prueba gráfica actual; no se capturó ni se bloqueó la sesión |

Revisar también el contraste de la barra y music-wave con la transparencia personal actual. No se cambió esa preferencia. Mantener las casillas anteriores sin marcar hasta recibir evidencia específica.

## Tratamiento en v1.0.0

El usuario autorizó cerrar con estas pruebas específicas pendientes como limitaciones conocidas. No constituyen un bloqueo para preparar la versión ni se marcan como aprobadas. La apariencia general y la colección ya cuentan con conformidad visual del usuario. No se ha ejecutado automáticamente bloqueo, apertura de aplicaciones o captura del escritorio durante este cierre.
