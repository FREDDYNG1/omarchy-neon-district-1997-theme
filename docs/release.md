# Publicación de v1.0.0

El usuario autorizó finalizar el paquete en una ejecución y crear el commit inicial solo si no existen bloqueadores críticos. No están autorizados la etiqueta, el remoto ni el push durante este cierre.

## Decisiones cerradas

- MIT íntegra, Copyright (c) 2026 Litotep, para código, configuración, documentación y prompts originales cuyos derechos puedan licenciarse.
- Avisos y licencias de terceros conservados. Imágenes y preview.png fuera de MIT.
- preview.png aceptada como vista previa provisional; no se requieren capturas reales ahora.
- Pruebas manuales pendientes aceptadas como limitaciones conocidas, sin inventar resultados.
- Validaciones previas reutilizadas; una única auditoría final del conjunto previsto para Git.

## Estado para el commit local

La revisión de términos oficiales y procedencia aporta fundamento de distribución gráfica sin extender MIT a imágenes. Véase [ASSET-LICENSING.md](ASSET-LICENSING.md). No se identificó otro bloqueo legal material concreto con la evidencia revisada; no se garantiza copyright o ausencia universal de derechos ajenos.

El usuario proporcionó expresamente la dirección de correo para el commit inicial con autor Litotep. Es una dirección institucional, no noreply; se usa tal como fue indicada y queda en los metadatos Git. No se copia aquí ni se modifica la configuración global. Las pruebas manuales pendientes y el uso provisional de preview.png ya están aceptados como limitaciones.

## Commit inicial local

El commit inicial contiene v1.0.0 preparada y la documentación de sus límites. Para consultar su identificador, autor y asunto desde el repositorio:

```bash
git log -1 --format=fuller
git status --short
```

No existe etiqueta v1.0.0, remoto ni publicación. La identidad se proporciona solo a la invocación del commit; no se cambia la configuración global.

Solo después de autorización de publicación remota:

```bash
git tag -a v1.0.0 -m "Neon District 1997 v1.0.0"
gh repo create omarchy-neon-district-1997-theme --public --source=. --remote=origin
git push -u origin main
git push origin v1.0.0
```

Los comandos de publicación remota anteriores no se han ejecutado. El estado final del índice y la auditoría están en [final-audit.json](final-audit.json). No aplicar cambios al escritorio para publicar este repositorio.
