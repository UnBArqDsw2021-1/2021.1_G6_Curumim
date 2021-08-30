# Product Backlog
## Introdução
&emsp;&emsp;Da perspectiva das metodologias ágeis, principalmente o SCRUM, o backlog do produto se trata de um conjunto de requisições do cliente e de pendências que serão implementadas no produto pela equipe de desenvolvimento. Os itens que compõem o backlog geralmente são as histórioas de usuário, mas esse artefato pode conter qualquer requisição do cliente e pode estar organizado de forma a possuir muitos graus de granularidade sempre com o objetivo de facilitar e promover entregas e iterações de qualidade.

## Metodologia
&emsp;&emsp;O presente artefato foi desenvolvido ao final da [design sprint](./base/design-sprint/doc-design-sprint.md) e ajustado mais tarde na etapa de modelagem de forma a ser um compilado detalhado e bem especificado de tudo o que foi levantado para o desenvolvimento do projeto.<br>
&emsp;&emsp;Dessa forma, foram analizados os artefatos até então produzidos e definidos os itens que estão presentes em três níveis de granularidade (épicos, features e histórias de usuário), sempre levando em consideração as prioridades e a restreabilidade.

## 1. Épicos
&emsp;&emsp;Um épico determina um conjunto de features que precisam ser desenvolvidas e tem o objetivo de realizar um Tema o qual seria um grau de granularidade superior que englobaria um conjunto de épicos<br>
&emsp;&emsp;Como foram poucos os temas identificados no projeto de forma que sempre abordariam grupos bem definidos de funcionalidades e não haveriam muitas subdivisões em épicos diferentes, a equipe optou por trabalhar com os épicos sendo o primeiro grau de granularidae e definiu os quatro épicos a seguir.

