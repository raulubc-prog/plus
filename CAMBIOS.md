# Cambios — Plus Desplazamiento

Web: https://raulubc-prog.github.io/plus/ · Enlace modo manual: https://raulubc-prog.github.io/plus/?modo=mano

Historial de GitHub reiniciado el 19/10/2026 (v2.3.19) por privacidad; las versiones anteriores solo quedan descritas aquí.

## 21/10/2026
- **v2.3.28** — Foto a la Orden de Trabajo con la cámara: "Hacer foto a la Orden de Trabajo" abre la cámara dentro de la web con un recuadro para encajar la tabla de arriba y "Capturar" (se lee solo lo de dentro del recuadro). Si el navegador no deja usar la cámara en la web, abre la cámara del móvil; "Elegir foto" sigue para fotos ya hechas. La imagen de la cámara no sale del móvil.
- **v2.3.27** — "Obra con foto de la Orden de Trabajo" (modo "Apuntar a mano"): haces una foto a la Orden de Trabajo de la carpeta de montaje y la web rellena la obra con lo que pone en "Localización" (y la dirección para la ruta). La foto se lee en el propio móvil con Tesseract.js (Apache-2.0, servido desde el repo, sin internet); la foto y el resto del texto no se guardan ni se envían. Tú revisas, pones los km y la añades. Aviso de privacidad ampliado. Ejemplos con A Coruña → Santiago (antes Zaragoza → Huesca). (La v2.3.26, con carga de obras desde carpetas, no se publicó.)

## 20/10/2026
- **v2.3.25** — Ejemplos de nombres de obra y de parada cambiados por lugares inventados ("Huesca centro", "paso: compañero Tudela").
- **v2.3.24** — La flecha ▸/▾ también en las tarjetas de cada día del modo "Apuntar a mano".
- **v2.3.23** — En "Días con plus", cada fila lleva ▸ (▾ al abrirla) para que se vea que se despliega. Aviso de privacidad más completo: sin cookies ni rastreo, OSRM es un servidor de FOSSGIS en la UE, GitHub Pages registra la IP de cada visita, y no escribir nombres de otras personas. Atribución de OpenStreetMap (ODbL) junto a "Km carretera".
- **v2.3.22** — Para enseñar al comité (borrador del acuerdo y textos legales):
  - Aviso arriba: "Prototipo. Los importes son orientativos y no sustituyen al cálculo oficial de la empresa."
  - "Plus desde" vacío por defecto y, junto al campo, en el resultado y en el PDF: "Sin acuerdo firmado no hay devengo: los importes son orientativos." "Km para el plus" sigue por defecto en "Km fijos de la obra". Quien ya tenía ajustes guardados los conserva.
  - Nueva opción en "Cálculo": "Por duración de la ruta (OSRM)". Pasa los km de más a horas con la velocidad media de la ruta casa → obra según OSRM, en vez de los 90 km/h fijos. OSRM solo se consulta al elegir esta opción o al pulsar "Calcular km por carretera". Si OSRM no responde, se calcula con km ÷ velocidad y se avisa en pantalla. La tabla de obras muestra la duración y la velocidad de la ruta.
  - Pie: "© 2026 Plus Desplazamiento · Uso gratuito, se ofrece tal cual, sin garantía, y puede retirarse sin previo aviso." Versión igual en cabecera y pie.
- **v2.3.21** — Seguridad y privacidad, sin cambios visibles en el uso:
  - Las fuentes (Barlow) y la librería del PDF (jsPDF) se sirven desde el propio repo: ninguna visita pasa ya por Google Fonts ni por un CDN externo. Lo único que sale fuera sigue siendo lo que dice el aviso: OSRM (si lo pides) y Google Maps (si abres la ruta).
  - Política de contenido (CSP): la página solo puede conectarse a OSRM; cualquier otro envío de datos queda bloqueado por el navegador.
  - Archivos de copia (obras y modo manual): se comprueba el tipo de cada dato antes de guardarlo; un archivo mal formado ya no deja la app rota. Límite de 5 MB. Si una copia trae ajustes distintos a los tuyos (€/hora, umbral…), el mensaje de carga los enumera en vez de cambiarlos en silencio.
  - Al arrancar, si en el móvil quedó guardado un ajuste con tipo raro, se repara solo.

