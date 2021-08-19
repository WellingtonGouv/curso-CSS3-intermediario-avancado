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

<br>
<br>
