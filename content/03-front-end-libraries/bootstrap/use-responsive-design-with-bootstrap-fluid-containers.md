---
id: bad87fee1348bd9acde08712
title: Utilizar Design Responsivo com containers fluídos Bootstrap
challengeType: 0
forumTopicId: 18362
dashedName: use-responsive-design-with-bootstrap-fluid-containers
---

# --description--

Na seção de HTML5 e CSS do freeCodeCamp, nós construímos um App de Fodos de gato. Agora vamos voltar para ele, Desta vez, nós vamos estilizá-lo usando o famoso framework Bootstrap CSS responsivo.

Bootstrap descobrirá a largura da sua tela e responder redimensionando seus elementos HTML - daí o nome  <dfn>responsive design</dfn>.

Com o design responsivo, não há necessidade de uma versão mobile para o seu website. Ele irá ter boa aparência em dispositivos com qualquer largura de tela.

Você pode adicionar o Bootstrap a qualquer app adicionando o seguinte código no topo do seu HTML:

`<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css" integrity="sha384-BVYiiSIFeK1dGmJRAkycuHAHRg32OmUcww7on3RYdg4Va+PmSTsz/K68vbdEjh4u" crossorigin="anonymous"/>`

Neste caso, nós já adicionamos ele para você nesta página, nos bastidores. Note que usar tanto `>` quanto `/>` para fechar a tag `link` é aceitável.
Para começar, nós devemos aninhar todo o nosso HTML (exceto a tag `link` e o elemento `style`) em um elemento `div` com a classe `container-fluid`.

# --hints--

Seu elemento `div` deve ter a classe `container-fluid`.

```js
assert($('div').hasClass('container-fluid'));
```

Seu elemento `div` deve ter uma tag de fechamento.

```js
assert(
  code.match(/<\/div>/g) &&
    code.match(/<div/g) &&
    code.match(/<\/div>/g).length === code.match(/<div/g).length
);
```

Todos os elementos HTML depois da tag de fechamento `style` devem ser aninhados em `.container-fluid`.

```js
assert($('.container-fluid').children().length >= 8);
```

# --seed--

## --seed-contents--

```html
<link href="https://fonts.googleapis.com/css?family=Lobster" rel="stylesheet" type="text/css">
<style>
  .red-text {
    color: red;
  }

  h2 {
    font-family: Lobster, Monospace;
  }

  p {
    font-size: 16px;
    font-family: Monospace;
  }

  .thick-green-border {
    border-color: green;
    border-width: 10px;
    border-style: solid;
    border-radius: 50%;
  }

  .smaller-image {
    width: 100px;
  }
</style>

<h2 class="red-text">CatPhotoApp</h2>

<p>Clique aqui para <a href="#">fotos de gato</a>.</p>

<a href="#"><img class="smaller-image thick-green-border" src="https://bit.ly/fcc-relaxing-cat" alt="A cute orange cat lying on its back."></a>

<p>Coisas que gatos amam:</p>
<ul>
  <li>erva de gato</li>
  <li>apontadores laser</li>
  <li>lasanha</li>
</ul>
<p>Top 3 coisas que gatos odeiam:</p>
<ol>
  <li>tratamento para pulgas</li>
  <li>trovão</li>
  <li>outros gatos</li>
</ol>
<form action="https://freecatphotoapp.com/submit-cat-photo">
  <label><input type="radio" name="indoor-outdoor"> Interior</label>
  <label><input type="radio" name="indoor-outdoor"> Exterior</label>
  <label><input type="checkbox" name="personality"> Amoroso(a)</label>
  <label><input type="checkbox" name="personality"> Preguiçoso(a)</label>
  <label><input type="checkbox" name="personality"> Maluco(a)</label>
  <input type="text" placeholder="cat photo URL" required>
  <button type="submit">Enviar</button>
</form>
```

# --solutions--

```html
<link href="https://fonts.googleapis.com/css?family=Lobster" rel="stylesheet" type="text/css">
<style>
  .red-text {
    color: red;
  }

  h2 {
    font-family: Lobster, Monospace;
  }

  p {
    font-size: 16px;
    font-family: Monospace;
  }

  .thick-green-border {
    border-color: green;
    border-width: 10px;
    border-style: solid;
    border-radius: 50%;
  }

  .smaller-image {
    width: 100px;
  }
</style>
<div class="container-fluid">
  <h2 class="red-text">CatPhotoApp</h2>

<p>Clique aqui para <a href="#">fotos de gato</a>.</p>

<a href="#"><img class="smaller-image thick-green-border" src="https://bit.ly/fcc-relaxing-cat" alt="A cute orange cat lying on its back."></a>

<p>Coisas que gatos amam:</p>
<ul>
  <li>erva de gato</li>
  <li>apontadores laser</li>
  <li>lasanha</li>
</ul>
<p>Top 3 coisas que gatos odeiam:</p>
<ol>
  <li>tratamento para pulgas</li>
  <li>trovão</li>
  <li>outros gatos</li>
</ol>
<form action="https://freecatphotoapp.com/submit-cat-photo">
  <label><input type="radio" name="indoor-outdoor"> Interior</label>
  <label><input type="radio" name="indoor-outdoor"> Exterior</label>
  <label><input type="checkbox" name="personality"> Amoroso(a)</label>
  <label><input type="checkbox" name="personality"> Preguiçoso(a)</label>
  <label><input type="checkbox" name="personality"> Maluco(a)</label>
  <input type="text" placeholder="cat photo URL" required>
  <button type="submit">Enviar</button>
</form>
</div>
```
