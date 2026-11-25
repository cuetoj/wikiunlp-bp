# La imprenta antigua en la Biblioteca Pública

**Impresores, talleres y marcas del siglo XVI a partir de Wikidata**

Aplicación web interactiva que reúne a los impresores, talleres y compañías tipográficas del siglo XVI presentes en las colecciones de las Salas Museo, Farini y Costa Álvarez de la [Biblioteca Pública de la Universidad Nacional de La Plata](https://www.biblio.unlp.edu.ar). Muestra dónde y cuándo trabajaron, y las marcas de impresor que se conservan en la Biblioteca.

El proyecto lo desarrollan la Biblioteca Pública y [Wikimedistas de la Universidad Nacional de La Plata](https://meta.wikimedia.org/wiki/Wikimedistas_de_la_Universidad_Nacional_de_La_Plata).

🔗 **Ver el sitio:** https://github.com/cuetoj/wikiunlp-bp

## Qué ofrece

- **Mapa:** las ciudades donde trabajaron los impresores. Al hacer clic en una ciudad se abren las fichas de quienes trabajaron allí, con imagen, firma o marca, fechas, ocupaciones y lugar de nacimiento.
- **Línea de tiempo:** la actividad de cada impresor, hecha con [HistropediaJS](https://js.histropedia.com). Se puede filtrar por ciudad.
- **Lista de impresores:** una tabla que se puede ordenar, buscar y descargar en CSV. Cada dato faltante lleva directamente al lugar donde se completa en Wikidata.
- **Marcas de impresores:** una galería de las marcas fotografiadas en ejemplares de la Biblioteca, con enlace a la obra en el catálogo y a Wikimedia Commons.
- **Filtros comunes** a todas las vistas: período, ciudad, persona o compañía, y ocupación.

Los colores de las fichas distinguen mujeres, varones y compañías, para dar visibilidad a las mujeres impresoras.

## De dónde salen los datos

Los datos se consultan en vivo cada vez que se abre la página. No hay una base de datos propia: todo lo que se muestra está en Wikidata y en Wikimedia Commons.

- **[Wikidata](https://www.wikidata.org):** se toman los elementos vinculados al [WikiProyecto Wikimedistas UNLP (Q114008937)](https://www.wikidata.org/wiki/Q114008937), sea porque el proyecto los mantiene (P6104) o porque están en su lista de seguimiento (P5008). De esos elementos se incluyen las personas con alguna ocupación vinculada al libro (impresor, tipógrafo, editor, grabador, ilustrador, entre otras) y las compañías.
- **Período:** se muestran quienes estuvieron activos en algún momento entre 1500 y 1599. La consulta busca un rango más amplio (1400–1699) para no perder a quien nació antes o murió después del siglo.
- **Servicios de consulta:** la página consulta primero [QLever](https://qlever.cs.uni-freiburg.de/wikidata) y, si no responde, el [Wikidata Query Service](https://query.wikidata.org). Desde la ventana "Acerca de" del sitio se puede abrir la consulta completa en cualquiera de los dos.
- **[Wikimedia Commons](https://commons.wikimedia.org):** las imágenes y la galería de marcas salen de la categoría [Marcas de impresores en la Biblioteca Pública de la Universidad Nacional de La Plata](https://commons.wikimedia.org/wiki/Category:Marcas_de_impresores_en_la_Biblioteca_P%C3%BAblica_de_la_Universidad_Nacional_de_La_Plata) y de los archivos cuyo origen (P7482) es la Biblioteca. Cuando hay varias imágenes, se priorizan las de la Biblioteca.

## Cómo colaborar

Como los datos vienen de Wikidata y Commons, cualquier mejora que se haga allí aparece en el sitio la próxima vez que se abra.

- **Completar datos:** en la Lista de impresores, cada guion (—) lleva directamente al dato que falta en Wikidata. Las fichas tienen el enlace "Ver y mejorar en Wikidata".
- **Sumar un impresor:** en su elemento de Wikidata, agregá la propiedad P5008 (lista de seguimiento) con el valor [Q114008937](https://www.wikidata.org/wiki/Q114008937). Para aparecer en el mapa y la línea de tiempo, el elemento también necesita una ocupación vinculada al libro (P106), un lugar de trabajo (P937) con coordenadas y alguna fecha.
- **Subir marcas de impresor** a la categoría de la Biblioteca en Wikimedia Commons.
- **Reportar errores o proponer mejoras al sitio:** abrí un *issue* en este repositorio.

## Tecnología

Es una sola página HTML, con CSS y JavaScript sin compilar, que no necesita servidor propio. Usa estas bibliotecas, cargadas desde CDN:

- [Leaflet](https://leafletjs.com) y [Leaflet.markercluster](https://github.com/Leaflet/Leaflet.markercluster) para el mapa;
- [MapLibre GL](https://maplibre.org) con [maplibre-gl-leaflet](https://github.com/maplibre/maplibre-gl-leaflet) para el mapa base de [CARTO](https://carto.com) con nombres en español;
- [HistropediaJS](https://js.histropedia.com) para la línea de tiempo.

Para verla en tu computadora, descargá `index.html` y abrilo en el navegador. Algunos navegadores muestran avisos al abrir archivos locales; publicada en GitHub Pages funciona sin ellos.

El mapa base usa una clave de CARTO incluida en el código. Si reutilizás este proyecto en otro sitio, pedí tu propia clave en CARTO.

## Responsables

- [Nadia Erica Buckmeier](mailto:nbuckmeier@biblio.unlp.edu.ar)
- [Julian Cueto](mailto:jjcueto@biblio.unlp.edu.ar)

## Licencias

- **Código:** [MIT](LICENSE).
- **Textos y diseño:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/deed.es).
- **Datos:** Wikidata, bajo [CC0](https://creativecommons.org/publicdomain/zero/1.0/deed.es).
- **Imágenes:** Wikimedia Commons, con la licencia indicada en cada una.

© 2026 Biblioteca Pública y Wikimedistas de la Universidad Nacional de La Plata.
