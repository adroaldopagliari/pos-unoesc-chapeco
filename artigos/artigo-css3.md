####Unoesc Chapec�
####P�s-gradua��o em Desenvolvimento Web, Cloud e dispositivos m�veis - WebMob
####Disciplina: HTML5+CSS3
####Professor: Jean Carlo Nascimento
####Acad�mico(a): Adroaldo Jos� Pagliari
##Artigo de revis�o de CSS3


####Funcionalidade: Transform 2D � Translate

#####O que �?

A propriedade **_translate_** permite que determinado elemento seja rotacionado entre os seus eixos (XY). Assim como em um plano cartesiano as coordenadas de X e Y representam as coordenadas dos elementos, onde ao incrementar positivamente o valor de X o elemento � rotacionado a direta, enquanto que incrementando positivamente Y o elemento � deslocado para baixo. De forma an�loga,por�m inversa, caso os valores forem negativos o elemento � deslocado para a esquerda e para cima, respectivamente.

#####Onde usar:

Em qualquer elemento HTML que possua um formato 2D (**_Divs_**, Imagens, etc).

#####Como usar:

  seletor { transform: translate(x, y); } 
  seletor { transform: translateX(x); } 
  seletor { transform: translateY(y); } 

#####Exemplo de uso

Sintaxe para reposicionamento do elemento:

elemento {
    -webkit-transform: translate(45px, 70px);
    -moz-transform: translate(25px, 50px);  
     transform: translate(50px,100px);  
} 

#####Referencia(s):

http://www.maujor.com/tutorial/interativo-css3/
http://css3clickchart.com/#translate-transform

####Funcionalidade: Box Sizing

#####O que �?

A propriedade CSS3 **_box sizing determina se valores como, borda, margem ou o preenchimento de determinado elemento ir� influenciar em sua altura e largura permitindo maior flexibilidade na diagrama��o do conte�do da p�gina. � poss�vel utilizar esse recurso do CSS3 para alterar ou n�o o tamanho de um componente atrav�s da varia��o dos valores das propriedades acima.

#####Onde usar:

Em qualquer elemento HTML que seja poss�vel definir as propriedades *border*, *margin* ou *pad*.

#####Como usar:

seletor {
    box-sizing: content-box|border-box|initial|inherit;
    width: x;
    border: y;
    float: left;
}

#####Exemplo de uso

Sintaxe para utiliza��o da propriedade (Desconsiderar a borda):

.div4 {
    width: 300px;
    height: 100px;    
    padding: 50px;
    border: 1px solid red;
    box-sizing: border-box;
}

#####Referencia:

http://www.w3schools.com/cssref/css3_pr_box-sizing.asp
http://css3clickchart.com/#box-sizing


####Funcionalidade: Text shadow

#####O que �?

Atrav�s da propriedade **_text-shadow_**, implementada a partir do CSS3 � poss�vel definir sombras em textos sem a necessidade de utilizar outras t�cnicas, como sobreposi��o de imagens por exemplo. Os valores admitidos pela propriedade s�o: A cor da sombra, a posi��o da sombra com rela��o ao eixo X (Altura) e Y (largura), e o raio (blur). De forma semelhante a implementa��o da transforma��o de elementos 2D (Transform), � poss�vel utilizar valores negativos para os valores de X e Y � dessa forma o posicionamento se d� de forma contr�ria, � esquerda e acima. 

#####Onde usar:

Em qualquer elemento que possua texto em seu conte�do.

#####Como usar:

seletor {
text-shadow: cor x y raio; border: #000 1px solid;
}

#####Exemplo de uso

Sintaxe para sombreamento do texto em uma div.

div {
text-shadow: #600 1px 2px 5px;
border: #000 1px solid;
}

#####Referencia:

http://www.infowester.com/css3sombras.php


####Funcionalidade: Gradiente (background-image)

#####O que �?

Por meio da propriedade **_background-image_** pode-se definir um efeito de varia��o gradativa de cor, conhecido como gradiente, antes poss�vel apenas por outros meios como por exemplo, atrav�s de imagens e Javascript. � poss�vel ainda definir a propor��o que o efeito ir� utilizar percentualmente.

