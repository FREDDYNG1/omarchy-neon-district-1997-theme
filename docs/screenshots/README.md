# Capturas reales pendientes

Para v1.0.0 se acepta expresamente como vista previa provisional [preview.png](../../preview.png), una cuadrícula de los ocho fondos; no es una captura de escritorio. No hay capturas reales aprobadas ni se ha capturado contenido automáticamente.

## Colección sugerida

| Archivo futuro | Contenido | Estado |
|---|---|---|
| desktop.png | Escritorio con el tema activo | Pendiente de captura y revisión |
| quickshell.png | Barra y superficies de Quickshell | Pendiente |
| kitty.png | Terminal con perfil independiente y contenido de demostración | Pendiente |
| launcher.png | Menú o lanzador | Pendiente |
| vscode.png | VS Code con código de demostración | Pendiente |

Los archivos de la tabla no existen todavía y no se enlazan como si estuvieran disponibles.

## Capturar desde la sesión gráfica

Desde una terminal de Omarchy, prepara un destino local de revisión **fuera de este repositorio**. Sustituye la variable por la ubicación elegida; no ejecutes una captura hasta ocultar datos sensibles:

```bash
capture_dir="$HOME/Pictures/neon-district-review"
mkdir -p "$capture_dir"
OMARCHY_SCREENSHOT_DIR="$capture_dir" omarchy capture screenshot region save
# Alternativa para una vista completa, solo después de revisar ambas pantallas:
# OMARCHY_SCREENSHOT_DIR="$capture_dir" omarchy capture screenshot fullscreen save
```

El comando nativo imprime la ruta guardada. Está documentado aquí, no ejecutado. No se intenta cambiar sockets o controladores. Para mostrar Kitty, abre manualmente su perfil independiente indicado en README. Usa contenido de ejemplo, un prompt sin nombre de usuario/ruta y una carpeta de demostración en los editores. Cierra información privada sin finalizar la sesión.

Revisa cada imagen completa y sus recortes: títulos de ventanas, usuarios, rutas, notificaciones, redes, sesiones, documentos, correo y credenciales. Recorta o redacta localmente lo necesario, elimina metadatos innecesarios con herramientas ya disponibles y vuelve a revisar. No copies imágenes sin revisar al repositorio. Añadir archivos aquí será una acción posterior, tras aprobación del usuario.

Antes de incorporarlas, revisar también derechos de los recursos visibles según [ASSET-LICENSING.md](../ASSET-LICENSING.md). Una captura solo documenta apariencia; no prueba desbloqueo ni acciones funcionales.

Las capturas reales no son un bloqueo para v1.0.0. No se crean imágenes simuladas ni se capturan ventanas en este cierre.
