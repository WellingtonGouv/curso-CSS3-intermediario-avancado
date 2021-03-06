# Curso CSS3 - Intermediário e Avançado

> Este repositório contém o que eu estou aprendendo no curso de CSS3. Nele possui exemplos de comandos e também projetos mais avançados para praticá-los.

## Projetos

Acesse os projetos feitos utilizando o css.

* <a href="https://github.com/WellingtonGouv/curso-CSS3-intermediario-avancado/tree/main/Projetos/Projeto%20Site%20de%20Notícias"> Projeto Site de Notícias </a>
* <a href="https://github.com/WellingtonGouv/curso-CSS3-intermediario-avancado/tree/main/Projetos/Projeto%20Chalé%20Hotel"> Chalé Hotel </a>

## Introdução 

Como vimos <a href="https://github.com/WellingtonGouv/curso-CSS3">anteriormente</a>, o CSS3 é utilizado para estilização de páginas HTML. Neste repositório, iremos observar comandos mais intermediários e avançados.

## Conteúdo

### Seletores

Anteriormente, vimos que podemos utilizar seletores definir as estilizações no CSS. Os seletores podem ser utilizados de várias maneiras dependendo do que você deseja estilizar. Podemos usar os seguintes tipos de seletores:

* Seletor Universal
* Seletor de texto
* Seletor de classe
* Seletor de ID
* Seletor de filho
* Seletor de descendente
* Seletor de irmão adjacente
* Seletor de irmão geral

<br>

#### Seletor Universal

Utilizamos o seletor universal para aplicar estilo em todos os elementos do documento.<br>
Exemplo:

```css
* {
    border: 1px solid red;
}
```

##### Resultado

<img src="Prints Exemplos\seletor_universal_exemplo.png">

<br>
<br>

#### Seletor de texto

Podemos utilizar o seletor de texto para aplicar estilo em elementos pelo tipo. <br>
Exemplo:

```css
h1 {
    color: green;
}
```

##### Resultado

<img src="Prints Exemplos\seletor_texto_exemplo.png">

<br>
<br>

#### Seletor de classe

Utilizamos um seletor de classe para selecionar um elemento cujo atributo class tem o valor especificado depois do ponto. <br>
Exemplo:

```css
.verde {
    color: green;
}

p.verde {
    color: green;
}
```

##### Resultado

<img src="Prints Exemplos\seletor_classe_exemplo.png">

<br>
<br>

#### Seletor de ID