#####Onde usar:

O efeito pode ser obtido a partir de um navegador que tenha suporte para tal. � poss�vel definir a propriedade em um elemento de imagem ou *div*, por exemplo.

#####Como usar (Firefox):

seletor {
background-image: -moz-linear-gradient(cor1, cor2);
}

#####Exemplo de uso

Sintaxe para efeito de gradiente no Firefox, o efeito iniciara a partir de 20% da altura do elemento *div*.

div {
background-image: -moz-linear-gradient(green, red 20%);
}

#####Referencia:

http://www.w3c.br/pub/Cursos/CursoCSS3/css-web.pdf


####Funcionalidade: Transitions

#####O que �?

A propriedade CSS3 **_transitions_** permite inserir um efeito de troca de estado de determinado elemento da p�gina. � poss�vel atrav�s dele criar transi��es e anima��es por um determinado per�odo de tempo. Ainda � poss�vel definir um tempo de atraso (*delay*) para o efeito.

#####Onde usar:

Em qualquer elemento que se deseja obter o efeito. O uso mais comum s�o elementos estruturais como *divs*, *sections*, *articles*.

#####Como usar:

seletor {
-webkit-transition: background-color linear .8s;
-moz-transition: background-color linear .8s;
}

#####Exemplo de uso

Sintaxe para aplica��o do efeito no evento de mouseover em um elemento da p�gina; a cor � alterada gradativamente (8 segundos).

.element {
    background-color: red;
    -webkit-transition: background-color linear .8s;
    -moz-transition: background-color linear .8s;
    -o-transition: background-color linear .8s;
    transition: background-color linear .8s;
}

.element:hover {
    background-color: blue;
}

#####Referencia:

http://css3clickchart.com/#transitions


####Funcionalidade: Reflections

#####O que �?

Outra propriedade introduzida no CSS3 � o **_box-reflect_** que permite que determinado elemento sem refletido, como o pr�prio nome sugere, sem a necessidade de utilizar imagens ou Javascript. O efeito produz um resultado interessante e real�stico, por�m � dependente tamb�m da implementa��o do browser utilizado. � poss�vel definir a posi��o do efeito, o espa�o entre o conte�do original e o refletido (*offset*), e tamb�m um imagem como m�scara, a qual ser� utilizada como moldura ao refletir. 

#####Onde usar:

O uso mais comum � em elementos de imagens, por�m � poss�vel utilizar em outros elementos estruturais.

#####Como usar:

seletor {
-webkit-box-reflect: below 0px
}

#####Exemplo de uso

Abaixo um exemplo da utiliza��o do box-reflect utilizando uma imagem como moldura. A reflex�o ser� abaixo da imagem original e sem espa�amento entre ambas.

.img {
   -webkit-box-reflect: below 0px url(shape.png);
}

#####Referencia:

http://designshack.net/articles/css/mastering-css-reflections-in-webkit/
http://webdesign.tutsplus.com/tutorials/cross-browser-css-reflections-glows-and-blurs--webdesign-6294


####Funcionalidade: Animations

#####O que �?

A propriedade **_animation_** permite a inser��o de efeitos complexos de anima��o na p�gina, sem a necessidade da utiliza��o de Javascript ou Flash, por exemplo. � poss�vel definir o estado inicial do elemento, incorporar um tempo, um atraso entre as altera��es de estado e essencialmente *keyframes*, que se tratam dos estilos que o elemento ir� assumir em determinado espa�o de tempo. Ainda outros efeitos podem ser obtidos atrav�s dos valores associados a quantas vezes a anima��o dever� ser executada, a velocidade e a dire��o.

#####Onde usar:

Em elementos estruturais, como por exemplo, *div*, *sections*, etc.

#####Como usar:

/* C�digo da anima��o*/
@keyframes example {
    0%   {background-color: red;}
    25%  {background-color: yellow;}
    50%  {background-color: blue;}
    100% {background-color: green;}
}

/* Elemento a ser animado */
seletor {
    width: 100px;
    height: 100px;
    background-color: red;
    animation-name: example;
    animation-duration: 4s;
}

#####Exemplo de uso

