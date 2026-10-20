# Procedencia y procesamiento de wallpapers

Colección original creada con el generador integrado image_gen. Los prompts se conservan en wallpaper-prompts.md. No se usaron fotografías de terceros para sustituir la generación ni se solicitaron personajes, marcas o diseños de franquicias. Esto describe el proceso y no constituye una garantía de derechos exclusivos sobre resultados de IA.

## Resolución real

Ocho originales PNG de 1672×941. Real-ESRGAN x4 reconstruyó imágenes de 6688×3764; después se redujeron proporcionalmente con Lanczos y un recorte central mínimo a 1920×1080. Exportación final WebP Q95, método 6, con pérdida, sin filtros agresivos de nitidez. No son generaciones nativas Full HD o 4K.

Backend **upscayl-ncnn 20251207-174704**, [release oficial](https://github.com/upscayl/upscayl-ncnn/releases/tag/20251207-174704). Modelo **realesrgan-x4plus**, procedente de los recursos oficiales de Upscayl, con hashes conservados en wallpapers.json. Parámetros: bloques 128, `-j 1:1:1`, escala 4, sin TTA. Ejecutado en una GPU NVIDIA RTX 3060 Ti accesible desde la sesión gráfica. La reproducción del procesamiento requiere comprobar un dispositivo Vulkan válido; el índice no se debe asumir.

[Real-ESRGAN](https://github.com/xinntao/Real-ESRGAN) y [Upscayl](https://github.com/upscayl/upscayl) son proyectos externos con sus propias licencias. No se redistribuyen sus ejecutables ni modelos y no son dependencias para utilizar este tema.

Los originales, maestros PNG, resultados SR y comparaciones de trabajo se conservaron fuera del paquete público. El paquete incluye solo WebP finales, vista previa y manifiesto; no permite reproducir exactamente la generación a partir de prompts solamente. Los hashes de originales y maestros documentan las entradas y salidas preservadas.

## Revisión

Se revisaron luces, cables, ventanas, gradientes, reflejos y posibles glifos inventados. Los ocho WebP finales fueron aprobados expresamente por el usuario tras revisar los resultados SR. La superresolución puede crear detalle plausible que no existía en la entrada; no debe interpretarse como recuperación fiel de información perdida.

## Créditos

- Dirección visual y selección de la colección: proyecto Neon District 1997.
- Generación asistida por IA: image_gen.
- Reconstrucción: Real-ESRGAN mediante Upscayl NCNN/Vulkan.
- Integración: motor de temas de Omarchy, Hyprland y Quickshell.
- Iconos referenciados: Yaru-magenta-dark, distribuidos por separado.

MIT cubre código, configuración, documentación y prompts originales en lo que corresponda, con titular confirmado: Litotep (2026). No cubre estos fondos automáticamente. El fundamento contractual de distribución revisado y sus límites están en [ASSET-LICENSING.md](ASSET-LICENSING.md); licencias de herramientas y referencias en [THIRD-PARTY.md](THIRD-PARTY.md).
