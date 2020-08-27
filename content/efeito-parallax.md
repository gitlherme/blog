---
title: "Como adicionar o efeito parallax em suas páginas da forma mais simples possível"
date: 2018-09-23T16:56:49-03:00

#thumbnailImage: //example.com/image.jpg
---
O efeito parallax é algo bem comum nos dias de hoje. Você consegue perceber a presença deles nos mais diversos sites que você acessa. Mas, afinal, o que é esse tal parallax?
<!--more-->
O parallax é bem recorrente em sites one-page, ou seja, sites com uma só pagina, e serve para dar aquela sensação de profundidade na interface.

Sem mais enrolação, mãos ao código!

Bom, para iniciar criei uma tela simples, com 4 sections, colocando um pouco de conteúdo em cada uma delas, só para podermos fazer o efeito de uma forma mais legal, simulando uma one-page.

Na primeira section, adicionei a class "parallax" e é nela onde aplicaremos o efeito.

![](https://miro.medium.com/max/30/1*oCsiOrFRgMh-nUzEAzkWXw.jpeg?q=20)

![](https://miro.medium.com/max/700/1*oCsiOrFRgMh-nUzEAzkWXw.jpeg)

Agora, no arquivo .css, defini alguns paddings, apenas para dar uma distância maior entre um conteúdo e outro, além de dar um text-align: center, para centralizar horizontalmente nosso conteúdo dentro da section com a class "parallax".

![](https://miro.medium.com/max/30/1*rNectk9mi7ojmr7f8rm_oQ.jpeg?q=20)

![](https://miro.medium.com/max/700/1*rNectk9mi7ojmr7f8rm_oQ.jpeg)

Até agora, temos algo parecido com isso.

![](https://miro.medium.com/max/30/1*3MnBEaY_KmoMdfJwI-ZHlg.jpeg?q=20)

![](https://miro.medium.com/max/700/1*3MnBEaY_KmoMdfJwI-ZHlg.jpeg)

Agora vamos para a parte onde a mágica acontece!!!

![](https://miro.medium.com/max/30/1*tq9SGC3-o6B_0V82nbezuQ.jpeg?q=20)

![](https://miro.medium.com/max/700/1*tq9SGC3-o6B_0V82nbezuQ.jpeg)

Primeiramente, adicionei um background a section parallax. Neste caso usei essa imagem aqui (<https://unsplash.com/photos/AMssSjUaTY4>), depois disso, coloquei um background-repeat: no repeat, para que o nosso background não ficasse se repetindo, independentemente do tamanho da imagem.

E agora, com apenas duas propriedades, damos o efeito parallax completo a nossa página.

Usando o background-size: cover, definimos que a imagem de fundo se ajuste o mais largamente possível mantendo a proporção.

Por último, mas de forma alguma menos importante, coloquei o background-attachment: fixed, pois é ele que faz com que o background não role junto com a página, dando o tão desejado efeito parallax à ela. Nossa página com o efeito parallax está pronta!

![](https://miro.medium.com/max/30/1*kV21IuqseLq2Zj0Cz3OIgA.jpeg?q=20)

![](https://miro.medium.com/max/700/1*kV21IuqseLq2Zj0Cz3OIgA.jpeg)

Para ver esse efeito funcionando, você pode acessar: <http://gitlherme.github.io/tutoriais/efeito-parallax>