---
title: 'Página de início e muito mais CSS'
date: 2020-06-02T18:00:08+01:00
tags: ['html', 'css', 'programação web']
---

!!!!!!!!!!Criar título!

CSS: Cores e medidas
Navegação
CSS: selectores com descendentes e ascendentes, classes

Conteúdos:

cores, selectores de cor, cores em hexadecimal, experiências em h1.
hexadecimal

medidas: px, em e %

Absolutas:
cm  centimeters
mm  millimeters
in  inches (1in = 96px = 2.54cm)
px *  pixels (1px = 1/96th of 1in)
pt  points (1pt = 1/72 of 1in)
pc  picas (1pc = 12 pt)

Relativas:
em  Relative to the font-size of the element (2em means 2 times the size of the current font) 
ex  Relative to the x-height of the current font (rarely used)  
ch  Relative to the width of the "0" (zero) 
rem Relative to font-size of the root element 
vw  Relative to 1% of the width of the viewport*  
vh  Relative to 1% of the height of the viewport* 
vmin  Relative to 1% of viewport's* smaller dimension 
vmax  Relative to 1% of viewport's* larger dimension  
% Relative to the parent element

Navegação
- Código HTML
- CSS: selectores mais complexos




Nesta lição do percurso de aprendizagem [Programação web com HTML/CSS](/html-css) vamos aprender a criar uma página de início e vamos ver o CSS mais a fundo.

## Recursos

