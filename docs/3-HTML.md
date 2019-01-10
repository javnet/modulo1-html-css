# Curso de HTML e CSS

## Día 3

- Listas
- Táboas
- Multimedia no HTML: Imaxes



### Listas

- Os tags *ul* e *ol* permiten crear listas desordenadas e ordenadas.

- As listas desordenadas mostrar cada elemento cun punto (bullet) e as ordenadas cun número.

- Exemplo de lista desordenada:

  ```html
  <ul>
    <li>Tinky Winky</li>
    <li>Dipsy</li>
    <li>Laa-Laa</li>
    <li>Po</li>
    <li>Noo-Noo</li>
  </ul>
  ```

- Exemplo de lista ordenada:

  ```html
  <ol>
  	<li>Primeiro</li>
  	<li>Segundo</li>
  	<li>Terceiro</li>
  </ol>
  ```

- Os dous tipos de listas permiten aniñamento, exemplo:

  ```html
  <ul>
  	<li>A Mariña Occidental
  		<ol>
  			<li>Viveiro</li>
  			<li>Xove</li>
  			<li>Vicedo</li>
  		</ol>
  	</li>
  	<li>A Mariña Oriental
  		<ol>
  			<li>Ribadeo</li>
  			<li>Barreiros</li>
  			<li>Trabada</li>
  		</ol>
  	</li>
  </ul>
  ```

- As listas de definición son listas avanzadas que permiten asociar un termo a unha definición, o seu uso é bastante limitado.

- Os tags que usa son *dl* para inicial abrir a lista de definición e despois *dt* para especificar o termo e *dd* para a definición. Exemplo:

  ```html
  <dl>
  	<dt>HTML</dt>
  	<dd>Linguaxe de etiquetado</dd>
  	<dt>CSS</dt>
  	<dd>Linguaxe de follas de estilo</dd>
  	<dt>JavaScript</dt>
  	<dd>Linguaxe de programación interpretado</dd>
  </dl>
  ```


### Táboas

- As táboas son conxuntos estructurados de filas e columnas. Sirven para mostrar contido tabular e nada máis.

- No pasado usáronse para maquetar como base da grella. Isto considérase unha moi mala práctica.

- Definimos un elemento de táboa co tag *table* que un tag de bloque.

- As táboas en HTML están compostas por filas co tag *tr* (table row) que conteñen celas definidas polo tag *td* (table data), exemplo básico:

  ```html
  <table>
  	<tr>
  		<td>Columna 1</td>
  		<td>Columna 2</td>
  	</tr>
  	<tr>
  		<td>Valor 1</td>
  		<td>Valor 2</td>
  	</tr>
  </table>
  ```

- No exemplo anterior creamos unha táboa de 2 filas con 2 celas cada fila formando deste xeito 2 columnas, ou sexa, unha táboa 2x2.

- Se unha cela queremos definila como cela de cabeceira podemos mudar o seu tag por *th* que é unha etiqueta semántica, exemplo anterior modificado:

  ```html
  <table>
  	<tr>
  		<th>Columna 1</th>
  		<th>Columna 2</th>
  	</tr>
  	<tr>
  		<td>Valor 1</td>
  		<td>Valor 2</td>
  	</tr>
  </table>
  ```

- Se queremos que unha fila ou cela ocupe máis que o seu espazo natural podemos usar os atributos *rowspan* e *colspan*. É importante manter a estrutura lóxica ou a táboa mostraráse descolocada. Por exemplo se queremos crear unha táboa con 2 filas pero que a primeira fila só teña unha cela e a segunda dúas faremos isto:

  ```html
  <table>
  	<tr>
  		<th colspan="2">Columna ancha</th>
  	</tr>
  	<tr>
  		<td>Valor 1</td>
  		<td>Valor 2</td>
  	</tr>
  </table>
  ```

- Usamos o tag *caption* dentro da táboa se queremos darlle un título semántico á táboa:

  ````html
  <table>
  	<caption>Título da táboa</caption
  	...
  </table>
  ````

- Do mesmo xeito que os tags *section, article, aside, footer, etc...* tamén temos tags estructurais que definen semánticamente partes dunha táboa. Estes son 

  - *thead*: define as filas e celas de encabezado.
  - tbody: define as filas e celas principais da táboa
  - tfoot: define as filas e celas de pé de táboa

### Multimedia no HTML: Imaxes, audio e video

- As imaxes no HTML están soportadas completamente dende mediados dos 90 pero o soporte completo de audio e o video chegou coa especificación do HTML5

- Os navegadores soportan imaxes en moitos formatos, pero os máis habituais son:

  - JPEG: ou JPG, é o máis famoso e é apropiado para fotos.
  - PNG: é máis moderno e máis apropiado para imaxes con cores planos e soporta transparencias.
  - GIF: úsase sobre todo para animacións.

- Para insertar unha imaxe nun documento HTML usamos o tag *img*:

  ```html
  <img src="imaxe.jpg" alt="texto descriptivo da imaxe">
  ```

- O tag *img* é un tag de tipo inline polo tanto non crea unha nova liña ao insertalo.

- O audio está soportado en HTML dende hai tempo co elemento *bgsound* pero só polo Internet Explorer e só soporta audio en formato MIDI (mid).

- O HTML5 trae o tag *audio* que está soportado por todos os navegadores.

- Os formatos de audio soportados son varios pero é habitual que se use o MP3. Aquí tedes unha lista de formatos de audio (e video) soportados: https://developer.mozilla.org/en-US/docs/Web/HTML/Supported_media_formats

- Para insertar audio nunha web:

  ```html
  <audio src="audio.mp3" controls>
  ```

- Aparte do atributo controls que mostra os controles de play/pause/volume hai outros atributos importantes:

  - *autoplay*: fai que o sonido comece a reproducirse automáticamente
  - loop: reproduce o audio de novo ao rematar
  - Máis atributos aquí: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/audio#Attributes

