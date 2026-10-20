# Validación de distribución

Fecha: 2026-10-20. Versión preparada: v1.0.0. Resultado automático detallado: [validation.json](validation.json).

- Ocho WebP decodificables, 1920×1080, con bytes y SHA-256 coincidentes con los fondos finales aprobados.
- TOML válido, 30 claves de paleta contando mode; iconos de una línea con variante instalada localmente.
- Copia y clon Git de prueba en un HOME temporal, sin activar el tema real.
- Staging con las funciones nativas de Omarchy para repositorios clonados; generación con las plantillas originales de 4.0.6.
- Archivos generados Hyprland/Neovim Lua, TOML y JSON válidos; sin marcadores de plantilla pendientes.
- Overrides de Quickshell con secciones y claves existentes en las plantillas nativas; fusión comprobada.
- Perfil independiente de Kitty analizado con su parser y una configuración principal ficticia, sin abrir ventanas.
- Referencias Markdown locales existentes; ningún enlace simbólico o archivo de distribución vacío.
- Instalación por copia en una ruta temporal ajena al HOME real; sin rutas de usuario codificadas en el paquete.

El código de prueba y sus clones temporales son auxiliares locales, no forman parte del paquete distribuido. Se ejercitó staging y generación de datos, no se ejecutó el comando de activación real. Para comprobar los fondos desde la raíz del repositorio:

```bash
sha256sum -c docs/wallpapers.sha256
```

## Evidencia histórica y límites

La activación real del 2026-10-20 terminó correctamente. Su informe privado registra 12 comprobaciones automáticas satisfactorias, entre ellas IPC de Hyprland/Quickshell, dos monitores Full HD, fondos, configuración generada, sincronización de aplicaciones y preservación de archivos protegidos. El usuario aprobó apariencia general, colores y ocho wallpapers. Se conserva aquí únicamente un resumen; no se redistribuyen registros privados ni inventarios personales.

Estas pruebas no se presentan como una nueva ejecución de IPC o una validación funcional completa de cada aplicación. Bloqueo/desbloqueo, perfil Kitty visual, menús/notificaciones, complementos personales y apariencia específica de los editores/btop siguen en [manual-tests.md](manual-tests.md). No se bloqueará la sesión automáticamente.

MIT está finalizada para código y configuración con Copyright (c) 2026 Litotep. El fundamento de distribución gráfica y sus límites se documentan en ASSET-LICENSING.md; los gráficos quedan fuera de MIT. preview.png se acepta como vista previa provisional; las pruebas manuales se mantienen como limitaciones conocidas. El repositorio remoto no existe y v1.0.0 no se ha publicado.