- **[Sessão #261 (HTML/CSS #2)]({{<ref "/sessions/session-261">}})** – Sessão do CoderDojo LX correspondente a esta secção.
- **[Apresentação da sessão #261 (HTML/CSS #2)](https://bit.ly/cdlx-html2)** – A apresentação usada nessa sessão.
- **[nanonautas-sessao2](https://glitch.com/~nanonautas-sessao2)** – Projecto com que podes começar esta lição. Também podes começar onde terminaste a ligação anterior.
- Os exemplos do livro correspondentes a esta sessão:
  - **[nanonautas-p18](https://glitch.com/~nanonautas-p18)** – Projecto até à página 18 do livro.
  - **[nanonautas-p22](https://glitch.com/~nanonautas-p22)** – Projecto até à página 22 do livro.
  - **[nanonautas-p28](https://glitch.com/~nanonautas-p28)** – Projecto até à página 28 do livro.

## Mais uma página

Abre o projecto que completaste na lição anterior, [Introdução à Web, ao HTML e ao CSS]({{<relref "post/html-css1.md">}}). Se preferires, podes abrir o nosso projecto de arranque para esta lição, [nanonautas-sessao2](https://glitch.com/~nanonautas-sessao2), e remisturá-lo.

{{< note >}}
Talvez esteja na altura de dar um nome apropriado ao teu projecto, se não o fizeste ainda. No Glitch, no editor do projecto, clica sobre o nome do teu projecto no canto superior esquerdo. Dá-lhe um nome apropriado.
{{< /note >}}

Neste momento o sítio web dos Nanonautas tem já duas páginas web, `as-nossas-cancoes.html` e `sobre-nos.html`. Aqui vai a estrutura de pastas e arquivos neste momento:

{{< fileTree >}}
<code>/</code> [pasta raiz]
  * css
    * minha-folha-de-estilo.css
  * as-nossas-cancoes.html
  * sobre-nos.html
{{< /fileTree >}}

Se bem te lembras, os Nanonautas tinham decidido que o seu sítio web teria quatro páginas *além de uma página inicial*. 
- **Início** – Página com ligações para as seguintes páginas:
  - **Sobre nós** – Página com o seguinte conteúdo:
    - Informação sobre a nossa banda
    - O nosso novo CD
    - Comprem a nossa t-shirt
  - **As nossas canções** – Página com o seguinte conteúdo:
    - Informação sobre as nossas canções
    - Vídeos
  - **Vejam-nos tocar** – Página com o seguinte conteúdo:
    - Onde nos podem ver tocar
    - Próximos concertos
  - **Dar um concerto** – Página com o seguinte conteúdo:
    - Como dar um concerto
    - Dicas top

Ou seja, temos neste momento duas páginas de cinco, pelo que ainda faltam três páginas web.

Vamos criar a terceira página. Cria o arquivo `vejam-nos-tocar.html` (já sabes como):
```HTML
<!DOCTYPE html>

<html>
  <head>
    <meta charset="UTF-8">
    <title>Vejam-nos Tocar</title>
    <link type="text/css" rel="stylesheet" href="css/minha-folha-de-estilo.css"/>
  </head>
  <body>
    <h1>Vejam-nos Tocar</h1>
    <p>[coloca aqui a data e hora do próximo concerto]</p>
  </body>
</html>
```
No painel direito, clica sobre a página que acabaste de criar. A página é muito simples, por enquanto.

{{< note >}}
O painel direito do editor do Glitch é o painel de visualização do sítio web. Se não estiver aberto, procura o menu «Show▼» e escolhe «Next to The Code».
{{< /note >}}

A estrutura de pastas e arquivos passou a ser:

{{< fileTree >}}
<code>/</code> [pasta raiz]
  * css
    * minha-folha-de-estilo.css
  * as-nossas-cancoes.html
  * sobre-nos.html
  * vejam-nos-tocar.html
{{< /fileTree >}}

Já só nos faltam duas páginas web: a página inicial e a página sobre como dar um concerto.

## A página inicial

Se olhares para o teu site neste momento, verás que só se chega a cada uma das páginas clicando nela na lista arquivos que surge ao visualizar o sítio web. Isto não é aceitável. Temos de ter uma página inicial e temos de fazer com que essa página inicial tenha ligações (na realidade hiperligações) para as restantes páginas. Vamos então criá-la.

Cria um novo arquivo chamado `index.html`.

{{< warning >}}
Atenção! O arquivo da página inicial tem de ter exactamente o nome indicado: <code>index.html</code>. As restantes páginas podem ter arquivos com outros nomes à escolha, mas não esta.
{{< /warning >}}

Coloca o seguinte no novo arquivo:
```HTML
<!DOCTYPE html>

<html>
  <head>
    <meta charset="UTF-8">
    <title>Início</title>
    <link type="text/css" rel="stylesheet" href="css/minha-folha-de-estilo.css"/>
  </head>
  <body>
    <h1>Somos os Nanonautas!</h1>
    <p>Este é o nosso sítio web. Clique numa ligação para visitar uma página:</p>
    <ul>
      <li><a href="sobre-nos.html">Sobre Nós</a></li>
      <li><a href="as-nossas-cancoes.html">As Nossas Canções</a></li>
      <li><a href="vejam-nos-tocar.html">Vejam-nos Tocar</a></li>
    </ul>
  </body>
</html>
```

A estrutura de pastas e arquivos passou a ser:

{{< fileTree >}}
<code>/</code> [pasta raiz]
  * css
    * minha-folha-de-estilo.css
  * as-nossas-cancoes.html
  * index.html
  * sobre-nos.html
  * vejam-nos-tocar.html
{{< /fileTree >}}

Olha para o painel direito. Notas a diferença? Agora já não é mostrada uma lista de arquivos e pastas: é mostrada a página inicial, e nem precisaste de clicar sobre o arquivo `index.html` para que isso aconteça!

Será que acontece o mesmo no teu sítio web ao vivo? Procura o menu «Show▼» e clica em «In a New Window». Abre-se uma nova janela/separador com a nova página inicial. Repara também como a nova página inicial tem ligações para as restantes páginas. Já tens um verdadeiro sítio web, agora! 

Repara que a página mostrada é a inicial, apesar de o endereço na barra de endereços não incluir `index.html`. Clica numa das ligações para as outras páginas. Repara no endereço da barra de endereços: agora já inclui o nome do arquivo correspondente. Vai à barra de endereço e substitui o nome do arquivo por `index.html`. Carrega em `<enter>`. Estás de novo na página inicial, mas desta vez o nome do seu arquivo surge na barra de endereço.

Para não nos baralharmos, aqui vão os vários endereços associados ao novo sítio web no caso do nosso código (no teu caso é semelhante, mas com o nome do teu projecto no lugar de `nanonautas-p18`):
- https://nanonautas-p18.glitch.me/ – A página inicial, `index.html`.
- https://nanonautas-p18.glitch.me/index.html – A página inicial, `index.html`.
- https://nanonautas-p18.glitch.me/as-nossas-cancoes.html – A página com as canções dos Nanonautas, `as-nossas-cancoes.html`.
- https://nanonautas-p18.glitch.me/sobre-nos.html – A página sobre os Nanonautas, `sobre-nos.html`.
- https://nanonautas-p18.glitch.me/vejam-nos-tocar.html – A página sobre os concertos dos Nanonautas, `vejam-nos-tocar.html`.

Como podes ver, há dois endereços válidos para a página inicial: um com `index.html`, outro sem este nome de arquivo. Isto é normal. Os servidores web geralmente sabem que, se receberem um pedido de página usando uma ligação para uma pasta do sítio (incluindo a sua *raiz*), devem responder ao navegado enviando-lhe o HTML guardado no arquivo `index.html`, se este arquivo existir.

## Ligações em HTML

Olha com atenção para o arquivo `index.html`. O que há de novo nele? As listas não numeradas, com os elementos `UL` e `LI` já tu conheces. O que é novo é o que está dentro dos itens da lista: ligações a outras páginas. Essas ligações recorrem a um novo elemento `A` (de *anchor*, ou âncora), com as respectivas etiquetas de abertura e fecho. Por exemplo,
```HTML
<a href="sobre-nos.html">Sobre Nós</a>
```

O elemento `A` tem duas partes muito importantes. A primeira é o seu conteúdo, ou seja, o que quer que se encontre entre as etiquetas de abertura e fecho. Esse conteúdo é o texto que vai poder ser clicado para ir para a página indicada pelo endereço. A segunda é esse endereço, que se indica como valor do atributo `href`. Como a página inicial está na mesma pasta (de raiz) do teu projecto, o endereço é simplesmente o nome do arquivo que guarda a página web a que nos queremos ligar.

{{< note >}}
Aos endereços começados por <code>https://<i>nome_de_dominio</i>/</code> ou <code>http://<i>nome_de_dominio</i>/</code> chama-se <strong>endereços absolutos</strong>, pois contêm o endereço completo de uma página web. Aos restantes endereços chama-se endereços relativos (ao próprio sítio web). Até agora só usámos endereços relativos. A única excepção foi o endereço do retrato dos Nanonautas, lembras-te?
{{< /note >}}

Nota que o endereço pode ser um URL completo, ou seja, um endereço absoluto. Por exemplo, o código HTML
```HTML
<p>A <a href="https://pt.wikipedia.org/" target="_blank">Wikipédia</a> é fantástica!</p>
```
resulta no seguinte:

{{< blockquote >}}
<p>A <a href="https://pt.wikipedia.org/" target="_blank">Wikipédia</a> é fantástica!</p>
{{< /blockquote >}}

Nota ainda que, neste caso, adicionámos o atributo `target` (alvo) com o valor `"_blank"`. Este atributo controla onde será aberta a página web endereçada pela ligação. Quando não se usa este atributo, a página de destino é aberta na mesma janela/separador onde está a página web com a ligação. Quando se usa o atributo com o valor escolhido, `"_blank"`, a página de destino é aberta numa nova janela/separador. Experimenta clicar na ligação, para veres. Compara agora com o que aconteceria se o código fosse
```HTML
<p>A <a href="https://pt.wikipedia.org/">Wikipédia</a> é fantástica!</p>
```
que resulta no seguinte:

{{< blockquote >}}
<p>A <a href="https://pt.wikipedia.org/"">Wikipédia</a> é fantástica!</p>
{{< /blockquote >}}

{{< warning >}}
Usa endereços absolutos apenas para ligar a páginas de outros sítios web (e, se houver escolha, prefere os endereços seguros, começados por `https://`). Em ligações para outras páginas do teu sítio web, prefere endereços relativos.
{{< /warning >}}

## A página em falta

A última página que nos falta é sobre como dar um concerto. Vamos supor que o nome do arquivo correspondente é `dar-um-concerto.html`. Vamos já actualizar a página inicil (arquivo `index.html`) de modo a conter uma ligação para essa página, que criaremos de seguida:
```HTML
    …
    <ul>
      <li><a href="sobre-nos.html">Sobre Nós</a></li>
      <li><a href="as-nossas-cancoes.html">As Nossas Canções</a></li>
      <li><a href="vejam-nos-tocar.html">Vejam-nos Tocar</a></li>
      <li><a href="dar-um-concerto.html">Dar um Concerto</a></li>
    </ul>
    …
```

Cria agora o arquivo para a nova página. Usa o mesmo nome, `dar-um-concerto.html`, que colocaste na ligação. Coloca no novo arquivo o seguinte código HTML:
```HTML
<!DOCTYPE html>

<html>
  <head>
    <meta charset="UTF-8">
    <title>Dar um Concerto</title>
    <link type="text/css" rel="stylesheet" href="css/minha-folha-de-estilo.css"/>
  </head>
  <body>
    <h1>Dar um Concerto</h1>
    <p>Dar um concerto pode ser muito divertido! Ou pode ser completamente
    assustador! Às vezes pode ser as duas coisas ao mesmo tempo.</p>
    <p>Por isso fizemos uma lista com os nossos principais conselhos para se
    fazerem grandes concertos.</p>
    <h2>Faz cópias de uma set-list</h2>
    <p>Uma <strong>set-list</strong> é uma lista com todas as canções pela ordem em
    que serão tocadas.</p>
    <p>Faz cópias para todos.</p>
    <p>Faz as cópias em letras <strong>GRANDES!</strong> para que as consigas ler
    mesmo que estejam no chão, junto aos teus pés, ou se a iluminação não for muito
    boa.</p>
    <h2>Não te esqueças das peças sobressalentes</h2>
    <p>Alguns instrumentos têm partes que precisam de ser substituídas quando se
    gastam ou se partem. Por exemplo:</p>
    <ul>
      <li>cordas de guitarra</li>
      <li>palhetas de saxofone e de clarinete</li>
      <li>baquetas de bateria</li>
    </ul>
    <p>Faz uma lista das peças sobressalentes que poderão ser precisas e assegura-te
    de que sabes onde elas estão em caso de emergência.</p>
    <h2>Planeia onde irás ficar no palco</h2>
    <p>Antes de começares a instalar os teus instrumentos, dedica alguns minutos a
    decidires onde tudo irá ficar.</p>
    <ul>
      <li>A bateria ficará no centro do palco? Ou a um lado?</li>
      <li>Haverá tomada eléctrica para o amplificador se o teu guitarrista ficar do
      lado direito?</li>
    </ul>
    <p>É muito melhor pensar em tudo isto <strong>antes</strong> de começares a
    instalar os instrumentos. É deveras irritante teres de começar a desligar coisas
    e a trocar posições já depois de estar tudo instalado!</p>
    <h2>Sabe onde vais, sabe a que horas tocas</h2>
    <p>Se fores dar um concerto a um local onde nunca estiveste antes, certifica-te
    de que sabes onde é. Imprime um mapa, ou liga o GPS antes de saíres. Não há nada
    pior do que estarmos perdidos num local desconhecido meia hora antes de termos
    de entrar em palco.</p>
    <p>Quando lá chegares, a primeira coisa que deves fazer é <strong>descobrir
    a que horas entras em palco</strong>. Ao longo da noite muitas vezes há
    alterações. Pergunta aos responsáveis pelo evento a que horas actuas. Não
    fiques desprevenido!</p>
  </body>
</html>
```

{{< note >}}
Confirma que o teu sítio web, e todas as suas páginas, se assemelham a <a href="https://nanonautas-p22.glitch.me" target="_blank">este projecto</a>. Se algo falhar, compara o teu projecto com o que podes encontrar <a href="https://glitch.com/~nanonautas-p22" target="_blank">aqui</a> (clica em «View Source»).
{{< /note >}}

Agora já temos o sítio web completo. A sua estrutura é a seguinte:
{{< fileTree >}}
<code>/</code> [pasta raiz]
  * css
    * minha-folha-de-estilo.css
  * as-nossas-cancoes.html
  * dar-um-concerto.html
  * index.html
  * sobre-nos.html
  * vejam-nos-tocar.html
{{< /fileTree >}}

Vamos agora olhar para alguma novidades HTML introduzidas na nova página:

{{< code numbered="true" >}}
<!DOCTYPE html>

<html>
  <head>
    […]
  </head>
  <body>
    <h1>Dar um Concerto</h1>
    <p>Dar um concerto […] tempo.</p>
    <p>Por isso fizemos […] concertos.</p>
    [[[<h2>Faz cópias de uma set-list</h2>]]]
    <p>Uma [[[<strong>set-list</strong>]]] é uma lista com todas as canções pela ordem em
    que serão tocadas.</p>
    …
  </body>
</html>
{{< /code >}}

1. A primeira semi-novidade é o elemento `H2`. Ainda não o tinhamos usado no nosso sítio web, mas já tinhamos falado dele. Este elemento serve para indicar um título de secção de nível 2 (as secções em que um capítulo de um livro se divide, por exemplo). A prática mais usual é haver apenas um elemento `H1` por página, que é como quem diz, cada página conter apenas um «capítulo», e depois dividir a página em secções, cada qual com o seu título num elemento `H2`. Se houver subsecções, então usa-se `H3`, e assim sucessivamente.

2. A segunda novidade é o elemento `STRONG`. Ele é usado para marcar um pedaço de texto que queremos que seja reforçado. Normalmente isso resulta em que esse pedaço de texto seja mostrado em negrito, mas isso pode ser alterado usando o CSS, se preferires outra forma visual de representar texto reforçado.

{{< note >}}
Mais tarde veremos que há melhores formas ainda de estruturarmos as nossas páginas. Por exemplo, podemos colocar todo o conteúdo principal de uma página (elemento <code>MAIN</code>: <code>&lt;main>…&lt;/main></code>) dentro de um artigo (elemento <code>ARTICLE</code>: <code>&lt;article>…&lt;/article></code>), que faz o papel daquilo a que chamámos «capítulo», por analogia com um livro. Esse artigo teria o seu título (<code>H1</code>) e seria dividido em secções (elemento <code>SECTION</code>: <code>&lt;section>…&lt;/section></code>), cada uma com o seu título <code>H2</code>.
{{< /note >}}

## Uma grande dose de estilo

No final desta secção vais obter o resultado que podes ser neste projecto: [nanonautas-p28](https://nanonautas-p28.glitch.me/). Dá uma espreitadela. Vê cada uma das páginas. Reparaste que o conteúdo das páginas é exactamente o mesmo? O que vamos alterar é «apenas» o seu aspecto. E, já sabes, para isso é que queremos as folhas de estilo.

Vamos então começar, mas aos poucos. No painel esquerdo do Glitch, clica em `css/minha-folha-de-estilo.html`. Apaga todo o conteúdo desse arquivo e substitui-o pelo seguinte:

{{< code numbered="true" >}}
[[[body { 
}]]]

[[[html {
}]]]
{{< /code >}}

1. A primeira regra tem o selector `body`, por isso aplica-se ao elemento `BODY`, ou seja, a todo o corpo da página web, i.e., à caixa onde se encontrará todo o conteúdo da nossa página web.
2. A segunda regra tem o selector `html`, por isso aplica-se ao elemento `HTML`, ou seja, a toda a página web, incluindo o seu corpo, mas não só.

Neste momento as duas regras estão vazias, sem quaisquer declarações. Vamos introduzir as declarações aos poucos. À medida que introduzimos as declarações, vai observando o resultado no painel da direita. Faz também experiências com diferentes valores.

### A borda

Acrescenta as seguintes declarações à regra com selector `body`:

{{< code numbered="true" >}}
body { 
  [[[background-color: Thistle;]]]
  [[[border: 2px solid Gray;]]]
  [[[border-radius: 16px;]]]
}

html {
}
{{< /code >}}

1. Especifica que o valor a usar para a propriedade `background-color` do `BODY`, ou seja, a sua cor do fundo, é `Thistle`, que é um cor-de-rosa arroxeado a se poderia chamar, numa tradução directa, cor-de-cardo. Experimenta outras cores, como `Fuchsia`, `Yellow` ou `Red`. Vê mais informação no [cssreference.io](https://cssreference.io/property/background-color/).
2. Especifica as características da borda do `BODY`:`2px` é a espessura da borda (experimenta `20px`), `solid` torna a borda contínua (experimenta `dotted`) e `Gray` indica que a borda deve ser desenhada a cinzento (experimenta `Red`). Vê mais informação no [cssreference.io](https://cssreference.io/property/border/).
3. Especifica que o raio de curvatura a usar nos vértices da borda é de 16 píxeis. Experimenta outros valores. Vê mais informação no [cssreference.io](https://cssreference.io/property/border-radius/).

{{< note >}}
Um píxel é um dos quadradinhos coloridos que formam o ecrã do teu computador.
{{< /note >}}

### O tipo de letra

Acrescenta as seguintes declarações à regra com selector `body`:

{{< code numbered="true" >}}
body { 
  background-color: Thistle;
  border: 2px solid Gray;
  border-radius: 16px;
  [[[font-family: sans-serif;]]]
}

html {
}
{{< /code >}}

Já vimos o que esta declaração faz na primeira lição, [Introdução à Web, ao HTML e ao CSS]({{<relref "post/html-css1.md#folhas-de-estilo">}}). Lembras-te?

### Margens, bordas e enchimentos

Muitos elementos do HTML são representados em «caixas», ou seja, o respectivo conteúdo é colocado dentro de uma **caixa de conteúdo** rectangular. Essa caixa de conteúdo pode ser rodeada por uma **borda**, com uma dada **espessura**. O **enchimento** é o espaço entre a caixa de conteúdo e a sua borda. A **margem** é espaço extra fora da borda, usado para manter a caixa afastada de outros elementos. Nota que o enchimento, a espessura da borda e a margem podem ser diferentes em cada um dos quatro lados da caixa (**topo**, **base**, **esquerda** e **direita**). Vê a figura abaixo para melhor perceberes os conceitos:

{{< figure src="/post/box-model.png" title="Modelo de caixas do HTML." >}}

### A margem

Acrescenta as seguintes declarações à regra com selector `body`:

{{< code numbered="true" >}}
body { 
  background-color: Thistle;
  border: 2px solid Gray;
  border-radius: 16px;
  font-family: sans-serif;
  [[[margin-left: auto;]]]
  [[[margin-right: auto;]]]
}

html {
}
{{< /code >}}

1. Especifica que a margem esquerda deve ser automática. Ou seja, ajusta-se ao que for necessário para acomodar a caixa do corpo da página, com o seu conteúdo e com as restrições à largura que lhe serão impostas mais tarde. Vê mais informação no [cssreference.io](https://cssreference.io/property/margin-left/).
2. Especifica que a margem direita deve ser automática. Ou seja, ajusta-se ao que for necessário para acomodar a caixa do corpo da página, com o seu conteúdo e com as restrições à largura que lhe serão impostas mais tarde. Vê mais informação no [cssreference.io](https://cssreference.io/property/margin-right/).

Sendo as duas margens automáticas, o corpo da página ficará centrado na página. Como não impusemos ainda nenhuma restrição à largura do corpo da página, este ocupará toda a página, pelo que as margens esquerda e direita são neste momento zero.

Neste momento recomendamos que vás ao menu «Show▼» e cliques em «In a New Window». Experimenta estreitar e alargar a janela. Que acontece à margem? É sempre zero?

Acrescenta as seguintes declarações à regra com selector `body`:

{{< code numbered="true" >}}
body { 
  background-color: Thistle;
  border: 2px solid Gray;
  border-radius: 16px;
  font-family: sans-serif;
  margin-left: auto;
  margin-right: auto;
  [[[max-width: 1024px;]]]
  [[[min-width: 256px;]]]
}

html {
}
{{< /code >}}

1. Especifica que a caixa com o corpo da página não pode exceder 1024 píxeis de largura (*width*). Vê mais informação no [cssreference.io](https://cssreference.io/property/max-width/).
2. Especifica que a caixa com o corpo da página não pode ter uma largura inferior a 256 píxeis. Vê mais informação no [cssreference.io](https://cssreference.io/property/min-width/).

Para testares o efeito da largura máxima, vê de novo o teu sítio web numa janela/separador à parte. Alarga e estreita a janela para veres o que acontece.

Para testares o efeito da largura mínima, vê o teu sítio web no painel direito do editor do Glitch. Alarga-o e estreita-o veres o que acontece. Repara que quando a largura do painel é inferior a 256 píxeis, a tua página web não estreita mais: é necessário deslizar para a esquerda e para a direita para a ver na íntegra.

Também podes testar diferentes valores para a largura máxima e mínima do corpo da página.

### O enchimento

Acrescenta as seguintes declarações à regra com selector `body`:

{{< code numbered="true" >}}
body { 
  background-color: Thistle;
  border: 2px solid Gray;
  border-radius: 16px;
  font-family: sans-serif;
  margin-left: auto;
  margin-right: auto;
  max-width: 1024px;
  min-width: 256px;
  [[[padding-top: 8px;
  padding-bottom: 24px;
  padding-left: 24px;
  padding-right: 24px;]]]
}

html {
}
{{< /code >}}

1. Estas declarações especificam o enchimento a usar de cada lado da caixa de conteúdo. Os valores foram escolhidos de modo a deixar o conteúdo «respirar» melhor dentro da sua caixa com borda. Vê mais informação no [cssreference.io](https://cssreference.io/property/padding/).

Experimenta alterar os valores para veres o efeito. Alarga e estreita o painel da direita, de visualização, para perceberes melhor o conceito de enchimento.

### O fundo da página

Para completarmos a lição, temos de ver as declarações mais difíceis, que controlam o aspecto do fundo da página web, fora da caixa do corpo da página. O CSS é neste caso mais difícil de perceber, pois estamos a usar o CSS para obter um padrão bonito para o fundo.

Acrescenta as seguintes declarações à regra com selector `html`, pois elas aplicam-se a toda a página, e não apenas ao corpo (`body`):

{{< note >}}
Se as declarações dentro da regra com o selector <code>html</code> se aplicam a toda a página, então também se aplicam ao seu corpo. Nesse caso as declarações sobre o fundo da página não deveriam afectar também o fundo do corpo? Na realidade sim, afectariam, mas como demos ao corpo as suas próprias declarações sobre o fundo, estas sobrepõem-se às declarações mais gerais da página. Isto acontece porque a regra com selector <code>body</code> é mais específica que a regra com selector <code>html</code>.
{{< /note >}}

{{< code numbered="true" >}}
body { 
  background-color: Thistle;
  border: 2px solid Gray;
  border-radius: 16px;
  font-family: sans-serif;
  margin-left: auto;
  margin-right: auto;
  max-width: 1024px;
  min-width: 256px;
  padding-top: 8px;
  padding-bottom: 24px;
  padding-left: 24px;
  padding-right: 24px;
}

html {
  [[[background: radial-gradient(circle, SkyBlue, SkyBlue 50%, LightCyan 50%, SkyBlue)]]];
  [[[background-size: 200px 200px;]]]
}
{{< /code >}}

1. Lê primeiro o número 2. Depois volta aqui. (Esperando… OK!) Aqui dizemos em que é que consiste cada quadrado do mosaico do fundo. Para isso usamos uma função do CSS, `radial-gradient()`.  Vê mais informação na [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/radial-gradient).
2. Parece estranho poder-se definir o tamanho do fundo, não é? Na realidade, isso pode ser útil, especialmente quando a propriedede `background-repeat` tem o valor `repeat`, que é o valor pré-definido. Nesse caso o fundo fica dividido num mosaico de pequenos rectângulos (ou quadrados) com a dimensão utilizada. Nota que escolhemos para já quadrados bastante grandes, mas isso é apenas para se perceber melhor o efeito. Vê mais informação no [cssreference.io](https://cssreference.io/property/background-size/).

A função `radial-gradient()` gera uma imagem de fundo com uma gradação radial entre cores (radial significa que é do centro para a periferia). Não esquecer que o nosso mosaico do fundo é constituído por quadrados. Esta função gera uma imagem para um desses quadrados, que é repetida por todos os outros.

Como funciona a função `radial-gradient()`? Ela recebe vários valores (chamados **argumentos** da função). Vamos ver o que significam, por ordem:
- `circle` – A gradação radial tem uma natureza circular.
- `SkyBlue` – Cor da gradação no centro do quadrado.
- `SkyBlue 50%` – A cor da gradação a 50% da distância entre o centro do quadrado e os vértices do quadrado. Como é a mesma cor que no centro, acaba por resultar um círculo com um azul-celeste uniforme.
- `LightCyan 50%` – Parece ser o mesmo que o argumento anterior, embora com outra cor, e de facto os 50% referem-se à mesma posição. Mas como está **depois** do argumento anterior, esta nova cor, ciano-claro, funciona como início de uma nova gradação em direcção ao exterior do quadrado. Ou seja, à distância de 50% entre o centro e os vértices do quadrado há uma transição abrupta entre azul-celeste e ciano-claro.
- `SkyBlue` – Não se especificando uma posição, e sendo o último argumento, essa posição toma o valor pré-definido de 100%. Ou seja, esta cor, que é de novo azul-celeste, é o fim da gradação e ocorre no vértice do quadrado.

Isto é muito denso, sem dúvida. Brinca um pouco com os valores. Vê os vários efeitos que consegues.

Finalmente, para deixarmos o fundo como previsto, altera o tamanho do quadrado do fundo:
```CSS
…

html {
  …
  background-size: 8px 8px;
}
```

E é isto! Navega um pouco pelo teu sítio web e aprecia-o. Nada mau, hein?

{{< note >}}
Confirma que o teu sítio web, e todas as suas páginas, se assemelham a <a href="https://nanonautas-p28.glitch.me" target="_blank">este projecto</a>. Se algo falhar, compara o teu projecto com o que podes encontrar <a href="https://glitch.com/~nanonautas-p18" target="_blank">aqui</a> (clica em «View Source»).
{{< /note >}}


<!--
{{< note >}}
Ligação seguinte: <a href="{{<relref "post/html-css2.md">}}">!!!!!!!!!!!!!</a>.
{{< /note >}}
-->