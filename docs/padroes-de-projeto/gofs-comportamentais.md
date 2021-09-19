# GOFs Comportamentais

## Command


## Iterator


## Mediator


## Observer


## State


## Strategy


## Template Method


## Visitor

&emsp;&emsp;O visitor permite a separação dos algoritmos com os objetos nos quais eles operam.

### Aplicabilidade

- Você pode utilizar o Visitor quando precisar realizar uma operação em todos os elementos da estrutura de objetos complexa. Ex: uma árvore de objetos. Ou seja, é possível executar uma operação sobre um conjunto de objetos com diferentes classes implementando diversas variantes da mesma operação correspondentes às classes alvo.

- É possível utilizar o Visitor para remover a lógica de negócio de comportamentos auxiliares. Pois o mesmo permite tornar classes primárias da aplicação mais focadas em seu trabalho principal.

- Utilize o padrão quando um comportamento faz sentido apenas dentro de algumas classes de uma uma hierarquia de classe. Você pode extrair esse comportamento para uma classe visitante separada e implementar somente aqueles métodos visitantes que aceitam objetos de classes relevantes, deixando o resto vazio.

&emsp;&emsp;Nosso projeto não se encaixa nos casos de aplicação do padrão.

## Memento


## Chain Of Responsibility



## Bibliografia

> - LARMAN, Craig. <b>Utilizando UML e Padrões</b>: Uma introdução à análise e ao projeto orientados a objetos e ao desenvolvimento iterativo. 3. ed. [S. l.: s. n.], 2004.


## Versionamento
| Versão | Data | Modificação | Autor |
|--|--|--|--|
|1.0|10/09/2021| Abertura do documento | Mateus O. Patrício |
|1.1|13/09/2021| Adição do padrão Visitor| Mateus O. Patrício |