# GOFs Estruturais

## Adapter


## Composite

&emsp;&emsp;O Composite é um padrão de design de particionamento e descreve um grupo de objetos que é tratado da mesma maneira que uma única instância do mesmo tipo de objeto. O objetivo de um Composite é agrupar objetos em estruturas de árvore para representar hierarquias parte-todo. Ele permite que você tenha uma estrutura de árvore e peça a cada folha da árvore que execute uma tarefa. "O Composite é baseado no Polimorfismo e fornece variações protegidas a um cliente então não sofre impacto se seus objetos relacionados forem atômicos ou compostos" (LARMAN, 2004). 

O padrão Composite possui 4 participantes:

- Component: Uma interface ou classe base abstrata para os objetos na estrutura em árvore. Esta classe define o comportamento padrão para todos os objetos e comportamentos para acessar e gerenciar componentes filhos na árvore.
- Leaf: É uma classe que estende Component para representar folhas na estrutura de árvore que não tem nenhum filho.
- Composite: É uma classe que estende Component para representar nós na estrutura da árvore, podendo conter filhos. Esta classe armazena componentes Leaf e implementa os comportamentos definidos em Component para acessar e gerenciar componentes filhos.
- Client: interage com o Component para acessar e manipular objetos na composição.

&emsp;&emsp;Em nosso projeto, é possível utilizar o Composite para gerar o [mural](../../../base/requisitos/modelagem/lexicos/#lexico-mural), onde teremos BoardController sendo o Component, e as leaf sendo a classe Events e a classe Anotations. Abaixo temos um exemplo em javascript:

![Composite code](../../assets/imagens/gofs/composite-code.png)

<center>[Figura 2: Board Composite Code](../../assets/imagens/gofs/composite-code.png)</center>

&emsp;&emsp;Em nível de modelagem, temos esse exemplo onde só foram descritos os métodos e atributos específicos utilizados no composite. É possível ver as classes mais completas no [Diagrama de classes](../modelagem/modelagem-estatica/diagrama-de-classes.md) do projeto.

![Composite modelagem](../../assets/imagens/gofs/CompositeModelagem.png)

<center>[Figura 3: Composite](../../assets/imagens/gofs/CompositeModelagem.png)</center>

## Bibliografia

> - LARMAN, Craig. <b>Utilizando UML e Padrões</b>: Uma introdução à análise e ao projeto orientados a objetos e ao desenvolvimento iterativo. 3. ed. [S. l.: s. n.], 2004.

> - Composite Design Pattern. Geeks For Geeks Disponível em: <https://www.geeksforgeeks.org/composite-design-pattern/>. Acesso em: 10 de setembro de 2021.


## Versionamento
| Versão | Data | Modificação | Autor |
|--|--|--|--|
|1.0|10/09/2021| Abertura do documento | João Pedro |
|1.1|10/09/2021| Adicionando topico Composite | João Pedro, Eliseu Kadesh |
