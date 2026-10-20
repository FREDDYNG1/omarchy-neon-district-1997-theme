# Auditoría de privacidad de distribución

Revisión del 2026-10-20, limitada a los archivos preparados para distribución.

- Copia mediante lista explícita: paleta, iconos por nombre, seis superficies Quickshell, dos perfiles/paletas Kitty, ocho fondos, vista previa y documentación pública.
- Excluidos respaldos, registros originales de activación, inventarios de archivos personales, preferencias de aplicaciones, vaults, configuraciones de monitores, hooks, complementos, scripts de activación particulares, originales voluminosos, modelos y ejecutables.
- Escaneo de texto sin rutas HOME absolutas de usuario, claves privadas ni patrones comunes de credenciales. Los nombres de los dos complementos personales se mantienen únicamente como identificadores de compatibilidad solicitados; no se incluyen sus datos ni código.
- Imágenes decodificadas y comprobadas sin campos EXIF/XMP. Vista previa inspeccionada: cuadrícula de fondos con sus títulos, sin contenido de ventanas personales.
- Referencias de instalación mediante HOME y rutas relativas; copia y generación comprobadas en un HOME temporal distinto.
- .gitignore excluye clases de datos privados y temporales; no sustituye la revisión antes de git add y cada commit.
- Sin remoto, sin push, sin commit de autor supuesto. La identidad pública del autor debe elegirse antes del primer commit.
- Tema activo y temas previos sin cambios durante esta preparación. Se observó un cambio concurrente en una configuración personal de la sesión, que esta tarea no escribió ni restauró; no se declara íntegramente inmutable la sesión en vivo. Respaldo privado de activación conservado y hash del archivo verificado.

El escaneo de patrones no garantiza detectar todo secreto posible. Antes de publicar, revisar el diff completo, identidad Git, términos de las imágenes y cada futura captura. No se incluyen los informes privados para demostrar estas comprobaciones.

## Actualización de Etapa 5.1

Se revisaron nuevamente todos los archivos distribuibles, incluidos LICENSE y el aviso original MIT de Omarchy. Se comprobó la ausencia de rutas personales absolutas, patrones comunes de tokens/claves/direcciones IPv4 privadas, enlaces simbólicos y archivos vacíos. Las imágenes no contienen campos personales EXIF/XMP detectados. Esto es una comprobación de contenido y patrones, no una garantía absoluta de ausencia de todo secreto imaginable.

Los nombres de titulares que figuran en avisos de terceros son atribuciones públicas, no identidades de la cuenta local. Los dos identificadores de complementos se conservan para documentar la compatibilidad solicitada. No se extrajo la identidad del titular propio del nombre de usuario o de Git.

La comparación de 175 entradas protegidas al inicio y al final de esta revisión no mostró diferencias: temas instalados, estado activo y selección de fondo, Kitty, Hyprland, shell.json y complementos permanecieron iguales durante Etapa 5.1. La diferencia histórica de transparencia se investigó sin restaurarla.

La copia de instalación se verificó en un HOME temporal diferente y pasó el manifiesto de hashes. Es una prueba de portabilidad de archivos; no se creó una cuenta real ni se probó el escritorio de otro usuario. Se reutilizó la validación nativa previa, sin ejecutar activaciones, commits o etiquetas en esta etapa.

En la comprobación de Etapa 5.1, Git local estaba en main, sin archivos rastreados, historial, tags o remotos. No hay configuración local de identidad/credenciales de publicación. En aquella comprobación, los archivos sin rastrear eran candidatos de distribución y todavía necesitaban revisión y autorización antes del primer commit. La lista de exclusiones se comprobó con nueve casos, incluidas capturas sin revisar y credenciales locales.

[Informe de esta revisión](stage5-1-audit.json), [licencias de recursos](ASSET-LICENSING.md) y [diagnóstico de transparencia](shell-state-review.md). En Etapa 5.2 se completó LICENSE con el titular Litotep, confirmado expresamente por el usuario; este punto ya no bloquea la publicación.

## Cierre rápido de publicación

Se autoriza una única auditoría final del conjunto candidato a Git, con resultados en [final-audit.json](final-audit.json). Las comprobaciones funcionales previas se reutilizan; las pruebas manuales pendientes quedan como limitaciones conocidas. preview.png es la vista previa provisional autorizada. Documentación y prompts originales quedan bajo MIT en lo que corresponda. El fundamento de distribución gráfica está en ASSET-LICENSING.md; el estado de la identidad Git se explica en [release.md](release.md). No se publica un remoto, etiqueta ni push.

Cierre del commit inicial: el usuario indicó expresamente su correo de autor. Se usa únicamente en metadatos Git; el correo es institucional y no se presenta como noreply. La identidad se pasa a la invocación del commit sin escribir configuración global. Se conserva la auditoría previa y solo se actualizan los documentos de estado; no se publica un remoto.
