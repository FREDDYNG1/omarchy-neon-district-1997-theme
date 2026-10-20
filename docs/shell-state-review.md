# Revisión no destructiva de la transparencia de barra

Comparación del 2026-10-20: el respaldo anterior a la activación documenta bar.transparent=false; la configuración de sesión revisada ahora contiene true. El inventario de Etapa 5 detectó el cambio durante aquella preparación. No se conserva en Git ninguna copia completa de shell.json ni sus datos privados.

La configuración JSON comparada con la recuperada del respaldo difiere semánticamente en bar.transparent. La implementación nativa permite alternarlo con doble clic en el centro vacío de la barra o con omarchy bar transparent. Ambas vías escriben una preferencia personal. No existe evidencia para identificar quién o qué acción concreta la cambió: es una explicación posible, no una causa demostrada.

Neon District distribuye colores y seis superficies TOML, sin shell.json ni override de bar.transparent. El sincronizador de tema revisado no asigna esa preferencia. Por tanto no hay evidencia de que el paquete haya causado el cambio. El tema define colores que pueden influir visualmente en la barra transparente y en el cálculo de su texto.

En el código personal inspeccionado, litotep.music-wave toma su color de bar.barForeground; la barra transparente puede modificar su contraste indirectamente. litotep.taskbar usa su propia superficie/colores y no se encontró una lectura directa de bar.transparent. Esto no demuestra funcionamiento visual: ambas pruebas siguen pendientes.

El archivo de sesión es una preferencia local; los TOML del paquete son datos de tema y no deben coincidir con todo ese JSON. No se necesita incluir ni restaurar shell.json para publicar. Conviene revisar visualmente la barra y music-wave con la preferencia elegida y mencionar que la transparencia depende del usuario.

No se escribió, sobrescribió ni revirtió shell.json y no se cambiaron complementos.
