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

Relembrar que na ultima sessão conseguimos recriar o "bouncing ball". Código de demonstração disponivel [aqui](https://glitch.com/edit/#!/bola-saltitante).

## What if we wanted to add more balls?

Ask the ninjas how they would go about adding more balls. Encourage independent thinking here. They should come to the realization that adding any further balls will be quite tedious...so we need a better solution.

## First steps to OOP

In the same file and below all the functions(it's best not to add your classes in a separate file to avoid confusion), use the JavaScript _Class_ syntax to create a basic class.

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

Make sure to explain to them the basic idea of a class (the blueprint) and how we can create instances of a class. Explain the constructor function and liken it to the existing code we have. Emphasize the connection between the code we have and the class, ie "we're not doing anything wildly different here, just wrapping our existing functions in fancy syntactical sugar".

## Porting the code

Now it's time to bring over the code you wrote last time. Add the variables in the constructor, and store them using `this.` syntax. Again, make sure to explain step-by-step what you are doing. It may not become fully apparent to them, but slowly they will start to understand. The idea is to show them the benefits that encapsulating your code brings.

Function-by-function, start to copy paste code into the blocks and encourage the use of comments.

The final class might look something like this:

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
