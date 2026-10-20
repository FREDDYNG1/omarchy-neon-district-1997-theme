# Diseño técnico

El motor nativo genera las configuraciones a partir de colors.toml. Se conservan seis overrides de superficies Quickshell porque permiten selección oscura y texto legible sin editar shell.json ni complementos. Iconos: una línea con Yaru-magenta-dark.

## Contraste

Ratios de luminancia relativa sRGB calculados para colores sólidos opacos:

| Par | Ratio aproximado |
|---|---|
| Texto principal / fondo | 15.46:1 |
| Texto principal / superficie | 14.24:1 |
| Texto secundario / superficie | 7.13:1 |
| Texto seleccionado / selección | 13.39:1 |
| Magenta / superficie | 6.37:1 |
| Cian / superficie | 10.50:1 |
| Azul para texto / superficie | 6.67:1 |
| Rojo / superficie | 5.95:1 |
| Verde / superficie | 12.96:1 |
| Borde inactivo / superficie | 3.56:1 |

Estos ratios no garantizan todas las combinaciones de resaltado, transparencias o aplicaciones. El violeta artístico #7A5CFF no se usa como azul de texto: se aclara a #A18CFF. Una pestaña magenta requiere texto oscuro; el perfil Kitty lo especifica.

## ANSI

| Índice | Clave | Índice brillante | Clave brillante |
|---|---|---|---|
| 0 | background | 8 | muted |
| 1 | red | 9 | bright_red |
| 2 | green | 10 | bright_green |
| 3 | yellow | 11 | bright_yellow |
| 4 | blue | 12 | bright_blue |
| 5 | magenta | 13 | bright_magenta |
| 6 | cyan | 14 | bright_cyan |
| 7 | foreground | 15 | bright_foreground |

Los HEX completos están en colors.toml y kitty-palette.conf. El perfil Kitty incluye primero la configuración personal predeterminada y luego la paleta. El parser se valida sin abrir ventanas; su aspecto visual sigue pendiente de confirmación específica.
