# Componentes de terceros

Revisión: 2026-10-20. La licencia propia no sustituye avisos o derechos ajenos.

| Componente | Distribución en este paquete | Tratamiento |
|---|---|---|
| Omarchy | Paleta Kitty derivada de su plantilla y datos de superficies adaptados; sin scripts de sincronización ni Lua generado | MIT, aviso conservado en LICENSES/Omarchy-MIT.txt |
| Yaru-magenta-dark | Solo el nombre en icons.theme; ningún SVG/PNG ni script | Los iconos Yaru son CC BY-SA 4.0; scripts GPL-3.0 según upstream |
| Hyprland, Quickshell, Kitty y editores | Referencias de compatibilidad y configuraciones de datos; sin binarios o código de esas aplicaciones | No se relicencian las aplicaciones |
| upscayl-ncnn 20251207-174704 | Herramienta utilizada fuera del paquete; sin ejecutable o código | AGPL-3.0 según LICENSE de esa versión |
| Real-ESRGAN | Nombre y procedencia del proceso; sin código ni pesos | Código upstream BSD-3-Clause; no implica verificar por sí solo todas las condiciones de pesos convertidos |
| Modelos oficiales distribuidos por Upscayl | Solo URLs/hashes del manifiesto; no se empaquetan bin/param | Trazabilidad documentada; no se redistribuyen pesos. Fundamento de distribución gráfica en ASSET-LICENSING.md; sin obligación automática sobre las salidas. |

La generación local de pruebas produjo configuraciones Lua, JSON y otros archivos fuera del repositorio. No se redistribuyen esos resultados. No se encontraron otros fragmentos de código externos en el paquete de datos revisado. Los prompts y documentos fueron preparados con asistencia de IA; no se consideran por eso exentos de derechos ajenos.

La matriz no identifica una incompatibilidad que obligue a relicenciar el tema por el mero uso de herramientas externas. La concesión propia se limita a material que pueda licenciarse. Una futura inclusión de iconos, modelos, binarios, fuentes o capturas con recursos ajenos exige otra revisión.

## Fuentes revisadas

- [Aviso MIT de Omarchy](https://raw.githubusercontent.com/omacom/omarchy/quattro/LICENSE), coincidente con la licencia MIT declarada por el paquete local 4.0.6-1.
- [Yaru: Copying or Reusing](https://github.com/ubuntu/yaru#copying-or-reusing). La etiqueta GPL3 global del paquete local no describe por sí sola la licencia de sus iconos.
- [upscayl-ncnn, licencia de la versión utilizada](https://raw.githubusercontent.com/upscayl/upscayl-ncnn/20251207-174704/LICENSE).
- [Real-ESRGAN BSD-3-Clause](https://github.com/xinntao/Real-ESRGAN/blob/master/LICENSE).

No se copiaron licencias GPL/AGPL/CC de proyectos que no se redistribuyen. El aviso MIT de Omarchy se conserva para el material derivado incluido.
