# GOFs Criacionais

## Factory Method

&emsp;&emsp;O Factory Method é um padrão bastante adotado por diversas linguagens. Consiste basicamente na definição de uma interface comum para criação de objetos, deixando para as subclasses a responsabilidade de instanciá-los. Essa estrutura é composta pelas interfaces Product, ConcreteProduct, Creator e ConcreteCreator.

- Product: Se caracteriza como a interface comum dos produtos a serem criados;
- ConcreteProduct: Responsável pela implementação da interface Product, definindo produtos concretos;
- Creator: É uma classe abstrata sendo responsável pela declaração da operação factoryMethod, que retorna um objeto Product. Podendo ainda definir uma implementação padrão e assim retornar um ConcreteProduct específico ou também pode definir alguns métodos que invocam FactoryMethod;
- ConcreteCreator: Basicamente estende a classe Creator, realiza a redefinição do factoryMethod para retornar uma instância de um ConcreteProduct criado;

&emsp;&emsp;Em nosso projeto, é possível utilizar o Factory Method na classe "UserController", onde pode ser implementado uma interface com os atributos e métodos necessários, uma ConcreteProduct que realize a implementação dos métodos, e por meio de uma ConcreteCreater realizar a redefinição especifica para cada tipo de usuário.

<center>
	![Factory Method](../../assets/imagens/gofs/factory-method.png)<br>
	[Figura 1: Factory Method](../../assets/imagens/gofs/factory-method.png)
</center>

## Abstract Factory

&emsp;&emsp;O Abstract Factory é um padrão de projeto criacional que tem como principal objetivo, permitir a criação de famílias de objetos relacionados ou dependentes sem ter que especificar suas classes concretas. Se considerarmos que o [Curumim](https://github.com/UnBArqDsw2021-1/2021.1_G6_Curumim) terá uma interface gráfica com um sistema operacional diferente do sistema operacional dos elementos gráficos, por exemplo, teremos uma incompatibilidade que deverá ser resolvida, e essa será o nosso impulso a trabalhar com esse padrão de projeto. O Abstract Factory tem como participantes:

- AbstractFactory: declara uma interface para operações de criação de produtos quaisquer;
- ConcreteFactory: implementa as operações que criam objetos de produtos específicos;
- AbstractProduct: declara uma interface para um tipo de objeto produto;
- Product: define um objeto produto a ser criado pela fábrica específica correspondente, implementando a interface declarada em AbstractProduct;
- Client: usa as interfaces declaradas em AbstractFactory e AbstractProduct;

&emsp;&emsp;Em nosso projeto, podemos utilizar o AbstractFactory na classe "AuthController", por exemplo. Ao iniciar o processo de autenticação, será preciso fazer uma redefinição específica para cada tipo de [usuário](../../base/requisitos/modelagem/lexicos/#lexico-usuario) — com o "ConcreteFactory" —, já que o [administrador](../../base/requisitos/modelagem/lexicos/#lexico-administrador) poderá acessar por meio do "Desktop", enquanto os demais usuários pelo meio ["Mobile"](../../base/requisitos/modelagem/lexicos/#lexico-mobile).

<center>
	![Auth-Controller](../../assets/imagens/gofs/auth-controller.png)<br>
	[Figura 2: AuthController](../../assets/imagens/gofs/auth-controller.png)
</center>

&emsp;&emsp;Na imagem abaixo, podemos visualizar uma representação clara do Abstract Factory. Para que não haja uma incompatibilidade, temos também uma fábrica "esférico" e uma "piramidal", e cada um com suas redefinições específicas e necessárias.

<center>
	![Abstract-Factory](../../assets/imagens/gofs/abstract-factory.png)<br>
	[Figura 3: Abstract Factory](../../assets/imagens/gofs/abstract-factory.png)
</center>

## Prototype

&emsp;&emsp;O padrão de projeto Prototype nos permitirá copiar objetos existentes sem que essa parte do código tenha dependência em classes. Quando quisermos criar um objeto igual, não precisamos acionar essas classes, basta fazer a exata cópia do objeto já criado. 

&emsp;&emsp;No nosso projeto, poderemos utilizar quando precisarmos utilizar o mesmo botão, por exemplo, em diferentes lugares. Com o mesmo formato, mesmas cores e demais configurações. Na imagem abaixo, visualizamos a ideia principal desse padrão de projeto: clonar esses produtos que tenham a mesma configuração. 

<center>
	![Prototype](../../assets/imagens/gofs/prototype.png)<br>
	[Figura 4: Prototype](../../assets/imagens/gofs/prototype.png)
</center>

## Singleton

## Multiton

## Object Pool
-->

## Bibliografia

> - LARMAN, Craig. <b>Utilizando UML e Padrões</b>: Uma introdução à análise e ao projeto orientados a objetos e ao desenvolvimento iterativo. 3. ed. [S. l.: s. n.], 2004.
> - Composite Design Pattern. Geeks For Geeks Disponível em: <https://www.geeksforgeeks.org/composite-design-pattern/>. Acesso em: 11 de setembro de 2021.
> - VALENTIM, Ricardo Alexsandro de Medeiros; SOUZA NETO, Plácido Antônio de. O impacto da utilização de design patterns nas métricas e estimativas de projetos de software: a utilização de padrões tem alguma influência nas estimativas?. 2005.
> - DE ALBUQUERQUE, Marcelo Torres; ROJAS, Alexandre; RIBEIRO, Paulo Cezar M. Utilizando Design Patterns GoF no apoio ao desenvolvimento de um Framework Java. Cadernos do IME-Série Informática, v. 30, p. 13-27, 2010.
> - Abstract Factory. Disponível em: <https://refactoring.guru/pt-br/design-patterns/abstract-factory>. Acesso em: 17 de setembro de 2021.
> - Prototype. Disponível em: <https://refactoring.guru/pt-br/design-patterns/prototype>. Acesso em: 17 de setembro de 2021.
> - Videoaulas e materiais complementares presentes no moodle da disciplina Arquitetura e Desenho de Software. Disponível em https://aprender3.unb.br/course/view.php?id=8603. Acesso em: 17 de setembro de 2021.

## Versionamento
| Versão | Data | Modificação | Autor |
|--|--|--|--|
|1.0|11/09/2021| Abertura do documento | Nilo Mendonça |
|1.1|11/09/2021| Adição da bibliografia e do padrão Factory Method | Nilo Mendonça |
|1.2|17/09/2021| Adição da bibliografia e do padrão Abstract Factory e Prototype | Gabriel Bonifácio |