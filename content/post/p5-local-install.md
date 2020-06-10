---
title: "Como instalar o p5 no teu ambiente local"
date: 2020-06-10T09:46:26+01:00
tags: ["tutorial", "p5"]
authors: ["Matias Silva"]
draft: false
---

Este tutorial ajuda-te a começar os teus projetos p5 no teu computador sem necessidade de recorrer a serviços como o Glitch. É muito útil para quando não tiveres Internet ou quiseres optar pela rapidez de correr tudo na tua máquina!

1. Instalar o [VS Code](https://code.visualstudio.com/) ou [Atom](https://atom.io/)

Precisas de um editor de texto para poderes programar.

2. Instalar o [node.js](https://nodejs.org/en/download/)

3. Instalar o [p5-manager](https://www.npmjs.com/package/p5-manager)

4. Entrar numa diretoria à tua escolha usando `cd` no terminal

4. Correr `p5 generate --bundle <nome do projeto>` no terminal

{{< note >}}
Não sabes o que é um terminal? Não gostas de o terminal do Windows? Recomendamos o Git Bash que podes [instalar aqui](https://git-scm.com/downloads).
{{< /note >}}

5. Agora precisas de um web server. Usa `python -m http.server 8000` para começar o teu server.

6. Acede ao teu novo projeto pondo `localhost:8000` no teu browser

7. Tenta mudar a cor do background, guarda, e faz refresh da pagina. 

Funcionou? Fixe! Se não, pergunta-nos no [canal Slack](https://join.slack.com/t/coderdojo-lx/shared_invite/zt-ehkglu7a-P6Xy_UiSQ4CKs48h83bidA), envia-nos um email, ou pergunta nas nossas sessões!