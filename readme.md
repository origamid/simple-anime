## Simple Anime

Plugin simples para animação de entrada no site.

```js
// 1 - Copie o arquivo simple-anime.js da pasta dist e cole no seu site.

// 2 - Link o arquivo utilizando a tag script /js/plugins é apenas um exemplo, caso você tenha colocado o arquivo dentro da pasta de plugins
<script src="./js/plugins/simple-anime.js"></script>;

// 3 - Inicie a classe do slide:

new SimpleAnime();
```

```html
<!-- 4 Adicione o atributo data-anime ao elemento que
deseja animar. Informe o total em milessegundos, que o JavaScript
deve esperar até a animação iniciar -->

<h1 data-anime="500">Título do Site</h1>
<p data-anime="1000">Descrição da Página</p>
<button data-anime="1500">Clique Aqui</button>

<!-- 5 Para criar animações diferentes, adicione classes
aos elementos que deseja diferenciar. E defina o transform
inicial da animação na classe -->

<h1 data-anime="500" class="fadeInDown">Título do Site</h1>
<p data-anime="1000" class="fadeInDown">Descrição da Página</p>
<button data-anime="1500">Clique Aqui</button>
```

```css
/*
6 CSS personalizado dependendo da animação desejada
Devem ser adicionadas na frente do código essencial do item 7.
*/
.fadeInDown {
  transform: translate3d(0, -20px, 0);
}
.fadeInUp {
  transform: translate3d(0, 20px, 0);
}
.fadeInRight {
  transform: translate3d(20px, 0, 0);
}
.fadeInLeft {
  transform: translate3d(-20px, 0, 0);
}

/* 7 Adicione o CSS Essencial abaixo */
[data-anime] {
  opacity: 0;
}
.anime {
  opacity: 1;
  transform: none;
  transition: transform 0.8s, opacity 0.8s;
}
```
