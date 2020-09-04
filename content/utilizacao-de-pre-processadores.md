---
title: "Utilizacao De Pré-processadores"
date: 2020-09-04T19:14:32-03:00
draft: false
---

O mundo do desenvolvimento vive em constante evolução. A cada dia que passa vimos um novo framework Javascript, novas tecnologias para desenvolvimento de todas as formas. E com o CSS não poderia ser diferente.

Os pré-processadores vieram pra ajudar no desenvolvimento dos nossos códigos de estilo. Com eles podemos otimizar muito o tempo que passamos criando códigos, devido as features que eles oferecem.

---

## O que é um pré-processador e como eles funcionam

Os pré processadores nada mais são do que interpretadores de código. Eles, basicamente, pegam sua configuração que foi feita num arquivo de pré-processamento e converte isso para arquivos `.css` , e dependendo da sua configuração, você pode até minificar esses arquivos automaticamente.

## As vantagens de se usar um pré-processador

Você pode estar pensando: "Cara, se eles só convertem o que eu fiz pra um arquivo `.css`, qual a vantagem de usá-los ao invés de só criar um arquivo CSS?"

E a resposta pra isso é que os pré-processadores nos trazem outros benefícios que nos ajudam no desenvolvimento do código, como por exemplo variáveis (essas já podem ser criadas por padrão no CSS, mas a forma que elas são declaradas nos pré-processadores costumam ser mais simples), funções, condicionais (if/else), laços de repetição (for/while) e algumas outras coisas que já estamos acostumados a ver no mundo da programação, mas que não funcionam nativamente no CSS.

### Certo, mas o que exatamente isso significa, como posso me aproveitar disso?

Pra entender um pouco melhor o "poder" que os pré-processadores, iremos criar dois exemplos abaixo, um utilizando CSS puro e outro utilizando o SASS, um dos pré-processadores mais utilizados no mercado.

> Vamos supor que você queira criar um pequeno sistema de grid, onde a cada número que você aumenta na classe, ele coloca um width maior pro seu elemento, começando com 100px e sempre adicionando mais 100px de acordo com a classe, algo como a imagem abaixo.

![](https://i.imgur.com/xNyCjU2.png)

Traduzindo esse código para CSS, ficaria algo parecido com isso 👇🏽

```css
.classe-1 {
  width: 100px;
  border: 1px solid red;
}

.classe-2 {
  width: 200px;
  border: 1px solid red;
}

.classe-3 {
  width: 300px;
  border: 1px solid red;
}

.classe-4 {
  width: 400px;
  border: 1px solid red;
}

.classe-5 {
  width: 500px;
  border: 1px solid red;
}
```

Certo, definimos as classes, e a cada número que a gente aumenta na classe, adicionamos 100px no width da classe.
Com o pré-processador, a gente pode se beneficiar de um laço de repetição, que faria a mesma coisa de forma bem mais simples. Algo como o bloco de código abaixo.

```scss
@for $i from 1 through 5 {
  .classe-#{$i} { 
        width: 100px * $i; 
        border: 1px solid red;
    }
}
```

Ou seja, economizamos muitas linhas de código, não precisamos ficar dando aquele CTRL + C e CTRL + V e ir mudando as coisas como é comum fazer no CSS, com um pequeno trecho de código podemos chegar no mesmo resultado.

## Como começar a utilizar um pré-processador

Para entendermos como começar a utilizar um pré-processador, iremos utilizar o [SASS](https://sass-lang.com/).

Para podermos utilizar o SASS, é recomendado que tenhamos o Node e o NPM instalados na nossa máquina. Você pode os instalar no site oficial do Node, clicando [aqui](https://nodejs.org/).

Para instalarmos na nossa máquina, basta rodarmos o comando `npm install -g sass` .

![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/947701c6-7b03-4582-8849-c630b93df909/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200904%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200904T221622Z&X-Amz-Expires=86400&X-Amz-Signature=b47a07ca10931e33eb2350d1de1ada263bb15ea672201a5bf49dff5d98efe7b1&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)

Após instalarmos, vamos criar um pequeno HTML para podermos explicar nosso estilo utilizando o SASS.

```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Iniciando com SASS</title>
	<link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="classe-1">Classe 1</div>
  <div class="classe-2">Classe 2</div>
  <div class="classe-3">Classe 3</div>
  <div class="classe-4">Classe 4</div>
  <div class="classe-5">Classe 5</div>
</body>
</html>
```

Vamos criar também um arquivo com a extensão .css e outro com a extensão .scss, a extensão do arquivo SASS. E no momento temos os três arquivos, como mostrado na imagem abaixo.

![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/3598465a-11e2-499a-a121-7f246ea42f4e/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200904%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200904T221712Z&X-Amz-Expires=86400&X-Amz-Signature=6414585037cad8e527713c503486619ba3b9df78074272f7b95d6bc4fc55174c&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)

Vamos replicar aquele código que colocamos mais acima, do for, para ver o SASS funcionando, então, dentro do arquivo ``style.scss`` adicionamos o seguinte código.

```scss
body {
  display: flex;
} /* Esse body servirá apenas para deixar os itens um ao lado do outro */

@for $i from 1 through 5 {
  .classe-#{$i} { 
        width: 100px * $i; 
        border: 1px solid red;
    }
}
```

Se formos visualizar nossa página no momento, ela ainda não sofreu nenhuma alteração.

![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/67ccef85-97a4-4e7f-bdf0-93456cc9b652/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200904%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200904T221738Z&X-Amz-Expires=86400&X-Amz-Signature=b5e7976710f88b41744b31202c2d3d56de013c13cfbdf6709763ad7e148a337a&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)

Isso acontece pois, o nosso arquivo CSS ainda está vazio, sem as alterações que fizemos no nosso arquivo SASS. Então vamos fazer com que as mudanças que fizemos no arquivo .scss seja refletido no arquivo .css. Para isso, rodaremos o seguinte comando: ``sass style.scss style.css``. Isso fará com que o SASS pegue todas as mudanças apontadas no primeiro arquivo (style.scss) e irá inserir no segundo arquivo (style.css).

E agora, se abrirmos nosso CSS, poderemos ver que todo o código foi gerado, exatamente da mesma forma que queríamos lá no começo.

![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/88bbe9b1-0a53-4ab6-9870-631e07ca7e8a/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200904%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200904T221801Z&X-Amz-Expires=86400&X-Amz-Signature=b4d66132df358ecadd27f97e8af3ff5904150fa8f3cfbb1843731dfb752fb6e8&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)

E se formos olhar no navegador, o resultado é o esperado.

![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/072b48f7-5c54-4f28-8db2-fd5ac6dceec7/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200904%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200904T221839Z&X-Amz-Expires=86400&X-Amz-Signature=6a035f426b38d8d55b2675542ae442af5a23b98d585e030a12f34031e45c9dc6&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)

E aí, o que achou? Acha que os pré-processadores realmente valem a pena no desenvolvimento? Qual sua opinião sobre isso?

Compartilhe nas redes e me marque usando o @gitlherme. 

E por hoje é só, espero que esse post de alguma forma possa ter sido útil pra você! 💙