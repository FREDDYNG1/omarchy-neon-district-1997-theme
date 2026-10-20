# Compatibilidad

| Componente | Mecanismo y alcance |
|---|---|
| Omarchy | 4.0.6, paquete 4.0.6-1 verificado; otras versiones sin validar |
| Hyprland | Lua generado desde plantillas nativas, bordes activo/inactivo; no incluye monitores ni reglas personales |
| Quickshell | `shell.toml` generado y seis archivos `shell.<seccion>.toml` fusionados nativamente; no incluye Waybar |
| Kitty | Paleta nativa más perfil opcional independiente en extras; overrides personales siguen siendo responsabilidad del usuario |
| Neovim | Configuración Lua generada por Omarchy; preferencias personales pueden prevalecer |
| VS Code | Tema local generado/sincronizado por Omarchy; no se instala una extensión remota específica del tema |
| Obsidian | CSS generado en los vaults que registre Omarchy; no se distribuyen vaults |
| btop | Paleta generada nativamente |
| Menús, notificaciones y bloqueo | Superficies de Quickshell; pruebas manuales específicas pendientes |
| Iconos | Nombre `Yaru-magenta-dark` en icons.theme; requiere variante instalada |
| Pantallas | Wallpapers 16:9 Full HD; dos monitores registrados durante validación real; sin configuración de hardware incluida |

Los complementos personales `litotep.taskbar` y `litotep.music-wave` estaban registrados y habilitados durante la activación de referencia. No se incluyen ni son dependencias del tema. Su prueba funcional visual específica sigue pendiente. No se modifica `shell.json` ni el código de complementos.

En Omarchy 4.0.6, un tema clonado con `.git` no puede aportar Lua ni ciertas configuraciones ejecutables de terminal/editor en la raíz; Omarchy las regenera. Este paquete suministra paleta y datos de superficies. El perfil de Kitty permanece en extras y solo se usa a petición del usuario.

Los templates personales de cada instalación pueden cambiar el resultado. La prueba aislada utiliza las plantillas originales instaladas; no prueba cada combinación de extensiones y overrides. No se garantiza soporte para motores antiguos basados en Waybar.

## Preferencias locales y licencias

El paquete no distribuye shell.json; la preferencia bar.transparent pertenece a la sesión del usuario. La barra transparente puede calcular otro texto y afectar el color de widgets que lo hereden, por ejemplo music-wave. No constituye por sí sola una incompatibilidad del tema; ver [diagnóstico](shell-state-review.md). Yaru se referencia por nombre; no se incluyen sus recursos. Ver [terceros](THIRD-PARTY.md).