Podemos utilizar o seletor de ID para selecionar um elemento cujo atributo id tem o valor especificado após o símbolo de cerquilha (#). <br>
Exemplo:

```css
#cabecalho {
    border: 1px solid blue;
}
```

##### Resultado

<img src="Prints Exemplos\seletor_id_exemplo.png">

<br>
<br>

#### Seletor de filho

Utilizamos o seletor de filho para estilizar um elemento que é filho direto de outro, ou seja, ele está dentro de outro elemento diretamente. <br>
Exemplo:

```css
li>a {
    color: red;
    text-decoration: none;
}
```

##### Resultado

<img src="Prints Exemplos\seletor_filho_exemplo.png">

<br>
<br>

#### Seletor de descendente

Podemos utilizar o seletor de descendente para estilizar um elemento que é descendente de outro, ou seja, é igual o seletor de filho mas ele não precisa estar conectado diretamente. <br>
Exemplo:

```css
div a {
    color: green;
}
```

##### Resultado

<img src="Prints Exemplos\seletor_descendente_exemplo.png">

<br>
<br>

#### Seletor de irmão adjacente

Utilizamos o seletor de irmão adjacente para estilizar um elemento que está próximo ao outro.<br>
Exemplo:

```css
h1+p {
    color: red;
}
```

##### Resultado

<img src="Prints Exemplos\seletor_irmao_adjacente_exemplo.png">

<br>
<br>

#### Seletor de irmão geral

Podemos utilizar o seletor de irmão geral para estilizar o elemento que é irmão do outro, não necessariamente estando próximos um do outro. <br>
Exemplo:

```css
h1~p {
    color: red;
}
```

##### Resultado

<img src="Prints Exemplos\seletor_irmao_geral_exemplo.png">

***

### Herança e especificidade

No CSS, as estilizações podem herdar atributos, ou seja, se eu definir uma cor no body

```css
body {
    color: red;
}
```

todos os atributos dentro do body terão a cor vermelha. Também possuem alguns atributos que não são herdados, como o background ou o border. Se colocarmos um border no body, ele só fica no body.

```css
body {
    color: green;
    border: 1px solid red;
}
```

#### Resultado

<img src="Prints Exemplos\herança_exemplo.png">

<br>
<br>

Podemos, também, especificar qual estilo queremos seguir. Por padrão, o CSS sempre considera a estilização escrita por último, mas podemos utilizar a característica `important` para definir o estilo a ser seguido. O `important` é muito interessante mas não é recomendado utilizar muito.

```css
p {
    color: blue !important;
}

p {
    color: red;
}
```

#### Resultado

<img src="Prints Exemplos\especificidade_importante_exemplo.png">

<br>
<br>

Se um seletor for mais específico que outro a regra mais específica
será aplicada (terá precedência sobre regras mais gerais).

```css
* {
    color: red;
}

h2 {
    color: blue;
}

h2.verde {
    color: green;
}

h2#amarelo {
    color: yellow;
}
```

Neste exemplo, a característica a ser seguida será o h2 em amarelo, pois seletor em ID é mais específico que o de classe, que é mais específico que o de texto, que é mais específico que o seletor universal.

#### Resultado

<img src="Prints Exemplos\especificidade_exemplo.png">

***

### Barra de navegação vertical

Com os itens aprendidos anteriormente, podemos criar uma barra de nagaveção vertical para o nosso site. Nessa barra, utilizamos ma imagem como background. Nela, quando passamos o mouse em cima, realizamos uma movimentação.

```css
ul {
    margin: 0;
    padding: 0;
    list-style-type: none;
}

ul a {
    width: 200px;
    height: 40px;
    display: block;
    color: #000;
    text-decoration: none;
    text-indent: 40px;
    line-height: 40px;
    background: url(../images/menu.png) no-repeat left bottom;
}

a:hover {
    background-position: right bottom;
    color: #fff;
}
```

Utilizamos o `list-style-type` para retirar o caractere que aparece normalmente nas listas. O `text-indent`funciona parecido com o `padding`, mas é utilizado para indentar textos. Já o `line-height` é utilizado para alterar o tamanho da linha.

#### Resultado

<img src="Prints Exemplos\barra_vertical_exemplo.png">

***

### Marcando página atual

Podemos utilizar duas abordagens para marcar a página atual nos menus. Podemos utilizar a seguinte abordagem que é bem comum utilizando com linguagens de programação.

```css
a:hover, .selecionado a {
    background-position: right bottom;
    background-color: #f99200;
    color: #fff;
}
```

```html
<h2>Home</h2>
        <ul>
            <li class="selecionado">
                <a href="index.html"> Home </a> 
            </li>
            <li>
                <a href="sobre.html"> Sobre </a> 
            </li>
            <li>
                <a href="servicos.html"> Serviços </a> 
            </li>
            <li>
                <a href="noticias.html"> Notícias </a> 
            </li>
            <li>
                <a href="contato.html"> Contato </a> 
            </li>
        </ul>
```

Podemos utilizar outra abordagem para marcar a página atual.

```css
#home #navegacao .home a, 
#sobre #navegacao .sobre a,
#servicos #navegacao .servicos a,
#noticias #navegacao .noticias a,
#contato #navegacao .contato a {
    background-position: right bottom;
    background-color: #f99200;
    color: #fff;
}
```

```html
<body id="home">
        <h2>Home</h2>
        <ul id="navegacao">
            <li  class="home"> 
                <a href="index.html"> Home </a> 
            </li>
            <li class="sobre"> 
                <a href="sobre.html"> Sobre </a> 
            </li>
            <li class="servicos"> 
                <a href="servicos.html"> Serviços </a> 
            </li>
            <li class="noticias"> 
                <a href="noticias.html"> Notícias </a> 
            </li>
            <li class="contato"> 
                <a href="contato.html"> Contato </a> 
            </li>
        </ul>
    </body>
```

#### Resultado

<img src="Prints Exemplos\marcando_pagina_exemplo.png">

***

### Barra de navegação horizontal

Com os itens aprendidos anteriormente, podemos criar uma barra de nagaveção horizontal para o nosso site. Nessa barra, utilizamos ma imagem como background.

```css
ul {
    margin: 0;
    padding: 0;
    list-style-type: none;

    width: 720px;
    background: #159cb0 url(../images/fundo-horizontal.png) repeat-x;
    float: left;
}

ul a {
    display: block;
    padding: 0 2em;
    line-height: 2.2em;
    text-decoration: none;
    color: #fff;
    background: url(../images/divisor.png) repeat-y left top;
}

ul li {
    float : left;
}
```

Para os elementos da lista ficarem um do lado do outro, definimos como `display: block` e o `float: left`.

#### Resultado

<img src="Prints Exemplos\barra_horizontal_exemplo.png">

***

### Navegação com abas

Podemos utilizar outra maneira pra criar um menu que é a navegação com abas. Neste exemplo, utilizamos duas imagens para o background, uma com o lado esquerdo da aba e outro com o lado direito.

```css
ul li {
    float: left;
    background: url(../images/aba-direita.png) no-repeat top right;
}

li a {
    display: block;
    padding: 0 2em;
    line-height: 3em;
    text-decoration: none;
    background: url(../images/aba-esquerda.png) no-repeat top left;
    color: #fff;
}
```

#### Resultado

<img src="Prints Exemplos\navegacao_abas_exemplo.png">

***

### Layout Fixo

O layout de largura fixa significa que não importa o tamanho da tela, o seu site irá ficar do mesmo tamnho. Se diminuir a tela, temos que usar o scroll do mouse para conseguir visualizá-lo.

#### Resultado

<img src="Prints Exemplos\layout_fixo.png">

***

### Layout Líquido

Podemos utilizar de um layout líquido nos nossos sites, que se ajusta do tamanho da tela, mas atenção, layout líquido é diferente de layout responsivo. <br>
Para isso, podemos definir os tamanhos baseados na porcentagem da tela, e não em píxels, pois isso faz que os elementos se ajustem a medida que a tela vai mudando de tamanho. Ao diminuir, podemos definir um tamanho padrão utilizando o `min-width`.

#### Resultado

<img src="Prints Exemplos\layout_liquido_exemplo.png">

***

### Imagens Líquidas

Assim como o layout líquido, podemos usar imagens líquidas no nosso site. Se ajustando a medida que o tamanho da tela aumenta ou diminui.

#### Resultado

<img src="Prints Exemplos\imagens_liquidas_exemplo.png">

***

### Coluna Falsa

Podemos criar uma coluna falsa usando uma imagem.

#### Resultado 

<img src="Prints Exemplos\coluna_falsa_exemplo.png">

***

### Estilizando tabelas

Podemos estilzar as tabelas com o css. Podemos adicionar ou retirar bordas, definir espaçamentos e muito mais. <br>

Exemplo:

```css
th {
    text-transform: uppercase;
    border-top: 1px solid #999;
    border-bottom: 1px solid #111;
    text-align: left;
    font-size: 90%;
    letter-spacing: 0.1em;
}
```

#### Resultado 

<img src="Prints Exemplos\estilizando_tabelas_exemplo.png">

***

### Estilizando Formulários

Também podemos estilizar os formulários com o css. Podemos usar o `fieldset` parar agrupar os elementos e o `legend` como legenda.

```css
ieldset{
    margin: 1em 0;
    padding: 1em;
    border: 1px solid #ccc;
    background: #f8f8f8;
}

legend {
    font-weight: bold;
}
```

Podemos usar o `cursor` para definir o tipo de cursor que aparece quando passamos por cima.

```css
label {
    display: block;
    cursor: pointer;
}
```

Podemos definir o estilo pra um tipo de input de duas maneiras:

```css
input[type="text"] {
    width: 20em;
}
```

ou

```css
input.radio, input.checkbox, input.submit {
    width: auto;
}
```

#### Resultado 

<img src="Prints Exemplos\estilizar_formularios_exemplo.png">

***

### Estilizando formulários com imagens

Podemos estilizar nossos formulários de outra maneira bem mais bonita, utilizando imagens. <br>
Existem alguns comandos que podem alterar a opacidade do background, adicionando o seguinte comando com os códigos da cor e no fim a opacidade.

```css
background-color: rgba(255, 255,255,0.3);
```

Podemos utilizar o seguinte comando para arredonda a div.

```css
border-radius: 10px;
```

E também podemos criar um background com degradê.

```css
background: linear-gradient(to bottom, #faa600, #f68a00);
```

#### Resultado 

<img src="Prints Exemplos\estilizar_formularios_imagens_exemplo.png">

***

### Arredondando com imagens

Podemos utilizar um efeito de arredondamento utilizando imagens. Utilizaremos uma imagem no topo, uma no meio para dar um efeito de degradê e uma embaixo.

#### Resultado

<img src="Prints Exemplos\arredondando_imagens_exemplo.png">

***

### Efeito Parallax

Podemos realizar um efeito de parallax com o css. Esse efeito simula como se quando usarmos o scroll na página, o background fica parado mas ele muda.

#### Resultado

<img src="Prints Exemplos\parallax_exemplo.png">

***

### Fontes customizadas

Podemos utilizar fontes customizadas no nosso site, não sendo necessário que o usuário tenha essa fonte. 

Exemplo:

```css
@font-face {
    font-family: "Madelina Script";
    src:url("../fonts/MadelinaScript.woff");
}
```

#### Resultado

<img src="Prints Exemplos\fontes_exemplo.png">

***