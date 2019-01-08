# Curso de HTML e CSS

## Día 1

- Introdución ao HTML
- Fontes de documentación
- Servidor e cliente
- Anatomía dun tag
- Estrutura básica dun documento HTML



### Introdución ao HTML

- O HTML é a linguaxe de etiquetado propia do protocolo HTTP, un sistema cliente servidor proposto a principios dos anos 90 por Tim Berners-Lee no CERN como un sistema de intercambio de información para investigadores.
- O éxito do HTML foi a simplicidade detrás da idea. Un sistema para enlazar documentación. Baseado en arquivos de texto editables facilmente. Unha linguaxe moi simple e sinxela de aprender. 
- Por outra banda tamén afectou o feito de que fose pensado como unha linguaxe aberta. Cun sistema de cliente servidor de código aberto que todo o mundo podía modificar segundo as súas necesidades.
- A xente empezou a usala para publicar contido. Modificaron os servidores. Os clientes (que logo se chamarían navegadores). 
- Apareceron os primeiros grandes navegadores como Mosaic que despois se convertiu en Netscape e logo derivou na fundación Mozilla e seu navegador Firefox.
- Cos cambios no HTML apareceron novos elementos e tags, o máis importante daquela foi o tag <img> que implementou Mosaic e permitía mostrar imaxes nos documentos HTML. Pero non había moito control e foi necesaria a creación dun organismo regulador: a **w3c**.
- Empezaron a aparecer versións de HTML (a primeira no 1995, versión 2.0) que implementaban ordenadamente novas características: formularios, tablas, ... No 1997 saiu a versión 3.2.
- No ano 1998 sae a primeira gran versión de HTML, a 4. Con ela sae a primeira versión de CSS que introduce un concepto importante: separación de contido e presentación. A pesar da importancia do CSS non vai ser ata mediados dos 2000 cando se empece a usar no seu potencial completo.
- A principios dos 2000 a w3c nun intento de facer o HTML máis estricto propuxo facelo máis cercano ao XML (unha linguaxe da mesma familia máis estricta) e naceu ou XHTML.
- Os navegadores ainda que xa soportaban video usando incrustacións de programas externos como applets de Java ou RealPlayer dende mediados dos 90 pero non foron realmente viables para o consumo de multimedia ata que se popularizou o flash.
- A finais da decada dos 2000 a web cada vez se usaba para máis cousas, convertiuse nunha plataforma de contido, aplicacións, software, multimedia. O XHTML estaba a quedar limiado e o Flash e outras tecnoloxías pechadas estaban cubrindo os ocos.
- A mediados dos 2000 empeza a usarse masivamente unha tecnoloxía que levaba anos soportada nos navegadores: AJAX, o cal permitiu crear unha web máis dinámica e comezouse a ver a web como unha plataforma capaz de articularse para moitas máis cousas que para presentar contido estático.
- Daquela unha parte da w3c descontenta co estado actual do HTML creou un grupo de traballo para desenvolver unha nova especificación do HTML para axudar a establecer a web como unha plataforma autosuficiente e aberta. Naceu o HTML5.
- O HTML5 soportaba audio e video, mellor acceso ao hardware (xeolocalización, 3d), etiquetas semánticas, Canvas e moitas novas funcionalidades adaptadas para a web moderna.
- Apple matou ao Flash ao non soportalo no seu iphone. O resto de compañías de mobiles seguiron esa tendencia. O HTML5 volveu a gañar a web.
- Agora a web usase con multiples dispositivos, está en moitos  máis gracias á internet das cousas, é máis multimedia, e por suposto plataforma de traballo e comunicación. Este avance tecnolóxico moldea o futuro do HTML e á inversa. Comezamos.

### Fontes de documentación

- Principal fonte de documentación: [MDN](https://developer.mozilla.org/)
  - É a máis completa, actualizada e fiable.
  - Google, Microsoft, Apple contribúen.
  - Hai contido en varios idiomas pero a referencia é o ingles.

### Servidor e cliente

- Un servidor web pode ser:
  - unha máquina física permanentemente contectada a internet cun software específico correndo que lle permite servir páxinas web
  - o software que se executa nesa máquina
- Un servidor web escoita peticións e da respostas, esas peticións e respostas poden ser de moitos xeitos diferentes.
- A tecnoloxía que usa para facer este intercambio de petición/resposta é HTTP. E a parte máis importante das peticións son as URLs.
- Unha URL é un identificador de recurso único, non hai dúas iguais e ten dúas partes principais: o **host** e o **path**. Hai máis partes que veremos máis adiante como o querystring.
-  Que pasa cando "cargamos" unha web no navegador:
  - O navegador é o cliente.
  - Aparte da información que contén a URL o navegador engádelle o **método**. Hai varios métodos pero imos centrarnos no GET. Que basicamente dille ao server que devolva o que hai nesa URL.
  - O navegador crea unha petición coa URL e o método. Establece unha conexión TCP á IP do servidor e manda a petición.
  - O servidor responde a esa petición, a resposta pode crearse de moitos xeitos: ficheiro en disco ou resposta dinámica (por exemplo, con contido dunha base de datos). A resposta chega ao cliente e péchase a conexión TCP.
  - O proceso repítese para cada petición. O protocolo HTTP non ten estado, polo tanto cada petición para o servidor é nova e non sabe das anteriores.
- (DEMO: dia-1/server.js)

### Anatomía dun tag

- O HTML é un lenguaxe de etiquetado. 
- O HTML define unha serie de elementos co que se construen páxinas web.
- Os elementos están representados por tags.
- Os tags normalmente están compostos por un tag de inicio e un tag de peche. O contido que hai no medio pode ser texto ou outros tags.
- Hai tags que non precisan pecharse, chega con abrilos. Por exemplo as imaxes.
- Os tags poden ter atributos os atributos modifican determinados aspectos dos tags.
- Os tags aníñanse entre si ata formar documentos HTML.

### Estrutura básica dun documento HTML

- O tag que define un documento html e que o engloba completamente é o tag <html>
- Os documentos HTML están formados por dúas partes principais: <head> e <body>
- O head conten metainformación do documento.
- O body é o que vemos na pantalla do navegador.
- Os documentos HTML están compostos por elementos HTML aniñados. A complexidade pode ser moi grande.
- O documento HTML só representa o contido, nunca a presentación.

