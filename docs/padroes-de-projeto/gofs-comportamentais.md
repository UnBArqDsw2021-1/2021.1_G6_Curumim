# GOFs Comportamentais

## Command


## Iterator


## Mediator
&emsp;&emsp;Define um objeto que encapsula como um conjunto de objetos
interage. O Mediator promove o acoplamento fraco ao evitar que os objetos se refiram
explicitamente uns aos outros, permitindo que você varie suas interações
independentemente. Definição de Erich Gamma, Richard Helm, Ralph Johnson e John
Vlissides.<br>
&emsp;&emsp;O padrão Mediator é responsável por controlar e coordenar a interação de um conjunto de objetos.

&emsp;&emsp;
![foto](../../assets/imagens/gofs/mediator_diagrama.jpg)
<center>[Figura ?: Mediator](../../assets/imagens/gofs/mediator_diagrama.jpg)</center>

&emsp;&emsp;O diagrama acima demonstra a interação de objetos da seguinte situação: O sistema conta com um chat onde acontece uma troca de mensagens entre os usuários, porém essa comunicação acontece de uma forma relativamente complexa, pois o Guardian pode se comunicar com qualquer um dos outros dois usuários, Administrador e/ou Professor(a). Logo, considera-se necessário criar um mediador para intermediar as mensagens e o chat fluir de uma melhor forma. Nesse caso os objetos conhecem apenas o Mediator.

## Observer


## State


## Strategy


## Template Method


## Visitor


## Memento


## Chain Of Responsability



## Bibliografia

> - [1] LARMAN, Craig. <b>Utilizando UML e Padrões</b>: Uma introdução à análise e ao projeto orientados a objetos e ao desenvolvimento iterativo. 3. ed. [S. l.: s. n.], 2004.
> - [2] GAMMA, Erich; HELM, Richard; JOHNSON, Ralph; VLISSIDES, John. Design
Patterns: Elements of Reusable Object-Oriented Software. Estados Unidos:
Hardback, 1995. 416 p. Erich Gamma, Richard Helm, Ralph Johnson, John
Vlissides


## Versionamento
| Versão | Data | Modificação | Autor |
|--|--|--|--|
|1.0|10/09/2021| Abertura do documento | Mateus O. Patrício |
|1.1|16/09/2021| Introdução ao Mediator e inclusão de bibliografia [2] | Edson Soares |
|1.2|16/09/2021| Inclusão do diagrama Mediator | Edson Soares |
|1.3|17/09/2021| Explicação do diagrama | Edson Soares |