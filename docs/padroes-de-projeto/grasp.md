# GRASP - Padrões de Software para Atribuição de Responsabilidade Geral

&emsp;&emsp;Padrões GRASP são uma ajuda na hora de entender como desenhar um software orientado à objetos de maneira metódica, racional e explicável (LARMAN, 2004). Têm o intuito de tornar o código mais flexível, facilitando a manutenção e a extensibilidade.

## Criador


## Especialista


## Controlador


## Invenção pura
&emsp;&emsp;O conceito de invenção pura aborda a utilização de soluções que não necessariamente se encaixem em algum padrão de projeto.
Com o objetivo de fortalecer a [alta coesão](#alta-coesao) e o [baixo acoplamento](#baixo-acoplamento), basicamente esse padrão consiste em atribuir um conjunto bem definido de responsabilidades para classes artificiais que não se encontram fundamentalmente no domínio do escopo projeto.<br>
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

## Variações protegidas


## Polimorfismo



## Bibliografia

> - LARMAN, Craig. <b>Utilizando UML e Padrões</b>: Uma introdução à análise e ao projeto orientados a objetos e ao desenvolvimento iterativo. 3. ed. [S. l.: s. n.], 2004.


## Versionamento
| Versão | Data | Modificação | Autor |
|--|--|--|--|
|1.0|01/09/2021| Abertura do documento | Mateus O. Patrício |