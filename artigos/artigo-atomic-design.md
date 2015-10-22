##Atomic Design


#####Adroaldo Pagliari (Unoesc Chapecó)
#####adroaldo@outlook.com


######Resumo

A grande expansão e popularização do mundo Web em conjunto com a constante necessidade das equipes de desenvolvimento irem ao encontro de metodologias e ferramentas ágeis fez com que fosse necessário alterarmos a maneira como construímos Interfaces. As novas tecnologias e conceitos que sucederam o advento da Internet trouxeram novos e flexíveis mecanismos de desenvolvimento, entretanto, a forma como o layout é produzido e entregue ao usuário-final ainda é um gargalo no fluxo do projeto – nesse contexto o Designer Brad Frost criou um paradigma de construção e implementação para a camada de Front-End chamado de Atomic Design, composto por elementos que fazem referência as partes comuns dos sistemas: Átomos, Moléculas, Organismos, Templates e Páginas.

######O que é?

 A semântica do termo Atomic Design é uma analogia a conceitos básicos de química e biologia: Átomos, Moléculas e Organismos, referindo-se a partes específicas de um sistema comum, tags/elementos, um conjunto de tags/elementos cujo significado seja relevante dentro do contexto, e um agrupamento desses últimos, respectivamente. Em adição a esses conceitos, um conjunto de moléculas formam Templates, que por sua vez dão vida as páginas.
A ideia base do Atomic Design é tornar o desenvolvimento do layout da aplicação modular, escalável e responsivo, por meio de padrões e conceitos. Esse pensamento se “traduz” nas palavras de Stephen Hay: “We’re not designing pages, we’re designing system of components” – Atomic Design está fortemente relacionado a modularidade, a visão de que um sistema é composto por partes menores, que se agrupam e formam um microcosmo.

######Como funciona?

No Atomic Design cada elemento é tratado individualmente e definido em etapas iniciais do projeto, essa ideia parece simples a priori, porém, rompe com o ciclo tradicional de desenvolvimento de Interfaces, cujo framework em cascatas faz com que o modelo seja constantemente reproduzido nas etapas seguintes, tornando o processo moroso. 
Cada átomo, molécula e organismo, será definido separadamente, isto é, teremos estilos para cada parte do sistema – de forma semelhante a guias de estilo; eles serão agrupados (includes) em templates e nessa etapa entregáveis ao usuário. Para a construção dos estilos utilizando o conceito, é possível utilizar a ferramenta idealizada pelo próprio criador do paradigma Brad Frost: Patternlab, que conta com propriedades atuais - os modelos podem ser adaptados e são interativos.

######Para que usar?
	
A utilização do conceito de Atomic Design tem como principal vantagem pensar o sistema, quanto ao layout, em partes, o que é trivial ao ser humano e, por conseguinte modularizar a interface. A modularização garante que os componentes sejam padronizados e reutilizados, além de aumentar a produtividade da equipe de Front-End que pode entregar ao usuário o projeto de layout da aplicação sem complexos modelos, produzidos em outras ferramentas.
Outro ponto culminante na sua adoção é o fato de que atualmente diversos dispositivos com características diferentes irão se comunicar e/ou consumir nossas aplicações, ou seja, o Design do sistema/página deve ser projetado responsivamente desde o seu início. Nesse âmbito o Atomic Design se encaixa bem, desde que suas regras sejam adotadas, definindo-se nas style-guides o comportamento para cada necessidade.

######Onde usar?
A recomendação é para que o Atomic Design seja utilizado na construção de interfaces de sistemas e não de simples páginas - onde o custo-benefício geralmente não é interessante. Sistemas Web que possuem diversos componentes, onde haja necessidade de otimização, escalabilidade e alta produtividade são ambientes propícios à adoção do conceito.

######Exemplos

1.	Átomos 

Definição do estilo

.h3 {
  font-size:15px;
  line-height:20px;
  }

.h4 {
  font-size:12px;
  line-height:20px;
  }
p.atom { margin-bottom:20px; }

Estrutura da página

<p class="atom">
<h3>blablabla</h3>
<h4>blablabla</h4>
</label>

2.	Moléculas

Definição do estilo

Form.meuForm {
font:12px/20px 'Open Sans Bold', sans-serif;
  display:block;
  margin:0 0 5px;    }

Estrutura da página
<form class=”meuForm”>
<font …>
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


######Referências

http://bradfrost.com/blog/post/atomic-web-design/
http://arquiteturadeinformacao.com/mobile/atomic-design-redesenhando-os-entregaveis-de-designers-e-desenvolvedores/
http://webnerd.com.br/dev/atomic-design-uma-nova-visao-sobre-o-design-na-web/
http://nomadev.com.br/atomic-design-por-que-usar/
