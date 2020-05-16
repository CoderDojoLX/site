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
Class Bola {
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
Class Bola {
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

## Creating the first ball

Now it's time to create an object of your class. Introduce the keyword `new` to them and provide useful analogies. Start by creating one instance of the class using `let bola;` before the `setup()` function. This ensures the variable is a global variable. Then in `setup()` instantiate the class using something like this:

```js
bola = new Bola(random(10, 40), width / 2, height / 2);
```

Now add the three functions that must be called in draw:

```js
// houve alguma colisão com as paredes?
bola.verificarParedes();
// salta, bola, salta!
bola.saltar(acel);
// desenhar a bola
bola.desenhar();
```

The code should run the same as last time. Some tweaks should be made in setup to preserve styles and colors.

## Manipulating arrays

Now it's time to move to arrays. Use JS syntax to create an array: `let bolas = [];` and replace the bolas declaration you had before. Now simply use the `push` function to append items to the array like so: `bolas.push(new Bola(random(10, 40), width/2, height/2));`.

To iterate over the balls, use a `for...of` loop like so:

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

That should be it!

## Final tweaks

You can implement many additional functions once you have the core idea going. Perhaps encourage them to play around, add new colors, user interaction, etc.

An implementation of spawning a new ball every time the mouse is pressed is shown below:

```js
function mousePressed() {
  bolas.push(new Bola(random(10, 40), mouseX, mouseY));
}
```
