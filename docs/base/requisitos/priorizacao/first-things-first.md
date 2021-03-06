# First Things First <br> <span class="rotulo-extra">Iniciativa Extra</span>
## Introdução
&emsp;&emsp;O First-Things-First é uma técnica de priorização utilizada baseada em custo, valor e risco dos requisitos de um projeto. A ideia é estabelecer uma ordem de prioridades na hora em que se fará a implementação de algumas funcionalidades, utilizando, então, o valor, custo e risco para se avaliar o impacto dessas implementações.

## Metodologia

&emsp;&emsp;Para a classificação dos benefícios, custo, valor e riscos dos requisitos funcionais, os [10 integrantes do grupo] fizeram um debate utilizando a plataforma [Microsoft Teams](https://www.microsoft.com/pt-br/microsoft-teams/group-chat-software) e chegaram a um consenso quanto a priorização de cada requisito.<br>
&emsp;&emsp;Os cálculos dessa técnica são dados de forma que:

- O valor total é a soma (Benefício Relativo * Peso Relativo + Penalidade Relativa * Peso Relativo);
- A prioridade de cada requisito é igual ao valor total % / (custo % * Peso custo + risco % * Peso Risco).

## Requisitos Funcionais

&emsp;&emsp;A tabela a seguir detalha e identifica os requisitos funcionais que foram elicitados, seus custos, benefícios, risco, e também a prioridade baseada no artefato [Moscow](./moscow.md) que também foi realizado pela equipe e que juntamente com o First-Things-First auxilia na priorização dos requisitos.

ID | Requisitos | Prioridade |
|--|--|--|
| **RF_01** | Ter sistema de comunicação entre [responsáveis](../../modelagem/lexicos/#lexico-responsavel) e professores.                    | 0,364 |
| **RF_02** | Ter sistema de comunicação entre [responsáveis](../../modelagem/lexicos/#lexico-responsavel) e administradores da instituição. | 0,209 |
| **RF_03** | [Responsáveis](../../modelagem/lexicos/#lexico-responsavel) receberem notificações sobre novas atividades.                     |0,302 |
| **RF_04** | [Responsáveis](../../modelagem/lexicos/#lexico-responsavel) receberem notificações sobre entrada e saída das crianças.          |0,268 |
| **RF_05** | [Responsáveis](../../modelagem/lexicos/#lexico-responsavel) receberem notificações sobre novos eventos.                        | 0,249 |
| **RF_06** | Administrador poder criar e configurar turmas.                                  |1,153 |
| **RF_07** | Administrador poder registrar as crianças.                                      |1,546 |
| **RF_08** | Administrador poder registrar os professores.                                   |1,546 |
| **RF_09** | Administrador poder criar e configurar eventos.                                 |0,399 |
| **RF_10** | Poder disponibilizar relatórios gerais.                                         |0,314 |
| **RF_11** | [Responsáveis](../../modelagem/lexicos/#lexico-responsavel) terem acesso as informações e dados de suas crianças.              |1,023 |
| **RF_12** | Professor poder registrar e gerenciar atividades.                               |1,076 |
| **RF_13** | Professor poder lançar presença.                                                |0,344 |
| **RF_14** | Professor poder notificar [responsáveis](../../modelagem/lexicos/#lexico-responsavel) com observações.                         |0,463 |

[link para a tabela completa no excel](https://docs.google.com/spreadsheets/d/1VO7EnKcoZ7DF_uIbGJHg4b3MkhtVpMwE/edit#gid=667435397)

## Bibliografia

> - E. WIEGERS, Karl. 1999. First Things First: Prioritizing Requirements.
> - First Things First - [Projeto de Requisitos de Software - Yellow](https://github.com/Requisitos-de-Software/2019.2-Yellow): [https://yellow.netlify.app/elicitacao/priorizacao/first_things_first/](https://yellow.netlify.app/elicitacao/priorizacao/first_things_first/). Último acesso em 17/09/2021.

## Versionamento

| Versão | Data | Modificação | Autor | 
|--|--|--|--|
| 0.1 | 29/07/2021 | Reunião para decidir a priorização dos requisitos | Bruno Félix, Daniel Porto, Edson de Araújo, Eliseu Kadesh, Enzo Gabriel, Francisco Emanoel, João Pedro, Mateus Oliveira, Gabriel Bonifácio e Nilo Mendonça |
| 1.0 | 31/07/2021 | Abertura do documento | Eliseu Kadesh |
| 1.1 | 03/08/2021 | Padronização do documento | Eliseu Kadesh |
| 2.0 | 05/08/2021 | Finalização da padronização do documento | Eliseu Kadesh |
| 2.1 | 06/08/2021 | Correções após revisões | Daniel Porto |
| 2.2 | 21/08/2021 | Correção dos links dos léxicos | Gabriel Bonifácio |
| 2.3 | 17/09/2021 | Atualização de informações de acordo com o feedback da entrega 1 | Gabriel Bonifácio |
| 2.4 | 19/09/2021 | Revisão por pares | Bruno Félix e Daniel Porto |