## Introdução
&emsp;&emsp;Os diagramas de estados, também chamados de diagrama de máquina de estados, é um dos tipos de diagramas UML que visa demonstrar as transições entre os diferentes objetos que compõem o sistema. Basicamente ele visa armazenar o status de um objeto em um determinado momento para então poder modificar essa tal status de acordo com a entrada recebida.<br>
&emsp;&emsp;O uso do diagrama de estados normalmente está voltado para a modelagem dinâmica de classes, assim como os diagramas de atividades, porém o foco deste diagrama é descrever a evolução de estados de um objeto da classe (SILVA, 2007).<br>

&emsp;&emsp;Os principais elementos que constituem um diagrama de estados são:

- Estado inicial: Ponto inicial, onde começa a utilização do objeto;
- Evento ou Transição: Representa uma ação externa sobre um objeto;
- Estado: Representa um dos possíveis estados que um objeto pode ter;
- Ações: Processo associado à transição de estados. São representadas por "/", seguidas das ações contidas no estado. As ações são: 
	- Ação de entrada: executada para chegar a algum estado; 
	- Ação de atividade: é executada dentro do estado;
	- Ação de saída: executada quando se sai de um estado.
- Estado final: Ponto de saída do objeto.

## Diagramas
&emsp;&emsp;A seguir, os diagramas produzidos pelo grupo.

#### Comunicação entre os [responsáveis](../../../base/requisitos/modelagem/lexicos/#lexico-responsavel) e o [Centro Educacional](../../../base/requisitos/modelagem/lexicos/#lexico-centro-educacional)
![Comunicação](../../../assets/imagens/diagrama-estados/comunicacao.png)
<center>[Figura 1: Comunicação](../../../assets/imagens/diagrama-estados/comunicacao.png)</center>
&emsp;&emsp;No diagrama 1 foram retratados os estados durante a comunicação entre os responsáveis e o centro educacional.<br>
&emsp;&emsp;O diagrama se inicia no estado de <b>comunicando com o centro educacional</b>, uma vez que se deseja garantir a autenticação do usuário, seguindo para dois estados possíveis, um em que o <b>usuário já tem cadastro</b> e então a tarefa é fazer o login. O outro estado é que o <b>usuário não tem cadastro</b> e então a tarefa é fazer o cadastro. Por fim o caminho continua com os estados <b>acessando o chat da aplicação</b>, <b>enviando mensagem</b> e por último, <b>aguardando mensagem</b>.<br>

#### Realização do cadastro de [crianças](../../../base/requisitos/modelagem/lexicos/#lexico-crianca) e [professores](../../../base/requisitos/modelagem/lexicos/#lexico-professor)
![Cadastro de crianças e professores](../../../assets/imagens/diagrama-estados/cadastro-crianca-professor.png)
<center>[Figura 2: Cadastro de crianças e professores](../../../assets/imagens/diagrama-estados/cadastro-crianca-professor.png)</center><br>
&emsp;&emsp;No diagrama 2 foram retratados os estados durante a realização de um cadastro de criança ou professor por um administrador.<br>
&emsp;&emsp;O diagrama se inicia no estado de <b>buscando aluno/professor</b>, um vez que se deseja evitar a duplicação de cadastros, seguindo para dois estados possíveis, um em que o <b>usuário já existe</b>, então a tarefa é encerrada e outro em que são <b>exigidos os dados do novo usuário</b>, por fim o caminho se ramifica entre os estados de <b>descartar o cadastro</b> ou <b>salvar os dados preenchidos</b>.<br>

#### Realização do gerenciamento de [turmas](../../../base/requisitos/modelagem/lexicos/#lexico-turma)
![Gerenciamento de turmas](../../../assets/imagens/diagrama-estados/gerencia-turma.png)
<center>[Figura 3: Gerenciamento de turmas](../../../assets/imagens/diagrama-estados/gerencia-turma.png)</center><br>
&emsp;&emsp;No diagrama 3 foram retratados os estados durante a realização do gerenciamento de turmas.<br>
&emsp;&emsp;O processo se inicia em <b>buscando pela turma ou evento</b>, se ramificando em <b>cadastrando nova turma/evento</b> caso não exista, ou <b>visualizando a turma/evento</b> caso exista, sendo possível entrar em dois outros estados, o de <b>editando a turma/evento</b> ou <b>removendo a turma/evento</b>, sendo então nos estados de editar e cadastrar turma/evento a possibilidade de dois estados, o de <b>salvando</b> ou o <b>descartando</b> a criação/edição, sendo por fim finalizada a atividade.<br>

#### [Lançamento de presenças](../../../base/requisitos/modelagem/lexicos/#lexico-lancar-presenca)
![Lançamento de presenças](../../../assets/imagens/diagrama-estados/lancamento-presenca.png)
<center>[Figura 4: Lançamento de presenças](../../../assets/imagens/diagrama-estados/lancamento-presenca.png)</center>
&emsp;&emsp;No diagrama 4 foram retratados os estados durante o lançamento de presenças.<br>
&emsp;&emsp;O processo se inicia no estado <b>buscando turma</b> que se ramifica em dois estados, um em que a <b>turma não foi encontrada</b>, então a tarefa é encerrada. O outro é o estado em que a turma foi encontrada, aí o caminho continua com os estados <b>visualizando alunos</b>, <b>marcando alunos presentes</b> e por fim, <b>salvando cadastro</b>.<br>

## Bibliografia
> - [Diagrama de estados do projeto QRodízio](https://unbarqdsw.github.io/2020.1_G10_QRodizio/modelagem/diagramas_dinamicos/diagramas_estado.html#introducao);
> - [Diagrama de estados do projeto Stock](https://unbarqdsw.github.io/2020.1_G12_Stock/#/Modeling/Diagrams/Estado);
> - LUCIDCHART. O que é um diagrama de máquina de estados?. Disponível em: <https://www.lucidchart.com/pages/pt/o-que-e-diagrama-de-maquina-de-estados-uml>. Acesso em: 17 de ago. 2021.
> - Máquina de Estados. Disponível em: <http://msoo.pbworks.com/f/Diagrama+de+Estados.pdf>. Acesso em: 17 de ago. 2021.
> - SILVA, R. P. (2007). “UML 2 em Modelagem Orientada a Objetos”, 1ª ed., Florianópolis, SC, Brasil, Visual Books.

## Versionamento
| Versão | Data | Modificação | Autor |
| :-: | -- | -- | -- |
|1.0| 18/08/2021 | Adição da introduçao, da metodologia, dos diagramas e da bibliografia  | Nilo Mendonça |
|1.1| 21/08/2021 | Adição da léxicos  | Bruno Félix |
|1.2| 21/08/2021 | Revisão por pares  | Enzo Gabriel e Gabriel Bonifácio |
<<<<<<< HEAD
|1.3| 17/09/2021 | Revisão e correção do documento segundo feedback da professora | Edson Soares e Nilo Mendonça |
=======
|1.3| 18/09/2021 | Revisão do documento segundo feedback da professora  | Nilo Mendonça |
|1.4| 19/09/2021 | Revisão do documento segundo feedback da professora | Bruno Félix |
>>>>>>> a00ecc8cf0325f66992f77992500f73bd65d3e9d