Anima��o simulando o quicar de uma bola, com tempo de dura��o de 1segundo. Um *keyframe* foi definido para simular a posi��o inicial da bola, e seu estado final.

.result-animations {
    -webkit-animation-name: bounceball;
    -webkit-animation-duration: 1s;   
}

@-webkit-keyframes bounceball {

    from {
        bottom: 0;
    }
    to {
        bottom: 60px; }}
@keyframes bounceball {

    from {
        bottom: 0;
    }

    to {
        bottom: 60px;
    }
}

#####Referencia:

http://css3clickchart.com/#keyframe-animations
http://www.w3schools.com/css/css3_animations.asp

####Funcionalidade: Opacity

#####O que �?

A propriedade **_opacity_** permite inserir um efeito de transpar�ncia em um elemento da p�gina de forma simples no CSS3. Apesar de ser um recurso extremamente simples, � interessante no sentido de que � poss�vel adicionar um efeito antes n�o obtido sem codifica��o ou edi��o de imagens. Ainda pode-se definir o grau de transpar�ncia a ser assumido, por�m � interessante ressaltar que o efeito ser� aplicado ao elemento pai e a seus filhos (HTML/DOM). 

#####Onde usar:

A utiliza��o mais comum � em elementos estruturais.

#####Como usar:

seletor {
opacity: number|initial|inherit;
}

#####Exemplo de uso

Aplica��o do efeito de transpar�ncia nos elementos div (50%).

div {
   opacity: 0.5
}

#####Referencia:

http://css3clickchart.com/#opacity
http://www.w3schools.com/cssref/css3_pr_opacity.asp


####Funcionalidade: Media queries

#####O que �?

Um dos recursos mais interessantes introduzidos no CSS3 � a **_media queries_**, que permite que o conte�do de um elemento seja ajustado de acordo com o dispositivo que ir� acessar a p�gina HTML, ou seja, � poss�vel avaliar o tipo de media, e suas caracter�sticas para determinar qual � a melhor op��o de *layout*. Esse recurso vem ao encontro da interoperabilidade do HTML, e busca auxiliar no processo de quebra de estrutura, e m� forma��o visual da p�gina em determinado dispositivo. Basicamente � necess�rio definir o tipo de m�dia, juntamente com suas caracter�sticas e a partir disso definir qual a melhor op��o de visualiza��o.

#####Onde usar:

Em elementos estruturais, que d�o corpo a p�gina.

#####Como usar:

@media mediatype and (media features){
  .element {
    doSomething;
  }
}

#####Exemplo de uso

Aplica��o da regra (cor de fundo) caso a largura seja 900px.

@media screen and (min-width: 900px) {
  .class {
    background: #666;
  }
}

#####Referencia:

http://tableless.com.br/introducao-sobre-media-queries/
http://wpmidia.com.br/desenvolvimento-web/design-responsivo-css3-media-queries/


####Funcionalidade: Columns

#####O que �?

A propriedade **_column_** permite que o conte�do de uma p�gina seja quebrado em colunas, facilitando assim a leitura, e ampliando a capacidade de edi��o dos *layouts* das p�ginas (Diagrama��o). Ainda sobre a propriedade, � poss�vel definir a quantidade de colunas, o espa�amento entre elas, bem como o estilo de suas bordas.

#####Onde usar:

Em elementos estruturais que possuam conte�do textual.

#####Como usar (Firefox e Chrome):

elemento {
-moz-column-count: x;
-moz-column-gap: ypx;
-moz-column-rule: zpx type color;
 
-webkit-column-count: x;
-webkit-column-gap: ypx;
-webkit-column-rule: zpx type color;
}

#####Exemplo de uso

Aplica��o da regra (cor de fundo) caso a largura seja 900px.

div4 {
/* borda inserida para facilitar o entedimento */
border: 1px solid #699;
-moz-column-count: 2;
-moz-column-gap: 20px;
-moz-column-rule: 1px solid #6e8eb9;
 
-webkit-column-count: 2;
-webkit-column-gap: 20px;
-webkit-column-rule: 1px solid #6e8eb9;
}

#####Referencia:

http://www.kadunew.com/blog/css/10-efeitos-com-propriedades-css3
