# Curso CSS3 - Intermediário e Avançado

> Este repositório contém o que eu estou aprendendo no curso de CSS3. Nele possui exemplos de comandos e também projetos mais avançados para praticá-los.

## Projetos

Acesse os projetos feitos utilizando o css.

* Projeto Site de Notícias </a>
* Chalé Hotel

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

<img src="Prints Exemplos\especificidade_important_exemplo.png">

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