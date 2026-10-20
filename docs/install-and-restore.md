# Instalación y reversión

## Revisión previa

Desde un clon local, sigue la copia sin sobrescritura descrita en README. Omarchy 4.0.6 reconoce el slug neon-district-1997. `omarchy theme install URL` clona y activa de inmediato, y elimina el destino previo con igual nombre: úsalo solo cuando desees ese comportamiento y cuentes con respaldo.

Antes de activar, registra estado y copia el fondo exacto fuera de current/theme. Estos comandos crean únicamente un respaldo nuevo en tu directorio de estado; no aplican el tema:

```bash
backup_dir="$HOME/.local/state/neon-district-1997-backups/$(date -u +%Y%m%dT%H%M%SZ)"
mkdir -p "$backup_dir"
previous_theme=$(cat "$HOME/.local/state/omarchy/current/theme.name")
printf '%s\n' "$previous_theme" > "$backup_dir/theme-before.txt"
previous_background=$(readlink -f "$HOME/.local/state/omarchy/current/background")
wallpaper_copy="wallpaper-before.${previous_background##*.}"
cp -- "$previous_background" "$backup_dir/$wallpaper_copy"
printf '%s\n' "$wallpaper_copy" > "$backup_dir/wallpaper-copy.txt"
printf '%s\n' "$previous_background" > "$backup_dir/background-path-before.txt"
sha256sum "$backup_dir/$wallpaper_copy" > "$backup_dir/wallpaper-before.sha256"
```

La copia conserva la extensión real del original. Guarda la ruta de backup_dir para otra terminal. Ningún respaldo debe añadirse al repositorio.

## Destinos que revisar y respaldar

El comportamiento preciso depende de la versión, aplicaciones instaladas y hooks personales. Inspecciona los sincronizadores nativos de tu instalación antes de aplicar; no ejecutes scripts descargados sin revisarlos.

| Destino | Qué conservar |
|---|---|
| Estado de Omarchy | Tema generado, theme.name, selección y copia real del fondo |
| Hyprland y Quickshell | Configuración pertinente, shell.json, overrides, hooks y complementos; el tema no contiene configuración de monitores |
| Terminales y btop | Configuración que apunte a paletas generadas; conservar Kitty principal sin sustituirlo por el perfil de prueba |
| VS Code | Preferencias del usuario, tema local Omarchy, registro de extensiones locales y archivos de estado afectados |
| Obsidian | Tema Omarchy y preferencias de apariencia de cada vault registrado; nunca publicar los vaults |
| GNOME/GSettings | Valores previos de color-scheme, gtk-theme e icon-theme |
| Navegadores | Políticas color.json existentes y constancia de cuáles no existían |
| Otras aplicaciones/hooks | Solo destinos efectivamente afectados por los sincronizadores locales |

En la instalación de referencia, el helper nativo actualizó `color.json` bajo `/etc/chromium/policies/managed/`, `/etc/opt/chrome/policies/managed/` y `/etc/brave/policies/managed/`. No se garantiza esa lista en otro equipo; revisa también los navegadores instalados. La elevación corresponde al mecanismo oficial de Omarchy. No hay un helper propio de este tema.

Registra contenido, permisos, enlaces y destinos ausentes. Verifica hashes y ensaya la recuperación en un directorio aislado antes de activar. Una copia del wallpaper y el nombre del tema no sustituyen un respaldo de preferencias de aplicaciones.

## Activación y restauración

Desde la sesión gráfica, cuando los respaldos estén verificados:

```bash
omarchy theme set neon-district-1997
```

Para volver, recupera la ruta real de tu respaldo, carga el nombre guardado y aplica el fondo después de que terminen los hooks:

```bash
# backup_dir debe contener la ruta del respaldo creado anteriormente.
previous_theme=$(cat "$backup_dir/theme-before.txt")
omarchy theme set "$previous_theme"
wallpaper_copy=$(cat "$backup_dir/wallpaper-copy.txt")
omarchy theme bg set "$backup_dir/$wallpaper_copy"
```

Restaura selectivamente preferencias y archivos afectados desde tu respaldo si necesitas recuperar el estado exacto. Retira un archivo nuevo únicamente si antes no existía y confirmas que lo creó la activación. Respeta modificaciones posteriores y permisos de los archivos de sistema. No hagas una extracción masiva sobre / ni restaures monitores, controladores o complementos que no cambiaron.

Conserva el tema previo y el respaldo. La reversión se realiza por decisión del usuario; el paquete no instala un mecanismo de reversión automática.
