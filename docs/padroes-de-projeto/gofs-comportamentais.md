# GOFs Comportamentais

## Command

&emsp;&emsp;O command é um padrão comportamental que transforma uma solicitação em um objeto independente que possui todas as informações sobre essa soliticação.<br>
&emsp;&emsp;Esse padrão encapsula ações como objetos, permitindo que o sistema tenha um baixo acoplamento, separando os objetos que emitem uma soliticação dos objetos que processam a soliticação. As soliticações eo código que as processa são chamdos respectivamente de eventos e manipuladores de eventos.<br><br>

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
&emsp;&emsp;Sendo assim, como as coleções do projeto não têm uma complexidade elevada e as situações de iterações são bem específicas e pentuais, conclui-se que esse padrão não se aplicaria de forma muito vantajosa.

## Mediator


## Observer
&emsp;&emsp;O padrão de projeto Observer, ou Observador, permite que objetos interessados sejam notificados sobre mudanças de estado ou ocorrência de eventos em outros objetos que estão sendo observado por eles.<br>
&emsp;&emsp;Esse padrão propõe a implementação de mecanismos de inscrição onde objetos possam estar contidos para receber as mudanças de estados e os eventos ocorridos no objeto observado. Praticamente, trata-se de um conjunto de métodos públicos que permitam com que os objetos observadores se incluam e se retirem do vetor de observadores também contido na classe observada. Além disso, é preciso de um método que notifique cada objeto contido no vetor de observadores.

![Observer](../assets/imagens/gofs/gof-observer.png)
<center>[Figura 1: Padrão observer](../assets/imagens/gofs/gof-observer.png)</center>

&emsp;&emsp;Esse padrão é muito bem aplicado em situações onde a mudança de estado de objetos pode acarretar a mudança de estado de outros objetos de forma bem específica. Sendo assim, notou-se que esse padrão não se aplicaria muito bem no escopo do nosso projeto pois não foi encontrada nenhuma situação semelhante no que tange o funcionamento do sistema.


## State

## Strategy


## Template Method


## Visitor


## Memento


## Chain Of Responsability



## Bibliografia

> - LARMAN, Craig. <b>Utilizando UML e Padrões</b>: Uma introdução à análise e ao projeto orientados a objetos e ao desenvolvimento iterativo. 3. ed. [S. l.: s. n.], 2004.


## Versionamento
| Versão | Data | Modificação | Autor |
|--|--|--|--|
|1.0|10/09/2021| Abertura do documento | Mateus O. Patrício |