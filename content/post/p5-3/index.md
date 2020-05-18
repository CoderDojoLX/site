---
title: 'Sessão 3: p5.js@Glitch'
date: 2020-05-16T13:22:08+01:00
tags: ['p5', 'sessao-remota']
---

Guia para mentores e interessados para a Sessão #3 de p5.js (programação criativa).

> [Código de demonstração (guia) para a sessão](https://glitch.com/edit/#!/bola-saltitante-oop)

{{< note >}}
Já te certificaste que tens permissão para editar os ficheiros de todos os ninjas?
{{< /note >}}

## Recapitular o progresso

Relembrar que na última sessão conseguimos recriar o «bouncing ball». Código de demonstração disponível [aqui](https://glitch.com/edit/#!/bola-saltitante).

## E se quisermos adicionar mais bolas?

Pergunte aos ninjas com poderiam adicionar mais bolas. Encoraje pensamento independente, neste momento. Eles devem chegar à conclusão que adicionar mais bolas é muito moroso e entediante… por isso precisamos de uma melhor solução.

## Primeiros passos na POO

No mesmo ficheiro e abaixo de todas as funções (é melhor não colocar as classes em arquivos separados para evitar confusão), use a sintaxe de _Class_ para criar uma classe básica.

```js
class Bola {
    constructor(raio, x, y){

    }

    saltar(){

    }

    verificarParedes(){

    }

    desenhar(){

    }
}
```

Assegure-se de explicar a ideia básica de uma classe (um modelo ou plano) e como se podem criar instâncias de uma classe. Explicar a função de construção (construtor) e mostrar como se assemelha ao código já existente. Emfatisar a ligação entre o código que temos e a classe, i.e., «não estamos a fazer nada de muito diferente do que já fizemos, estamos só a embrulhar as funções existentes numa nova sintaxe simpática, um pouco de «açúcar» sintático.

## Transportar o código

Agora está na altura de ir buscar o código que escrevemos da última vez. Adicione as variáveis no construtor e inicialize-as usando a sintaxe `this.`. De novo, assegure-se de explicar passo a passo o que está a fazer. Pode não ser totalmente claro para eles, mas aos poucos irão percebendo. A ideia é mostrar-lhes os benefícios trazidos por encapsularmos o nosso código.

Função a função, comece a cortar e colar o código para os blocos e encoraje a utilazação de comentários.

A classe final poderá assemelhar-se ao seguinte:

```js
class Bola {
  constructor(raio, x, y) {
    this.raio = raio;
    this.x = x;
    this.y = y;
    this.vel = random(2, 6);
    this.cor = color(random(60, 255), random(60, 255), random(60, 255));
  }

  saltar(acel) {
    // adicionar o efeito da gravidade
    this.vel += acel;
    // adicionar a velocidade à posição
    this.y += this.vel;
  }

  verificarParedes() {
    // verificar se o y não excede
    if (this.y + this.raio > height) {
      this.y = height - this.raio;
      this.vel *= -1;
    }
  }

  desenhar() {
    fill(this.cor);
    circle(this.x, this.y, this.raio * 2);
  }
}
```

## Criando a primeira bola

Agora é altura de criar um objecto (uma «instância») da classe. Apresente-lhes a palavra-chave `new` e faça analogias úteis. Comece por criar uma variável para guardar a instância da classe usando `let bola;` antes da função `setup()`. Isto garante que a variável é global. Depois, na função `setup()`, instancie a classe usando algo com o seguinte:

```js
bola = new Bola(random(10, 40), width / 2, height / 2);
```

Agora adicione as três funções (ou «métodos») que devem ser invocadas na função `draw()`:

```js
// houve alguma colisão com as paredes?
bola.verificarParedes();
// salta, bola, salta!
bola.saltar(acel);
// desenhar a bola
bola.desenhar();
```

O código deve funcionar tal como antes. Deve-se fazer alguns ajuste na função `setup()` para preservar estilos e cores.

## Manipulando *arrays*

Vamos avançar para os *arrays*. Use a syntaxe JavaScript para criar um *array* `let bolas = [];`, substituindo a declaração de `bola` já existente. Agora use simplesmente a função `push()` para acrescentar itens ao *array*: `bolas.push(new Bola(random(10, 40), width/2, height/2));`.

Para percorrer as bolas (ou «iterar» ao longo do *array*), use um ciclo `for...of`:

```js
for (bola of bolas) {
  // houve alguma colisão com as paredes?
  bola.verificarParedes();
  // salta, bola, salta!
  bola.saltar(acel);
  // desenhar a bola
  bola.desenhar();
}
```

E é isto!

## Ajustes finais

Pode implementar funções adicionais assim que a ideia principal já esteja a funcionar. Talvez seja boa ideia encorajá-los a brincar um pouco, adicionando cores, interacção com o utilizador, etc.

Uma implementação fazendo nascer uma nova bola sob o ponteiro do rato sempre que se clica nele é a seguinte:

```js
function mousePressed() {
  bolas.push(new Bola(random(10, 40), mouseX, mouseY));
}
```
