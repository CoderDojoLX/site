---
title: 'Página de início e muito mais CSS'
date: 2020-06-02T18:00:08+01:00
tags: ['html', 'css', 'programação web']
---

Nesta lição do percurso de aprendizagem [Programação web com HTML/CSS](/html-css) vamos aprender a criar uma página de início e vamos ver o CSS mais a fundo..

## Recursos

- **[Sessão #261 (HTML/CSS #2)]({{<ref "/post/sessions/session-261">}})** – Sessão do CoderDojo LX correspondente a esta secção.
- **[Apresentação da sessão #261 (HTML/CSS #2)](https://bit.ly/cdlx-html2)** – A apresentação usada nessa sessão.
- **[nanonautas-sessao2](https://glitch.com/~nanonautas-sessao2)** – Projecto com que podes começar esta lição. Também podes começar onde terminaste a ligação anterior.
– Os exemplos do livro correspondentes a esta sessão:
- **[nanonautas-p18](https://glitch.com/~nanonautas-p18)** – Projecto até à página 18 do livro.
- **[nanonautas-p22](https://glitch.com/~nanonautas-p22)** – Projecto até à página 22 do livro.
- **[nanonautas-p28](https://glitch.com/~nanonautas-p28)** – Projecto até à página 28 do livro.

## Mais uma página

Neste momento o sítio web dos Nanonautas tem já duas páginas web, `as-nossas-cancoes.html` e `sobre-nos.html`. Aqui vai a estrutura de pastas e arquivos neste momento:

{{< fileTree >}}
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
No painel direito (o de visualização do sítio web no editor do Glitch), clica sobre a página que acabaste de criar. A página é muito simples, por enquanto.

A estrutura de pastas e arquivos passou a ser:
{{< fileTree >}}
* css
  * minha-folha-de-estilo.css
* as-nossas-cancoes.html
* sobre-nos.html
* vejam-nos-tocar.html
{{< /fileTree >}}

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

Repara no que é novo aqui. As listas não numeradas, com os elementos `UL` e `LI` já tu conheces. O que é novo é o que está dentro dos itens da lista: ligações a outras páginas. Essas ligações recorrem a um novo elemento `A` (de *anchor*, ou âncora), com as respectivas etiquetas de abertura e fecho. Por exemplo,
```HTML
<a href="sobre-nos.html">Sobre Nós</a>
```

O elemento `A` tem duas partes muito importantes. A primeira é o seu conteúdo, ou seja, o que quer que se encontre entre as etiquetas de abertura e fecho. Esse conteúdo é o texto que vai poder ser clicado para ir para a página indicada pelo endereço. A segunda é esse endereço, que se indica como valor do atributo `href`. Como a página inicial está na mesma pasta (de raiz) do teu projecto, o endereço é simplesmente o nome do arquivo que guarda a página web a que nos queremos ligar.

Nota que o endereço pode ser um URL completo. Por exemplo, o código HTML
```HTML
<p>A <a href="https://pt.wikipedia.org/">Wikipédia</a> é fantástica!</p>
```
resulta no seguinte:

{{< blockquote >}}
<p>A <a href="https://pt.wikipedia.org/">Wikipédia</a> é fantástica!</p>
{{< /blockquote >}}

## 

{{< note >}}
Ligação seguinte: <a href="{{<relref "post/html-css2.md">}}">!!!!!!!!!!!!!</a>.
{{< /note >}}