| **ID** | **Descrição** |
| :-: | --- |
| **E1** | Perfil                     |
| **E2** | [Atividades](../base/requisitos/modelagem/lexicos/#lexico-atividade) e [professor](../base/requisitos/modelagem/lexicos/#lexico-professor)     |
| **E3** | Comunicação e [notificações](../base/requisitos/modelagem/lexicos/#lexico-notificacao) |
| **E4** | [Administração](../base/requisitos/modelagem/lexicos/#lexico-administrador)              |


## 2. Features
&emsp;&emsp;Uma feature determina um conjunto de histórias de usuário que precisam ser implementadas e satisfeitas e tem o objetivo de realizar um épico<br>
&emsp;&emsp;Segue a lista de features definida.

| **Épico** | **ID** | **Descrição** |
| :-: | :-: | --- |
| **E3** | **FT01** | Comunicação entre [responsáveis](../base/requisitos/modelagem/lexicos/#lexico-responsavel), [professores](../base/requisitos/modelagem/lexicos/#lexico-professor) e [administradores](../base/requisitos/modelagem/lexicos/#lexico-administrador) |
| **E3** | **FT02** | Recebimento de [notificações](../base/requisitos/modelagem/lexicos/#lexico-notificacao)                                     |
| **E4** | **FT03** | Criação e gerência de [turmas](../base/requisitos/modelagem/lexicos/#lexico-turma) e [eventos](../base/requisitos/modelagem/lexicos/#lexico-evento)                        |
| **E4** | **FT04** | Cadastro de [criança](../base/requisitos/modelagem/lexicos/#lexico-crianca) e [professor](../base/requisitos/modelagem/lexicos/#lexico-professor)                               |
| **E2** | **FT05** | Lançamento e acompanhamento da [presença](../base/requisitos/modelagem/lexicos/#lexico-presenca)                       |
| **E3** | **FT06** | Criação e gerência de [atividade](../base/requisitos/modelagem/lexicos/#lexico-atividade) e [anotações](../base/requisitos/modelagem/lexicos/#lexico-anotacao)                   |
| **E1** | **FT07** | Acompanhamento das [atividade](../base/requisitos/modelagem/lexicos/#lexico-atividade), [eventos](../base/requisitos/modelagem/lexicos/#lexico-evento)   e [agenda](../base/requisitos/modelagem/lexicos/#lexico-agenda)               |
| **E1** | **FT08** | Acompanhamento das [turmas](../base/requisitos/modelagem/lexicos/#lexico-turma)                                     |


## 3. Histórias de Usuário
&emsp;&emsp;Descrita da perspectiva de um [usuário](../base/requisitos/modelagem/lexicos/#lexico-usuario) final, uma história de usuário determina um objetivo final do mesmo na utilização de funcionalidades da aplicação desenvolvida. Para a presente especificação, esse item será a menor unidade de trabalho de forma com que a implementação precise satisfaze-la<br>
&emsp;&emsp;O padrão de escrita das histórias será o seguinte:
> Eu, como << TIPO DE [USUÁRIO](../base/requisitos/modelagem/lexicos/#lexico-usuario) >>, desejo << OBJETIVO >>.

&emsp;&emsp;Segue a lista de histórias de usuario definida e priorizada.

| **ID** | **Descrição** |
| :-: | :-: |
| **US01** | Eu, como [administrador](../base/requisitos/modelagem/lexicos/#lexico-administrador), desejo cadastrar uma [criança](../base/requisitos/modelagem/lexicos/#lexico-crianca) no [centro educacional](../base/requisitos/modelagem/lexicos/#lexico-centro-educacional) |
| **US02** | Eu, como [administrador](../base/requisitos/modelagem/lexicos/#lexico-administrador), desejo cadastrar um [professor](../base/requisitos/modelagem/lexicos/#lexico-professor) no [centro educacional](../base/requisitos/modelagem/lexicos/#lexico-centro-educacional) |
| **US03** | Eu, como [administrador](../base/requisitos/modelagem/lexicos/#lexico-administrador), desejo criar, editar e excluir uma [turma](../base/requisitos/modelagem/lexicos/#lexico-turma) para o [centro educacional](../base/requisitos/modelagem/lexicos/#lexico-centro-educacional) |
| **US04** | Eu, como [professor](../base/requisitos/modelagem/lexicos/#lexico-professor), desejo criar, editar e excluir [atividades](../base/requisitos/modelagem/lexicos/#lexico-atividade) para minha [turma](../base/requisitos/modelagem/lexicos/#lexico-turma) |
| **US05** | Eu, como [responsável](../base/requisitos/modelagem/lexicos/#lexico-responsavel), desejo fazer cadastro e login na aplicação |
| **US06** | Eu, como [responsável](../base/requisitos/modelagem/lexicos/#lexico-responsavel), desejo ter um espaço que contenha as [atividades](../base/requisitos/modelagem/lexicos/#lexico-atividade), [eventos](../base/requisitos/modelagem/lexicos/#lexico-evento) e [agenda](../base/requisitos/modelagem/lexicos/#lexico-agenda) dos próximos dias |
| **US07** | Eu, como [responsável](../base/requisitos/modelagem/lexicos/#lexico-responsavel), desejo visualizar a lista de todas as [atividades](../base/requisitos/modelagem/lexicos/#lexico-atividade) da minha [criança](../base/requisitos/modelagem/lexicos/#lexico-crianca) |
| **US08** | Eu, como [responsável](../base/requisitos/modelagem/lexicos/#lexico-responsavel), desejo visualizar os detalhes de uma [atividade](../base/requisitos/modelagem/lexicos/#lexico-atividade) da minha [criança](../base/requisitos/modelagem/lexicos/#lexico-crianca) |
| **US09** | Eu, como [administrador](../base/requisitos/modelagem/lexicos/#lexico-administrador), desejo criar, editar e excluir um [evento](../base/requisitos/modelagem/lexicos/#lexico-evento) para o [centro educacional](../base/requisitos/modelagem/lexicos/#lexico-centro-educacional) |
| **US10** | Eu, como [responsável](../base/requisitos/modelagem/lexicos/#lexico-responsavel), desejo visualizar a lista de todos os [eventos](../base/requisitos/modelagem/lexicos/#lexico-evento) do [centro educacional](../base/requisitos/modelagem/lexicos/#lexico-centro-educacional) |
| **US11** | Eu, como [responsável](../base/requisitos/modelagem/lexicos/#lexico-responsavel), desejo visualizar os detalhes de um [evento](../base/requisitos/modelagem/lexicos/#lexico-evento) do [centro educacional](../base/requisitos/modelagem/lexicos/#lexico-centro-educacional) |
| **US12** | Eu, como [professor](../base/requisitos/modelagem/lexicos/#lexico-professor), desejo criar, editar e excluir [anotações](../base/requisitos/modelagem/lexicos/#lexico-anotacao) para uma [criança](../base/requisitos/modelagem/lexicos/#lexico-crianca) |
| **US13** | Eu, como [responsável](../base/requisitos/modelagem/lexicos/#lexico-responsavel), desejo visualizar a [agenda](../base/requisitos/modelagem/lexicos/#lexico-agenda), com [anotações](../base/requisitos/modelagem/lexicos/#lexico-anotacao), da minha [criança](../base/requisitos/modelagem/lexicos/#lexico-crianca) |
| **US14** | Eu, como [professor](../base/requisitos/modelagem/lexicos/#lexico-professor), desejo visualizar a lista de todas as minhas [turmas](../base/requisitos/modelagem/lexicos/#lexico-turma) |
| **US15** | Eu, como [professor](../base/requisitos/modelagem/lexicos/#lexico-professor), desejo visualizar os detalhes, [atividades](../base/requisitos/modelagem/lexicos/#lexico-atividade) e [alunos](../base/requisitos/modelagem/lexicos/#lexico-aluno) de uma [turma](../base/requisitos/modelagem/lexicos/#lexico-turma) |
| **US16** | Eu, como [responsável](../base/requisitos/modelagem/lexicos/#lexico-responsavel), desejo receber [notificações](../base/requisitos/modelagem/lexicos/#lexico-notificacao) sobre uma [atividade](../base/requisitos/modelagem/lexicos/#lexico-atividade) da minha [criança](../base/requisitos/modelagem/lexicos/#lexico-crianca) |
| **US17** | Eu, como [responsável](../base/requisitos/modelagem/lexicos/#lexico-responsavel), desejo receber [notificações](../base/requisitos/modelagem/lexicos/#lexico-notificacao) sobre a [agenda](../base/requisitos/modelagem/lexicos/#lexico-agenda) e as [anotações](../base/requisitos/modelagem/lexicos/#lexico-anotacao) da minha [criança](../base/requisitos/modelagem/lexicos/#lexico-crianca) |
| **US18** | Eu, como [responsável](../base/requisitos/modelagem/lexicos/#lexico-responsavel), desejo receber [notificações](../base/requisitos/modelagem/lexicos/#lexico-notificacao) sobre um [evento](../base/requisitos/modelagem/lexicos/#lexico-evento) do [centro educacional](../base/requisitos/modelagem/lexicos/#lexico-centro-educacional) |
| **US19** | Eu, como [professor](../base/requisitos/modelagem/lexicos/#lexico-professor), desejo lançar [presença](../base/requisitos/modelagem/lexicos/#lexico-lancar-presenca) da minha [turma](../base/requisitos/modelagem/lexicos/#lexico-turma) |
| **US20** | Eu, como [responsável](../base/requisitos/modelagem/lexicos/#lexico-responsavel), desejo acompanhar o andamento das [presenças](../base/requisitos/modelagem/lexicos/#lexico-lancar-presenca) da minha [criança](../base/requisitos/modelagem/lexicos/#lexico-crianca) |
| **US21** | Eu, como [responsável](../base/requisitos/modelagem/lexicos/#lexico-responsavel), desejo receber [notificações](../base/requisitos/modelagem/lexicos/#lexico-notificacao) sobre a entrada e saída da minha [criança](../base/requisitos/modelagem/lexicos/#lexico-crianca) |
| **US22** | Eu, como [responsável](../base/requisitos/modelagem/lexicos/#lexico-responsavel), desejo conversar com o [administrador](../base/requisitos/modelagem/lexicos/#lexico-administrador)  do [centro educacional](../base/requisitos/modelagem/lexicos/#lexico-centro-educacional) |
| **US23** | Eu, como [responsável](../base/requisitos/modelagem/lexicos/#lexico-responsavel), desejo conversar com o [professor](../base/requisitos/modelagem/lexicos/#lexico-professor) da [turma](../base/requisitos/modelagem/lexicos/#lexico-turma) da minha [criança](../base/requisitos/modelagem/lexicos/#lexico-crianca) |
| **US24** | Eu, como [responsável](../base/requisitos/modelagem/lexicos/#lexico-responsavel), desejo receber [relatórios](../base/requisitos/modelagem/../base/requisitos/elicitacao/brainstorming/#rflexicos/#lexico-relatorio) esporádicos sobre tudo produzido pela minha [criança](../base/requisitos/modelagem/lexicos/#lexico-crianca) |

| **Épico** | **Feacture** | **ID** | **Rastreabilidade** | **MoSCoW** | **Pontuação** |
| :-: | :-: | :-: | :-: | :-: | :-: |
| **E4** | **FT04** | **US01** | [RF_07](../base/requisitos/elicitacao/brainstorming/#rf7) | Must |8|
| **E4** | **FT04** | **US02** | [RF_08](../base/requisitos/elicitacao/brainstorming/#rf8) | Must |5|
| **E4** | **FT03** | **US03** | [RF_06](../base/requisitos/elicitacao/brainstorming/#rf6) | Must |5|
| **E3** | **FT06** | **US04** | [RF_12](../base/requisitos/elicitacao/brainstorming/#rf12) | Must |5|
| **E1** | **FT07** | **US05** | [RF_11](../base/requisitos/elicitacao/brainstorming/#rf11) | Must |5|
| **E1** | **FT07** | **US06** | [RF_11](../base/requisitos/elicitacao/brainstorming/#rf11) | Must |8|
| **E1** | **FT07** | **US07** | [RF_11](../base/requisitos/elicitacao/brainstorming/#rf11) | Must |5|
| **E1** | **FT07** | **US08** | [RF_11](../base/requisitos/elicitacao/brainstorming/#rf11) | Must |5|
| **E4** | **FT03** | **US09** | [RF_09](../base/requisitos/elicitacao/brainstorming/#rf9) | Could |5|
| **E1** | **FT07** | **US10** | [RF_11](../base/requisitos/elicitacao/brainstorming/#rf11) | Must |5|
| **E1** | **FT07** | **US11** | [RF_11](../base/requisitos/elicitacao/brainstorming/#rf11) | Must |5|
| **E3** | **FT06** | **US12** | [RF_14](../base/requisitos/elicitacao/brainstorming/#rf) | Should |5|
| **E1** | **FT07** | **US13** | [RF_11](../base/requisitos/elicitacao/brainstorming/#rf11) | Must |5|
| **E1** | **FT08** | **US14** | [RF_12](../base/requisitos/elicitacao/brainstorming/#rf) | Must |5|
| **E1** | **FT08** | **US15** | [RF_12](../base/requisitos/elicitacao/brainstorming/#rf12) | Must |5|
| **E3** | **FT02** | **US16** | [RF_03](../base/requisitos/elicitacao/brainstorming/#rf3) | Should |8|
| **E3** | **FT02** | **US17** | [RF_14](../base/requisitos/elicitacao/brainstorming/#rf14) | Should |8|
| **E3** | **FT02** | **US18** | [RF_05](../base/requisitos/elicitacao/brainstorming/#rf5) | Won't |8|
| **E2** | **FT05** | **US19** | [RF_13](../base/requisitos/elicitacao/brainstorming/#rf13) | Could |3|
| **E2** | **FT05** | **US20** | [RF_11](../base/requisitos/elicitacao/brainstorming/#rf11) | Must |5|
| **E3** | **FT02** | **US21** | [RF_04](../base/requisitos/elicitacao/brainstorming/#rf4) | Could |8|
| **E3** | **FT01** | **US22** | [RF_02](../base/requisitos/elicitacao/brainstorming/#rf2) | Could |8|
| **E3** | **FT01** | **US23** | [RF_01](../base/requisitos/elicitacao/brainstorming/#rf1) | Should |8|
| **E1** | **FT07** | **US24** | [RF_10](../base/requisitos/elicitacao/brainstorming/#rf10) | Could |5|

## Bibliografia
> - Videoaulas e materiais complementares presentes no moodle da disciplina Arquitetura e Desenho de Software. Disponível em <https://aprender3.unb.br/course/view.php?id=8603>. Acesso em: 14 ago. 2021.
> - REINEHR, Sheila. Engenharia de Requisitos. sagah, Porto Alegre, 2020. Disponível em <https://integrada.minhabiblioteca.com.br/reader/books/9786556900674/>. Acesso em: 27/08/2021.
> - RADIGAN, Dan. O backlog do produto: sua lista de tarefas definitiva. Atlassian. Disponível em <https://www.atlassian.com/br/agile/scrum/backlogs>. Acesso em: 27/08/2021.
> - REHKOPF, Max. User Stories with Examples and Template. Atlassian. Disponível em <https://www.atlassian.com/agile/project-management/user-stories>. Acesso em: 27/08/2021.
> - Ventura, Plínio. Epic, Feature e User Story: O que são e como se relacionam estes três artefatos no contexto de um product backlog. Até o momento. Disponível em <https://www.ateomomento.com.br/epic-feature-e-user-story/>. Acesso em: 27/08/2021.

## Versionamento

| **Data** | **Versão** | **Modificação** | **Autor** |
| --- | --- | --- | --- |
| 04/08/2021 | 0.1 | Abertura do documento        | Bruno Félix |
| 05/08/2021 | 1.0 | Desenvolvimento do documento | Bruno Félix |
| 05/08/2021 | 1.1 | Revisão por pares | Daniel Porto, Enzo Gabriel |
| 06/08/2021 | 1.2 | Inserção Lexicos             | Bruno Félix |
| 13/08/2021 | 1.3 | Corrigindo links lexicos     | Bruno Félix |
| 14/08/2021 | 1.4 | Entrega 2 - Inserção do MoSCoW | Bruno Félix |
| 18/08/2021 | 1.5 | Entrega 2 - Retirada Tag Iniciativa Extra | Bruno Félix |
| 21/08/2021 | 1.6 | Correção dos links dos léxicos | Gabriel Bonifácio |
| 25/08/2021 | 1.7 | Adição da navegabilidade na raestreabilidade | Daniel Porto |
| 27/08/2021 | 2.0 | Adição da introdução, metodologia, bibliografia e maiores explicações sobre os itens | Daniel Porto |
| 28/08/2021 | 2.1 | Revisão por pares | Edson Soares, Eliseu Kadesh|