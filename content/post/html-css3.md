---
title: 'Navegação, cores, medidas e mais selectores'
date: 2020-06-02T18:00:08+01:00
tags: ['html', 'css', 'programação web']
---

{{< warning >}}
Atenção! Esta página ainda está em desenvolvimento!
{{< /warning >}}

Páginas 30 a 41 do livro

Exemplos 34, 35, 41=35+NAV EM TODAS e 43.

CSS: Cores e medidas
Navegação
CSS: selectores com descendentes e ascendentes, classes

Conteúdos:

cores, selectores de cor, cores em hexadecimal, experiências em h1.
hexadecimal

medidas: px, em e %

Navegação
- Código HTML
- CSS: selectores mais complexos




Nesta lição do percurso de aprendizagem [Programação web com HTML/CSS](/html-css) vamos aprender a criar uma barra de navegação para o nosso sítio web e vamos aprender um pouco mais sobre folhas de estilo em CSS, incluindo como usar cores nas declarações, que unidades de medida se podem usar e como usar selectores mais sofisticados.

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

Este é o tema mais interessante desta lição. Dá uma olhada no teu sítio web. Na página inicial, clica numa das ligações. Agora que estás muma outra página do teu sítio web, o que tens de fazer se quiseres ir para outra página? Exacto, tens de voltar atrás e repetir o processo. Chato. Quase todos os sítios web têm uma barra / menu de navegação. Aqui no sítio web do CoderDojo LX encontras um menu de navegação à esquerda. No caso do sítio web dos nanonautas, o que queremos é uma barra de navegação com bom aspecto, como a que podes ver aqui: 



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
Ligação seguinte: <a href="{{<relref "post/html-css2">}}">!!!!!!!!!!!!!</a>.
{{< /note >}}
-->