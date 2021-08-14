# Product Backlog

## 1. Épicos

| **ID** | **Descrição** |
| --- | --- |
| E1 | Perfil                     |
| E2 | [Atividades](/base/requisitos/modelagem/lexicos/#lexico-atividade) e [professor](/base/requisitos/modelagem/lexicos/#lexico-professor)     |
| E3 | Comunicação e [notificações](/base/requisitos/modelagem/lexicos/#lexico-notificacao) |
| E4 | [Administração](/base/requisitos/modelagem/lexicos/#lexico-administrador)              |


## 2. Features

| **Épico** | **ID** | **Descrição** |
| --- | --- | --- |
| E3 | FT01 | Comunicação entre [responsáveis](/base/requisitos/modelagem/lexicos/#lexico-responsavel), [professores](/base/requisitos/modelagem/lexicos/#lexico-professor) e [administradores](/base/requisitos/modelagem/lexicos/#lexico-administrador) |
| E3 | FT02 | Recebimento de [notificações](/base/requisitos/modelagem/lexicos/#lexico-notificacao)                                     |
| E4 | FT03 | Criação e gerência de [turmas](/base/requisitos/modelagem/lexicos/#lexico-turma) e [eventos](/base/requisitos/modelagem/lexicos/#lexico-evento)                        |
| E4 | FT04 | Cadastro de [criança](/base/requisitos/modelagem/lexicos/#lexico-crianca) e [professor](/base/requisitos/modelagem/lexicos/#lexico-professor)                               |
| E2 | FT05 | Lançamento e acompanhamento da [presença](/base/requisitos/modelagem/lexicos/#lexico-presenca)                       |
| E3 | FT06 | Criação e gerência de [atividade](/base/requisitos/modelagem/lexicos/#lexico-atividade) e [anotações](/base/requisitos/modelagem/lexicos/#lexico-anotacao)                   |
| E1 | FT07 | Acompanhamento das [atividade](/base/requisitos/modelagem/lexicos/#lexico-atividade), [eventos](/base/requisitos/modelagem/lexicos/#lexico-evento)   e [agenda](/base/requisitos/modelagem/lexicos/#lexico-agenda)               |
| E1 | FT08 | Acompanhamento das [turmas](/base/requisitos/modelagem/lexicos/#lexico-turma)                                     |


## 3. Histórias de Usuário

| **Épico** | **Feacture** | **ID** | **Descrição** | **Rastreabilidade** | **MoSCoW** |
| --- | --- | --- | --- | --- | --- |
| E4 | FT04 | US01 | Eu, como [administrador](/base/requisitos/modelagem/lexicos/#lexico-administrador), desejo cadastrar uma [criança](/base/requisitos/modelagem/lexicos/#lexico-crianca) no [centro de educacional](/base/requisitos/modelagem/lexicos/#lexico-centro-educacional) | RF_07 | Must |
| E4 | FT04 | US02 | Eu, como [administrador](/base/requisitos/modelagem/lexicos/#lexico-administrador), desejo cadastrar um [professor](/base/requisitos/modelagem/lexicos/#lexico-professor) no [centro de educacional](/base/requisitos/modelagem/lexicos/#lexico-centro-educacional) | RF_08 | Must |
| E4 | FT03 | US03 | Eu, como [administrador](/base/requisitos/modelagem/lexicos/#lexico-administrador), desejo criar, editar e excluir uma [turma](/base/requisitos/modelagem/lexicos/#lexico-turma) para o [centro de educacional](/base/requisitos/modelagem/lexicos/#lexico-centro-educacional) | RF_06 | Must |
| E3 | FT06 | US04 | Eu, como [professor](/base/requisitos/modelagem/lexicos/#lexico-professor), desejo criar, editar e excluir [atividades](/base/requisitos/modelagem/lexicos/#lexico-atividade) para minha [turma](/base/requisitos/modelagem/lexicos/#lexico-turma) | RF_12 | Must | 
| E1 | FT07 | US05 | Eu, como [responsável](/base/requisitos/modelagem/lexicos/#lexico-responsavel), desejo fazer cadastro e login na aplicação | RF_11 | Must |
| E1 | FT07 | US06 | Eu, como [responsável](/base/requisitos/modelagem/lexicos/#lexico-responsavel), desejo ter um espaço que contenha os [atividades](/base/requisitos/modelagem/lexicos/#lexico-atividade), [eventos](/base/requisitos/modelagem/lexicos/#lexico-evento) e [agenda](/base/requisitos/modelagem/lexicos/#lexico-agenda) dos próximos dias | RF_11 | Must |
| E1 | FT07 | US07 | Eu, como [responsável](/base/requisitos/modelagem/lexicos/#lexico-responsavel), desejo visualizar a lista de todas as [atividades](/base/requisitos/modelagem/lexicos/#lexico-atividade) da minha [criança](/base/requisitos/modelagem/lexicos/#lexico-crianca) | RF_11 | Must |
| E1 | FT07 | US08 | Eu, como [responsável](/base/requisitos/modelagem/lexicos/#lexico-responsavel), desejo visualizar os detalhes de uma [atividade](/base/requisitos/modelagem/lexicos/#lexico-atividade) da minha [criança](/base/requisitos/modelagem/lexicos/#lexico-crianca) | RF_11 | Must |
| E4 | FT03 | US09 | Eu, como [administrador](/base/requisitos/modelagem/lexicos/#lexico-administrador), desejo criar, editar e excluir um [evento](/base/requisitos/modelagem/lexicos/#lexico-evento) para o [centro de educacional](/base/requisitos/modelagem/lexicos/#lexico-centro-educacional) | RF_09 | Could |
| E1 | FT07 | US10 | Eu, como [responsável](/base/requisitos/modelagem/lexicos/#lexico-responsavel), desejo visualizar a lista de todos os [eventos](/base/requisitos/modelagem/lexicos/#lexico-evento) do [centro de educacional](/base/requisitos/modelagem/lexicos/#lexico-centro-educacional) | RF_11 | Must |
| E1 | FT07 | US11 | Eu, como [responsável](/base/requisitos/modelagem/lexicos/#lexico-responsavel), desejo visualizar os detalhes de um [evento](/base/requisitos/modelagem/lexicos/#lexico-evento) do [centro de educacional](/base/requisitos/modelagem/lexicos/#lexico-centro-educacional) | RF_11 | Must |
| E3 | FT06 | US12 | Eu, como [professor](/base/requisitos/modelagem/lexicos/#lexico-professor), desejo criar, editar e excluir [anotações](/base/requisitos/modelagem/lexicos/#lexico-anotacao) para uma [criança](/base/requisitos/modelagem/lexicos/#lexico-crianca) | RF_14 | Should |
| E1 | FT07 | US13 | Eu, como [responsável](/base/requisitos/modelagem/lexicos/#lexico-responsavel), desejo visualizar a [agenda](/base/requisitos/modelagem/lexicos/#lexico-agenda), com [anotações](/base/requisitos/modelagem/lexicos/#lexico-anotacao), da minha [criança](/base/requisitos/modelagem/lexicos/#lexico-crianca) | RF_11 | Must |
| E1 | FT08 | US14 | Eu, como [professor](/base/requisitos/modelagem/lexicos/#lexico-professor), desejo visualizar a lista de todas as minhas [turmas](/base/requisitos/modelagem/lexicos/#lexico-turma) | RF_12 | Must |
| E1 | FT08 | US15 | Eu, como [professor](/base/requisitos/modelagem/lexicos/#lexico-professor), desejo visualizar os detalhes, [atividades](/base/requisitos/modelagem/lexicos/#lexico-atividade) e [alunos](/base/requisitos/modelagem/lexicos/#lexico-aluno) de uma [turma](/base/requisitos/modelagem/lexicos/#lexico-turma) | RF_12 | Must |
| E3 | FT02 | US16 | Eu, como [responsável](/base/requisitos/modelagem/lexicos/#lexico-responsavel), desejo receber [notificações](/base/requisitos/modelagem/lexicos/#lexico-notificacao) sobre uma [atividade](/base/requisitos/modelagem/lexicos/#lexico-atividade) da minha [criança](/base/requisitos/modelagem/lexicos/#lexico-crianca) | RF_03 | Should |
| E3 | FT02 | US17 | Eu, como [responsável](/base/requisitos/modelagem/lexicos/#lexico-responsavel), desejo receber [notificações](/base/requisitos/modelagem/lexicos/#lexico-notificacao) sobre a [agenda](/base/requisitos/modelagem/lexicos/#lexico-agenda) e as [anotações](/base/requisitos/modelagem/lexicos/#lexico-anotacao) da minha [criança](/base/requisitos/modelagem/lexicos/#lexico-crianca) | RF_14 | Should |
| E3 | FT02 | US18 | Eu, como [responsável](/base/requisitos/modelagem/lexicos/#lexico-responsavel), desejo receber [notificações](/base/requisitos/modelagem/lexicos/#lexico-notificacao) sobre um [evento](/base/requisitos/modelagem/lexicos/#lexico-evento) do [centro de educacional](/base/requisitos/modelagem/lexicos/#lexico-centro-educacional) | RF_05 | Won't |
| E2 | FT05 | US19 | Eu, como [professor](/base/requisitos/modelagem/lexicos/#lexico-professor), desejo lançar [presença](/base/requisitos/modelagem/lexicos/#lexico-lancar-presenca) da minha [turma](/base/requisitos/modelagem/lexicos/#lexico-turma) | RF_13 | Could |
| E2 | FT05 | US20 | Eu, como [responsável](/base/requisitos/modelagem/lexicos/#lexico-responsavel), desejo acompanhar o andamento das [presenças](/base/requisitos/modelagem/lexicos/#lexico-lancar-presenca) da minha [criança](/base/requisitos/modelagem/lexicos/#lexico-crianca) | RF_11 | Must |
| E3 | FT02 | US21 | Eu, como [responsável](/base/requisitos/modelagem/lexicos/#lexico-responsavel), desejo receber [notificações](/base/requisitos/modelagem/lexicos/#lexico-notificacao) sobre a entrada e saída da minha [criança](/base/requisitos/modelagem/lexicos/#lexico-crianca) | RF_04 | Could |
| E3 | FT01 | US22 | Eu, como [responsável](/base/requisitos/modelagem/lexicos/#lexico-responsavel), desejo conversar com o [administrador](/base/requisitos/modelagem/lexicos/#lexico-administrador)  do [centro de educacional](/base/requisitos/modelagem/lexicos/#lexico-professor) | RF_02 | Could |
| E3 | FT01 | US23 | Eu, como [responsável](/base/requisitos/modelagem/lexicos/#lexico-responsavel), desejo conversar com o [professor](/base/requisitos/modelagem/lexicos/#lexico-professor) da [turma](/base/requisitos/modelagem/lexicos/#lexico-turma) da minha [criança](/base/requisitos/modelagem/lexicos/#lexico-crianca) | RF_01 | Should |
| E1 | FT07 | US24 | Eu, como [responsável](/base/requisitos/modelagem/lexicos/#lexico-responsavel), desejo receber [relatórios](/base/requisitos/modelagem/lexicos/#lexico-relatorio) esporádico sobre tudo produzido pela minha [criança](/base/requisitos/modelagem/lexicos/#lexico-crianca) | RF_10 | Could |


## Versionamento

| **Data** | **Versão** | **Modificação** | **Autor** |
| --- | --- | --- | --- |
| 04/08/2021 | 0.1 | Abertura do documento        | Bruno Félix |
| 05/08/2021 | 1.0 | Desenvolvimento do documento | Bruno Félix |
| 06/08/2021 | 1.1 | Inserção Lexicos             | Bruno Félix |
| 14/08/2021 | 1.2 | Inserção do MoSCoW           | Bruno Félix |
