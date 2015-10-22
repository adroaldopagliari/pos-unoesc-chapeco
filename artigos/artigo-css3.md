#####Unoesc Chapecó
#####Pós-graduação em Desenvolvimento Web, Cloud e dispositivos móveis - WebMob
#####Disciplina: HTML5+CSS3
#####Professor: Jean Carlo Nascimento
#####Acadêmico(a): Adroaldo José Pagliari
##Artigo de revisão de CSS3


####Funcionalidade: Transform 2D – Translate

#####O que é?

A propriedade **_translate_** permite que determinado elemento seja rotacionado entre os seus eixos (XY). Assim como em um plano cartesiano as coordenadas de X e Y representam as coordenadas dos elementos, onde ao incrementar positivamente o valor de X o elemento é rotacionado a direta, enquanto que incrementando positivamente Y o elemento é deslocado para baixo. De forma análoga,porém inversa, caso os valores forem negativos o elemento é deslocado para a esquerda e para cima, respectivamente.

#####Onde usar:

Em qualquer elemento HTML que possua um formato 2D (*Divs*, Imagens, etc).

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

#####O que é?

A propriedade CSS3 **_box sizing_** determina se valores como, borda, margem ou o preenchimento de determinado elemento irá influenciar em sua altura e largura permitindo maior flexibilidade na diagramação do conteúdo da página. É possível utilizar esse recurso do CSS3 para alterar ou não o tamanho de um componente através da variação dos valores das propriedades acima.

#####Onde usar:

Em qualquer elemento HTML que seja possível definir as propriedades *border*, *margin* ou *pad*.

#####Como usar:

seletor {
    box-sizing: content-box|border-box|initial|inherit;
    width: x;
    border: y;
    float: left;
}

#####Exemplo de uso

Sintaxe para utilização da propriedade (Desconsiderar a borda):

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

#####O que é?

Através da propriedade **_text-shadow_**, implementada a partir do CSS3 é possível definir sombras em textos sem a necessidade de utilizar outras técnicas, como sobreposição de imagens por exemplo. Os valores admitidos pela propriedade são: A cor da sombra, a posição da sombra com relação ao eixo X (Altura) e Y (largura), e o raio (blur). De forma semelhante a implementação da transformação de elementos 2D (*Transform*), é possível utilizar valores negativos para os valores de X e Y – dessa forma o posicionamento se dá de forma contrária, à esquerda e acima. 

#####Onde usar:

Em qualquer elemento que possua texto em seu conteúdo.

#####Como usar:

seletor {
text-shadow: cor x y raio; border: #000 1px solid;
}

#####Exemplo de uso

Sintaxe para sombreamento do texto em uma *div*.

div {
text-shadow: #600 1px 2px 5px;
border: #000 1px solid;
}

#####Referencia:

http://www.infowester.com/css3sombras.php


####Funcionalidade: Gradiente (background-image)

#####O que é?

Por meio da propriedade **_background-image_** pode-se definir um efeito de variação gradativa de cor, conhecido como gradiente, antes possível apenas por outros meios como por exemplo, através de imagens e Javascript. É possível ainda definir a proporção que o efeito irá utilizar percentualmente.

#####Onde usar:

O efeito pode ser obtido a partir de um navegador que tenha suporte para tal. É possível definir a propriedade em um elemento de imagem ou *div*, por exemplo.

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

#####O que é?

A propriedade CSS3 **_transitions_** permite inserir um efeito de troca de estado de determinado elemento da página. É possível através dele criar transições e animações por um determinado período de tempo. Ainda é possível definir um tempo de atraso (*delay*) para o efeito.

#####Onde usar:

Em qualquer elemento que se deseja obter o efeito. O uso mais comum são elementos estruturais como *divs*, *sections*, *articles*.

#####Como usar:

seletor {
-webkit-transition: background-color linear .8s;
-moz-transition: background-color linear .8s;
}

#####Exemplo de uso

Sintaxe para aplicação do efeito no evento de mouseover em um elemento da página; a cor é alterada gradativamente (8 segundos).

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

#####O que é?

Outra propriedade introduzida no CSS3 é o **_box-reflect_** que permite que determinado elemento sem refletido, como o próprio nome sugere, sem a necessidade de utilizar imagens ou Javascript. O efeito produz um resultado interessante e realístico, porém é dependente também da implementação do browser utilizado. É possível definir a posição do efeito, o espaço entre o conteúdo original e o refletido (*offset*), e também um imagem como máscara, a qual será utilizada como moldura ao refletir. 

