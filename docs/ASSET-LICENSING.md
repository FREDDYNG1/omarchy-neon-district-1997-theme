# Recursos gráficos: fundamento de distribución

## Alcance y decisión

Se incluyen los ocho wallpapers de backgrounds/ y preview.png como recursos gráficos del tema, **fuera de MIT**. La revisión concluye que existe fundamento razonado para distribuirlos con el proyecto encargado por Litotep, conforme a la procedencia y las condiciones estándar oficiales de OpenAI que se detallan abajo. No se afirma exclusividad, protección de autor automática ni dominio público.

La autorización del proyecto comprende preparar la colección para su distribución, descarga e instalación como parte del tema. No se concede mediante MIT una licencia gráfica general, ni se promete al receptor que pueda sublicenciar recursos ajenos. Cualquier derecho que se conceda queda limitado a los que legítimamente puedan concederse; los usos permitidos directamente por la ley no se restringen por esta declaración. La publicación remota sigue requiriendo autorización expresa.

## Procedencia contrastada

[provenance.md](provenance.md), los [prompts](wallpaper-prompts.md) y el [manifiesto](wallpapers.json) documentan ocho PNG generados con la herramienta integrada image_gen de OpenAI, no fotografías descargadas ni material de franquicias incorporado para sustituirlos. Los originales son 1672×941; se conservaron fuera del paquete junto a maestros y resultados de trabajo. No se identifica un modelo interno concreto por conjetura.

Los finales son neon-alley.webp, skyline-1997.webp, retro-terminal.webp, night-market.webp, cyber-train.webp, industrial-core.webp, data-rain.webp y synth-city.webp: WebP Q95, método 6, 1920×1080. preview.png deriva de esos ocho fondos. Los resultados fueron aprobados visualmente por el usuario.

## Fundamento contractual oficial

Fuentes consultadas el 2026-10-20:

- [OpenAI Terms of Use para particulares fuera de Europa](https://openai.com/policies/row-terms-of-use/), sección Content: asignan al usuario frente a OpenAI los derechos sobre Output que correspondan legalmente, advierten que puede no ser único y mantienen la responsabilidad sobre entradas y uso.
- [Europe Terms of Use](https://openai.com/policies/terms-of-use/), sección Content: contienen la misma asignación relevante sobre las salidas, dentro de lo permitido legalmente.
- [OpenAI Services Agreement](https://openai.com/policies/services-agreement/), secciones 4.1–4.4: contempla una asignación equivalente para servicios empresariales/API, con responsabilidad del cliente y sin garantizar exclusividad.
- [FAQ oficial sobre copyright de salidas API](https://help.openai.com/en/articles/5008634-will-openai-claim-copyright-over-what-outputs-i-generate-with-the-api): confirma que OpenAI no reclama copyright sobre las salidas generadas para el usuario o sus usuarios finales.
- [Service Terms](https://openai.com/policies/service-terms/) y [Sharing & publication policy](https://openai.com/policies/sharing-publication-policy/): complementan las obligaciones aplicables. No se representa el contenido generado como exclusivamente humano ni se garantiza indemnidad sobre imágenes transformadas.

**Conclusión de la revisión, no cláusula contractual nueva:** los regímenes estándar revisados coinciden en la asignación relevante; combinados con la generación OpenAI documentada para este proyecto, proporcionan base para su inclusión y distribución por el usuario. No conocer el plan o el identificador interno de modelo no demuestra por sí mismo una restricción de publicación y no se mantiene como bloqueo autónomo. No se ha acreditado un contrato especial que cambie esa conclusión; tampoco se afirma haber inspeccionado contratos privados de la cuenta.

El fundamento se limita a la relación con OpenAI y a los derechos que existan. No elimina derechos de terceros, no determina la protegibilidad en cada país y no promete autorización para explotar cualquier elemento que eventualmente resulte ajeno. Una reclamación concreta o evidencia de condiciones especiales exigiría reevaluación; no existe tal evidencia en los registros revisados.

## Superresolución y modelos

Se utilizó upscayl-ncnn 20251207-174704, NCNN/Vulkan, realesrgan-x4plus, bloques 128 y -j 1:1:1; salida 6688×3764 y reducción Lanczos proporcional con recorte mínimo a 1920×1080, sin enfoque agresivo. No son generaciones nativas 4K. Los pesos proceden de los recursos oficiales de Upscayl y sus hashes están documentados.

La licencia [AGPL-3.0 del backend](https://raw.githubusercontent.com/upscayl/upscayl-ncnn/20251207-174704/LICENSE), sección 2, no cubre automáticamente toda salida: depende de si su contenido constituye obra cubierta. El código de [Real-ESRGAN](https://github.com/xinntao/Real-ESRGAN/blob/master/LICENSE) es BSD-3-Clause. Estas licencias regulan herramientas/código; no son una concesión de copyright sobre imágenes ni una obligación automática de aplicar AGPL, BSD o MIT a los fondos.

No se distribuyen ejecutables, código o pesos de esas herramientas. No se ha verificado por separado una licencia para cada conversión bin/param; es una limitación de trazabilidad, no evidencia concreta de una prohibición sobre estos WebP. Cualquier futura distribución de pesos o herramientas requerirá revisar sus condiciones propias. Véase [THIRD-PARTY.md](THIRD-PARTY.md).

## Distinciones y límites

- **Uso/distribución contractual:** la base revisada permite sustentar la inclusión de las salidas del proyecto frente a OpenAI, sujeta a las obligaciones aplicables.
- **Derecho de autor:** su existencia, alcance y titularidad dependen de la ley y de aportaciones humanas. La asignación contractual y la superresolución no crean automáticamente protección ni exclusividad.
- **Licencia del paquete:** MIT cubre únicamente código, configuración, documentación y prompts originales que puedan licenciarse. Los fondos y preview.png no pasan a MIT por acompañarlos.

No se identificó una incertidumbre legal material concreta que obligue a bloquear la inclusión de esta colección con la evidencia revisada. Persisten límites generales de copyright y derechos de terceros; esto no equivale a una garantía universal de ausencia de reclamaciones.

Las pruebas manuales pendientes se mantienen como limitaciones conocidas. preview.png es la vista previa provisional autorizada; no hay capturas reales aprobadas. Las futuras capturas deberán revisarse por privacidad y por los recursos ajenos que reproduzcan, incluidos los iconos Yaru.
