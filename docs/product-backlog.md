# Product Backlog

## 1. Épicos

| **ID** | **Descrição** |
| --- | --- |
| E1 | Perfil                     |
| E2 | Atividades e [professor](/base/requisitos/modelagem/lexicos/#lexico-professor)     |
| E3 | Comunicação e [notificações](/base/requisitos/modelagem/lexicos/#lexico-turma) e [eventos](/base/requisitos/modelagem/lexicos/#lexico-notificacao) |
| E4 | [Administração](/base/requisitos/modelagem/lexicos/#lexico-administrador)              |


## 2. Features

| **Épico** | **ID** | **Descrição** |
| --- | --- | --- |
| E3 | FT01 | Comunicação entre [responsáveis](/base/requisitos/modelagem/lexicos/#lexico-responsavel), [professores](/base/requisitos/modelagem/lexicos/#lexico-professor) e [administradores](/base/requisitos/modelagem/lexicos/#lexico-administrador) |
| E3 | FT02 | Recebimento de [notificações](/base/requisitos/modelagem/lexicos/#lexico-turma) e [eventos](/base/requisitos/modelagem/lexicos/#lexico-notificacao)                                     |
| E4 | FT03 | Criação e gerência de [turmas](/base/requisitos/modelagem/lexicos/#lexico-turma) e [eventos](/base/requisitos/modelagem/lexicos/#lexico-evento)                        |
| E4 | FT04 | Cadastro de [criança](/base/requisitos/modelagem/lexicos/#lexico-crianca) e [professor](/base/requisitos/modelagem/lexicos/#lexico-professor)                               |
| E2 | FT05 | Lançamento e acompanhamento da [presença](/base/requisitos/modelagem/lexicos/#lexico-presenca)                       |
| E3 | FT06 | Criação e gerência de [atividade](/base/requisitos/modelagem/lexicos/#lexico-atividade) e [anotações](/base/requisitos/modelagem/lexicos/#lexico-anotacoes)                   |
| E1 | FT07 | Acompanhamento das [atividade](/base/requisitos/modelagem/lexicos/#lexico-atividade), [eventos](/base/requisitos/modelagem/lexicos/#lexico-evento)   e [agenda](/base/requisitos/modelagem/lexicos/#lexico-agenda), [eventos](/base/requisitos/modelagem/lexicos/#lexico-evento)                |
| E1 | FT08 | Acompanhamento das [turmas](/base/requisitos/modelagem/lexicos/#lexico-turma)                                     |


## 3. Histórias de Usuário

| **Épico** | **Feacture** | **ID** | **Descrição** | **Rastreabilidade** |
| --- | --- | --- | --- | --- |
| E4 | FT04 | US01 | Eu, como [administrador](/base/requisitos/modelagem/lexicos/#lexico-administrador), desejo cadastrar um criança no centro de ensino                                   | RF_07 |
| E4 | FT04 | US02 | Eu, como [administrador](/base/requisitos/modelagem/lexicos/#lexico-administrador), desejo cadastrar um [professor](/base/requisitos/modelagem/lexicos/#lexico-professor) no centro de ensino                                 | RF_08 |
| E4 | FT03 | US03 | Eu, como [administrador](/base/requisitos/modelagem/lexicos/#lexico-administrador), desejo criar, editar e excluir uma turma para o centro de ensino                  | RF_06 |
| E3 | FT06 | US04 | Eu, como [professor](/base/requisitos/modelagem/lexicos/#lexico-professor), desejo criar, editar e excluir atividades para minha turma                            | RF_12 |
| E1 | FT07 | US05 | Eu, como [responsável](/base/requisitos/modelagem/lexicos/#lexico-responsavel), desejo fazer cadastro e login na aplicação                                          | RF_11 |
| E1 | FT07 | US06 | Eu, como [responsável](/base/requisitos/modelagem/lexicos/#lexico-responsavel), desejo ter um espaço que contenha os atividades, eventos e agenda dos próximos dias | RF_11 |
| E1 | FT07 | US07 | Eu, como [responsável](/base/requisitos/modelagem/lexicos/#lexico-responsavel), desejo visualizar a lista de todas as atividades da minha criança                   | RF_12 |
| E1 | FT07 | US08 | Eu, como [responsável](/base/requisitos/modelagem/lexicos/#lexico-responsavel), desejo visualizar os detalhes de uma atividade da minha criança                     | RF_12 |
| E4 | FT03 | US09 | Eu, como [administrador](/base/requisitos/modelagem/lexicos/#lexico-administrador), desejo criar, editar e excluir um evento para o centro de ensino                  | RF_09 |
| E1 | FT07 | US10 | Eu, como [responsável](/base/requisitos/modelagem/lexicos/#lexico-responsavel), desejo visualizar a lista de todos os eventos do centro de ensino                   | RF_09 |
| E1 | FT07 | US11 | Eu, como [responsável](/base/requisitos/modelagem/lexicos/#lexico-responsavel), desejo visualizar os detalhes de um evento do centro de ensino                      | RF_09 |
| E3 | FT06 | US12 | Eu, como [professor](/base/requisitos/modelagem/lexicos/#lexico-professor), desejo criar, editar e excluir anotações para uma criança                             | RF_14 |
| E1 | FT07 | US13 | Eu, como [responsável](/base/requisitos/modelagem/lexicos/#lexico-responsavel), desejo visualizar a agenda, com anotações, da minha criança                         | RF_11 |
| E1 | FT08 | US14 | Eu, como [professor](/base/requisitos/modelagem/lexicos/#lexico-professor), desejo visualizar a lista de todas as minhas turmas                                   | RF_06 |
| E1 | FT08 | US15 | Eu, como [professor](/base/requisitos/modelagem/lexicos/#lexico-professor), desejo visualizar os detalhes, atividades e alunos de uma turma                       | RF_06 |
| E3 | FT02 | US16 | Eu, como [responsável](/base/requisitos/modelagem/lexicos/#lexico-responsavel), desejo receber notificações sobre uma atividade da minha criança                    | RF_03 |
| E3 | FT02 | US17 | Eu, como [responsável](/base/requisitos/modelagem/lexicos/#lexico-responsavel), desejo receber notificações sobre a agenda e as anotações da minha criança          | RF_14 |
| E3 | FT02 | US18 | Eu, como [responsável](/base/requisitos/modelagem/lexicos/#lexico-responsavel), desejo receber notificações sobre um evento do centro de ensino                     | RF_05 |
| E2 | FT05 | US19 | Eu, como [professor](/base/requisitos/modelagem/lexicos/#lexico-professor), desejo lançar presença da minha turma                                                 | RF_13 |
| E2 | FT05 | US20 | Eu, como [responsável](/base/requisitos/modelagem/lexicos/#lexico-responsavel), desejo acompanhar o andamento das presenças da minha criança                        | RF_13 |
| E3 | FT02 | US21 | Eu, como [responsável](/base/requisitos/modelagem/lexicos/#lexico-responsavel), desejo receber notificações sobre a entrada e saída da minha criança                | RF_04 |
| E3 | FT01 | US22 | Eu, como [responsável](/base/requisitos/modelagem/lexicos/#lexico-responsavel), desejo conversar com o adminstrador do centro de ensino                             | RF_02 |
| E3 | FT01 | US23 | Eu, como [responsável](/base/requisitos/modelagem/lexicos/#lexico-responsavel), desejo conversar com o [professor](/base/requisitos/modelagem/lexicos/#lexico-professor) da turma da minha criança                          | RF_01 |
| E1 | FT07 | US24 | Eu, como [responsável](/base/requisitos/modelagem/lexicos/#lexico-responsavel), desejo receber relatórios esporádico sobre tudo produzido pela minha criança        | RF_10 |


## Versionamento

| **Data** | **Versão** | **Modificação** | **Autor** |
| --- | --- | --- | --- |
| 04/08/2021 | 0.1 | Abertura do documento        | Bruno Félix |
| 05/08/2021 | 1.0 | Desenvolvimento do documento | Bruno Félix |