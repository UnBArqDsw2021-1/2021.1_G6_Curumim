## Introdução

&emsp;&emsp;Visando uma explanação inicial sobre o tema proposto, a equipe optou por aplicar a técnica de brainstoming para colher opiniões e as diferentes visões dos integrantes a cerca do projeto já elicitando alguns requisitos iniciais.<br>
&emsp;&emsp;O brainstorming é uma técnica muito dinâmica que permite uma discussão bem abrangente levando em consideração opiniões e pontos de vistas pessoais de cada participante sobre os aspectos do projeto e as possíveis abordagens.

## Metodologia

&emsp;&emsp;Utilizando a ferramenta [Google Jamboard](https://edu.google.com/intl/ALL_br/products/jamboard/), foi feita uma bateria com três rounds de um minuto e meio. Para cada round, cada integrante usou a funcionalidade de post-it do Jamboard para colocar uma ideia ou opinião sobre o que o sistema do projeto em questão deveria conter. No fim de cada round foi dado tempo para que todos os integrantes lessem os post-it dos demais com o intuito de inspirar novas ideias a partir do que já está no quadro.<br>
&emsp;&emsp;Ao final dos três rounds, começam as discussões. Foi dada a oportunidade para cada participante defender suas ideias e questionar as dos demais para que todos escolherem, juntos, um conjunto de requisitos iniciais.<br>
&emsp;&emsp;Após essas discussões, o grupo compreendeu melhor o escopo do projeto e se decidiu pela elicitação de 14 requisitos. Nesse Brainstorming, o grupo não elicitou requisitos não funcionais, tratando desses na utilização de outra técnica de elicitação ([Introspecção](./introspeccao.md)).

![Brainstorming](../../../assets/imagens/brainstorming/brainstorming.png)

<center>[Figura 1: Quadro de Brainstorming](../../../assets/imagens/brainstorming/brainstorming.png)</center>

## Requisitos Elicitados

&emsp;&emsp;A tabela a seguir detalha e identifica os requisitos iniciais que foram elicitados nessa etapa. Por motivos de rastreabilidade e identificação, os requisitos terão o prefixo **RF_** para indentificar que se trata requisitos funcionais.

|    ID     | Requisito                                                                       |
| :-------: | ------------------------------------------------------------------------------- |
| <span id="rf1"> **RF_01** </span> | Ter sistema de comunicação entre [responsáveis](../../modelagem/lexicos/#lexico-responsavel) e [professores](../../modelagem/lexicos/#lexico-professor).                    |
| <span id="rf2"> **RF_02** </span> | Ter sistema de comunicação entre [responsáveis](../../modelagem/lexicos/#lexico-responsavel) e [administradores](../../modelagem/lexicos/#lexico-administrador) da [instituição](../../modelagem/lexicos/#lexico-instituicao). |
| <span id="rf3"> **RF_03** </span> | [Responsáveis](../../modelagem/lexicos/#lexico-responsavel) receberem [notificações](../../modelagem/lexicos/#lexico-notificacao) sobre novas [atividades](../../modelagem/lexicos/#lexico-atividade).                     |
| <span id="rf4"> **RF_04** </span> | [Responsáveis](../../modelagem/lexicos/#lexico-responsavel) receberem [notificações](../../modelagem/lexicos/#lexico-notificacao) sobre entrada e saída da [crianças](../../modelagem/lexicos/#lexico-crianca).          |
| <span id="rf5"> **RF_05** </span> | [Responsáveis](../../modelagem/lexicos/#lexico-responsavel) receberem [notificações](../../modelagem/lexicos/#lexico-notificacao) sobre novos [eventos](../../modelagem/lexicos/#lexico-evento).                        |
| <span id="rf6"> **RF_06** </span> | [Administrador](../../modelagem/lexicos/#lexico-administrador) poder [criar](../../modelagem/lexicos/#lexico-cadastrar-turma) e configurar [turmas](../../modelagem/lexicos/#lexico-turma).                                  |
| <span id="rf7"> **RF_07** </span> | [Administrador](../../modelagem/lexicos/#lexico-administrador) poder registras as [crianças](../../modelagem/lexicos/#lexico-crianca).                                      |
| <span id="rf8"> **RF_08** </span> | [Administrador](../../modelagem/lexicos/#lexico-administrador) poder registrar os [professores](../../modelagem/lexicos/#lexico-professor).                                   |
| <span id="rf9"> **RF_09** </span> | [Administrador](../../modelagem/lexicos/#lexico-administrador) poder criar e configurar [eventos](../../modelagem/lexicos/#lexico-evento).                                 |
| <span id="rf10"> **RF_10** </span> | Poder disponibilizar [relatórios](../../modelagem/lexicos/#lexico-relatorio) gerais.                                         |
| <span id="rf11"> **RF_11** </span> | [Responsáveis](../../modelagem/lexicos/#lexico-responsavel) terem acessoa as informações e dados de suas crianças.             |
| <span id="rf12"> **RF_12** </span> | [Professor](../../modelagem/lexicos/#lexico-professor) poder registra e gerenciar [atividades](../../modelagem/lexicos/#lexico-atividade).                                |
| <span id="rf13"> **RF_13** </span> | [Professor](../../modelagem/lexicos/#lexico-professor) poder [lançar presença](../../modelagem/lexicos/#lexico-lancar-presenca).                                                |
| <span id="rf14"> **RF_14** </span> | [Professor](../../modelagem/lexicos/#lexico-professor) poder [notificar](../../modelagem/lexicos/#lexico-notificar) [responsáveis](../../modelagem/lexicos/#lexico-responsavel) com observações.                         |

## Bibliografia

> - BARBOSA. Simone. SILVA. Bruno. 2010. Interação Humano-computador.

## Versionamento

| Versão | Data | Modificação |Autor|
|:-:|--|--|--|
| 0.1| 24/07/2021 | Realização do Brainstorming | Bruno Félix, Daniel Porto, Edson Soares, Eliseu Kadesh, Enzo Gabriel, Francisco Emanoel, João Pedro, Mateus Oliveira e Nilo Mendonça |
| 1.0 | 28/07/2021 | Abertura do documento| Daniel Porto |
| 1.1 | 01/08/2021 | Atualização dos prefixos da identificação dos requisitos | Daniel Porto |
| 1.2 | 05/08/2021 | Atualização título dos requisitos 3 e 5 | Enzo Gabriel|
| 1.3 | 06/08/2021 | Adição dos hiperlinks dos léxicos | Daniel Porto |
| 1.4 | 11/08/2021 | Correção dos hiperlinks dos léxicos | Daniel Porto |
| 1.5 | 25/08/2021 | Ajuste para navegabilidade nos requisitos | Daniel Porto |
| 1.6 | 17/09/2021 | Atualização de informações de acordo com o feedback da entrega 1 | Gabriel Bonifácio |
| 1.7 | 19/09/2021 | Revisão por pares | Bruno Félix e Daniel Porto |