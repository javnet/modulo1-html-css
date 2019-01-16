# Curso de HTML e CSS

## Día 9

- O modelo de caixas
- Estilo de caixas

### O modelo de caixas

- O modelo de caixas de CSS é a base da creación de layouts nas webs. Todos os elementos que creamos están representados por unha caixa que ten unha serie de propiedades:

  ![img](https://mdn.mozillademos.org/files/13647/box-model-standard-small.png)

- Ancho e alto:

  - As propiedades `width` e `height` definen o ancho e alto das caixas respectivamente e poden ser definidas en calqura das unidades que vimos ata agora. Excepto o height que non pode ser definido en unidades de tanto por cento (%).
  - O valor por defecto é `auto`. Cando teñen ese valor é o navegador quen calcula o tamaño das caixas que por defecto é o 100% do ancho da caixa pai e o alto establecido polos contidos internos da caixa.

- Padding:

  - A propiedade `padding` determina o marxe interno da caixa; a distancia entre os contidos e o borde interno.
  - Podemos especificar padding de cada un dos lados da caixa coas propiedades `padding-top, padding-right, padding-bottom e padding-left`.

- Margin:

  - A propiedade margin determina o marxe externo da caixa; a distancia dos bordes da caixa con outras caixas que a rodean.
  - O tamaño do marxe podemos establecelo en calquera das unidades de tamaño que xa coñecemos.
  - Se establecemos o valor como `auto` o navegador collerá o maior marxe dispoñible. Isto é aplicable aos marxes laterais e sirve tradicionalmente para centrar un elemento nun contedor.
  - Ao igual que o `padding` podemos especificar para cada lado: `margin-top, margin-right, margin-bottom e margin-left`.
  - Os marxes teñen un comportamento especial que se chama *margin collapsing*: cando dúas caixas con marxe se tocan a distancia entre elas non é a suma dos marxes se non a distancia definida polo marxe máis grande.

- Borde:

  - A propiedade `border` e define o ancho, estilo e cor do borde, a liña habitualmente visible que rodea á caixa. Veremos máis adiante como definilo.

- De todo isto conclúese que o ancho total dunha caixa é a suma do seu ancho máis o padding de cada lado máis o borde de cada lado. Se queremos mudar este comportamento por defecto podemos usar a propiedade `box-sizing` que permite os seguites valores:

  - `content-box`: é o valor por defecto. Se establecemos un `width` da caixa de 100px para calcular o ancho total o navegador sumará o borde e o padding.
  - `border-box`: cambia o modelo de caixas. Se establecemos un ancho de 100px o total sempre será 100px independentemente o ancho do borde e do padding.

#### Overflow

- Ao poder establecer un ancho e alto das caixas manualmente pode ocurrir que nalgúns casos o contido non colla dentro da caixa, para establecer que pasa con ese contido usamos a propiedade `overflow` que permite establecer estes valores (entre outros menos habituais):
  - `auto`: se o contido non colle na caixa o que quede fora non se verá e aparecerán unhas barras de scroll na caixa para poder ver ese contido.
  - `hidden`: o contido que non colla non se verá.
  - `visible`: o contido que non colla verase fora da caixa. Este é o valor por defecto.

#### Límites de ancho e alto

- Cando definimos unha caixa con ancho ou alto porcentual, por exemplo 50% podemos definir uns valores máximos dos que non queremos que se pase aínda que o tamaño do contedor creza. 
- Para isto usamos as propiedades `max-width, max-height, min-width e min-height` e a caixa collera eses valores no caso de que o ancho ou alto calculado polas propiedades `width` e `height` saia dos límites que establecemos.

#### Display

- Todo o comportamento do modelo de caixas descrito nos anteriores puntos aplícase aos elementos de tipo **block**, pero xa sabemos que hai outros elementos que son de tipo **inline**. Veremos agora as particularidades de cada tipo con respecto ao modelo de caixas e como modificar mediante CSS o tipo de cada caixa. E veremos que hai outros tipos de caixas que podemos definir usando a propiedade `display` de CSS:

  - **Caixas de bloque**: os elementos de tipo bloque apílanse uns sobre outros e teñen por defecto o ancho do contedor do que son fillos. Podemos mudar o ancho e alto desas caixas con `width` e `height` e aplican o modelo de caixas tal como explicamos ata agora.
  - **Caixas inline**: os elementos inline flúen co texto, aparecen na mesma liña que o texto que os rodea e que outros elementos inline. O seu contido distribuirase en diferentes liñas se se pasa de tamaño. **Non** podemos establecer ancho e alto destas caixas pero si marxes, bordes e paddings.
  - **Caixas inline-block**: este modo novo pódese definir só por CSS e funciona como unha mistura dos anteriores. Podemos establecer un `width e height` e non dividirán o contido en diferentes liñas se se pasan de tamaño.

- Podemos modificar o tipo de caixa usando a propiedade `display` de CSS:

  ```css
  h1 {
      display: inline;
  }
  
  strong {
      display: block;
  }
  
  span {
      display: inline-block;
  }
  
  ```

- Hai outro tipo de caixa que se chama `flex`que veremos nos próximos capítulos.

### Estilo de caixas

#### Fondo

- O fondo dunha caixa é a área posterior ao espazo que ocupa o contido da caixa, padding e border. Pero non o marxe.

- Podemos especificar fondos de cor ou de imaxe usando unha serie de propiedades:

  - `background-color`: permite establecer unha cor de fondo. Por defecto as caixas teñen como cor de fondo `transparent`:

    ```css
    p {
        padding: 2rem;
        background-color: rebeccapurple;
        color: white;
    }
    ```

  - `background-image`: permite establecer unha imaxe como fondo usando a notación `url(...)`:

    ```css
    h1 {
        background-image: url(/images/fondo.png);
    }
    ```

  - `background-repeat`: por defecto os fondos de imaxe repítense para cubrir todo o espazo da caixa, esta propiedade permite definir como funciona esa repetición:

    - `no-repeat`: a imaxe de fondo non se vai repetir, só se mostrará unha vez.
    - `repeat-x`: a imaxe só se repetirá horizontalmente.
    - `repeat-y`: a imaxe só se repetirá verticalmente.
    - `repeat`: este é o valor por defecto e repetirá a imaxe horizontal e verticalmente ata cubrir todo o espazo da caixa.

  - `background-position`: no caso de ter un fondo cunha imaxe que non se repita esta propiedade vainos permitir posicionar esa imaxe. Por defecto soporta dous valores separados por espazo para especificar as coordenadas x e y da imaxe con respecto ao centro de coordenadas que é a esquina superior esquerda. Aparte de sorportar calquera das unidades coñecidas (px, rem, %), tamén soporta posicions con nome (e calquera combinación entre unhas e outras): 

    - left, center, right: para posicionamento horizontal
    - top, center, bottom: para posicionamento vertical

    ```css
    p {
        background-color: rebeccapurple;
        background-image: url(/images/fondo.png);
        background-repeat: no-repeat;
        background-position: 200px center;
    }
    ```

  - `background-size`: permite establecer o tamaño da imaxe especificada como fondo con `background-image`.  Os posibles valores son:

    - Dous valores separados por espazo: establece o tamaño da imaxe de fondo, os dous valores poden ser nas unidades típicas de css ou `auto`. O valor por defecto da propiedade é `auto auto`.
    - `contain`:  tenta encaixar a imaxe sen recortala dentro do fondo sen recortala nen modificar as proporcións.
    - `cover`: tenta encaixar a imaxe no background sen modificar as proporcións pero pode recortala se é necesario. Esta propiedade é moi útil para poñer imaxes de fondo en caixas de tamaño variable.

- Ampliando coñecemento na MDN:

  - Fondos múltiples: https://developer.mozilla.org/en-US/docs/Learn/CSS/Styling_boxes/Backgrounds#Multiple_backgrounds
  - A propiedade `background` permite establecer varias das propiedades comentadas anteriormente nunha sóa liña, podedes aprender máis dela aquí: https://developer.mozilla.org/en-US/docs/Web/CSS/background
  - Gradientes: https://developer.mozilla.org/en-US/docs/Learn/CSS/Styling_boxes/Backgrounds#Background_image_gradients

#### Borde

- O borde dunha caixa está definido por tres propiedades: anchura, estilo e cor. Por defecto as caixas teñen un borde de anchura `0`, negro e sólido (unha liña sen espazos).

- Podemos modificar o borde dunha caixa coa propiedade `border` que permite definir as tres propiedades na mesma liña ou establecelas por separado coas propiedades `border-width, border-style e border-color`:

  ```css
  h1 {
      border: 2px solid blue;
  }
  
  /* A seguinte regla é igual que a anterior pero por separado*/
  h1 {
      border-width: 2px;
      border-style: solid;
      border-color: blue;
  }
  ```

  - `border-width`: establece o ancho do borde en calquera unidade de CSS (excepto %).
  - `border-style`: os posibles valores de estilo son estes https://developer.mozilla.org/en-US/docs/Web/CSS/border-style#Values. Os típicos valores son `solid` (por defecto), `dotted` e `dashed` que establecen liñas sólidas, de puntos e de raias respectivamente.
  - `border-color`: establece a cor do borde usando calquera notación de cor de CSS.

- Se queremos facer bordes redondeados usamos a propiedade `border-radius` que permite establecer o radio de redondeo dos bordes:

  ```css
  p {
      border: 2px solid red;
      borde-radius: 20px;
  }
  ```

  Se queremos establecer un radio de redondeo diferente para cada esquina podemos establecer catro valores separados por espazo que establecerían por orde o radio de: equina superior esquerda, superior dereita, inferior dereita e inferior esquerda:

  ```css
  p {
      border: 2px solid red;
      borde-radius: 20px 20px 0 0;
      /*só teria os as esquinas superiores redondeadas*/
  }
  ```

#### Sombras

- Ao igual que o texto (`text-shadow`) as caixas poden ter sombras coa mesma notación:

  ```css
  h1 {
      box-shadow: 2px 2px 5px black;
  }
  ```

- Os valores son respectivamente: desplazamento horizontal, desplazamento vertical, radio de difusión e cor de sombra.