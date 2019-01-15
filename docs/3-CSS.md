# Curso de HTML e CSS

## Día 8

- Unidades e cores
- Estilo de textos
- Tipografía

### Unidades e cores

#### Unidades

- Moitas das propiedades de CSS que vimos ata agora e moitas das que veremos teñen valores numéricos, a maioría deles van asociados a unidades pero non todos.

- As unidades historicamente máis habituais son os píxeles (px), que son unidades absolutas e sempre miden o mesmo:

  ```css
  p {
    margin: 5px;
    padding: 10px;
    border: 2px solid black;
  }
  ```

- Hai outras unidades absolutas como cuartos de milimetro (q), milimetros (mm), centímetros (cm), pulgadas (in), etc... pero o seu uso non é habitual.

- Coa proliferación da web en dispositivos de diferentes tamaños de pantalla as unidades absolutas están quedando cada vez máis en desuso a favor das relativas que en xeral dependen de outros factores como o tamaño do contedor ou outros factores proporcionais:

  - **em**: `1em` coincide co tamaño da fonte do elemento onde se aplica, que normalmente ven herdada do elemento pai. Se non se fai ningún cambio de fonte o valor por defecto de `1em` nos navegadores é de 16px.
  - **rem**: moi similar ao anterior pero en lugar de ter en conta o tamaño da fonte herdada do elemento pai sempre colle o tamaño de fonte do elemento raíz que é o `html`. Polo que se usamos sempre unidades rem será moi sinxelo modificar a proporción simplemente modificando o tamaño de fonte do elemento `html` mediante CSS.
  - **vw, vh**: unidades que dependen do tamaño da ventana do navegador. `1vw` é unha centésima parte do ancho da ventana e `1vh` é unha centésima parte do alto da ventana. Son útiles para establecer tamaños de caixas como veremos máis adiante.
  - **porcentaxes**: se establecemos unha unidade coma porcentaxe estamos establecendo o porcentaxe do valor por defecto desa propiedade. Por exemplo `font-size: 200%;` establecería un tamaño de fonte doble da herdada para ese elemento e se usamos `width: 50%;` estableceríamos un ancho da metade do contedor para ese elemento.

- Se temos que establecer unha unidade con valor 0 non é necesario establecer as unidades, 0 sempre é cero usemos a unidade que usemos: `margin: 0;` por exemplo.

- Hai outras propiedades que admiten valores sen unidades, por exemplo `line-height` que establece o alto de liña dun texto. Por defecto é 1.2, sen unidades.

#### Cores

- Hai varios xeitos de especificar as cores en CSS e todas teñen o mesmo resultado.

- O modelo de cor dos dispositivos modernos é de 24bits polo que admite 16.7 millóns de cores posibles, estos son unha combinación de 3 canles de cor: vermello (R), verde (G) e azul (B). Cada unha destas unidades permite 256 valores numéricos, entre 0 e 255.

- Xeitos de especificar cores en CSS:

  - Cores con nome: CSS soporta un gran número de cores por defecto que teñen un nome asociado. Aquí podedes ver a lista completa: https://developer.mozilla.org/en-US/docs/Web/CSS/color_value#Color_keywords Para establecer un color con nome simplemente establecemos o nome:

    ```css
    h1 {
        color: rebeccapurple;
    }
    ```

  - Formato hexadecimal: é unha notación de cor que permite establecer o valor das 3 canles como 6 números hexadecimais (valores entre 0 e f: 0123456789abcdef) agrupados en pares. É unha notación bastante común e todos os programas de edición de gráficos permiten ver o valor hexadecimal de calquera cor:

    ```css
    h1 {
        color: #663399;
    }
    ```

  - Formato RGB: é un xeito máis moderno de establecer a cor no que simplemente indicamos os valores de cada canle en formato decimal (entre 0 e 255), úsase así:

    ```css
    h1 {
        color: rgb(102, 51, 153);
    }
    ```

  - O formato RGB permite establecer un cuarto valor que especifica a opacidade ou transparencia da cor, o valor vai entre 0 onde a cor sería completamente transparente e 1 onde sería unha cor sólida (igual que se non se establecera). Os valores intermedios establecerían diferentes grados de transparencia, p.e. 0.5 sería un 50% de transparencia. Úsase rgba en lugar de rgb:

    ```css
    h1 {
        color: rgba(102, 51, 153, 0.5);
    }
    ```

- Usando esta utilidade online pódese cambiar entre formatos de cor: https://serennu.com/colour/hsltorgb.php

### Estilos de texto

- Moitos dos elementos HTML que vimos ata agora poden conter texto e podemos darlle estilos visuais a ese texto mediante CSS: cores, tipografías, tamaños, aliñamentos, etc...
- En xeral os estilos agrúpanse en dous tipos: estilos de fonte e estilos de disposición.

#### Estilos de fonte

- Podemos darlle un cor á fonte usando a propiedade `color`:

  ```css
  p {
      color: red;
  }
  ```

