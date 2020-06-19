---
title: 'Navegação, cores, medidas e mais selectores'
date: 2020-06-02T18:00:08+01:00
tags: ['html', 'css', 'programação web']
---

Nesta lição do percurso de aprendizagem [Programação web com HTML/CSS]({{<relref "post/html-css">}}) vamos aprender a criar uma barra de navegação para o nosso sítio web e vamos aprender um pouco mais sobre folhas de estilo em CSS, incluindo como usar cores nas declarações, que unidades de medida se podem usar e como usar selectores mais sofisticados.

## Recursos

- **[Sessão #265 (HTML/CSS #4)]({{<ref "/sessions/session-265">}})** – Sessão do CoderDojo LX correspondente a esta secção.
- **[Apresentação da sessão #265 (HTML/CSS #4)](https://bit.ly/cdlx-html4)** – A apresentação usada nessa sessão.
- **[nanonautas-sessao4](https://glitch.com/~nanonautas-sessao4)** – Projecto com que podes começar esta lição. Também podes começar onde terminaste a lição anterior.
- Os exemplos do livro correspondentes a esta lição:
  - **[nanonautas-p34](https://glitch.com/~nanonautas-p34)** – Projecto até à página 34 do livro.
  - **[nanonautas-p35](https://glitch.com/~nanonautas-p35)** – Projecto até à página 35 do livro.
  - **[nanonautas-p41](https://glitch.com/~nanonautas-p41)** – Projecto até à página 41 do livro.
  - **[nanonautas-p43](https://glitch.com/~nanonautas-p43)** – Projecto até à página 43 do livro.

## Cores em CSS

Abre o projecto que completaste na lição anterior, [Página de início e muito mais CSS]({{<relref "post/html-css2">}}). Se preferires, podes abrir o nosso projecto de arranque para esta lição, [nanonautas-sessao4](https://glitch.com/~nanonautas-sessao4), e remisturá-lo. Não te esqueças de abrir o painel direito de visualização do sítio web, para poderes ir vendo o resultado de todas as alterações que fores fazendo.

Neste momento o sítio web dos Nanonautas tem já cinco páginas web, incluindo uma página inicial. Aqui vai a estrutura de pastas e arquivos neste momento:

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

Lembras-te como usaste a tua tua folha de estilo para dar cor a diferentes partes das tuas páginas web? Vamos agora estudar um pouco as diferentes formas de indicar as cores em CSS.

### Nomes de cores

Começa por abrir a tua folha de estilo, `css/minha-folha-de-estilo.css`. Cria uma nova regra, temporária, só para veres o efeito. Coloca-a logo no início da folha de estilo:

{{< code numbered="true" >}}
[[[h1]]] {
  [[[background-color]]]: [[[Yellow]]];
}

body {
  […]
}

html {
  […]
}
{{< /code >}}

1. Como vês, a nossa regra usa o selector `h1`, o que significa que se aplica apenas aos elementos `H1`, que se bem te recordas são os títulos dos nosos «capítulos». Por isso, apenas o fundo do título «Somos os Nanonautas!» apareceu a amarelo.
2. Recorda-te que esta é a propriedade que corresponde à cor (*color*) do fundo (*background*).
3. Finalmente, chegamos aqui à parte que nos interessa mais neste momento: a cor. O valor `Yellow` corresponde naturalmente à cor amarela. Mas será o CSS inteligente o suficiente para compreender qualquer cor? Vamos ver.

Vamos fazer mais umas experiências:
- Substitui `Yellow` por `Red`. Que tal? Parece que o CSS sabe o que é que *red* significa, em inglês.
- Experimenta `Blue`. Funciona, certo?
- Experimenta também `LightBlue`. Que tal?
- E se for `Light Blue`? Funciona? Pelos vistos não: o CSS não permite espaços entre as palavras que compõem o nome de uma cor.
- Vamos tentar uma cor mais sofisticada: `LightSeaGreen`. Uau! Verde-mar claro!
- Também podes experimentar nomes em português, mas como o CSS usa o inglês como base, o mais certo é falhares.
- E que tal, digamos, `Mauve`?  Então? Pelos vistos, a cor malva é demasiado sofisticada para o CSS…
 
Conclusão? O CSS permite-nos indicar muitas cores textualmente, pelo seu nome, mas não todas as que se podem exprimir em inglês. Consulta a página [CSS3 Color Names](https://www.cssportal.com/css3-color-names/) e verás que o CSS reconhece 148 nomes de cores. Também podes ver essas cores todas [aqui](https://all-css-color-names.glitch.me/).

### Quantidade de cores no computador

Embora as cores do mundo real sejam muito mais ricas do que as cores que podemos representar nos nossos computadores, os nossos computadores são capazes de representar muito mais cores do que as cores representadas pelos 147 nomes de cores que o CSS reconhece. Na realidade, os nossos computadores usualmente distinguem 256 × 256 × 256 = 16&nbsp;777&nbsp;216 cores. Isso: dezasseis milhões, setecentas e setenta e sete mil, duzentas e dezasseis cores!

### RGB e a função `rgb()` do CSS

Mas, de onde vêem essas cores todas? Nos nossos computadores, as cores são representadas na forma de misturas de três cores:

![Adição de vermelho, verde e azul](https://upload.wikimedia.org/wikipedia/commons/2/28/RGB_illumination.jpg)

As três cores são:
- R – *red* ou vermelho
- G – *green* ou verde
- B – *blue* ou azul

Consoante a intensidade de cada uma destas três cores, assim terás uma cor diferente. Mas, e os 16&nbsp;777&nbsp;216? Eles surgem porque o usual é estas três intensidades poderem tomar valores entre 0 e 255, ou seja, 256 valores diferentes. Como há três intensidades (R, G e B), isso resulta em 256 × 256 × 256 = 16&nbsp;777&nbsp;216 cores diferentes. Vê todas estas diferentes cores na seguinte imagem:

![Todas as cores possíveis  no computador](https://allrgb.com/images/domain-warped-simplex-noise-as-hsv.png)

{{< note >}}
Mas nota que os computadores não representam de todo todas as cores que nós, humanos, distinguimos! Há muito mais do que 16&nbsp;777&nbsp;216, para os humanos. Na realidade, infinitas. :-)
{{< /note >}}

Faz agora a seguinte alteração:
{{< code numbered="true" >}}
h1 {
  background-color: [[[rgb(0, 0, 0)]]];
}

[…]
{{< /code >}}

1. Vês alguma diferença? Claro que sim! O que não vês é tudo negro. :-) É que a cor `rgb(0, 0, 0)` (estamos a usar a função `rgb()`do CSS) significa intensidade zero nas três cores R, G e B, logo o resultado é… preto. Letras pretas sobre fundo preto dão no que vês.

Agora experimenta os seguintes valores:
- `rgb(255,   0,   0)` – Vermelho
- `rgb(  0, 255,   0)` – Verde
- `rgb(  0,   0, 255)` – Azul
- `rgb(255, 255,   0)` – Amarelo
- `rgb(255,   0, 255)` – Magenta
- `rgb(  0, 255, 255)` – Ciano
- `rgb(255, 255, 255)` – Branco
- `rgb(224, 176, 255)` – Malva (afinal é possível, mas não com um nome de cor, como `Mauve`)
- `rgb(111,  78,  55)` – Café

Isto dá-te uma grande flexibilidade para escolheres as tuas cores. Mas a verdade é que esta forma de indicar as cores em CSS é pouco usada. O mais usual é usar-se códigos hexadecimais. Já vamos ver o que isso é.

### Numeração hexadecimal

Internamente, os computadores trabalham com numeração binária, ou seja, com números que são representados apenas com dois dígitos ou algarismos: o 0 (zero) e o 1 (um). Infelizmente, para nós humanos escrever os números em numeração binária é bastante infernal. Por exemplo, 78 em numeração binária é 1001110.

Sendo a numeração binária inconveniente, muitas vezes usa-se a numeração hexadecimental, que é muito fácil converter para numeração binária, e que é mais fácil de usar por nós humanos. Mas o que significa hexadecimal? Significa que usamos não dois dígitos ou algarismos, como na numeração binária, nem dez algarismos, como na numeração decimal (a que usamos todos os dias), mas sim 16 dígitos.

Os algarismos na numeração decimal são os que já conheces: 0, 1, 2, 3, 4, 5, 6, 7, 8 e 9. E os da numeração hexadecimal? Podíamos inventar símbolos para cada um deles, mas como os programadores são muito práticos, decidiram usar os mesmos que na numeração decimal: 0, 1, 2, 3, 4, 5, 6, 7, 8 e 9. O problema é que não chegam: faltam seis algarismos. Mais uma vez de forma muito prática, os programadores decidiram usar as primeiras seis letras. Ou seja, na numeração hexadecimal há 16 algarismos:
- 0
- 1
- 2
- 3
- 4
- 5
- 6
- 7
- 8
- 9
- A (com valor 10)
- B (com valor 11)
- C (com valor 12)
- D (com valor 13)
- E (com valor 14)
- F (com valor 15)

E como se representam os números? Recordas-te como funcionam os números na numeração decimal? Os algarismos têm *pesos* diferentes consoante a posição (vamos esquecer os números com parte fraccionária). Por exemplo, o número 5432 significa 5 milhares, 4 centenas, 3 dezenas e 2 unidades. Podemos escrever este número das seguintes formas:
- 5432
- 5 × 1000 + 4 × 100 + 3 × 10 + 2 × 1
- 5 × 10 × 10 × 10 + 4 × 10 × 10 + 3 × 10 + 2 × 1

Na numeração hexadecimal é o mesmo, mas não esquecendo que em vez de 10, estamos a trabalhar com 16 algarismos, de 0 a F. Então, que significa, por exemplo, o número #1538 (para distinguir os números em hexadecimal dos números em decimal, precedêmo-los do caractere #, que é o que o CSS faz)? Vejamos:
- #1538
- #1 × 16 × 16 × 16 + #5 × 16 × 16 + #3 × 16 + #8 × 1

{{< note >}}
Repara como agora já não temos 10, mas 16.
{{< /note >}}

Ora, como os números hexadecimais #1, #5, #3 e #8 são exactamente iguais aos números decimais 1, 5, 3 e 8, temos:
- 1 × 16 × 16 × 16 + 5 × 16 × 16 + 3 × 16 + 8 × 1

Agora é só fazer as contas, sabendo que 16 × 16 × 16 = 4096 e que 16 × 16 = 256:
- 1 × 4096 + 5 × 256 + 3 × 16 + 8 × 1
- 4096 + 1280 + 48 + 8
- 5432

Ou seja #1538 = 5432!

{{< note >}}
Repara como agora já não temos milhares, centenas e dezenas, mas sim… err… «milhares» hexadecimais que valem 4096, «centenas» hexadecimais que valem 256 e «dezenas» hexadecimais que valem 16. 
{{< /note >}}

Vamos ver outros exemplos. Lembras-te da cor café? Exacto, era representada por `rgb(111, 78, 55)`. Estes três números, representados em base 16, ou seja, em numeração hexadecimal, são #6F, #4E e #37. Vamos ver:
- #6F = #6 × 16 + #F × 1 = 6 × 16 + 15 × 1 = 96 + 15 = 111
- #4E = #4 × 16 + #E × 1 = 4 × 16 + 14 × 1 = 64 + 14 = 78
- #37 = #3 × 16 + #7 × 1 = 3 × 16 + 7 × 1 = 48 + 7 = 55

### Cores em hexadecimal no CSS

Então, e como se usam estes números hexadecimais em CSS? Basta pegar nos algarismos hexadecimais de cada valor R, G e B e contruir um único número grandão: `#6F4E37`. Experimenta o seguinte:

{{< code numbered="true" >}}
h1 {
  background-color: [[[#6F4E37]]];
}

[…]
{{< /code >}}

1. Repara como a representação hexadecimal no CSS é curtinha e compacta. Isto é exactamente o mesmo que `rgb(111, 78, 55)`, e por isso representa a cor café.

Vamos ver outro exemplo, o da cor malva. Esta cor é representada por `rgb(224, 176, 255)`. Estes três números, representados em base 16, ou seja, em numeração hexadecimal, são #E0, #B0 e #FF. Vamos ver:
- #E0 = #E × 16 + #0 × 1 = 14 × 16 + 0 × 1 = 224 + 0 = 224
- #B0 = #B × 16 + #0 × 1 = 11 × 16 + 0 × 1 = 176 + 0 = 176
- #FF = #F × 16 + #F × 1 = 15 × 16 + 15 × 1 = 240 + 15 = 255

Agora experimenta os seguintes valores no CSS:
- `#FF0000` = `rgb(255,   0,   0)` – Vermelho
- `#00FF00` = `rgb(  0, 255,   0)` – Verde
- `#0000FF` = `rgb(  0,   0, 255)` – Azul
- `#FFFF00` = `rgb(255, 255,   0)` – Amarelo
- `#FF00FF` = `rgb(255,   0, 255)` – Magenta
- `#00FFFF` = `rgb(  0, 255, 255)` – Ciano
- `#FFFFFF` = `rgb(255, 255, 255)` – Branco
- `#E0B0FF` = `rgb(224, 176, 255)` – Malva
- `#6F4E37` = `rgb(111,  78,  55)` – Café

Estas cores estão representadas na tabela abaixo, tanto usando o nome CSS (quando existe), como a notação hexadecimal e a função `rgb()`:
<style type="text/css">
  table {
    border: none;
    width: 100%;
  }
  td {
    border: 10px solid White;
    font-size: 12pt;
    text-align: center;
  }
</style>
<table >
  <tbody>
    <tr>
      <td style="text-align: right; width: 100px;"><strong>Vermelho:</strong></td>
      <td style="background-color: Red">Red</td>
      <td style="background-color: #FF0000">#FF0000</td>
      <td style="background-color: rgb(255, 0, 0)">rgb(255, 0, 0)</td>
    </tr>
    <tr>
      <td style="text-align: right; width: 100px;"><strong>Verde:</strong></td>
      <td style="background-color: Lime">Lime</td>
      <td style="background-color: #00FF00">#00FF00</td>
      <td style="background-color: rgb(0, 255, 0)">rgb(0, 255, 0)</td>
    </tr>
    <tr>
      <td style="text-align: right; width: 100px;"><strong>Azul:</strong></td>
      <td style="background-color: Blue">Blue</td>
      <td style="background-color: #0000FF">#0000FF</td>
      <td style="background-color: rgb(0, 0, 255)">rgb(0, 0, 255)</td>
    </tr>
    <tr>
      <td style="text-align: right; width: 100px;"><strong>Amarelo:</strong></td>
      <td style="background-color: Yellow">Yellow</td>
      <td style="background-color: #FFFF00">#FFFF00</td>
      <td style="background-color: rgb(255, 255, 0)">rgb(255, 255, 0)</td>
    </tr>
    <tr>
      <td style="text-align: right; width: 100px;"><strong>Magenta:</strong></td>
      <td style="background-color: Magenta">Magenta</td>
      <td style="background-color: #FF00FF">#FF00FF</td>
      <td style="background-color: rgb(255, 0, 255)">rgb(255, 0, 255)</td>
    </tr>
    <tr>
      <td style="text-align: right; width: 100px;"><strong>Ciano:</strong></td>
      <td style="background-color: Cyan">Cyan</td>
      <td style="background-color: #00FFFF">#00FFFF</td>
      <td style="background-color: rgb(0, 255, 255)">rgb(0, 255, 255)</td>
    </tr>
    <tr>
      <td style="text-align: right; width: 100px;"><strong>Malva:</strong></td>
      <td>-</td>
      <td style="background-color: #E0B0FF">#E0B0FF</td>
      <td style="background-color: rgb(224, 176, 255)">rgb(224, 176, 255)</td>
    </tr>
    <tr>
      <td style="text-align: right; width: 100px;"><strong>Café:</strong></td>
      <td>-</td>
      <td style="background-color: #6F4E37; color: White">#6F4E37</td>
      <td style="background-color: rgb(111, 78, 55); color: White">rgb(111, 78, 55)</td>
    </tr>
  </tbody>
</table>

{{< note >}}
Já viste com o verde do RGB se chama `Lime` em CSS? Estranho!
{{< /note >}}

Haveria muito mais a dizer sobre as cores, mas para já chega (e já é muito!).

Resta dizer-te que escolher cores é muito mais fácil do que parece. Experimenta estas ferramentas:
- [Selector de cores da Google](https://bit.ly/cdlx-color1)
- [Selector de cores de Dixon & Moe](https://bit.ly/cdlx-color2)
- [Selector de cores da MDN](https://bit.ly/cdlx-color3)

{{< note >}}
MDN significa *MDN Web Docs* (antes significava *Mozilla Developer Network*) e é um sítio web com imensos recursos para quem quer criar para a Web.
{{< /note >}}

{{< warning >}}
Não te esqueças de remover a regra <code>h1</code> com que estivemos a fazer experiências!
{{< /warning >}}

## Unidades de medida

Vamos fazer aqui um pequeno desvio, para falar de unidades. Abre a tua folha de estilos. Altera temporariamente a declaração do enchimento do corpo da página:

{{< code numbered="true" >}}
body {
  […]
  padding-left: [[[100px]]];
  […]
}

html {
  […]
}
{{< /code >}}

1. O que sucedeu? O conteúdo do corpo passou a ter um enchimento, que o separa da borda, de 100 `px`. O significado original de `px` era píxeis (os quadradinhos com as três cores R, G e B nos quais o teu ecrã se divide), mas acabou por evoluir, e hoje tem um significado mais fugidio. Algo como isto: «a unidade mais pequena representável no ecrã mais ainda claramente visível pelo olho humano». Experimenta com outros valores. Por exemplo, `0px`.

Agora experimenta as seguintes medidas:
- `25%` – Isto significa 25% (ou 1/4) da largura do elemento por fora do corpo do HTML (que é a página HTML).
- `10em` – Isto significa 10 × o tamanho da fonte que está a ser utilizado.

Brinca um pouco com diferentes valores.

{{< warning >}}
Não te esqueças de voltar a colocar <code>24px</code> o enchimento do corpo da página!
{{< /warning >}}

## Navegação

Este é o tema mais interessante desta lição. Dá uma olhada no teu sítio web.

Na página inicial, clica numa das ligações. Agora que estás muma outra página do teu sítio web, o que tens de fazer se quiseres ir para outra página? Exacto, tens de voltar atrás e repetir o processo. Chato. Quase todos os sítios web têm uma barra / menu de navegação. Aqui no sítio web do CoderDojo LX encontras um menu de navegação à esquerda. No caso do sítio web dos nanonautas, o que queremos é uma barra de navegação com bom aspecto, como a que podes ver nesta figura: 

{{< figure src="navegacao.png" title="Barra de navegação do sítio web dos Nanonautas." >}}

O aspecto global do sítio web seria o seguinte:

{{< figure src="sitio-web-com-navegacao.png" title="Sítio web dos Nanonautas com barra de navegação." >}}

### O elemento `NAV`

Em HTML, os elementos de navegação são colocados dentro de um elemento `NAV`. Vai à página `index.html`, copia a lista de ligações para outras páginas (inclui as etiquetas `<ul>` e `</ul>`) e coloca essa lista dentro de um elemento `NAV` (com equiquetas `<nav>` e `</nav>`) no início do corpo do documento HTML, ou seja, logo após `<body>`. Adiciona também à lista um novo item com uma ligação para a página inicial:

{{< code numbered="true" >}}
<!DOCTYPE html>

<html>
  […]
  <body>
    [[[<nav>]]]
      <ul>
        [[[<li><a href="index.html">Início</a></li>]]]
        <li><a href="sobre-nos.html">Sobre Nós</a></li>
        <li><a href="as-nossas-cancoes.html">As Nossas Canções</a></li>
        <li><a href="vejam-nos-tocar.html">Vejam-nos Tocar</a></li>
        <li><a href="dar-um-concerto.html">Dar um Concerto</a></li>
      </ul>
    [[[</nav>]]]
    <h1>Somos os Nanonautas!</h1>
    <p>Este é o nosso sítio web. Clique numa ligação para visitar uma página:</p>
    <ul>
      <li><a href="sobre-nos.html">Sobre Nós</a></li>
      <li><a href="as-nossas-cancoes.html">As Nossas Canções</a></li>
      <li><a href="vejam-nos-tocar.html">Vejam-nos Tocar</a></li>
      <li><a href="dar-um-concerto.html">Dar um Concerto</a></li>
    </ul>
  </body>
</html>
{{< /code >}}

1. Etiqueta de abertura do elemento `NAV`. Este elemento contém a lista / menu / barra de navegação. Neste momento é uma lista, como já dever ter visto (abre de novo o painel de visualização do sítio web, à direita, se necessário), mas vamos usar CSS para dar a esta lista o aspecto visual de uma barra.
2. Este novo item adiciona à lista de navegação uma ligação para a página inicial. Mas espera… não estamos na página inicial? Estamos, mas esta barra vai ser colocada nas restantes páginas, e é importante que tenha o mesmo aspecto em todas elas.
3. Etiqueta de fecho do elemento `NAV`.

{{< note >}}
Na realidade a barra de navegação poderia ter um aspecto diferente em cada página, deixando claro qual a página em que nos encontramos. Para já, porém, não faremos essa melhoria.
{{< /note >}}

Agora copia o elemento de navegação `NAV` que criaste (inclui as etiquetas `<nav>` e `</nav>`). Cola esse elemento no início do corpo do documento HTML, ou seja, logo após `<body>`, de cada uma das restantes páginas HTML: `sobre-nos.html`, `as-nossas-cancoes.html`, `vejam-nos-tocar.html` e `dar-um-concerto.html`.

Usa a nova navegação para passar de umas páginas para as outras. Muito mais conveniente, certo?

### Estilizando a barra de navegação

No final desta secção vais obter o resultado que podes ser neste projecto: [nanonautas-p41](https://nanonautas-p41.glitch.me/). Dá uma espreitadela. Vê cada uma das páginas. Confere a navegação.

Vamos então começar, mas aos poucos. No painel esquerdo do Glitch, clica em `css/minha-folha-de-estilo.html`. Adiciona as seguintes regras:

{{< code numbered="true" >}}
body { 
}

html {
}

[[[nav ul {
}]]]

[[[nav ul li {
}]]]

[[[nav ul li:last-child {
}]]]

[[[nav ul li a {
}]]]
{{< /code >}}

1. A primeira das novas regras tem o selector `nav ul`. Isso significa que se aplica apenas a elementos `UL` *aninhados* dentro de um elemento `NAV`. Porque não usar apenas `ul`? Porque uma dessas regras aplicar-se-ia a *todos* os `UL`, mesmo os que não fossem de navegação. E nós não queremos que isso aconteça: uma coisa é o aspecto geral das listas, outra é o aspecto das listas *de navegação*.
2. A segunda das novas regras tem o selector `nav ul li`. Isso significa que se aplica apenas a elementos `LI` *aninhados* dentro de um elemento `UL` que esteja por sua vez *aninhado* dentro de um elemento `NAV`. Porque não usar apenas `li`? Porque uma dessas regras aplicar-se-ia a *todos* os `LI`, mesmo os que não fossem itens de listas de navegação. E nós não queremos que isso aconteça: uma coisa é o aspecto geral dos itens das listas genéricas, outra é o aspecto dos itens das *listas de navegação*.
3. A terceira das novas regras tem o selector `nav ul li:last-child`. Este caso é idêntico ao anterior, mas com uma diferença importante: só se aplica *ao último item* da lista de navegação. O selector `:last-child` serve justamente para este fim.
4. A quarta das novas regras tem o selector `nav ul li a`. Isso significa que se aplica apenas a elementos `A` *aninhados* dentro de um elemento `LI` que esteja *aninhado* dentro de um elemento `UL` que esteja por sua vez *aninhado* dentro de um elemento `NAV`. Porque não usar apenas `a`? Porque uma dessas regras aplicar-se-ia a *todos* os `A`, mesmo os que não fossem ligações em itens de listas de navegação. E nós não queremos que isso aconteça: uma coisa é o aspecto geral das ligações, outra é o aspecto das ligações nos *itens das listas de navegação*.

Neste momento as quatro regras estão vazias, sem quaisquer declarações. Vamos introduzir as declarações aos poucos. À medida que introduzimos as declarações, vai observando o resultado no painel da direita. Faz também experiências com diferentes valores.

### O aspecto da lista de navegação

Vais alterar a regra que tem o selector `nav ul`. Isso significa que esta regra se aplica apenas a elementos `UL` *aninhados* dentro de um elemento `NAV`. Porque não usar apenas `ul`? Porque uma dessas regras aplicar-se-ia a *todos* os `UL`, mesmo os que não fossem de navegação. E nós não queremos que isso aconteça: uma coisa é o aspecto geral das listas, outra é o aspecto das listas *de navegação*.

{{< warning >}}
Não te esqueças de ir sempre observando o efeito de cada declaração que adicionares!
{{< /warning >}}

#### O estilo da lista

Acrescenta a seguinte declaração à regra com selector `nav ul`:

{{< code numbered="true" >}}
[…]

nav ul {
  [[[list-style-type: none;]]]
}

[…]
{{< /code >}}

1. Especifica que a lista não deve ser representada com nenhum símbolo ou prefixo antes de cada item. Neste caso, isso irá eliminar as bolas usuais da representação dos itens de um elemento `UL`.

#### A cor do fundo

Acrescenta a seguinte declaração à regra com selector `nav ul`:

{{< code numbered="true" >}}
[…]

nav ul {
  list-style-type: none;
  [[[background-color: #B577B5;]]]
}

[…]
{{< /code >}}

1. Especifica que o valor a usar para a propriedade `background-color` das listas de navegação, ou seja, a sua cor do fundo.

{{< note >}}
Se quiseres saber a que cor corresponde um número hexadecimal, usa a ferramenta <a href="https://www.color-hex.com/" target="_blank">color-hex</a>. Por exemplo, podes ver informação sobre a cor <a href="https://www.color-hex.com/color/b577b5" target="_blank">#B577B5</a>.
{{< /note >}}

#### A borda

Acrescenta as seguintes declarações, uma a uma, à regra com selector `nav ul`:

{{< code numbered="true" >}}
[…]

nav ul {
  list-style-type: none;
  background-color: #B577B5;
  [[[border: 4px solid #111111;]]]
  [[[border-radius: 10px;]]]
}

[…]
{{< /code >}}

1. Especifica a borda a usar para a lista de navegação: com 4 píxeis de espessura, contínua e cinzenta escura.
2. Especifica o raio de curvatura da borda da lista de navegação, para esta ficar arredondada.

#### O tipo de letra (ou fonte)

Acrescenta as seguintes declarações, uma a uma, à regra com selector `nav ul`:

{{< code numbered="true" >}}
[…]

nav ul {
  list-style-type: none;
  background-color: #B577B5;
  border: 4px solid #111111;
  border-radius: 10px;
  [[[font-family: sans-serif;]]]
  [[[font-weight: bold;]]]
}

[…]
{{< /code >}}

1. Especifica que o texto da lista de navegação deve usar um tipo de letra (ou fonte) sem serifas.
2. Indica que o peso (*weight*) do tipo de letra do texto da lista de navegação deve ser **negrito** (*bold*).

#### O enchimento

Acrescenta a seguinte declaração à regra com selector `nav ul`:

{{< code numbered="true" >}}
[…]

nav ul {
  list-style-type: none;
  background-color: #B577B5;
  border: 4px solid #111111;
  border-radius: 10px;
  font-family: sans-serif;
  font-weight: bold;
  [[[padding: 16px;]]]
}

[…]
{{< /code >}}

1. Especifica que o enchimento entre a borda e o conteúdo da lista de navegação deve ser de 16 píxeis de todos os lados.

### O aspecto dos itens da lista de navegação

Vais alterar a regra que tem o selector `nav ul li`. Isso significa que se aplica apenas a elementos `LI` *aninhados* dentro de um elemento `UL` que esteja por sua vez *aninhado* dentro de um elemento `NAV`. Porque não usar apenas `li`? Porque uma dessas regras aplicar-se-ia a *todos* os `LI`, mesmo os que não fossem itens de listas de navegação. E nós não queremos que isso aconteça: uma coisa é o aspecto geral dos itens das listas genéricas, outra é o aspecto dos itens das *listas de navegação*.

{{< warning >}}
Não te esqueças de ir sempre observando o efeito de cada declaração que adicionares!
{{< /warning >}}

#### A organização dos itens da lista

Acrescenta a seguinte declaração à regra com selector `nav ul li`:

{{< code numbered="true" >}}
[…]

nav ul li {
  [[[display: inline;]]]
}

[…]
{{< /code >}}

1. Especifica que os itens da lista não são dispostos como blocos sobrepostos, mas sim dispostos em linha, uns após os outros.

#### Uma linha vertical entre cada item da lista

Acrescenta a seguinte declaração à regra com selector `nav ul li`:

{{< code numbered="true" >}}
[…]

nav ul li {
  display: inline;
  [[[border-right: 2px solid #111111;]]]
}

[…]
{{< /code >}}

1. Especifica que os itens da lista devem, cada um deles, ter uma borda direita com 2 píxeis de espessura, contínua e com cor `#111111` (cinzendo escuro).

#### Enchimento de cada lado do conteúdo dos itens da lista

Acrescenta as seguintes declarações, uma por uma, à regra com selector `nav ul li`:

{{< code numbered="true" >}}
[…]

nav ul li {
  display: inline;
  border-right: 2px solid #111111;
  [[[padding-right: 8px;]]]
  [[[padding-left: 8px;]]]
}

[…]
{{< /code >}}

1. Especifica que os itens da lista devem ter um enchimento à direita, entre o conteúdo e a borda, de 8 píxeis de largura.
2. Especifica que os itens da lista devem ter um enchimento à esquerda, entre o conteúdo e a borda, de 8 píxeis de largura.

### O caso especial do último item da lista

Vais alterar a regra que tem o selector `nav ul li:last-child`. Isso significa que se aplica apenas *ao último* dos elementos `LI` *aninhados* dentro de um elemento `UL` que esteja por sua vez *aninhado* dentro de um elemento `NAV`. Esta regra vai servir para eliminar o traço vertical (borda direita) do último item da lista.

Acrescenta a seguinte declaração à regra com selector `nav ul li:last-child`:

{{< code numbered="true" >}}
[…]

nav ul li:last-child {
  [[[border-right: none;]]]
}

[…]
{{< /code >}}

1. Especifica que o último item da lista não tem borda direita.

### O aspecto das ligações nos itens da lista de navegação

Vais alterar a regra que tem o selector `nav ul li a`. Isso significa que se aplica apenas a elementos `A` *aninhados* dentro de um elemento `LI` que esteja *aninhado* dentro de um elemento `UL` que esteja por sua vez *aninhado* dentro de um elemento `NAV`. Porque não usar apenas `a`? Porque uma dessas regras aplicar-se-ia a *todos* os `A`, mesmo os que não fossem ligações em itens de listas de navegação. E nós não queremos que isso aconteça: uma coisa é o aspecto geral das ligações, outra é o aspecto das ligações nos *itens das listas de navegação*.

{{< warning >}}
Não te esqueças de ir sempre observando o efeito de cada declaração que adicionares!
{{< /warning >}}

Acrescenta a seguinte declaração à regra com selector `nav ul li a`:

{{< code numbered="true" >}}
[…]

nav ul li a {
  [[[text-decoration: none;]]]
  [[[color: #111111;]]]
}

[…]
{{< /code >}}

1. Especifica que as ligações nos itens da lista não devem ter qualquer «decoração», ou seja, que não devem surgir sublinhados, como é habitual acontecer com as ligações nas páginas HTML.
2. Especifica que o texto das ligações nos itens da lista deve ter cor `#111111` (cinzendo escuro).

## Dicas *top*

Supõe que queremos ter uma forma fácil de colocar, no texto das nossas páginas, dicas importantes. Gostaríamos que elas surgissem bem destacadas do restante texto. Eis o que desejamos:

{{< figure src="dicas-top.png" title="Aspecto das dicas top a criar." >}}

Infelizmente, o HTML não tem ideia o que sejam dicas (o mais parecido que tem são notas à margem, com o elemento `ASIDE`, que não se verá aqui). Como resolver o problema? Na realidade é muito fácil: basta usar definirmos uma classe chamada `dica-top` e usá-la num vulgar parágrafo (elemento `P`). Vamos ver o que isto é.

Abre a página HTML `dar-um-concerto.html`. Procura a lista de partes de instrumentos e acrescenta o seguinte parágrafo:

{{< code numbered="true" >}}
    […]
    <ul>
      <li>cordas de guitarra</li>
      <li>palhetas de saxofone e de clarinete</li>
      <li>baquetas de bateria</li>
    </ul>
    <p [[[class="dica-top"]]]>Se tocares uma nota errada ou te enganares, não pares de
    tocar – continua e finge que foi de propósito!</p>
    […]
{{< /code >}}

1. Nota como usámos o atributo `class` dos elementos HTML (neste caso num elemento `P`), dando-lhe o valor `dica-top`. Isso vai *classificar* o parágrafo como pertencendo à classe das dicas top.

No painel da direita, clica na ligação «Dar um Concerto». Procura o novo parágrafo. Tem algo que o distinga dos restantes parágrafos? Não tem nada, pois não? A questão é que não dissemos ainda como apresentar parágrafos da classe `dica-top`. Abre a tua folha de estilo e, no final, coloca o seguinte, inserindo as declarações uma por uma, e observando o resultado sempre que introduzires uma nova declaração:

{{< code numbered="true" >}}
[…]

[[[p.dica-top]]] {
  border: 4px solid #00AFEB;
  border-radius: 10px;
  padding: 16px;
  background-color: #C5EBFB;
}

[[[p.dica-top::before]]] {
  color: Black;
  [[[content: "DICA TOP: ";]]]
  font-weight: bold;
}
{{< /code >}}

1. Este selector aplica-se a elementos `P` (parágrafos). No entanto, como tem o selector `.dica-top`, só se aplica aos parágrafos dessa classe! Ou seja, não afecta os restantes parágrafos. A declarações dentro da regra são semelhantes a outras que já viste.
2. Este selector também só se aplica a elementos `P` da classe `dica-top`. Mas, tendo o selector `.before`, serve para especificar conteúdo especial que deve ser adicionado **antes** (*before*) do parágrafo. A propriedade `color` especifica a cor do texto e a propriedade `font-weight` especifica a força do tipo de letra a usar.
3. A propriedade `content` serve para especificar o conteúdo exacto a colocar antes das dicas *top*. Neste caso esse conteúdo é o texto «DICA TOP:»

Vai à página «Dar um Concerto» e vê a diferença.

E é isto! Navega um pouco pelo teu sítio web e aprecia-o. Nada mau, hein?

{{< note >}}
Confirma que o teu sítio web, e todas as suas páginas, se assemelham a <a href="https://nanonautas-p43.glitch.me" target="_blank">este projecto</a>. Se algo falhar, compara o teu projecto com o que podes encontrar <a href="https://glitch.com/~nanonautas-p43" target="_blank">aqui</a> (clica em «View Source»).
{{< /note >}}


<!--
{{< note >}}
Ligação seguinte: <a href="{{<relref "post/html-css2">}}">!!!!!!!!!!!!!</a>.
{{< /note >}}
-->