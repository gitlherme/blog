---
title: "Como mudar o texto de uma área ao focar em outra usando HTML e Javascript"
date: 2020-02-21T14:24:45-03:00
draft: false
---

Ao desenvolver a [calculadora freelancer](https://calculadorafreelancer.guilhermevieira.dev), eu comecei a tentar manipular alguns elementos de forma que eu ainda não tinha manipulado. E esse post aqui é pra mostrar como é fácil mudar o texto de um elemento ao focar em outro. Bora lá? 

<!--more-->

Pra gente manipular esses elementos, primeiros precisamos ter o HTML e linkar nosso javascript nele.

Crie uma pasta e dentro dela crie dois arquivos: `index.html` e `main.js`.

Deixe o `index.html` com o seguinte conteúdo.

```
  <html lang="pt-br">
    <head>
      <meta charset="UTF-8">
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
      <title>Document</title>
    </head>
    <body>
      <div id="elemento-mudado">
        Este é o texto que será mudado.
      </div>
      <input type="text" id="elemento-focado">
      <script src="main.js"></script>
    </body>
  </html>
```

Agora abra o `main.js` e vamos começar a fazer a mágica acontecer.

Vamos começar puxando do nosso arquivo HTML, os elementos que iremos usar pra fazer o manipulamento.

Adicione o seguinte bloco de código no seu arquivo .js
```
  let inputFoco = document.querySelector('#elemento-focado'),
      divContent = document.querySelector('#elemento-mudado')
```

Aqui iniciamos duas variáveis, e elas contém exatamente os elementos que serão manipulados durante o processo.

Após isso, precisamos criar uma função pra sempre que o elemento `<input>` receber um foco, mudar o conteúdo da nossa `<div>`.

```
inputFoco.addEventListener('focus', () => {
  let newContent = document.createTextNode('Texto a ser adicionado')
  divContent.appendChild(newContent)
  document.innerHTML = showResult
})
```

No bloco de código acima fizemos o seguinte: quando o elemento `<input>` receber o foco, criamos a variável `newContent`, e dentro dela criamos um nó com o [document.createTextNode](http://devfuria.com.br/javascript/dom-create-text-node/).

Na linha abaixo, adicionamos o nosso conteúdo na nossa `<div>` usando o [appendChild](https://developer.mozilla.org/pt-BR/docs/Web/API/Node/appendChild).

Por último, renderizamos nosso elemento no HTML, usando o [document.innerHTML](https://developer.mozilla.org/pt-BR/docs/Web/API/Element/innerHTML).

Então até o momento temos o seguinte cenário.

Nossa página está assim.
![img](https://res.cloudinary.com/gitlherme/image/upload/v1582310265/blog/manipulando-input/Screenshot_4_ndsjbn.png)

E ao clicar no input, ela fica da seguinte forma.
![img](https://res.cloudinary.com/gitlherme/image/upload/v1582310265/blog/manipulando-input/Screenshot_1_nnrbbb.png).

Muito bem, mas ao focarmos no `<input>` queremos que o texto seja trocado pelo novo, e não que apenas seja adicionado. Para isso, vamos criar uma função para que sempre que focarmos no elemento, antes de trocar o texto, seja removido o texto que existe nele.

Então, da nossa função que foi feita para adicionar o conteúdo, vamos criar a função `clearElement`.

```
function clearElement(element) {
  element.innerHTML = ""
}
```
Essa nossa função é bem simples e funciona da seguinte forma: ela recebe um elemento e limpa o conteúdo desse elemento no nosso HTML.

Feito isso, basta chamar essa função antes de adicionarmos o novo conteúdo. Volte ao `addEventListener` e o deixe da seguinte forma:

```

inputFoco.addEventListener('focus', () => {
  /* Adicionando a função para limpar abaixo */
  clearElement(divContent)
  /* Criando o novo conteúdo */
  let newContent = document.createTextNode('Texto a ser adicionado')
  divContent.appendChild(newContent)
  document.innerHTML = showResult
})
```

Agora, sempre que focarmos no elemento, vamos remover aquele texto que existia e colocar um novo no lugar.

Fácil, né? 😄

O resultado do que fizemos pode ser visto clicando [aqui](https://codepen.io/gitlherme/pen/dyoONvY).

Caso tenha alguma dúvida, pode me perguntar lá no [Twitter](https://twitter.com/gitlherme).

E por hoje é só. 💜