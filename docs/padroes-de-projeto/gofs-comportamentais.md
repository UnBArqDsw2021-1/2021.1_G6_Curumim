# GOFs Comportamentais

## Command

&emsp;&emsp;O command é um padrão comportamental que transforma uma solicitação em um objeto independente que possui todas as informações sobre essa solicitação.<br>
&emsp;&emsp;Esse padrão encapsula ações como objetos, permitindo que o sistema tenha um baixo acoplamento, separando os objetos que emitem uma soliticação dos objetos que processam a soliticação. As soliticações eo código que as processa são chamados respectivamente de eventos e manipuladores de eventos.<br>
&emsp;&emsp;No nosso projeto, a command é utilizada em algumas situações. No exemplo mostramos a command sendo usada para englobar as ações que o admin pode fazer envolvendo os professores.

~~~javascript
function TeacherButtons() {
    return (
        <div className="teacherButtonsDiv">
            <button className="registerTeacherButton" onclick="RegisterCommand(teacher)">Registrar</button>
            <button className="excludeTeacherButton" onclick="ExcludeCommand(teacher)">Excluir</button>
            <button className="updateTeacherButton" onclick="UpdateCommand(teacher)">izar</button>
            <button className="addTeacherToClassButton" onclick="addToClassCommand(teacherAtual, class)">Adicionar a uma turma</button>
        </div>
    )
}
~~~

&emsp;&emsp;A própria interface da aplicação é a cliente que utiliza a command, por meio dos botões.

~~~javascript
function registerTeacher(teacher) { 
    teachersList.push(teacher) // Registrando um professor
}

function excludeTeacher(teacher) { 
    thisTeacher = childrenList.indexOf(teacher.name)
    childrenList.remove(thisKid) // Excluindo um professor
}

function updateTeacher(teacher) { 
    thisTeacher = childrenList.indexOf(teacher.name)
    thisTeacher = thisKid // Atualizando um professor
}

function addTeacherToClass(teacher, class) { 
    class.teacher(teacher) // Adicionando um professor a uma sala
}

var Command = function (action, teacher) {
    this.action = execute;
    this.value = teacher;
}

var RegisterCommand = function (value) {
    return new Command(registerTeacher, value);
};

var ExcludeCommand = function (value) {
    return new Command(excludeTeacher, value);
};

var UpdateCommand = function (value) {
    return new Command(updateTeacher, value);
};

var addToClassCommand = function (value) {
    return new Command(addTeacherToClass, value);
};
~~~

&emsp;&emsp;Por fim as ações de registrar, excluir, atualizar e atribuir a turma, com o objeto professor, que contém os atributos capturados na interface.


## Iterator
&emsp;&emsp;O padrão Iterator, ou Iterador, permite com que se navegue em coleções de elementos. Propõe a criação de classes que implementem métodos especialmente pensados para realizar as iterações dado um conunto de elementos.

