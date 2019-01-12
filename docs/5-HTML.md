# Curso de HTML e CSS

## Día 5

- Etiquetas avanzadas
- Accesibilidade
- Lighthouse

### Etiquetas avanzadas

- Aparte das etiquetas que vimos nos días anteriores o HTML define moitas máis, aquí podedes ver todas: https://developer.mozilla.org/en-US/docs/Web/HTML/Element.
- As que vimos no curso son as máis usadas pero entre todas hai outras de relativa importancia que listo a continuación:
  - *address*: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/address
  - *blockquote*: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/blockquote
  - *figure* & *figcaption*: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/figure
  - *pre*: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/pre
  - *abbr*: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/abbr
  - *br*: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/br
  - *strong*: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/strong
  - *em*: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/em

### Accesibilidade

- A accesibilidade no HTML son un conxunto de prácticas para facer as webs máis usables para xente con discapacidades.
- A idea principal é facer un HTML que sexa igual para todo o mundo, sen importar as súas circunstancias.
- Aparte diso crear un HTML accesible mellora a optimización da web para buscadores.
- Hai lugares do mundo onde a accesibilidade en determinado tipo de webs é obrigada por lei.
- Polo tanto dende que se escribe o primeiro tag de HTML hai que pensar na accesibilidade.

#### Accesibilidade no HTML

- É sinxelo facer HTML accesible porque a linguaxe préstase a iso.
- Ao longo do curso xa falamos de accesibilidade en varios puntos:
  - Uso de etiquetas semánticas: evitamos usar etiquetas xenéricas e procuramos usar etiquetas que din algo do seu contido.
  - Estructurar ben as páxinas evitando elementos que non son apropiados para iso como as tablas e preferir elementos como section, article, aside, header e nav, etc...
  - Tentar facer que as páxinas sexan usables sen rato, só co teclado. Para iso hai que ordenar ben os elementos e usar atributos como *tabindex*.
  - Escribir labels e textos descriptivos correctamente e usar as etiquetas semánticas en cada caso correctamente, en especial nos formularios.
  - Se usamos táboas hai que usar as etiquetas semanticas para dividir as filas en encabezados, corpo e pé de táboa. Usar a etiqueta caption para describir o contido xeral da táboa.
  - Uso de texto alternativo en imaxes, tanto usando o atributo alt como as etiquetas figure e figcaption.
- Accesibilidade avanzada: https://developer.mozilla.org/en-US/docs/Learn/Accessibility/WAI-ARIA_basics

### Lighthouse

- O Lighthouse é un software de Google para avaliar a calidade dos sitios web.
- Ven instalado por defecto nas versións novas de Google Chrome.
- Aquí máis información: https://developers.google.com/web/tools/lighthouse/?hl=es
- (Demo de Lighthouse)