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

### Estrutura de Objetos
&emsp;&emsp;Para exemplificar a aplicação do padrão Mediator na interação dos objetos do chat entre Guardian, Administrador e Professor(a). Apresentamos um diagrama de objetos que se comunicam através de um intermediário.<br>
&emsp;&emsp;Na estrutura abaixo incluímos um componente do frontend que consiste em um botão para representar o envio de mensagem. Podemos observar a interação desse componente da seguinte maneira: O botão inicia desativado, sempre que um caractere seja digitado no campo de texto, o botão muda seu estado para ativado. Aqui podemos observar que o padrão mediator possibilita diversos objetos interagindo uns com os outros por meio de um mediador.
![foto](../../assets/imagens/gofs/estrutura_objetos.jpg)
<center>[Figura ?: Estrutura de objetos](../../assets/imagens/gofs/estrutura_objetos.jpg)</center>

### Diagrama de classe (Chat)
&emsp;&emsp;
![foto](../../assets/imagens/gofs/mediator_diagrama_classe.jpg)
<center>[Figura ?: Interação dos objetos](../../assets/imagens/gofs/mediator_diagrama_classe.jpg)</center>

&emsp;&emsp;O diagrama acima demonstra a interação de objetos da seguinte situação: O sistema conta com um chat onde acontece uma troca de mensagens entre os usuários, porém essa comunicação acontece de uma forma relativamente complexa, pois o Guardian pode se comunicar com qualquer um dos outros dois usuários, Administrador ou com o(a) Professor(a). Logo, considera-se necessário criar um mediador para intermediar as mensagens e o chat fluir de uma melhor forma. Nesse caso os objetos conhecem apenas o Mediator.

### Implementação (Protótipo)
        function User(name)
        {
        this.name = name
        this.chatroom = null
        }

        User.prototype = {
        send: function(message, toUser)
        {
            this.chatroom.send(message, this, toUser)
        },
        receive: function(message, fromUser)
        {
            return {"sender": fromUser.name, "receiver": this.name, "message": message}
        }
        }

        function Chatroom()
        {
        this.users = {}
        }

        Chatroom.prototype = {
        addUser: function(user)
        {
            this.users[user.name] = user
            user.chatroom = this
        },
        send: function(message, fromUser, toUser)
        {
            toUser.receive(message, fromUser)
        }
        }

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

&emsp;&emsp;O Memento permite salvar e restaurar estados anteriores de um objeto sem revelar os detalhes de sua implementação.

### Aplicabilidade

- É possível utilizar o padrão quando quizer reproduzir cópias do estado de um objeto permitindo então restaurar a um estado anterior do mesmo. O Memento faz cópias completas do estado de um objeto, isso inclui campos privados, e as armazena separadamente do objeto. Duas grandes aplicações do padrão são para a funcionalidade de desfazer e quando se lida com transações, permitindo revertê-las.

- Você pode utilizar o padrão caso o acesso direto à informações de um objeto violar o seu encapsulamento. Com o memento o próprio objeto é responsável por criar sua cópia.

&emsp;&emsp;No nosso projeto faz mais sentido a utilização do padrão criacional Prototype, por se tratar de objetos intuitivos.

## Chain Of Responsibility

&emsp;&emsp;O Chain of Responsibility utiliza a passagem de pedidos por uma corrente de handlers. Onde ao receber um pedido, cada handler decide se deve processar ou passar o pedido para o próximo handler.

### Aplicabilidade

- Utilize o padrão se for esperado que seu programa processse diferentes tipos de pedido em várias maneiras, mas os exatos tipos de pedidos e suas sequências não são previamente conhecidos. O padrão permite a ligação de vários handlers em sequência, quando um handler recebe um pedido o mesmo decide se pode ou não processá-lo, desta forma todos os handlers podem processar o pedido.

- Se for necessário a execução de vários handlers em uma ordem pre-determinada. Como é possível escolher a ordem da corrente de handlers, todos os pedidos irão passar pelos handlers na ordem planejada.

- Caso necessário mudar o conjunto de handlers e suas encomendas em tempo de execução. Ao providenciar setters para campos de referência dentro das classes handlers, é possível inserir, remover ou reordenar os handlers de forma dinâmica.

&emsp;&emsp;Nosso projeto não se encaixa nos casos de aplicação do padrão.

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
|1.1|13/09/2021| Adição do padrão Visitor | Mateus O. Patrício |
|1.2|16/09/2021| Introdução ao Mediator e inclusão de bibliografia [2] | Edson Soares |
|1.3|16/09/2021| Inclusão do diagrama Mediator | Edson Soares |
|1.4|17/09/2021| Explicação do diagrama de classe | Edson Soares |
|1.5|19/09/2021| Adição dos padrões Memento e Chain of Responsibility | Mateus O. Patrício |
|1.6|19/09/2021| Revisão por pares | Daniel Porto e Edson Araujo |
|1.7|19/09/2021| Construção da estutura de objetos | Edson Soares |
|1.8|19/09/2021| Implementação | Edson Soares |
|1.9|19/09/2021| Revisão do padrão Mediator | Bruno Felix e Eliseu Kadesh |
