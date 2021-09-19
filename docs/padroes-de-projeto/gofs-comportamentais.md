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

> - LARMAN, Craig. <b>Utilizando UML e Padrões</b>: Uma introdução à análise e ao projeto orientados a objetos e ao desenvolvimento iterativo. 3. ed. [S. l.: s. n.], 2004.
> - SHVETS, Alexander. **Dive Into Design Patterns**. Disponível em <https://refactoring.guru/design-patterns>. Acesso em 18/09/2021.
> - DOFACTORY. **Javascript Design Patterns**. Disponível em <https://www.dofactory.com/javascript/design-patterns/>. Acesso em 18/09/2021.


## Versionamento
| Versão | Data | Modificação | Autor |
|--|--|--|--|
|1.0|10/09/2021| Abertura do documento | Mateus O. Patrício |
|1.1|18/09/2021| Adição dos padrões Command, Iterator, Observer e State | Daniel Porto, Enzo Gabriel |