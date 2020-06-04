---
title: 'Introdução à Web, ao HTML e ao CSS'
date: 2020-06-02T18:00:08+01:00
tags: ['html', 'css', 'programação web']
---

Nesta lição do percurso de aprendizagem [Programação web com HTML/CSS](/html-css) vamos ver o que é a web, o que são sítios e páginas web, e como podemos programar para a web usando o HTML e o CSS.

## Recursos

- **[Sessão #259 (HTML/CSS #1)]({{<ref "/post/sessions/session-259">}})** – Sessão do CoderDojo LX correspondente a esta secção.
- **[Apresentação da sessão #259 (HTML/CSS #1)](https://bit.ly/cdlx-html1)** – A apresentação usada nessa sessão.
- **[nanonautas-começa-aqui](https://glitch.com/~nanonautas-comeca-aqui)** – Projecto com que deves começar esta lição.
– Os exemplos do livro correspondentes a esta sessão:
- **[nanonautas-p8](https://glitch.com/~nanonautas-p8)** – Projecto até à página 8 do livro.
- **[nanonautas-p10](https://glitch.com/~nanonautas-p10)** – Projecto até à página 10 do livro.
- **[nanonautas-p13](https://glitch.com/~nanonautas-p13)** – Projecto até à página 13 do livro.
- **[nanonautas-p16](https://glitch.com/~nanonautas-p16)** – Projecto até à página 16 do livro.

## A Internet, a Web, páginas, sítios e endereços

Vamos começar por definir alguns conceitos, com ajuda da nossa amiga [Wikipédia](https://pt.wikipedia.org/):

- **[Internet](https://www.wikiwand.com/pt/Internet)** – Sistema global de redes de computadores interligadas que usam um conjunto próprio de *protocolos* chamado Internet Protocol Suite ou TCP/IP e tem como objectivo servir cada vez mais utilizadores no mundo inteiro.
- **[Web ou World Wide Web](https://www.wikiwand.com/pt/World_Wide_Web)** – Sistema de documentos de vários tipos (texto, imagens, vídeos, sons, etc.), muitos deles **hipetexto**, interligados e acessíveis na Internet.
- **[Sítio web](https://www.wikiwand.com/pt/S%C3%ADtio_eletr%C3%B3nico)** – Conjunto de **páginas web** relacionadas disponíveis num mesmo *nome de domínio*, por exemplo o [sítio web dos Nanonautas](https://nanonautas-final.glitch.me/) (que é onde chegaremos no final deste percurso de aprendizagem).
- **[Página web](https://www.wikiwand.com/pt/P%C3%A1gina_web)** – Um documento ou recurso em **hipertexto** disponível na Web a que se pode aceder usando um navegador e que tem um dado endereço, ou melhor, um dado **URL**.
- **[Hipertexto](https://www.wikiwand.com/pt/Hipertexto)** – Documento com ligações (mais precisamente, hiperligações) a outros documentos ou recursos.
- **[URL](https://www.wikiwand.com/pt/URL)** ou **endereço** – Localizador de um recurso na web, usualmente uma página web. Aos URL também se chama muitas vezes endereços web ou simplesmente endereços. Por exemplo, o endereço do sítio web dos Nanonautas é dado por este URL: `https://nanonautas-final.glitch.me/`.
- **[Navegador](https://www.wikiwand.com/pt/Navegador_web)** – Uma aplicação para aceder à informação que está na Web. Quando o utilizador pede ao navegador para mostrar uma dada página de um sítio web, indicando o seu endereço, o navegador vai buscar essa página web ao *servidor* web apropriado e mostra essa página numa janela do computador.

Há nestas definições três palavras ou expressões meio esquisitas: «protocolo» e «nome de domínio». Vamos ver o que significam:

- **[Protocolo](https://www.wikiwand.com/pt/Protocolo_(ci%C3%AAncia_da_computa%C3%A7%C3%A3o))** – Simplificando muito, um protocolo é um conjunto de regras ou convenções que permite que tudo corra bem, isto é que a comunicação entre dois computadores aconteça. Os protocolos são importantes não apenas na diplomacia, mas também na comunicação entre computadores! Já reparaste que os endereços web começam todos com `http` ou `https`? Isso indica ao navegador que o protocolo a usar para comunicar com o computador (a que se chama *servidor*) onde se encontra o recurso (por exemplo, uma página web) é o [HTTP](https://www.wikiwand.com/pt/Hypertext_Transfer_Protocol) (*hypertext transfer protocol* ou protoloco de transferência de hipertexto). A versão com um «s» no fim significa que se usa uma combinação do HTTP com outro protolo (chamado TLS) que garante que a comunicação é segura, ou seja, que ninguém que intercepte a comunicação conseguirá fazer cabo-e-rabo do que está a ser comunicado.
- **[Servidor](https://www.wikiwand.com/pt/Servidor_(computa%C3%A7%C3%A3o))** – Um programa ou dispositivo (por exemplo, um computador) que fornece *serviços* (daí o nome «servidor») a outros programas ou dispositivos, a que se chama clientes. No caso de um servidor web, os clientes são normalmente os nossos navegadores web, que comunicam com os servidores web usando o protocolo HTTP, pedindo-lhes páginas web e recebendo essas páginas como resposta.
- **[Nome de domínio](https://www.wikiwand.com/pt/Nome_de_dom%C3%ADnio)** – Os nomes de domínio são usados para dar nomes a conjuntos relacionados de computadores. Por exemplo, `coderdojo-lx.pt` é o nome de domínio do CoderDojo LX. Um outro nome de domínio do CoderDojo LX é `www.coderdojo-lx.pt`, que é onde se encontra o [sítio web do CoderDojo LX](https://www.coderdojo-lx.pt/).


Reparaste no exemplo que demos mais acima, do [sítio web dos Nanonautas](https://nanonautas-final.glitch.me/)? Explora-o bem. Vê se consegues:

- Identificar todas as páginas web do sítio.
- Perceber qual o endereço de cada uma dessas páginas.

Quantas páginas são? Cada uma tem o seu próprio endereço (URL), não é? Ou quase… Deste conta que há dois endereços que resultam na mesma página? Pois é, veremos isso mais tarde, mas a verdade é que os dois endereços `https://nanonautas-final.glitch.me/` e `https://nanonautas-final.glitch.me/index.html` correspondem à mesma página, que é a página inicial do sítio web dos Nanonautas.

Reparaste também que os endereços terminam todos em `.html`? Vamos ver isso a seguir.

Antes, porém, vamos apresentar Os Nanonautas!

## Os Nanonautas

![Os Nanonautas](http://nanonautas.pt/wp-content/uploads/exemplos/p84melhorada/imagens/nanonautas.jpg)

Os Nanonautas são uma banda! Os seus membros são:

### Daniel – Vocalista extraordinário

![Retrato do Daniel](http://nanonautas.pt/wp-content/uploads/exemplos/p84melhorada/imagens/daniel.png)

O Daniel é o vocalista dos Nanonautas. Ele gosta de estar sempre a cantar – e não apenas quando actua com os Nanonautas! Os seus pais dizem que ele aprendeu a cantar antes de aprender a falar!.

O Daniel também toca clarinete e anda a aprender saxofone alto.

### Sam – Homem da secção rítmica


![Retrato do Sam](http://nanonautas.pt/wp-content/uploads/exemplos/p84melhorada/imagens/sam.png)

O Sam traz a música no sangue desde o dia em que nasceu. Os seus pais tocam instrumentos e deram-lhe a primeira bateria quando ele tinha apenas cinco anos, o que causou problemas com os vizinhos. Em algumas canções toca guitarra baixo e noutras toca bateria. O Sam adora tocar nos Nanonautas, mas detesta ter que carregar a bateria de um lado para outro.

### Holly – Se tem cordas, ela toca

![Retrato da Holly](http://nanonautas.pt/wp-content/uploads/exemplos/p84melhorada/imagens/holly.png)

Guitarra acústica? Guitarra eléctrica como solista? Cavaquinho? Harpa? A Holly sabe tocar tudo isso. Começou por fazer guitarras em casa com caixotes de cartão e elásticos até que o seu tio teve pena dela e lhe ofereceu uma guitarra espanhola no Natal. Após algumas aulas na escola, levantou voo!

### Dervla – Maestrina dos teclados

![Retrato da Dervla](http://nanonautas.pt/wp-content/uploads/exemplos/p84melhorada/imagens/dervla.png)

A Dervla tem o 4.º ano de piano, mas em segredo prefere tocar teclados electrónicos. Ela gosta de sons de sintetizador e de discutir com a Holly quem deverá tocar as partes de baixo.


## Objectivo

Agora que os Nanonautas estão apresentados, é hora de saber o que eles precisam: um novo sítio web! Puseram-se a pensar sobre o que o novo sítio web deveria ser e chegaram às seguintes ideias:

- Dizer onde será o próximo concerto
- Anunciar CD e t-shirt
- Ligações para vídeos deles no YouTube
- Conselhos sobre compra e manutenção de instrumentos
- Conselhos sobre ensaiar sem irritar vizinhos

Tentaram organizar as ideias e chegaram à seguinte estrutura com cinco páginas web:

- **Início** – Página com ligações para as seguintes páginas:
  - **Sobre nós** – Página com o seguinte conteúdo:
    - Informação sobre a nossa banda
    - O nosso novo CD
    - Comprem a nossa t-shirt
  - **As nossas canções** – Página com o seguinte conteúdo:
    - Informação sobre as nossas canções
    - Vídeos
  - **Vejam-nos tocar** – Página com o seguinte conteúdo:
    - Onde nos podem ver tocar
	- Próximos concertos
  - **Dar um concerto** – Página com o seguinte conteúdo:
    - Como dar um concerto
    - Dicas top

Para ter uma ideia mais precisa do que eles pensaram, dá de novo uma olhada no [sítio web final dos Nanonautas](https://nanonautas-final.glitch.me/). A ideia é ires desenvolvendo aos poucos o sítio web dos nanonautas até ele ter exactamente o aspecto e conteúdos que viste!

## Vamos começar!

### O que precisas

- Descarrega o [ZIP de imagens](https://bit.ly/cdlx-nanonautas-imagens). Nota bem que há um botão para descarregar a imagem no canto superior direito.
- Descomprime o arquivo `imagens.zip` que descarregaste. Não te limites a abri-lo: tenta descomprimi-lo mesmo.
- Se ainda não tens conta no [Glitch](https://glitch.com/), então:
  - Se tens pelo menos 13 anos, podes criar tu mesmo uma conta.
  - Se tiveres menos de 13 anos, pede ajuda a um encarregado de educação.
- Vai para a [página da equipa CoderDojo LX](https://glitch.com/@cdlx) no Glitch.
- Abre o projecto `nanonautas-comeca-aqui`. Se não encontrares o projecto, [clica aqui](https://glitch.com/~nanonautas-comeca-aqui).
- Remistura o projecto, carregando no botão «Remix This», que encontras no canto inferior direito. Remisturar é fazer uma cópia tua do projecto, para o poderes alterar à vontade.

### O teu novo projecto

Tens à tua frente o teu novo projecto! Neste momento só tem uma página web, que podes ver do lado esquerdo. Essa página está guardada num arquivo (ou ficheiro) chamado `sobre-nos.html`. Clica sobre ele, para veres o seu conteúdo à direita, no editor. Verás que o conteúdo é simplesmente
```
Isto não é HTML!
```
Procura o menu «Show▼» e escolhe «Next to The Code». Abrir-se-á uma janela que mostra o conteúdo do teu sítio web. Como ainda só tens uma página, verás lá listado o arquivo `sobre-nos.html`. Clica sobre ele para o veres na web.

Que achas? Pouco entusiasmente, não é? Espera, as coisas vão melhorar, não tarda.

## Páginas HTML

Reparaste no nome do ficheiro? Ele termina na extensão `.html`. Embora o teu navegador não ligue muito a essa extensão, ela ajuda-nos a perceber que se trata de uma página web no formato [HTML](https://www.wikiwand.com/pt/HTML) (*hypertext markup language* ou linguagem de marcação para hipertexto). O HTML é uma linguagem que permite representar e compor o conteúdo das páginas web, e é um dos principais temas em aprendizagem aqui. O HTML forma um trio maravilha com o [CSS](https://www.wikiwand.com/pt/Cascading_Style_Sheets) (*cascading style sheets* ou folhas de estilo em cascata), usadas para controlar o estilo ou aspecto das páginas web, e com o [JavaScript](https://www.wikiwand.com/pt/JavaScript), uma linguagem de programação que permite criar páginas web dinâmicas. Em conjunto, o HTML, o CSS e o JavaScript permitem criar páginas web fantásticas!

{{< note >}}
O trio maravilha da web, pelo menos do lado do cliente, i.e., do lado do navegador, é constituído pelo <strong>HTML</strong>, para representares o conteúdo estruturado das tuas páginas, pelo <strong>CSS</strong>, para controlares num só local o aspecto de <em>todas</em> as tuas páginas, e pelo <strong>JavaScript</strong>, para tornares as tuas páginas <em>dinâmicas</em> e <em>interactivas</em>.
{{< /note >}}

Voltando ao Glitch, já viste que o conteúdo do arquivo `sobre-nos.html` é simplesmente uma linha de texto:
```
Isto não é HTML!
```
Tal como essa linha indica, o arquivo ainda não contém verdadeiro HTML. Vamos resolver esse problema. Apaga a linha `Isto não é HTML!` do arquivo `sobre-nos.html` e coloca no lugar dela o seguinte o código HTML:
```HTML
<!DOCTYPE html>

<html>
  <head>
    <meta charset="UTF-8" />
    <title>Sobre Nós</title>
  </head>
  <body>
    <h1>Sobre Nós</h1>
    <p>Somos os Nanonautas.</p>
    <p>Chamamo-nos Holly, Dervla, Daniel e Sam.</p>
  </body>
</html>
```

Se tudo correr bem, se clicares sobre o arquivo `sobre-nos.html` na janela do lado direito, verás a tua primeira página Web! Nada mau, certo? OK, OK, ainda não é grande coisa… Melhor virá, mais à frente. :-)

Reparaste certamente que o HTML tem montes de `<` e `>`. A ideia é que estes caracteres funcionam como *parênteses agudos* que envolvem aquilo a que se chama **etiquetas**.

A primeira etiqueta é especial: `<!DOCTYPE html>`. Ela deve ser colocada na linha inicial de todas as páginas web e indica claramente ao navegador (que as vai mostrar) que o seu conteúdo… é HTML! Isso mesmo, a etiqueta especial indica que se trata de HTML. Só depois dessa primeira linha com a etiqueta especial que vimos é que começa o HTML propriamente dito.

### Principais elementos de uma página web

A primeira etiqueta HTML que encontras é `<html>`. Grande parte das etiquetas HTML tem uma etiqueta de abertura, tal como `<html>`, e uma etiqueta de fecho, que é muito semelhante à etiqueta de abertura, mas tem uma `/` após o parênteses agudo esquerdo, tal como `</html>`. Cada etiqueta tem também um *nome* que identifica o *elemento* HTML que está em causa. Entre as etiquetas de abertura e fecho encontra-se o *conteúdo* do elemento.

Em resumo:

- **`<html>`** – Etiqueta de abertura do elemento `HTML`.
- **`</html>`** – Etiqueta de fecho do elemento `HTML`.
- **Entre `<html>` e `</html>`** – Conteúdo do elemento `HTML`.

Mas afinal, o que é o elemento `HTML`? O elemento `HTML` identifica toda a informação sobre a página web. Por isso é que todo o resto da nossa página web é parte do conteúdo deste elemento. O elemento `HTML` contém dois outros elementos (`HEAD` e `BODY`), cada um identificado pelas respectivas etiquetas:

- **Elemento `HEAD`** – Identificado pelas etiquetas `<head>` e `</head>`, este elemento funciona como um cabeçalho do documento, sendo o seu conteúdo informação que se aplica à página web como um todo.
- **Elemento `BODY`** – Identificado pelas etiquetas `<body>` e `</body>`, este elemento funciona como corpo do documento, ou seja, o seu conteúdo é onde se coloca o conteúdo da página web, que é aquilo que se vê quando navegas para essa página.

### Alguns outros elementos fundamentais

Tanto o cabeçalho como o corpo da nossa página web têm vários outros elementos de que ainda não falámos:

- **Elementos do `HEAD`**:
  - **Elemento `META`** (etiqueta `<meta>`) – Este é um elemento sem conteúdo, ou seja, não tem etiqueta de fecho. Ou melhor, a sua etiqueta é ao mesmo tempo de abertura e fecho. Em bom rigor, a sua etiqueta, como a de todos os elementos sem conteúdo, ou vazios, deveria terminar em `/>`. Ou seja, deveria ser `<meta charset="UTF-8" />`. Bom, e para que é que isto serve? Dentro da etiqueta, além do seu nome, `meta`, encontras um par *`atributo`*=*`valor`*: o atributo é `charset` e o valor é `"UTF-8"`. Isto serve para dizer qual é o tipo de código usado para representar os caracteres, que neste caso é o [UTF-8](https://www.wikiwand.com/pt/UTF-8), e não é muito importante por agora.
  - **Elemento `TITLE`** (etiquetas `<title>` e `</title>`) – Este elemento faz sempre alguma confusão. Ele indica qual é o título da página web. Ele é usualmente igual, ou pelo menos parecido, com o primeiro elemento `H1` da página. Só que enquanto o `H1` se vê na própria página, o `TITLE` só se vê no título da janela ou do tabulador onde a página está a ser mostrada. Para perceberes bem a diferença, faz o seguinte:
    - Altera o conteúdo do elemento `TITLE` para «Sobre Nós – Nanonautas», ou seja, `<title>Sobre Nós – Nanonautas</title>`.
    - Procura o menu «Share▼», clica em «Live App» e clica sobre o botão «copy» logo abaixo.
    - Abre uma nova *janela* (e não separador!), pressionando em `<ctrl-N>`, no Windows, ou em `<cmd-N>`, no Mac.
    - Clica sobre o barra de endereço da nova janela e cola lá o endereço que copiaste. Pressiona `<enter>`.
    - Clica sobre o arquivo `sobre-nos.html`. Verás a tua nova página. Agora olha para o título da tua janela ou separador. Vês que o conteúdo do elemento `TITLE` foi lá parar? Agora já percebes para que serve.
- **Elementos do `BODY`**:
  - **Elemento `H1`** – O «H» em «H1» vem de *header*, ou cabeçalho, e o 1 significa de nível 1. O HTML possui outros elementos deste tipo, mas de níveis superiores: `H2` a `H6`. Pensa num livro escolar. É muito provável que esse livro esteja organizado em secções. As secções mais importantes do livro são usualmente conhecidas por capítulos. Os títulos dos capítulos são representados em HTML através do elemento `H1`. Supõe agora que os capítulos desse livro são divididos em subsecções, todas com a mesma importância e cada uma delas com o seu título. Os títulos dessas subsecções são representados  em HTML através do elemento `H2`. E se essas secções tiverem sub-subsecções? Aí entra em jogo o elemento `H3`. Vê abaixo um exemplo (clica no botão «HTML» para veres o HTML da página). Na nossa página, como vês, só temos um «capítulo», por isso só temos um elemento `H1` para conter o seu título.
  - **Elemento `P`** – O texto de uma secção da tua página web, seja ela de nível 1 (após um elemento `H1`), de nível 2 (após um elemento `H2`) ou de outro nível qualquer (até 6) deve ser organizado em parágrafos. Cada elemento `P` identifica um parágrafo.

{{< codePen GRoRvXm >}}

{{< note >}}
Quando pensares no texto, organiza-o de modo a que cada parágrafo consista numa ideia, pensamento ou ponto principal. Organizar o texto em múltiplos parágrafos ajuda-te a organizar ideias, e ajuda o leitor a perceber melhor essas ideias.
{{< /note >}}

{{< note >}}
Normalmente só há um elemento `H1` por página web. É como se cada página correspondesse a um capítulo.
{{< /note >}}

{{< warning >}}
Não uses os elementos `H1` ou `H2` simplesmente porque queres que o texto dentro desse elemento apareça maior. Usa os elementos do HTML para dar estrutura e lógica às tuas páginas. Deixa as questões relacionadas com o aspecto para o CSS.
{{< /warning >}}

### HTML é para conteúdo *estruturado* da página web

É importante que percebas que o que escreves em HTML corresponde ao *conteúdo estruturado* das tuas páginas web. O HTML não especifica o *aspecto* das tuas páginas. Isso será o papel do CSS, que veremos em breve. Esta divisão é muitíssimo importante:

- Permite-te concentrares-te no conteúdo e estrutura da página enquanto escreves HTML.
- Permite-te usar o CSS para controlares o aspecto das tuas páginas de forma coerente: um só ficheiro CSS permite-te controlar o aspecto de *todas* as páginas do teu sítio web!

## Folhas de estilo

O segundo elemento do nosso trio maravilha é o CSS. Vamos usar o CSS para criar uma folha de estilo. Faz o seguinte:
- No Glitch, no painel à esquerda, clica no menu «New File▼».
- Insere `css/minha-folha-de-estilo.css` no espaço.
- Clica no botão «Add This File»

Verás que foi criado um novo arquivo, chamado `minha-folha-de-estilo.css`, numa pasta chamada `css`.

{{< note >}}
No Glitch as pastas são criadas automaticamente, se ainda não existirem, sempre que o nome dos ficheiros a criar contém o caractere <code>/</code>, que funciona como separador entre os nomes da(s) pasta(s) e o nome do arquivo. 
{{< /note >}}

Neste momento, a estrutura dos teus ficheiros e pastas é a seguinte:
{{< fileTree >}}
<code>/</code> [pasta raiz]
  * css
    * minha-folha-de-estilo.css
  * sobre-nos.html
{{< /fileTree >}}

No painel da direita deverá também ter ficado visível a nova pasta. Confirma-o.

O novo arquivo que criámos termina com a extensão `.css`, para mais facilmente o identificarmos como uma folha de estilo representada em CSS.

{{< note >}}
Uma folha de estilo serve para tu, num único local, indicares quais a regras visuais a aplicar aos elementos das páginas web representadas em HTML que usem essa folha de estilos. Ou seja, uma folha de estilo controla o <strong>aspecto</strong> das páginas do teu sítio web.
{{< /note >}}

Neste momento a folha de estilo `minha-folha-de-estilo.css` está vazia. Coloca nela o seguinte código.

```CSS
body {
  font-family: sans-serif;
}
```

Se fores agora ver, no painel da direita, o aspecto da tua página web `sobre-nos.html`, verás que… nada mudou! Isso acontece porque tens de dizer que ao navegador que folha de estilo queres que seja aplicada à tua página web. Como ainda não o fizeste, nada mudou.

Para resolveres o problema, clica no arquivo `sobre-nos.html` no painel da esquerda e adiciona o elemento `LINK` abaixo, de modo a ficares com o seguinte conteúdo:
```HTML
<!DOCTYPE html>

<html>
  <head>
    <meta charset="UTF-8">
    <title>Sobre Nós</title>
    <link type="text/css" rel="stylesheet" href="css/minha-folha-de-estilo.css"/>
  </head>
  <body>
    <h1>Sobre Nós</h1>
    <p>Somos os Nanonautas.</p>
    <p>Chamamo-nos Holly, Dervla, Daniel e Sam.</p>
  </body>
</html>
```

{{< note >}}
Toma atenção que nestas caixas de código as linhas mais longas não se vêem todas. Tens de deslizar na horizontal o conteúdo da caixa para as veres por completo.
{{< /note >}}

O elemento `LINK` é um elemento vazio. Por isso não tem etiqueta de abertura e fecho. Pelo contrário, tem apenas uma etiqueta que termina em `/>`. Este elemento chama-se `LINK` porque faz uma ligação entre a página web e um recurso usado por essa página. Neste caso faz a ligação entre a tua página web `sobre-nos.html` e a tua folha de estilos `css/minha-folha-de-estilo.css`. O elemento tem três atributos:
- **`type`** – Indica o tipo do recurso. O valor `"text/css"` indica que o recurso é do tipo CSS.
- **`rel`** – Indica a relação (daí `rel`) entre a página web e o recurso. O valor `"stylesheet"` indica que a relação é entre a página web e uma folha de estilo.
- **`href`** – Indica a localização do recurso, na forma de um URL. O nome do attributo vem de *hypertext reference*, ou seja, referência de hipertexto. O valor `"css/minha-folha-de-estilo.css"` indica a localização da nossa folha de estilo de forma abreviada (ou seja, relativa à posição da nossa página web).

Experimenta agora ver a página web `sobre-nos.html` no painel da direita. Notas alguma diferença? Não? Vê com atenção. O tipo de letra (ou fonte) usado não é o mesmo. Agora temos uma fonte sem serifas. «Sem quê?», dizes. [Serifas](https://www.wikiwand.com/pt/Serifa). Clica na ligação para investigares. Vê também a explicação [aqui](https://www.w3schools.com/css/css_font.asp). Basicamente as serifas são os tracinhos que se encontram na extremidade das hastes das letras, em alguns tipos de letra. Vê a diferença:

<p style="font-family: 'Times New Roman', Times, serif; font-size: 100px" >Com serifa.</p>

<p style="font-family: Arial, Helvetica, serif; font-size: 100px" >Sem serifa.</p>

Agora já notas a diferença na forma como a nossa página é mostrada, certo?

Mas, porque é que o tipo de letra mudou? Temos de ir de novo à nossa folha de estilo para o perceber. O código abaixo consiste numa única **regra**. Esta regra tem duas partes:

{{< code numbered="true" >}}
[[[body]]] [[[{
  font-family: sans-serif;
}]]]
{{< /code >}}

1. **`body`** é o chamado **selector**. Ele indica que esta regra se aplica a todo o elemento `BODY` das nossas páginas. Ou seja, que se aplica ao corpo da página, ou ainda, à sua parte visível.
2. De **`{`** a **`}`** temos o **bloco de declarações**. É dentro deste bloco que se colocam as várias declarações, que no nosso caso é só uma. Cada uma destas declarações especifica o valor de uma dada propriedade estilística, ou seja, uma propriedade do aspecto visual da nossa página: 

{{< code numbered="true" >}}
body {
  [[[font-family]]]: [[[sans-serif]]];
}
{{< /code >}}

1. A propriedade **`font-family`** controla o tipo de letra a usar. Como a nossa regra se aplica a todo o corpo, este tipo de letra vai aplicar-se a todo o texto da nossa página web.
2. O valor **`sans-serif`** escolhido para a propriedade `font-family` indica que desejamos um tipo de letra sem serifas. A utilização de `sans-serif` diz ao navegadores para usarem um tipo de letra à sua escolha, desde que não tenha serifas. Tem a vantagem de não nos obrigar a indicar um tipo de letra específico.

Faz as seguintes experiências:
- Usa `serif` na regra acima. Qual o resultado?
- Usa `Courier` na regra acima. Qual o resultado?

## Imagens

A página `sobre-nos.html` ficaria muito melhor com uma imagem. Vamos adicioná-la. Para isso:
- Mantem o Glitch aberto no teu projecto.
- Vai ao explorador de ficheiros no teu sistema operativo e localiza a imagem `nanonautas.jpg`. Arrasta-a para cima do teu projecto Glitch. A tua imagem deve surgir nos «assets» do projecto. Clica sobre «assets», no painel esquerdo, para a veres.

Agora que já temos a imagem no projecto, vamos adicioná-la à página. Clica no arquivo `sobre-nos.html` no painel da esquerda e adiciona o elemento `IMG` abaixo, dentro do correspondente elemento `P`, de modo a ficares com o seguinte conteúdo:
```HTML
<!DOCTYPE html>

<html>
  <head>
    <meta charset="UTF-8">
    <title>Sobre Nós</title>
    <link type="text/css" rel="stylesheet" href="css/minha-folha-de-estilo.css"/>
  </head>
  <body>
    <h1>Sobre Nós</h1>
    <p><img src="URL da imagem" alt="Retrato dos Nanonautas"/></p>
    <p>Somos os Nanonautas.</p>
    <p>Chamamo-nos Holly, Dervla, Daniel e Sam.</p>
  </body>
</html>
```

Agora, no painel da direita, clica sobre `sobre-nos.html`. Vês a imagem? Não a vez, certo? Em vez dela, surge o texto «Retrato dos Nanonautas». Para corrigires o problema:
- Volta a clicar sobre «assets» no painel da esquerda.
- Clica sobre a tua imagem. O Glitch abre a imagem e mostra-te o endereço onde ela ficou.
- Clica no botão «Copy», à direita do endereço.
- Volta ao arquivo `sobre-nos.html`.
- Apaga o texto «URL da imagem» (mas não apagues as aspas!) e cola, entre as aspas, o endereço que copiaste.
- Clica sobre `sobre-nos.html` no painel da direita.

Se tudo correu bem, já deves conseguir ver a imagem!

Mas, afinal, como funciona o elemento `IMG`? Já deves ter reparado que é um elemento vazio, pois a sua etiqueta termina em `/>`. A parte interessante são os seus atributos:
- **`src`** – O nome é uma abreviatura de *source*, ou seja, fonte. O seu valor, que foi onde colocaste o endereço da imagem, indica onde a imagem pode ser encontrada.
- **`alt`** – O nome é uma abreviatura de *alternate text* ou texto alternativo. O seu valor, que neste caso é `"Retrato dos Nanonautas"`, é um texto que explica o que a imagem é. Lembras-te quando olhaste para a página `sobre-nos.html` antes de corrigir o endereço da imagem? Este texto surgia na página. Quando corrigiste o endereço, este texto deixou de se ver. O texto alternativo é usado sempre que não seja possível ver a imagem. O caso mais importante de utilização é quando quem está a navegar pelas nossas páginas é invisual. Os invisuais navegam na web com recurso a *software* que lhes lê o conteúdo das páginas. Sem esse texto alternativo, um invisual poderia saber que a página tem uma imagem, mas não poderia saber o que a imagem representa. É fundamental fazermos as nossas páginas acessíveis por todos!

## Mais uma página

Para completarmos esta lição, vamos adicionar mais uma página. Adiciona mais um arquivo ao teu projecto chamado `as-nossas-cancoes.html`. Se não te lembrares como se cria um arquivo, volta um pouco a trás nesta lição. Agora, coloca o seguinte conteúdo nesse arquivo:

{{< code numbered="true" >}}
<!DOCTYPE html>

<html>
  <head>
    <meta charset="UTF-8">
    <title>As Nossas Canções</title>
    <link type="text/css" rel="stylesheet" href="css/minha-folha-de-estilo.css"/>
  </head>
  <body>
    <h1>As Nossas Canções</h1>
    <p>Eis uma lista das canções que sabemos tocar:</p>
    [[[<ul>]]]
      [[[<li>Magical Mystery Bug</li>]]]
      <li>Boot It</li>
      <li>The Long and Winding Code</li>
      <li>Dojo Dancing</li>
      <li>Empty Elements</li>
      <li>Java Chameleon</li>
    </ul>
  </body>
</html>
{{< /code >}}

1. O elemento `UL` serve para criares uma lista. O nome `UL` vem de *unordered list*, ou seja, uma lista de itens sem número de ordem, em que cada item é marcado por uma bola. Dá uma olhada na página. Vês as bolas? Experimenta agora usar `<ol>` e `</ol>` em vez de `<ul>` e `</ul>`. Vês a diferença? Pois. O nome `OL` vem de *ordered list*, ou lista ordenada. Por isso as bolas foram substituídas por números. E quanto ao conteúdo deste elemento? Ele é constituído por uma lista de itens, cada um dos quais especificado através de um elemento `LI`:
2. O elemento `LI` representa cada um dos itens da lista. O seu nome significa *list item*, ou seja, item de lista. O conteúdo de cada um destes elementos é o texto (e outras coisas) que deve constar como item da lista.

Dá uma nova olhada na nova página, no painel direito. Parece-te bem? Perfeito! Agora falta adicionarmos as página em falta, incluindo uma página muito importante, que é a página de início. Sem ela, ao chegares ao teu sítio web só verias uma feia lista de páginas, não é? Vamos resolver este problema na próxima lição.

{{< note >}}
Confirma que o teu sítio web, e todas as suas páginas, se assemelham a <a href="https://nanonautas-p16.glitch.me" target="_blank">este projecto</a>. Se algo falhar, compara o teu projecto com o que podes encontrar <a href="https://glitch.com/~nanonautas-p16" target="_blank">aqui</a> (clica em «View Source»).
{{< /note >}}

{{< note >}}
Ligação seguinte: <a href="{{<relref "post/html-css2.md">}}">Página de início e muito mais CSS</a>.
{{< /note >}}