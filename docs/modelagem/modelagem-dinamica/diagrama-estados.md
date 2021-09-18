## Introdução
&emsp;&emsp;Os diagramas de estados, também chamados de diagrama de máquina de estados, é um dos tipos de diagramas UML que visa demonstrar as transições entre os diferentes objetos que compõem o sistema. Basicamente ele visa armazenar o status de um objeto em um determinado momento para então poder modificar essa tal status de acordo com a entrada recebida.

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

#### Realização do cadastro de [crianças](../../../base/requisitos/modelagem/lexicos/#lexico-crianca) e [professores](../../../base/requisitos/modelagem/lexicos/#lexico-professor)
![Cadastro de crianças e professores](../../../assets/imagens/diagrama-estados/cadastro-crianca-professor.png)
<center>[Figura 2: Cadastro de crianças e professores](../../../assets/imagens/diagrama-estados/cadastro-crianca-professor.png)</center><br>
&emsp;&emsp;No diagrama 2 foram retratados os estados durante a realização de um cadastro de criança ou professor por um administrador.<br>
&emsp;&emsp;O diagrama se inicia no estado de "buscando aluno/professor", um vez que se deseja evitar a duplicação de cadastros, seguindo para dois estados possíveis, um em que o usuário já existe, então a tarefa é encerrada e outro em que são exigidos os dados do novo usuário, por fim o caminho se ramifica entre os estados de descartar o cadastro ou salvar os dados preenchidos.<br>

#### Realização do gerenciamento de [turmas](../../../base/requisitos/modelagem/lexicos/#lexico-turma)
![Gerenciamento de turmas](../../../assets/imagens/diagrama-estados/gerencia-turma.png)
<center>[Figura 3: Gerenciamento de turmas](../../../assets/imagens/diagrama-estados/gerencia-turma.png)</center><br>
&emsp;&emsp;No diagrama 3 foram retratados os estados durante a realização do gerenciamento de turmas.<br>
&emsp;&emsp;O processo se inicia na busca pela turma ou evento, se ramificando em cadastrar nova turma/evento caso não exista, ou visualizar a turma/evento caso exista, sendo possível entrar em dois outros estados, o de editar a turma/evento ou deletar a turma/evento, sendo então nos estados de editar e cadastrar turma/evento a possibilidade de dois estado, o de salvar ou o descartar a criação/edição, sendo por fim finalizada a atividade.<br>

#### [Lançamento de presenças](../../../base/requisitos/modelagem/lexicos/#lexico-lancar-presenca)
![Lançamento de presenças](../../../assets/imagens/diagrama-estados/lancamento-presenca.png)
<center>[Figura 4: Lançamento de presenças](../../../assets/imagens/diagrama-estados/lancamento-presenca.png)</center>

## Bibliografia
> - LUCIDCHART. O que é um diagrama de máquina de estados?. Disponível em: <https://www.lucidchart.com/pages/pt/o-que-e-diagrama-de-maquina-de-estados-uml>. Acesso em: 17 de ago. 2021.
> - Máquina de Estados. Disponível em: <http://msoo.pbworks.com/f/Diagrama+de+Estados.pdf>. Acesso em: 17 de ago. 2021.

## Versionamento
| Versão | Data | Modificação | Autor |
| :-: | -- | -- | -- |
|1.0| 18/08/2021 | Adição da introduçao, da metodologia, dos diagramas e da bibliografia  | Nilo Mendonça |
|1.1| 21/08/2021 | Adição da léxicos  | Bruno Félix |
|1.2| 21/08/2021 | Revisão por pares  | Enzo Gabriel e Gabriel Bonifácio |
|1.3| 18/09/2021 | Revisão do documento segundo feedback da professora  | Nilo Mendonça |