- Darlle unha tipografía con `font-family`:

  ```css
  p {
      font-family: Arial; 
  }
  ```

  - As tipografías poden establecerse usando valores xenéricos: sans-serif, monospace e serif serían os valores xenéricos máis habituais para fontes sen serifa, monoespaciadas e con serifa. Especificando estes valores deixamos ao navegador que use a tipografía que considere máis apropiada para ese valor.

  - Tamén podemos establecer valores específicos usando o nome de fonte, por exemplo: Arial. Se o nome da tipografía ten varias palabras debemos poñelo entre aspas (""):

    ```css
    p {
        font-family: "Comic Sans";
    }
    ```

  - O normal é especificar varias tipografías separadas por comas e o navegador vai coller a primeira que teña dispoñible:

    ```css
    p {
        font-family: "Trebuchet MS", Arial, sans-serif;
    }
    ```

  - O normal neste último caso é establecer como última opción un nome xenérico para que no caso de que non teña dispoñible algun dos tipos anteriores sempre colla algunha similar.

- Para darlle tamaño ao texto usamos a propiedade `font-size` especificada en calquera das unidades que vimos anteriormente:

  ```css
  p {
      font-size: 200%;
  }
  
  p {
      font-size: 2rem;
  }
  
  p {
      font-size: 20px;
  }
  ```

- Hai outras propiedades como:

  - [font-style](https://developer.mozilla.org/en-US/docs/Web/CSS/font-style): permite establecer texto en cursiva.
  - [font-weight](https://developer.mozilla.org/en-US/docs/Web/CSS/font-weight): permite establecer o grado de grosor do texto.
  - [text-transform](https://developer.mozilla.org/en-US/docs/Web/CSS/text-transform): permite modificar as maiúsculas e minúsculas do texto.
  - [text-decoration](https://developer.mozilla.org/en-US/docs/Web/CSS/text-decoration): permite establecer diferentes tipos de subraiados.

- Se queremos darlle unha sombra ao texto usamos a propiedade `text-shadow` que define unha sombra establecendo o desplazamento horizontal, desplazamento vertical, grado de "difumine" e cor da sombra:

  ```css
  h1 {
      text-shadow: 2px 2px 5px black;
  }
  ```

- O exemplo anterior crearía unha sombra desplazada 2 pixeles horizontal e verticalmente con respecto ao texto e cun radio de difusión de 5px. A cor da sombra sería negro. 

#### Estilos de disposición

- A disposición do texto afecta ao aliñado, interliñado e separación de letras e palabras.

- Para cambiar o aliñamento do texto usamos a propiedade `text-align` que admite os valores tradicionais `left, center e right`. Tamén permite o valor justify para xustificar o texto aos bordes pero non é recomendado polas limitacións dos navegagores á hora de dividir palabras.

  ```css
  h1 {
      text-align: center;
  }
  ```

  

- Para cambiar o alto de liña usamos *line-height* que admite valores **sen** unidade. O valor por defecto é 1.2 e podemos. Por exemplo para poñer interliñado a doble espazo:

  ```css
  p {
      line-height: 2;
  }
  ```

- A separación entre letras e palabras pode controlarse coas propiedades letter-spacing e word-spacing que permiten valores nas unidades coñecidas e funcionan igual:

  ```css
  h1 {
      letter-spacing: -2px;
      word-spacing: 0.3rem;
  }
  ```

### Tipografías

- Ata agora aprendimos a asignar tipografías ao texto usando `font-family`, pero sempre dependíamos das tipografías que tivera dispoñibles o sistema operativo.

- Os navegadores modernos permiten usar tipografías aínda que non estén dispoñibles no sistema operativo cargando o propio arquivo da fonte.

- O método máis habitual é usar Google Fonts, só temos que escoller a fonte e teremos dispoñible o código CSS necesario para usar esa fonte, para a tipografía [Open Sans](https://fonts.google.com/specimen/Open+Sans?selection.family=Open+Sans) isto sería:

  ```css
  @import url('https://fonts.googleapis.com/css?family=Open+Sans');
  ```

  Este código teríamos que colocalo ao principio de todo do CSS xa que é un `@import`, despois diso poderíamos usar esta tipografía como se fose calquera outra instalada:

  ```css
  p {
      font-family: 'Open Sans', sans-serif;
  }
  ```

  sempre especificando un nome de tipografía xenérico ao final por se houbera algún problema cargando a tipografía de Google.

- No caso de que Google Fonts non teña a tipografía que queremos temos que conseguir o arquivo da tipografía orixinal.

- Despois teríamos que convertir esa tipografía a varios formatos, xa que non todos os navegadores soportan os mesmos formatos de fonte. Os navegadores modernos soportan os formatos *woff* e *woff2* polo que usando eses chegaría se non temos necesidades especiais.

- Para facer a conversión podemos usar un servizo web como este: https://www.fontsquirrel.com/tools/webfont-generator

- Estes servizos aparte de convertir a fonte aos formatos máis habituais tamén nos dan o código CSS a insertar ou importar no noso sitio web.

- Despois de facer a conversión temos que colocar os arquivos resultantes nunha carpeta no noso sitio web e temos que definir a fonte a usar mediante o statement `@font-face`:

  ```css
  @font-face {
      font-family: 'cantarellregular';
      src: url('cantarell-regular-webfont.woff2') format('woff2'),
           url('cantarell-regular-webfont.woff') format('woff');
      font-weight: normal;
      font-style: normal;
  
  }
  ```

- É importante fixarnos que as referencias a `url(...)` realmente apunten aos ficheiros no noso servidor.

- Ver a demo no día respectivo do curso.