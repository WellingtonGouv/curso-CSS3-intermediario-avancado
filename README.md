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