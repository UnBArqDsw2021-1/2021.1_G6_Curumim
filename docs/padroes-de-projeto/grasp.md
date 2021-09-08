# GRASP - Padrões de Software para Atribuição de Responsabilidade Geral

&emsp;&emsp;Padrões GRASP são uma ajuda na hora de entender como desenhar um software orientado à objetos de maneira metódica, racional e explicável (LARMAN, 2004). Têm o intuito de tornar o código mais flexível, facilitando a manutenção e a extensibilidade.

## Criador

A instanciação de objetos é uma atividade comum em todo sistema orientado a objetos. Entender qual classe deve ser responsável por instanciar objetos reduz complexidade desnecessária do sistema.

Segundo Larman (2004), uma classe B deve ser responsável por criar instâncias de classe A se uma, ou quanto mais melhor, das seguintes afirmações se aplicarem:

- Instâncias de B contêm ou agregam instâncias de A;
- Instâncias de B gravam instâncias de A;
- Instâncias de B utilizam instâncias de A;
- Instâncias de B têm os dados necessários para iniciação das instâncias de A.

## Especialista
&emsp;&emsp;
Antes de definir exatamente o que é o "Especialista", é importante entender que o [criador](#criador), por exemplo, é um especialista, mas com um olhar focado em criação de instâncias. 
Por um outro lado, o padrão de projeto Especialista se preocupa em atribuir responsabilidades para alguma entidade mais especialista, seja mais especialista em instâncias ou não. O importante é que seja em um aspecto do sistema que há alguma entidade a fazer melhor aquilo, como por exemplo, em cadastrar uma [criança](../../base/requisitos/modelagem/lexicos/#lexico-crianca), [lançar uma presença](../../base/requisitos/modelagem/lexicos/#lexico-lancar-presenca), entre outros.

Alguns problemas foram identificados: falta de um princípio geral para atribuir responsabilidades a objetos e a necessidade de fazer escolhas sobre a atribuição de responsabilidades a entidades. Diante dessas dificuldades, veio a solução: iniciar declarando claramente a responsabilidade e atribuir uma responsabilidade de informação a uma entidade.

Um malefício claro desse padrão é quando a solução sugerida pelo especialista não é desejável, o que pode acontecer em algumas situações, mas os benefícios são inquestionáveis: baixo acoplamento, o encapsulamento da informação é mantido e a definição de entidades mais fáceis de entender e manter é encojarada.

## Controlador


## Invenção pura
&emsp;&emsp;O conceito de invenção pura aborda a utilização de soluções que não necessariamente se encaixem em algum padrão de projeto.
Com o objetivo de fortalecer a [alta coesão](#alta-coesao) e o [baixo acoplamento](#baixo-acoplamento), basicamente esse padrão consiste em atribuir um conjunto bem definido de responsabilidades para classes artificiais que não se encontram fundamentalmente no domínio do escopo do projeto.<br>
&emsp;&emsp;Com base no [diagrama de classes](../../modelagem/modelagem-estatica/diagrama-de-classes) desenvolvido, esse padrão foi aplicado ao modelar as seguintes classes:

- **Authenticantion Controller:**

&emsp;&emsp;A classe **authController** foi modelada para conter a responsabilidade de aplicar toda as regras de autenticação do sistema. Basicamente todas as requisições do [usuário](../../base/requisitos/modelagem/lexicos/#lexico-usuario) serão direcionadas às [rotas](), as quais inicialmente invocarão os métodos da **authController**, para, somente se autorizado pelos mesmos, continuar para a aplicação das regras de negócio inicialmente requisitadas e, finalmente, retornar uma resposta para a camada de view.

![Authenticantion Controller](../assets/imagens/GRASPs/invencao_auth.png)
<center>[Figura 1: Classe authController](../assets/imagens/GRASPs/invencao_auth.png)</center>

- **Board:**

&emsp;&emsp;A classe [**Board**](../../base/requisitos/modelagem/lexicos/#lexico-mural) surgiu na necessidade de atribuir a responsabilidade de agrupar [atividades](../../base/requisitos/modelagem/lexicos/#lexico-atividade), [anotações](../../base/requisitos/modelagem/lexicos/#lexico-anotacao) e [eventos](../../base/requisitos/modelagem/lexicos/#lexico-evento) para a visualização por parte dos [responsáveis](../../base/requisitos/modelagem/lexicos/#lexico-responsavel). Essa classe tem sua validação na aplicação de regras específicas, como, por exemplo, a visualização de dados contidos nessas classes, em uma única tela, com a possibilidades de filtrar em um tipo de classe específica.<br>
&emsp;&emsp;Tais funcionalidades estão especificadas na [US06](../../product-backlog/#US06) e podem ser melhor visualizadas no [prótipo de alta fidelidade](../../base/design-sprint/prototipo-alta/#prototipo-produzido).

![Board](../assets/imagens/GRASPs/invencao_board.png)
<center>[Figura 2: Classe Board](../assets/imagens/GRASPs/invencao_board.png)</center>

## Alta Coesão


## Baixo Acoplamento


## Indireção

&emsp;&emsp;Esse padrão se configura por atribuir responsabilidades de mediador a classes intermediárias entre outros componentes, objetos ou serviços com objetivo, também, de contribuir com a [alta coesão](#alta-coesao) e o [baixo acoplamento](#baixo-acoplamento).<br>
&emsp;&emsp;**Camada Controller:** A indireção pode ser observada ao longo de todo o projeto simplesmente pela utilização da arquitetura **MVC**, visto que as classes contidas na camada de **controller** servem como mediadoras entre as camadas **view** e **model**. As classes controllers estão contidas nesse [diretório]().<br>
&emsp;&emsp;**Middlewares:** Além disso, o nosso projeto utilizará middlewares que são classes utilizadas internamente na api, pelos controllers na execução das regras de negócio, de forma a desacoplar métodos e rotinas estratégicas. Os middlewares do projeto estão contidos nesse [diretório]().

## Variações protegidas


## Polimorfismo



## Bibliografia

> - LARMAN, Craig. <b>Utilizando UML e Padrões</b>: Uma introdução à análise e ao projeto orientados a objetos e ao desenvolvimento iterativo. 3. ed. [S. l.: s. n.], 2004.
> - Padrões GRASP, UFU (Universidade Federal de Uberlândia). Disponível em http://www.facom.ufu.br/~bacala/ESOF/05a-Padr%C3%B5es%20GRASP.pdf. Acesso em: 03 set. 2021.
> - [Documento GRAPS do projeto Stock](https://unbarqdsw.github.io/2020.1_G12_Stock/#/Project/Estudos/GRASP);
> - Videoaulas e materiais complementares presentes no moodle da disciplina Arquitetura e Desenho de Software. Disponível em <https://aprender3.unb.br/course/view.php?id=8603>. Acesso em: 27 jul. 2021.
> - Canal Vertice digital. Analise e Orientação a Objetos - Princípios do GRASP - Indirection ou Indireção. YouTube. Disponível em <https://www.youtube.com/watch?v=zPlAYo2E92o>. Acesso em: 02 set. 2021.

## Versionamento
| Versão | Data | Modificação | Autor |
|--|--|--|--|
|1.0|01/09/2021| Abertura do documento | Mateus O. Patrício |
|1.1|01/09/2021| Adição da introdução e criador | Mateus O. Patrício |
|1.2|02/09/2021| Adição da invenção pura e indireção | Bruno Felix e Daniel Porto |
|1.3|03/09/2021| Adição do especialista | Gabriel Bonifácio |