![Observer](../assets/imagens/gofs/gof-iterator.png)
<center>[Figura 1: Padrão iterator.](../assets/imagens/gofs/gof-iterator.png)[ Fonte: dofactory.com](https://www.dofactory.com/javascript/design-patterns/iterator#diagram)</center>

&emsp;&emsp;Esse padrão pode ser aplicado nas situações de iteração de qualquer tipo de coleção de elementos mas pode ser considerada uma aplicação exagerada caso o sistema em questão trabalhe apenas com coleções simples e de baixa coomplexidade.<br>
&emsp;&emsp;Sendo assim, como as coleções do projeto não têm uma complexidade elevada e as situações de iterações são bem específicas e pontuais, conclui-se que esse padrão não se aplicaria de forma muito vantajosa.

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
~~~javascript
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
~~~
## Observer
&emsp;&emsp;O padrão de projeto Observer, ou Observador, permite que objetos interessados sejam notificados sobre mudanças de estado ou ocorrência de eventos em outros objetos que estão sendo observado por eles.<br>
&emsp;&emsp;Esse padrão propõe a implementação de mecanismos de inscrição onde objetos possam estar contidos para receber as mudanças de estados e os eventos ocorridos no objeto observado. Praticamente, trata-se de um conjunto de métodos públicos que permitam com que os objetos observadores se incluam e se retirem do vetor de observadores também contido na classe observada. Além disso, é preciso de um método que notifique cada objeto contido no vetor de observadores.

![Observer](../assets/imagens/gofs/gof-observer.png)
<center>[Figura 2: Padrão observer](../assets/imagens/gofs/gof-observer.png)</center>

&emsp;&emsp;Esse padrão é muito bem aplicado em situações onde a mudança de estado de objetos pode acarretar a mudança de estado de outros objetos de forma bem específica. Sendo assim, notou-se que esse padrão não se aplicaria muito bem no escopo do nosso projeto pois não foi encontrada nenhuma situação semelhante no que tange o funcionamento do sistema.


## State
&emsp;&emsp;O padrão State permite com que um objeto altere o seu comportamento de acordo com o seu estado interno. Dessa forma, esse padrão sugere a implementação de classes para representar os diferentes estados do objeto e definir o comportamento de seus métodos e funções.

![State](../assets/imagens/gofs/gof-state.jpg)
<center>[Figura 3: Padrão state.](../assets/imagens/gofs/gof-state.png)[ Fonte: dofactory.com](https://www.dofactory.com/javascript/design-patterns/state#diagram)</center>

&emsp;&emsp;Esse padrão é bem aplicado quando existem objetos que possam mudar de status de forma a modificar os seus comportamentos. Sendo assim, a equipe optou por adaptar a modelagem de forma a permitir a utilização desse padrão.<br>
&emsp;&emsp;Basicamente, esse padrão será utilizado para trabalhar duas classes semelhantes: ActivityController e a EventController. Será implementada a classe ProjectController para identificar o contexto de utilização de forma que ActivityController e a EventController representem o seu estado ou, mais apropriadamente, tipo.<br>
&emsp;&emsp;Para essa implementação, também será utilizado o auxílio do padrão criacional [Singleton]() na classe ProjectController.

![State](../assets/imagens/gofs/gof-state-diagram.png)
<center>[Figura 4: Padrão state.](../assets/imagens/gofs/gof-state-diagram.png)</center>

&emsp;&emsp;A seguir tem-se um exemplo resumido a nível do código do que pode ser feito na implementação desse padrão.

~~~javascript
class ProjectController {
    #currentType;
    #instance

    function creataInstance (type){
        if(!instance){
            instance = new ProjectController(type);
        }else if(instance.currentType.getType != type){
            instance.currentType.change();
        }

        return instance;
    }

    constructor(type){
        if (type === "Activity"){
            this.currentType = new ActivityController(this);

        }else if(type === "Event"){
            this.currentType = new EventController(this);
        }else{
            //Err invalid type
        }
    }
    function setType(type){
        this.currentType = type;
    }

    function create(req, res) {
        this.currentType.create(req, res);
    }

    function update(res, res) {
        this.currentType.creat(req, res);
    }
}

class ActivityController{
    #project;
    #type = "Activity";

    constructor(project){
        this.project = project
    }

    function getType(){
        return this.type;
    }

    function change(){
        this.project.setType(new EventController(this.project))
    }

    function create(req, res){
        //create an Activity
    }

    function update(req, res){
        //update an Activity
    }
}

class EventController{
    #project;
    #type = "Event";

    constructor(project){
        this.project = project
    }

    function getType(){
        return this.type;
    }

    function change(){
        this.project.setType(new ActivityController(this.project))
    }

    function create(req, res){
        //create an Event
    }

    function update(req, res){
        //update an Event
    }
}
~~~

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
> - SHVETS, Alexander. **Dive Into Design Patterns**. Disponível em <https://refactoring.guru/design-patterns>. Acesso em 18/09/2021.
> - DOFACTORY. **Javascript Design Patterns**. Disponível em <https://www.dofactory.com/javascript/design-patterns/>. Acesso em 18/09/2021.

## Versionamento
| Versão | Data | Modificação | Autor |
|--|--|--|--|
|1.0|10/09/2021| Abertura do documento | Mateus O. Patrício |
|1.1|16/09/2021| Introdução ao Mediator e inclusão de bibliografia [2] | Edson Soares |
|1.2|16/09/2021| Inclusão do diagrama Mediator | Edson Soares |
|1.3|17/09/2021| Explicação do diagrama de classe | Edson Soares |
|1.4|18/09/2021| Adição dos padrões Command, Iterator, Observer e State | Daniel Porto, Enzo Gabriel |
|1.5|19/09/2021| Construção da estutura de objetos | Edson Soares |
|1.6|19/09/2021| Implementação | Edson Soares |
|1.7|19/09/2021| Revisão do padrão Mediator | Bruno Felix e Eliseu Kadesh |
|1.8|19/09/2021| Revisão dos padrões Observer, State, Command e Iterator | Bruno Felix e Gabriel Bonifácio |
