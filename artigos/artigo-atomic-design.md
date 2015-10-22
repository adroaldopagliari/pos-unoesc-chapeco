Resumo
A grande expans�o e populariza��o do mundo Web em conjunto com a constante necessidade das equipes de desenvolvimento irem ao encontro de metodologias e ferramentas �geis fez com que fosse necess�rio alterarmos a maneira como constru�mos Interfaces. As novas tecnologias e conceitos que sucederam o advento da Internet trouxeram novos e flex�veis mecanismos de desenvolvimento, entretanto, a forma como o layout � produzido e entregue ao usu�rio-final ainda � um gargalo no fluxo do projeto � nesse contexto o Designer Brad Frost criou um paradigma de constru��o e implementa��o para a camada de Front-End chamado de Atomic Design, composto por elementos que fazem refer�ncia as partes comuns dos sistemas: �tomos, Mol�culas, Organismos, Templates e P�ginas.

O que �
 A sem�ntica do termo Atomic Design � uma analogia a conceitos b�sicos de qu�mica e biologia: �tomos, Mol�culas e Organismos, referindo-se a partes espec�ficas de um sistema comum, tags/elementos, um conjunto de tags/elementos cujo significado seja relevante dentro do contexto, e um agrupamento desses �ltimos, respectivamente. Em adi��o a esses conceitos, um conjunto de mol�culas formam Templates, que por sua vez d�o vida as p�ginas.
A ideia base do Atomic Design � tornar o desenvolvimento do layout da aplica��o modular, escal�vel e responsivo, por meio de padr�es e conceitos. Esse pensamento se �traduz� nas palavras de Stephen Hay: �We�re not designing pages, we�re designing system of components� � Atomic Design est� fortemente relacionado a modularidade, a vis�o de que um sistema � composto por partes menores, que se agrupam e formam um microcosmo.

Como funciona

	No Atomic Design cada elemento � tratado individualmente e definido em etapas iniciais do projeto, essa ideia parece simples a priori, por�m, rompe com o ciclo tradicional de desenvolvimento de Interfaces, cujo framework em cascatas faz com que o modelo seja constantemente reproduzido nas etapas seguintes, tornando o processo moroso. 
	Cada �tomo, mol�cula e organismo, ser� definido separadamente, isto �, teremos estilos para cada parte do sistema � de forma semelhante a guias de estilo; eles ser�o agrupados (includes) em templates e nessa etapa entreg�veis ao usu�rio. Para a constru��o dos estilos utilizando o conceito, � poss�vel utilizar a ferramenta idealizada pelo pr�prio criador do paradigma Brad Frost: Patternlab, que conta com propriedades atuais - os modelos podem ser adaptados e s�o interativos.

Para que usar
	
	A utiliza��o do conceito de Atomic Design tem como principal vantagem pensar o sistema, quanto ao layout, em partes, o que � trivial ao ser humano e, por conseguinte modularizar a interface. A modulariza��o garante que os componentes sejam padronizados e reutilizados, al�m de aumentar a produtividade da equipe de Front-End que pode entregar ao usu�rio o projeto de layout da aplica��o sem complexos modelos, produzidos em outras ferramentas.
	Outro ponto culminante na sua ado��o � o fato de que atualmente diversos dispositivos com caracter�sticas diferentes ir�o se comunicar e/ou consumir nossas aplica��es, ou seja, o Design do sistema/p�gina deve ser projetado responsivamente desde o seu in�cio. Nesse �mbito o Atomic Design se encaixa bem, desde que suas regras sejam adotadas, definindo-se nas style-guides o comportamento para cada necessidade.

Onde usar
	A recomenda��o � para que o Atomic Design seja utilizado na constru��o de interfaces de sistemas e n�o de simples p�ginas - onde o custo-benef�cio geralmente n�o � interessante. Sistemas Web que possuem diversos componentes, onde haja necessidade de otimiza��o, escalabilidade e alta produtividade s�o ambientes prop�cios � ado��o do conceito.

Exemplos


1.	�tomos 

Defini��o do estilo

.h3 {
  font-size:15px;
  line-height:20px;
  }

.h4 {
  font-size:12px;
  line-height:20px;
  }
p.atom { margin-bottom:20px; }

Estrutura da p�gina

<p class="atom">
<h3>blablabla</h3>
<h4>blablabla</h4>
</label>

2.	Mol�culas

Defini��o do estilo

Form.meuForm {
font:12px/20px 'Open Sans Bold', sans-serif;
  display:block;
  margin:0 0 5px;    }

Estrutura da p�gina
<form class=�meuForm�>
<font �>
</font></form>

3.	Organismos

.corpo {
  text-align: bottom;

  h3 {
    border-bottom: @gray-lighter solid 1px;
    color: @gray-light;
    padding-bottom: @space-sm;
  }

  p {
    color: @gray;
  }
}

4.	Templates



Refer�ncias
http://bradfrost.com/blog/post/atomic-web-design/
http://arquiteturadeinformacao.com/mobile/atomic-design-redesenhando-os-entregaveis-de-designers-e-desenvolvedores/
http://webnerd.com.br/dev/atomic-design-uma-nova-visao-sobre-o-design-na-web/
http://nomadev.com.br/atomic-design-por-que-usar/
