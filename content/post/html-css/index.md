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

Há aqui algumas palavras meio esquisitas. Um exemplo é *[protocolo](https://www.wikiwand.com/pt/Protocolo_(ci%C3%AAncia_da_computa%C3%A7%C3%A3o))*. Simplificando muito, um protocolo é um conjunto de regras ou convenções que permite que tudo corra bem, isto é que a comunicação entre dois computadores aconteça. Os protocolos são importantes não apenas na diplomacia, mas também na comunicação entre computadores! Já reparaste que os endereços web começam todos com `http` ou `https`? Isso indica ao navegador que o protocolo a usar para comunicar com o computador (a que se chama *servidor*) onde se encontra o recurso (por exemplo, uma página web) é o [HTTP](https://www.wikiwand.com/pt/Hypertext_Transfer_Protocol) (Hypertext Transfer Protocol). A versão com um «s» no fim significa que se usa uma combinação do HTTP com outro protolo (chamado TLS) que garante que a comunicação é segura, ou seja, que ninguém que intercepte a comunicação conseguirá fazer cabo-e-rabo do que está a ser comunicado.

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

