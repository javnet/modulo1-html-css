# Curso de HTML e CSS

## Día 5

- Breve historia do CSS
- Relación de HTML e CSS
- Anatomía do CSS
- Selectores simples

### Breve historia do CSS

- O CSS foi proposto no ano 1994 como unha linguaxe para especificar como os documentos HTML son presentados aos usuarios.
- A w3 escolleu entre múltiples propostas de follas de estilo, o CSS foi a escollida.
- No ano 1996 aparece a primeira especificación da w3: CSS1.
- Non é unha idea nova, dende os anos 80 habia diferentes sistemas de especificar a presentación de documentos XML e similares.
- No ano 1997 especificouse o CSS2 e no 1998 o CSS3 que é unha especificación aínda non rematada e é  que usamos agora.
- O soporte nos navegadores nos primeiros anos foi moi limitado e non foi ata metade dos anos 2000 cando comezou o seu uso serio.

### Relación de HTML e CSS

- O CSS aplícase ao HTML mediante unha serie de reglas que definen como determinados tags se mostran.

- Por exemplo: quero que todos os meus encabezados de primeiro nivel teñan o texto amarelo e fondo azul.

- O primeiro que fai o navegador é cargar o HTML

- No HTML hai referencias a reglas CSS, veremos que estas referencias poden ser de diferentes tipos.

- Cando todo está cargado o navegador convirte o HTML ao que se chama DOM que é unha representación en memoria da estructura do HTML.

- O navegador procesa o CSS e comproba se hai algunha regla aplicable ao DOM e aplícaa.

- Finalmente o navegador renderiza o DOM no viewport (parte do navegador onde se ve o contido do body)

- Exemplo:

  ```html
  <!DOCTYPE html>
  <html lang="gl">
    <head>
      <meta charset="utf-8">
      <title>CSS!</title>
        
      <style type="text/css">
  		h1 {
              color: yellow;
              background: blue;
  		}    
      </style>
        
    </head>
    <body>
      <h1>Ola amigas!</h1>
    </body>
  </html>
  ```

#### Xeitos de aplicar o CSS

- Hai tres xeitos de cargar CSS no noso HTML:

  - aplicar directamente as propiedades ás etiquetas (non recomendado):

    ```html
    <h1 style="color:yellow;background:blue">Isto non mola!</h1>
    ```

  - usando a etiqueta style no *head* (ver exemplo anterior). Tampouco é recomendado.

  - O xeito recomendado é usar un arquivo CSS externo, para iso temos que indicar no head a referencia a ese arquivo, este sería o HTML:

    ```html
    <!DOCTYPE html>
    <html lang="gl">
      <head>
        <meta charset="utf-8">
        <title>CSS!</title>
        
    	<link rel="stylesheet" href="style.css">
    
    </head>
      <body>
        <h1>Ola amigas!</h1>
      </body>
    </html>
    ```

    e este o arquivo CSS referenciado no *head*:

    ```
    h1 {
        color: yellow;
        background: pink;
    }
    ```

### Anatomía do CSS

- O CSS constrúese mediante declaracións agrupadas en bloques, e eses bloques están asociados a reglas que definen a que elementos HTML se aplican.

- As declaracións de CSS están compostos por propiedades e valores separadas internamente por dous puntos (:) e coa seguinte declaración con ";":

  ```css
  background: blue;
  ```

  - As propiedades indican o aspecto estilístico que queremos modificar: fonte, cor, fondo, posición...
  - Os valores indican como queremos mudar o aspecto estilístico anterior.

- Os bloques son grupos de declaracións agrupados entre chaves ({}):

  ```css
  {
      background: blue;
      color: yellow;
  }
  ```

- É obrigatorio que todas as declaracións estén agrupadas en bloques, fora dos bloques non deben aparecer.

- Os bloques teñen que estar precedidos por selectores, os selectores definen a que elementos se aplican as declaracións agrupadas no bloque. Estas declaracións poden facer referencia directa a tags, clases, ids:

  ```css
  h1 {
      background: blue;
      color: yellow;
  }
  ```

- Fora dos bloques poden aparecer os chamados CSS Statements, que son reglas especiais de CSS que definen tipos de letra, codificación de caracteres, media queries ou módulos que veremos nas seguintes seccións:

  ```css
  @import "ficheiro.css";
  ```

- Ao igual que no HTML o espazo en blanco nos ficheiros CSS son ignorados.
