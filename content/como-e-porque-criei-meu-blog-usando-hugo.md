---
title: "Como e porque criei meu blog usando Hugo"
date: 2019-08-06T13:13:50-03:00
#thumbnailImage: //example.com/image.jpg
---

Quando quis começar a compartilhar o pouco conhecimento que tenho, comecei a pensar em N alternativas diferentes. YouTube? Não parece minha vocação. Palestras? Talvez. Mas a conclusão na qual cheguei foi: vou criar um blog.

<!--more-->

> Mas por que criar um blog?

 Para mim, criar um blog, escrever posts, técnicos ou não, faz com que você, além de compartilhar conhecimento, também tenha uma forma de revisar tudo que você tem aprendido, e não tenha que sair pesquisando em um milhão de lugares para encontrar aquele post que iria te ajudar. E além de tudo isso, ainda é uma forma de você aumentar seu portfólio 🤩

> E porque criar um blog inteirinho e não usar uma plataforma pra isso (Medium, [Dev.to](http://dev.to))?

As plataformas para blog são realmente super legais, e eu comecei usando elas. Tanto que tenho posts no [Medium](http://medium.com/@gitlherme) e no [Dev.to](http://dev.to/gitlherme).

Porém eu sentia falta de algo MEU, onde eu pudesse ter total liberdade em escrever o que eu quisesse, usando a licença que eu quisesse, e principalmente, com o layout que eu achasse mais legal (frescura de front-end AHUEHAUE).

Então comecei a pesquisar, e no blog do [William Oliveira](http://woliveiras.com.br) eu conheci a [JAM Stack](https://woliveiras.com.br/posts/jamstack-introdu%C3%A7%C3%A3o-o-que-%C3%A9-jamstack/).

 Hoje em dia, com os geradores de sites estáticos como o [Jekyll](https://jekyllrb.com/) ou o [Hugo](https://gohugo.io/) (que foi o que eu fiz), você consegue criar um blog inteirinho, em menos de 5 minutos (é sério!).

E pra provar que eu não estou mentindo, vou mostrar de forma simples, como é rápido você criar o seu blog, de uma forma legal, usando o Hugo.

Primeiramente, precisamos ter o Hugo instalado no nosso sistema operacional, para isso, consulte  [este link](https://gohugo.io/getting-started/installing/).

Após isso, entre na pasta onde você deseja começar o seu blog, no nosso exemplo, vamos usar  uma pasta chamada "**blog**" que está dentro do Desktop.

Usando o comando `hugo new site blog` (e note que aqui você deve mudar o caminho de acordo com a sua pasta), nós criamos toda a estrutura de pastas que serão usadas no nosso site.

![](https://res.cloudinary.com/gitlherme/image/upload/v1565108321/blog/como-e-porque-criei-meu-blog-usando-hugo/Screenshot_2_w6c5gv.png)

Após isso, precisamos escolher um tema legal, você pode conferir todos eles  [aqui](https://themes.gohugo.io) , no meu caso eu usei o  [Hugo Tranquilpeak Theme](https://themes.gohugo.io/hugo-tranquilpeak-theme/).

Depois de escolhermos o tema, devemos instalar ele no nosso blog, para isso, precisamos ter o  [Git](https://git-scm.com/) instalado.

Com o Git instalado, nós entramos na pasta **themes** e executamos o comando `git clone`.

![](https://res.cloudinary.com/gitlherme/image/upload/v1565108321/blog/como-e-porque-criei-meu-blog-usando-hugo/Screenshot_1_hiznnt.png)

O último passo, é entrar no arquivo **config.toml **e definir que o tema que será usado é exatamente esse que baixamos.

![](https://res.cloudinary.com/gitlherme/image/upload/v1565108321/blog/como-e-porque-criei-meu-blog-usando-hugo/Screenshot_3_qlsjsu.png)

É legal ter em mente que alguns temas tem um site de exemplo dentro da sua própria pasta, assim você consegue visualizar como configurar o tema da melhor forma possível 😄.

Agora, para visualizarmos tudo que fizemos, usamos o comando `hugo server`.

![](https://res.cloudinary.com/gitlherme/image/upload/v1565112484/blog/como-e-porque-criei-meu-blog-usando-hugo/Screenshot_5_rxbklg.png)

Agora, basta entrarmos em _http://localhost:1313_ e lá está o nosso blog.

![](https://res.cloudinary.com/gitlherme/image/upload/v1565108322/blog/como-e-porque-criei-meu-blog-usando-hugo/Screenshot_4_wvx5wn.png)

Claro que essa é uma explicação super por cima, só quis mostrar quão fácil é gerar um site estático usando o Hugo. Caso você tenha se interessado em criar um blog dessa forma, pode dar uma olhada no tutorial do William sobre [Como desenvolver um blog com interface administrativa com Hugo e Netlify](https://woliveiras.com.br/posts/desenvolvendo-um-blog-com-interface-administrativa-com-hugo-e-netlify/) .

E eu fico por aqui, espero que tenham gostado do post e quero ver muitos blogs a partir de agora :)

Abraços e até um próximo post. 🚀
