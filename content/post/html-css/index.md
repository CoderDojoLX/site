---
title: 'Programação web com HTML/CSS'
date: 2020-05-31T18:00:08+01:00
tags: ['html', 'css', 'programação web']
---

Vamos programar para a web com o HTML/CSS! Constrói o teu próprio sítio web aprendendo HTML/CSS à medida que constróis o sítio web dos Nanonautas!

## Introdução

### Livro

Neste percurso de aprendizagem vamos seguir o livro [Criar com Código: Constrói o teu Sítio Web](http://www.planeta.pt/livro/criar-com-constroi-o-teu-sitio-web), de Clyde Hatter, editado pela Planeta. O livro pertence à colecção CoderDojo Nano que é promovida pela Fundação CoderDojo. Não deixes de ver [a página web de apoio ao livro](http://nanonautas.pt/).

### Sessões

Este percurso de aprendizagem foi seguido ao longo de algumas das nossas sessões remotas. Aqui vão elas:
- [Sessão #259 (HTML/CSS #1)]({{<ref "/post/sessions/session-259">}})
- [Sessão #261 (HTML/CSS #2)]({{<ref "/post/sessions/session-261">}})

Alguns dos materiais sugeridos abaixo correspondem a estas sessões. Mas não precisas de ter participado nas sessões para seguir este percurso de aprendizagem!

### Glitch

Nesta sequência aconselhamos-te a usar o [Glitch](https://glitch.com/). Se tens pelo menos 13 anos e ainda não tens conta no Glitch, cria já uma! Se tens menos de 13 anos, pede ajuda ao teu encarregado de educação.

Criámos no Glitch uma colecção onde encontras vários projecto de arranque ou os exemplos do sítio web dos Nanonautas correspondentes às várias páginas do livro. A colecção chama-se [Exemplos das sessões HTML/CSS: Programação Web](https://glitch.com/@cdlx/exemplos-das-sessoes-html-css-programacao-web). 

Os projectos de arranque são:
- [nanonautas-começa-aqui](https://glitch.com/~nanonautas-comeca-aqui) – Projecto com que deves começar este percurso de aprendizagem e que foi usado na sessão #259 (HTML/CSS #1).
- [nanonautas-sessao2](https://glitch.com/~nanonautas-sessao2) – Projecto com que podes começar a sessão #261 (HTML/CSS #2).

Os exemplos do livro são:
- [nanonautas-p8](https://glitch.com/~nanonautas-p8) – Sítio até à página 8 do livro.
- [nanonautas-p10](https://glitch.com/~nanonautas-p10) – Sítio até à página 10 do livro.
- [nanonautas-p13](https://glitch.com/~nanonautas-p13) – Sítio até à página 13 do livro.
- [nanonautas-p16](https://glitch.com/~nanonautas-p16) – Sítio até à página 16 do livro.
- [nanonautas-p18](https://glitch.com/~nanonautas-p18) – Sítio até à página 18 do livro.
- [nanonautas-p22](https://glitch.com/~nanonautas-p22) – Sítio até à página 22 do livro.
- [nanonautas-p28](https://glitch.com/~nanonautas-p28) – Sítio até à página 28 do livro.

Tens também o projecto que resultou da sessão #261 (HTML/CSS #2):
- [nanonautas-sessao2-final](https://glitch.com/~nanonautas-sessao2-final) – Projecto feito ao longo da sessão #261 (HTML/CSS #2).

Lembra-te que, à medida que segues na tua aprendizagem ou que lês o livro, podes ir conferindo o que fores fazendo com estes exemplos.

### Apresentações

Fomos preparando várias apresentações para cada uma das sessões que realizámos remotamente sobre este percurso de aprendizagem. Talvez aches útil vê-las! Estão aqui:
- [Apresentação da sessão #259 (HTML/CSS #1)](https://bit.ly/cdlx-html1)
- [Apresentação da sessão #261 (HTML/CSS #2)](https://bit.ly/cdlx-html2)

## A Internet, a Web, páginas, sítios e endereços

Vamos começar por definir alguns conceitos, com ajuda da nossa amiga [Wikipédia](https://pt.wikipedia.org/):

**[Internet](https://www.wikiwand.com/pt/Internet)** – Sistema global de redes de computadores interligadas que usam um conjunto próprio de *protocolos* chamado Internet Protocol Suite ou TCP/IP e tem como objectivo servir cada vez mais utilizadores no mundo inteiro.

**[Web ou World Wide Web](https://www.wikiwand.com/pt/World_Wide_Web)** – Sistema de documentos de vários tipos (texto, imagens, vídeos, sons, etc.), muitos deles **hipetexto**, interligados e acessíveis na Internet.

**[Sítio web](https://www.wikiwand.com/pt/S%C3%ADtio_eletr%C3%B3nico)** – Conjunto de **páginas web** relacionadas disponíveis num mesmo *nome de domínio*, por exemplo o [sítio web dos Nanonautas](https://nanonautas-final.glitch.me/) (que é onde chegaremos no final deste percurso de aprendizagem).

**[Página web](https://www.wikiwand.com/pt/P%C3%A1gina_web)** – Um documento ou recurso em **hipertexto** disponível na Web a que se pode aceder usando um navegador e que tem um dado endereço, ou melhor, um dado **URL**.

**[Hipertexto](https://www.wikiwand.com/pt/Hipertexto)** – Documento com ligações (mais precisamente, hiperligações) a outros documentos ou recursos.

**[URL](https://www.wikiwand.com/pt/URL)** – Localizador de um recurso na web, usualmente uma página web. Aos URL também se chama muitas vezes endereços web ou simplemente endereços. Por exemplo, o endereço da sítio web dos Nanonautas é dado por este URL: `https://nanonautas-final.glitch.me/`

Há aqui algumas palavras meio esquisitas. Um exemplo é *[protocolo](https://www.wikiwand.com/pt/Protocolo_(ci%C3%AAncia_da_computa%C3%A7%C3%A3o))*. Simplificando muito, um protocolo é um conjunto de regras ou convenções que permite que tudo corra bem, isto é que a comunicação entre dois computadores aconteça. Os protocolos são importantes não apenas na diplomacia, mas também na comunicação entre computadores! Já reparaste que os endereços web começam todos com `http` ou `https`? Isso indica ao navegador que o protocolo a usar para comunicar com o computador (a que se chama *servidor*) onde se encontra o recurso (por exemplo, uma página web) é o [HTTP](https://www.wikiwand.com/pt/Hypertext_Transfer_Protocol) (*hypertext transfer protocol* ou protoloco de transferência de hipertexto). A versão com um «s» no fim significa que se usa uma combinação do HTTP com outro protolo (chamado TLS) que garante que a comunicação é segura, ou seja, que ninguém que intercepte a comunicação conseguirá fazer cabo-e-rabo do que está a ser comunicado.

Outro exemplo é a palavra *[nome de domínio](https://www.wikiwand.com/pt/Nome_de_dom%C3%ADnio)*. Os nomes de domínio são usados para dar nomes a conjuntos relacionados de computadores. Por exemplo, `coderdojo-lx.pt` é o nome de domínio do CoderDojo LX. Um outro nome de domínio do CoderDojo LX é `www.coderdojo-lx.pt`, que é onde se encontra o [sítio web do CoderDojo LX](https://www.coderdojo-lx.pt/).

Reparaste no exemplo que demos mais acima, do [sítio web dos Nanonautas](https://nanonautas-final.glitch.me/)? Explora-o bem. Vê se consegues:

- Identificar todas as páginas web do sítio.
- Perceber qual o endereço de cada uma dessas páginas.

Quantas páginas são? Cada uma tem o seu próprio endereço (URL), não é? Ou quase… Deste conta que há dois endereços que resultam na mesma página? Pois é, veremos isso mais tarde, mas a verdade é que os dois endereços `https://nanonautas-final.glitch.me/` e `https://nanonautas-final.glitch.me/index.html` correspondem à mesma página, que é a página inicial do sítio web dos Nanonautas.

Reparaste também que os endereços terminam todos em `.html`? Vamos ver isso a seguir.

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

Os Nanonautas previsam de um novo sítio web. Puseram-se a pensar e chegaram às seguintes ideias para o sítio:

- Dizer onde será o próximo concerto
- Anunciar CD e t-shirt
- Ligações para vídeos nossos no YouTube
- Conselhos sobre compra e manutenção de instrumentos
- Conselhos sobre ensaiar sem irritar vizinhos

Tentaram organizar as ideias e chegaram à seguinte estrutura com cinco páginas web:

- **Início** – Página com ligações para as seguintes páginas:
  - **Sobre nós** – Página com o seguinte conteúdo:
    - Informação sobre a nossa banda
    - O nosso novo CD
    – Comprem a nossa t-shirt
  - **As nossas canções** – Página com o seguinte conteúdo:
    - Informação sobre as nossas canções
    - Vídeos
  - **Vejam-nos tocar** – Página com o seguinte conteúdo:
    - Onde nos podem ver tocar
	- Próximos concertos
  - **Dar um concerto** – Página com o seguinte conteúdo:
    - Como dar um concerto
    - Dicas top

Para ter uma ideia mais precisa do que eles pensaram, dá de novo uma olhada no [sítio web final dos Nanonautas](https://nanonautas-final.glitch.me/). A ideia é ires desenvolvendo ao pouco o sítio web dos nanonautas até ele ter o mesmo aspecto e conteúdo que viste.

## Vamos começar!

### O que precisas

- Descarrega o [ZIP de imagens](https://bit.ly/cdlx-nanonautas-imagens). Nota bem que há um botão para descarregar a imagem no canto superior direito.
- Descomprime o arquivo `imagens.zip` que descarregaste. Não te limites a abri-lo: tenta descomprimi-lo mesmo.
- Se ainda não tens conta no [Glitch](https://glitch.com/), então:
  - Se tens pelo menos 13 anos, podes criar tu mesmo uma conta.
  - Se tiveres menos de 13 anos, pede ajuda a um encarregado de educação.
- Vai para a [página da equipa CoderDojo LX](https://glitch.com/@cdlx) no Glitch.
- Abre o projecto `nanonautas-comeca-aqui`. Se não o encontrares, [clica aqui](https://glitch.com/~nanonautas-comeca-aqui).
- Remistura o projecto, carregando no botão «Remix This», que encontras no canto inferior direito. Remisturar é fazer uma cópia tua do projecto, para o poderes alterar à vontade.

### O teu novo projecto

Tens à tua frente o teu novo projecto! Neste momento só tem uma página web, que podes ver do lado esquerdo. Essa página está guardada num arquivo (ou ficheiro) chamado `sobre-nos.html`. Clica sobre ele, para veres o seu conteúdo à direita, no editor. Verás que o conteúdo é simplesmente
```
Isto não é HTML!
```
Procura o menu «Show» e escolhe «Next to The Code». Abrir-se-á uma janela que mostra o conteúdo do teu sítio web. Como ainda só tens uma página, verás lá listado o arquivo `sobre-nos.html`. Clica sobre ele para o veres na web.

Que achas? Pouco entusiasmente, não é? Espera, as coisas vão melhorar, não tarda.

## Páginas HTML

Reparaste no nome do ficheiro? Ele termina na extensão `.html`. Embora o teu navegador não ligue muito a essa extensão, ela ajuda-nos a perceber que se trata de uma página web no formato [HTML](https://www.wikiwand.com/pt/HTML) (*hypertext markup language* ou linguagem de marcação para hipertexto). O HTML é uma linguagem que permite representar e compor o conteúdo das páginas web, e é um dos principais temas em aprendizagem aqui. O HTML forma um trio com o [CSS](https://www.wikiwand.com/pt/Cascading_Style_Sheets) (*cascading style sheets* ou folhas de estilo em cascata), usadas para controlar o estilo ou aspecto das páginas web, e com o [JavaScript](https://www.wikiwand.com/pt/JavaScript), uma linguagem de programação que permite criar páginas web dinâmicas. Em conjunto, o HTML, o CSS e o JavaScript permitem criar páginas web fantásticas!

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

Reparaste certamente que o HTML tem montes de `<` e `>`. A ideia é que estes caracteres funcionam como *parênteses agudos* que envolvem aquilo a que se chama *etiquetas*.

A primeira etiqueta é especial. Ela deve ser colocada na linha inicial de todas as páginas web e indica claramente ao navegador que as vai mostrar que o seu conteúdo… é HTML! Isso mesmo, a etiqueta especial
```HTML
<!DOCTYPE html>
```
indica que se trata de HTML. Só depois dessa primeira linha com a etiqueta especial que vimos é que começa o HTML propriamente dito.

### Principais elementos de uma página web

A primeira etiqueta HTML que encontras é `<html>`. Grande parte das etiquetas HTML tem uma etiqueta de abertura, tal como `<html>`, e uma etiqueta de fecho, que é muito semelhante à etiqueta de abertura, mas tem uma `/` após o parênteses agudo esquerdo, tal como `</html>`. Cada etiqueta tem também um *nome* que identifica o *elemento* HTML que está em causa. Entre as etiquetas de abertura e fecho encontra-se o *conteúdo* do elemento.

Em resumo:

- `<html>` – Etiqueta de abertura do elemento `HTML`.
- `</html>` – Etiqueta de fecho do elemento `HTML`.
- Entre `<html>` e `</html>` – Conteúdo do elemento `HTML`.

Mas afinal, o que é o elemento `HTML`? O elemento `HTML` identifica todo o conteúdo da página web. Por isso é que todo o resto da nossa página web é parte do conteúdo deste elemento. O elemento `HTML` contém dois outros elementos (`HEAD` e `BODY`), cada um identificado pelas respectivas etiquetas:

- Elemento `HEAD` – Identificado pelas etiquetas `<head>` e `</head>`, este elemento funciona como um cabeçalho do documento, sendo o seu conteúdo informação que se aplica à página web como um todo.
- Elemento `BODY` – Identificado pelas etiquetas `<body>` e `</body>`, este elemento funciona como corpo do documento, ou seja, o seu conteúdo é onde se coloca o conteúdo da página web, que é aquilo que se vê quando navegas para essa página.

## Alguns outros elementos fundamentais

Tanto o cabeçalho como o corpo do nosso !!!!!


## HTML: Conteúdo *estruturado* da página web

É importante que percebas que o que escreves em HTML corresponde ao *conteúdo estruturado* das tuas páginas web. O HTML não especifica o *aspecto* das tuas páginas. Isso será o papel do CSS, que veremos em breve. Esta divisão é muitíssimo importante:

- Permite-te concentrares-te no conteúdo do documento quando escreves HTML
- Permite-te usar o CSS para controlares o aspecto das tuas páginas de forma coerente: um só ficheiro CSS permite-te controlar o aspecto de *todas* as páginas do teu sítio web!


