# Curso de HTML e CSS

## Día 2

- Creación de entornos de desenvolvemento
- Modelos de contido en HTML
- Revisitando a estructura básica dun documento HTML
  - O head
- O body e os elementos estructurais máis importantes
- Estructura dun sitio web e relación entre documentos HTML



### Creación de entornos de desenvolvemento

- Aínda que é viable escribir HTML directamente nos arquivos correspondentes, gardar e recargar o navegador para ver os cambios imos usar un módulo de Nodejs que nos axudará a dúas cousas:
  - Crear un servidor web local de probas
  - Auto actualizar o navegador cando cambiemos os arquivos
- O módulo que imos usar chámase [BrowserSync](https://www.browsersync.io/)
- Para configuralo seguimos estes pasos
  - Combrobamos que temos instalado Nodejs no noso equipo
  - Abrimos un terminal e imos ao directorio onde imos traballar, creamos o subdirectorio *www* e executamos:
    - `npm init -y`
    - `npm install browser-sync --save-dev`
  - Editamos o package.json e engadimos á sección de scripts esta liña:
    - `"start": "browser-sync start --server 'www' --files 'www'"`
  - Gardamos e executamos `npm start`
- Dende ese momento o navegador vai servir na url http://localhost:3000/ o contido que creemos dentro do subdirectorio *www* creado anteriormente e actualizarase cos cambios que fagamos automáticamente.

### Modelos de contido en HTML

Validador da W3C: https://validator.w3.org/#validate_by_input

- O modelo de contido de HTML define como se poden aniñar os tags.
- Os tags aparte de ter que estar ben formados só poden ter determinados fillos.
- Tradicionalmente só había dous tipos de tags: os tags de bloque (block) e os tags en liña (inline).
- HTML5 presenta un modelo máis complexo con [7 tipos de tags](https://www.w3.org/TR/2011/WD-html5-20110525/content-models.html#kinds-of-content). A razón disto é o soporte de tags máis semánticos, veremos isto máis adiante.
- Pero podemos seguir agrupándoos en gous meta-tipos:
  - Flow: que serían os anteriores tags de tipo block.
  - Phrasing: os tags de tipo inline.
- Podemos mudar como se renderizan con CSS pero aínda non chegamos aí.
- Cando o navegador renderiza o HTML non ten en conta o espazo que deixamos entre os tags.

#### Block tags

- O tag máis xenérico é o <div>
- Sempre se renderizan nunha liña nova.
- Poden conter outros block tags ou inline tags.
- Lista de tags de bloque: https://developer.mozilla.org/en-US/docs/Web/HTML/Block-level_elements#Elements

#### Inline tags

- O tag máis xenérico é o <span>
- Por defecto renderízanse na mesma liña.
- Só poden conter outros tags inline.
- Lista de tags inline: https://developer.mozilla.org/en-US/docs/Web/HTML/Inline_elements#Elements

### Práctica

- Crear un documento que teña block tags e inline tags ben aniñados.
- Validar o documento e ver que está correcto
- Modificar o documento para que non valide correctamente.

### Revisitando a estructura básica dun documento HTML

- Comezamos polo doctype, todos os documentos HTML deben comezar por tag especial fora do tag <html> que determina o tipo de documento: <!doctype html>

- Nas versións de HTML anteriores o doctype era moito máis complexo:

  ```html
  <!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
  ```

- Despois do doctype abrimos o <html>

- Dentro do tag <html> só son soportados dous tags principais o tag *head* e o tag *body*. O atributo principal dese tag é o *lang* que define o idioma do documento, p.ex. <html lang="gl">.

  - O head inclúe metainformación do documento: titulo, descrición, carga de código externo como CSS ou JavaScript, información sobre a codificación de caracteres do documento ou un variado número de tags *meta* que definen diferentes valores de metainformación. 
    Exemplo:

    ```html
    <!doctype html>
    <html lang="gl">
      <head>
        <meta charset="utf-8">
        <title>A mellor páxina do mundo</title>
        <meta name="description" content="Nesta páxina podes ver contido flipante">
      </head>
      <body>      
      </body>
    </html>
    ```

  - O body é a raíz de todo o contido que aparece na ventana (viewport) do navegador. Vamos a por iso.

### O body e os elementos estructurais máis importantes

Os exemplos de toda esta sección poden verse directamente nos ficheiros html do directorio *www* do día correspondente.

- O HTML moderno (HTML5) é semántico.
- Aínda que o *div* e o *span* vimos que son os tags xenéricos que definen os tipos de contido de bloque e na mesma liña estes non aporta información sobre o seu contido.
- Un tag *div* pode ter calquera contido pero se vemos un tag *footer* xa sabemos que o contido vai ser probablemente un pé de páxina.
- É moito máis sinxelo tanto para as persoas como para as máquinas leer HTML semántico.
- Isto é importante porque cando o buscador de Google indexe a nosa páxina vaille ser máis sinxelo procesala se os tags son semánticos e polo tanto aparecerá mellor posicionada nos resultados.
- En calquera caso debemos construír a nosa páxina pensando nas persoas e non nos buscadores.
- Cando falamos de HTML semántico referímonos ao uso de tags que den un significado estructural aos elementos da páxina. Por exemplo, o tag *footer* indica que o contido é un pé de páxina pero iso non implica que vaia aparecer abaixo da páxina, diso encárgase o CSS e axiña chegaremos aí.

#### Encabezados

- Os tags *h1, h2, h3, h4, h5 e h6* definen os 6 niveis de encabezados que pode ter unha páxina, se precisas un h7 é que algo estás facendo mal e deberías replantexar a estrutura.
- O h1 é o encabezado principal e o resto sub-encabezados.
- Non ten porque haber un só encabezado principal nunha páxina, antes si, agora xa non.
- Os encabezados mostránse con diferentes tipos de letra e tamaños, a razón disto é que antes de que escribamos CSS o navegador aplica un CSS moi básico a algúns tags. Volveremos sobre isto no futuro.
- É importantisimo que os encabezados nunha páxina sigan unha estructura lóxica e non falten nen sobren.
- Práctica: Exemplo do uso de h1, o encabezado máis importante. Buscamos ese h1 coas Developer Tools.

#### O header e a navegación

- O tag *header* define unha sección da páxina que conten o encabezado e navegación principal, como a cabeceira dunha carta.
- Dentro do *header* é recomendable que exista un tag *nav* que conten información sobre a navegación pola páxina.
- Pode haber varios headers nunha páxina aínda que é importante que exista un principal, dentro de cada *article* pode haber outros.

#### Os section, article, aside e footer

- O tag section define unha sección xenérica de contido nunha páxina, normalmente debe iniciarse cun tag h1 que siga a lóxica dos previos.
- O tag article representa unha parte de contido da páxina que tamén teña sentido se o extraemos da páxina.
- O article pode conter un *header* similar ao que falamos antes e tanto pode seguir a lóxica de encabezados da páxina como conter unha nova, ou sexa, volver a comezar por un h1.
- O tag *aside* define unha parte do contido da páxina que está algo relacionado co resto pero non moito, por exemplo, unha frase destacada, unha imaxe relacionada, etc...
- O footer define un pe de páxina, tanto do documento principal como dun *article*

#### Outros elementos

- O tag *p* define un parágrafo.
- O tag *main* define o contido principal do documento.

### Práctica

- Crear un documento que conteña todos os tags semánticos da sección anterior.
- Validar o documento e ver que está correcto
- Modificar o documento para que non valide correctamente.

### Estructura dun sitio web e relación entre documentos HTML

- Un sitio web é un conxunto de documentos HTML tanto estáticos (existen fisicamente en disco) coma dinámicos (créaos un programa con contido dunha base de datos, p.ex.)
- Os documentos HTML relaciónanse entre si mediante links.
- O tag *a* define un link.
- O atributo máis importante é o href que determina que páxina ten que mostrar o navegador ao facer click nel.
  - Os links poden ser internos, e enlazar a outras partes do documento actual mediante o atributo *id*.
  - Os links externos cargan outro documento novo.
- No href determinase a ruta que ten que cargar:
  - Se a ruta comeza por / é unha ruta absoluta e polo tanto empeza na raíz do sitio web.
  - Se non é así é unha ruta relativa á ruta actual.
  - (ver exemplos nos html do directorio www)
- Outro atributo importante é o title que describe a onde vai ir ese link.

### 