#####Onde usar:

O uso mais comum é em elementos de imagens, porém é possível utilizar em outros elementos estruturais.

#####Como usar:

seletor {
-webkit-box-reflect: below 0px
}

#####Exemplo de uso

Abaixo um exemplo da utilização do box-reflect utilizando uma imagem como moldura. A reflexão será abaixo da imagem original e sem espaçamento entre ambas.

.img {
   -webkit-box-reflect: below 0px url(shape.png);
}

#####Referencia:

http://designshack.net/articles/css/mastering-css-reflections-in-webkit/
http://webdesign.tutsplus.com/tutorials/cross-browser-css-reflections-glows-and-blurs--webdesign-6294


####Funcionalidade: Animations

#####O que é?

A propriedade **_animation_** permite a inserção de efeitos complexos de animação na página, sem a necessidade da utilização de Javascript ou Flash, por exemplo. É possível definir o estado inicial do elemento, incorporar um tempo, um atraso entre as alterações de estado e essencialmente *keyframes*, que se tratam dos estilos que o elemento irá assumir em determinado espaço de tempo. Ainda outros efeitos podem ser obtidos através dos valores associados a quantas vezes a animação deverá ser executada, a velocidade e a direção.

#####Onde usar:

Em elementos estruturais, como por exemplo, *div*, *sections*, etc.

#####Como usar:

/* Código da animação*/
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

Animação simulando o quicar de uma bola, com tempo de duração de 1segundo. Um *keyframe* foi definido para simular a posição inicial da bola, e seu estado final.

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

#####O que é?

A propriedade **_opacity_** permite inserir um efeito de transparência em um elemento da página de forma simples no CSS3. Apesar de ser um recurso extremamente simples, é interessante no sentido de que é possível adicionar um efeito antes não obtido sem codificação ou edição de imagens. Ainda pode-se definir o grau de transparência a ser assumido, porém é interessante ressaltar que o efeito será aplicado ao elemento pai e a seus filhos (HTML/DOM). 

#####Onde usar:

A utilização mais comum é em elementos estruturais.

#####Como usar:

seletor {
opacity: number|initial|inherit;
}

#####Exemplo de uso

Aplicação do efeito de transparência nos elementos div (50%).

div {
   opacity: 0.5
}

#####Referencia:

http://css3clickchart.com/#opacity
http://www.w3schools.com/cssref/css3_pr_opacity.asp


####Funcionalidade: Media queries

#####O que é?

Um dos recursos mais interessantes introduzidos no CSS3 é a **_media queries_**, que permite que o conteúdo de um elemento seja ajustado de acordo com o dispositivo que irá acessar a página HTML, ou seja, é possível avaliar o tipo de media, e suas características para determinar qual é a melhor opção de *layout*. Esse recurso vem ao encontro da interoperabilidade do HTML, e busca auxiliar no processo de quebra de estrutura, e má formação visual da página em determinado dispositivo. Basicamente é necessário definir o tipo de mídia, juntamente com suas características e a partir disso definir qual a melhor opção de visualização.

#####Onde usar:

Em elementos estruturais, que dão corpo a página.

#####Como usar:

@media mediatype and (media features){
  .element {
    doSomething;
  }
}

#####Exemplo de uso

Aplicação da regra (cor de fundo) caso a largura seja 900px.

@media screen and (min-width: 900px) {
  .class {
    background: #666;
  }
}

#####Referencia:

http://tableless.com.br/introducao-sobre-media-queries/
http://wpmidia.com.br/desenvolvimento-web/design-responsivo-css3-media-queries/


####Funcionalidade: Columns

#####O que é?

A propriedade **_column_** permite que o conteúdo de uma página seja quebrado em colunas, facilitando assim a leitura, e ampliando a capacidade de edição dos *layouts* das páginas (Diagramação). Ainda sobre a propriedade, é possível definir a quantidade de colunas, o espaçamento entre elas, bem como o estilo de suas bordas.

#####Onde usar:

Em elementos estruturais que possuam conteúdo textual.

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

Aplicação da regra (cor de fundo) caso a largura seja 900px.

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