## 19/10/2026
- **v2.3.20** — Instrucciones para sacar la Cronología rehechas paso a paso (Ajustes → Ubicación → Ajustes de ubicación → Cronología → Exportar), con aviso de que no está en Google Maps.
- **v2.3.19** — Privacidad: el ejemplo inicial pasa a ciudades y cifras inventadas (Zaragoza → Huesca); RETOMAR.md sale del repo; historial de GitHub reiniciado en un solo cambio.
- **v2.3.18** — Segunda revisión a fondo (prueba con 3 meses de datos, dos obras el mismo día, paradas de paso, cambio de hora, cruces de medianoche: todo correcto). Arreglos:
  - Modo manual: en el móvil, el botón "↻ repetir" ya no tapa el "Sin marcar" con nombres largos.
  - Día Casa → Casa (parada corta): si lo añades en "Días añadidos a mano" con su obra, ahora sí se calcula con los km de esa obra.
  - Copia del modo GPS ("Guardar obras en archivo") guarda también los días desmarcados, los ajustes y la casa, y al cargarla se recuperan. Antes, tras "Borrar todo", se perdían.
  - Copia del modo manual: al cargarla en otro móvil que ya tenía una obra con el mismo nombre, los días marcados salían como "obra quitada". Arreglado.
  - Cronología sin ninguna estancia larga: en vez de un error confuso, explica que escribas la casa en Ajustes.
  - Editar una obra en "Tus obras": al pasar del nombre a los km ya no se pierde lo escrito.
  - Ajustes imposibles (velocidad 0, umbral negativo, horario vacío) vuelven al valor por defecto en vez de dejar el cálculo en 0 €.
  - Datos guardados corruptos ya no dejan la pantalla en blanco.
  - "Casa (lat, lng)" admite comas decimales y el símbolo de grados.
  - Aviso ⚠ de viaje largo visible aunque el nombre de la obra sea largo.
  - Teclado: Enter sobre "↻ repetir" repite en vez de abrir la fila.

## 18/10/2026
- **v2.3.17** — Correo de contacto plus.desplazamiento@gmail.com al final de la página y en el aviso "Tus datos no salen de este móvil".
- **v2.3.16** — Arreglos tras revisión completa:
  - Cargar obras sin Cronología ya no borra los días añadidos a mano guardados.
  - "Días añadidos a mano" pide cargar antes la Cronología (antes se perdían sin avisar).
  - El ejemplo ya no usa tus días desmarcados.
  - Un archivo erróneo tras uno bueno ya no hace desaparecer la tarjeta de la Cronología cargada.
  - Exportar: el periodo sale bien con fechas abiertas ("hasta el…", "desde el…") y sin días ("sin días con plus").
  - El texto del cálculo en el PDF usa coma decimal en €/km y describe bien el modo "tiempo real".
  - La copia del modo manual recupera también los ajustes (precio hora, precio km, umbral…).
  - La copia sin Cronología ya no guarda la casa inventada del ejemplo.
  - Seguridad: los nombres de obra se muestran escapados en todas las tablas.
  - El selector de obra de "Días añadidos a mano" ya no puede elegir otra obra al reordenarse la lista.
- **v2.3.15** — Modo manual: al cargar una copia, "Tus obras" queda abierto para que se vea el mensaje de confirmación.
- **v2.3.14** — "Cronología cargada" pasa a desplegable: se ve el resumen (trayectos y fechas); "Cargar otra" y "Quitar esta Cronología" quedan dentro.
- **v2.3.13** — Arreglos al guardar y cargar obras: sin Cronología cargada, "Guardar copia" guardaba solo la obra de ejemplo (ahora guarda las obras reales del móvil). Los botones de cargar dejan elegir el archivo en cualquier Android. Mensajes claros al cargar.
- **v2.3.12** — En "Borrar datos": aviso de guardar copia antes, con botón "Guardar copia ahora"; el mensaje de confirmación también lo recuerda.
- **v2.3.11** — Desplegable "Borrar datos" al final (los dos modos): borrar días, borrar obras o borrar todo. Pide confirmación.
- **v2.3.10** — Título y logo vuelven al tamaño original. A ese tamaño no caben en una línea: el logo va justo debajo del título.
- **v2.3.9** — Título y logo "> 50 km" más grandes en el móvil.
- **v2.3.8** — Logo "> 50 km" a continuación del título, en la misma línea.
- **v2.3.7** — Título "Días con plus · mes" encima del importe y la lista de días.
- **v2.3.6** — Dentro del desplegable de cada día: "Ver punto" de su obra en Maps. En días sin obra: "Ver dónde paraste" (parada más lejana de casa).
- **v2.3.5** — Obras ordenadas por fecha (la más reciente arriba). Días sin obra (Casa → Casa sin parada larga) salen como "Sin obra" con explicación.
- **v2.3.4** — Sobre la 2.3.2: bloques en desplegables cerrados (aviso de datos, Días añadidos a mano, Obras, Copia de seguridad). Obras como en la 2.3.1.
- **v2.3.3** — (descartada, sustituida por la 2.3.4) Obras en tarjetas de dos líneas con km · días · €.
- **v2.3.2** — Cronología cargada resaltada en azul con "Cargar otra" y "Quitar esta Cronología". Campo "o precio km (€)" junto al precio hora: si se rellena, manda.
- **v2.3.1** — Enlace directo al modo: `?modo=mano` o `?modo=gps`.
- **v2.3.0** — Modo GPS por defecto; botones de carga en azul.

## Antes (17–18/10/2026)
- **v2.2.9** — Cabecera: título y versión → aviso de datos → pestañas.
- **v2.2.6–2.2.8** — Tabla de obras apilada en el móvil; un solo km por obra ("Km casa → obra").
- **v2.2.5** — Vista compacta: una fila por día (fecha · obra · €), se despliega al tocar.
- **v2.2** — Modo manual para quien no tiene Cronología; casa configurable.
