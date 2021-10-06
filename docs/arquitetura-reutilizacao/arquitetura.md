## Introdução
### Objetivo
&emsp;&emsp;O presente documento de arquitetura tem como objetivo elucidar e descrever os aspectos mais importantes no que tange os estilos e padrões arquiteturais acerca da concepção e desenvolvimento do projeto Curumim.

### Escopo
&emsp;&emsp;Através desse documento é possível se ter um entendimento detalhado sobre sobre os aspectos inerentes ao projetos contidos no conjunto "4 + 1" de visões arquiteturais definido pelo RUP[[1]](#bibliografia) e a visão de dados.<br>
&emsp;&emsp;Além disso, esse documento aborda uma representação mais detalhada da arquitetura, as metas arquiteturais, restrições e aspectos acerca da qualidade, tamanho e desempenho do produto<br>
&emsp;&emsp;Sendo assim, esse documento serve de guia para o entendimento do design e desenvolvimento do projeto.

### Definições, Acrônimos e Abreviações
&emsp;&emsp;A tabela a seguir contém as definições dos mais variados termos utilizados neste documento de arquitetura. Mais definições sobre termos pertencentes ao domínio do projeto podem ser encontrados no documento de [***Léxicos***](../../base/requisitos/modelagem/lexicos).

| Termo | Descrição |
| :-: | -- |
| RUP | Rational Unified Process |

### Visão geral
&emsp;&emsp;Esse documento de arquitetura é composto pelos seguintes tópicos:

 - [Introdução](#introducao): Provê uma visão ampla sobre o presente documento.
 - [Representação da arquitetura](#representacao-da-arquitetura): Descreve e representa a arquitetura escolhida para o projeto;
 - [Metas Arquiteturais e Restrições](#metas-arquiteturais-e-restrições): Descreve as metas arquiteturais e as restrições que têm impacto significativo na arquitetura;
 - [Visão de Casos de Uso](#visao-de-casos-de-uso): Descreve e detalha os casos de uso;
 - [Visão Lógica](#visao-logica): Descreve as partes arquitetonicamente significativas do modelo de projeto;
 - [Visão de Processos](#visao-de-processos): Descreve a decomposição do sistema em processos menores e seus agrupamentos;
 - [Visão de Implantação](#visao-de-implantacao): Descreve a disponibilização da aplicação para uso;
 - [Visão de Implementação](#visao-de-implementacao): Descreve a estrutura e decomposição do modelo de implementação do projeto;
 - [Visão de Dados](#visao-de-dados): Descreve a persistência de dados armazenados;
 - [Tamanho e Desempenho](#tamanho-e-desempenho): Descreve as principais características de dimensionamento afetam a arquitetura, bem como as restrições de desempenho;
 - [Qualidade](#qualidade): Descreve como a arquitetura contribui com as mais variadas características de qualidade.
 - [Bibliografia](#bibliografia): Fontes utilizadas para a construção desse artefato;
 - [Versionamento](#versionamento): Histórico de alterações do documento.

## Representação da arquitetura

## Metas Arquiteturais e Restrições

## Visão de Casos de Uso

&emsp;&emsp;A seguir iremos descrever nossa visão dos [casos de uso](../../modelagem/modelagem-dinamica/casos-de-uso) da arquitetura de software. Contendo cenários e/ou [casos de uso](../../modelagem/modelagem-dinamica/casos-de-uso) que representam o funcionamento do sistema.</br>
&emsp;&emsp;Nossos [casos de uso](../../modelagem/modelagem-dinamica/casos-de-uso) estão listados abaixo, juntamente com as descrições dos de maior impacto.

- UC01 - Cadastrar [criança](../../base/requisitos/modelagem/lexicos/#lexico-crianca);
- UC02 - Gerenciar [turmas](../../base/requisitos/modelagem/lexicos/#lexico-turma);
- UC03 - Cadastrar [professor](../../base/requisitos/modelagem/lexicos/#lexico-professor);
- UC04 - Gerenciar [eventos](../../base/requisitos/modelagem/lexicos/#lexico-evento);
- UC05 - Gerenciar [anotações](../../base/requisitos/modelagem/lexicos/#lexico-anotacao) sobre os [alunos](../../base/requisitos/modelagem/lexicos/#lexico-aluno);
- UC06 - Gerenciar [atividades](../../base/requisitos/modelagem/lexicos/#lexico-atividade) da [turma](../../base/requisitos/modelagem/lexicos/#lexico-turma);
- UC07 - Efetuar login;
- UC08 - Verificar senha;
- UC09 - Exibir mensagem de erro;
- UC10 - Visualizar todas as minhas [turmas](../../base/requisitos/modelagem/lexicos/#lexico-turma);
- UC11 - [Lançar presença](../../base/requisitos/modelagem/lexicos/#lexico-lancar-presenca) dos [alunos](../../base/requisitos/modelagem/lexicos/#lexico-aluno);
- UC12 - Efetuar cadastro;
- UC13 - Conversar com o [centro educacional](../../base/requisitos/modelagem/lexicos/#lexico-centro-educacional);
- UC14 - Conversar com os [administradores](../../base/requisitos/modelagem/lexicos/#lexico-administrador);
- UC15 - Conversar com os [professores](../../base/requisitos/modelagem/lexicos/#lexico-professor) da [turma](../../base/requisitos/modelagem/lexicos/#lexico-turma) da minha [criança](../../base/requisitos/modelagem/lexicos/#lexico-crianca);
- UC16 - Obter informações da minha [criança](../../base/requisitos/modelagem/lexicos/#lexico-crianca);
- UC17 - Visualizar [presenças](../../base/requisitos/modelagem/lexicos/#lexico-presenca);
- UC18 - Visualizar [atividades](../../base/requisitos/modelagem/lexicos/#lexico-atividade);
- UC19 - Visualizar [agenda](../../base/requisitos/modelagem/lexicos/#lexico-agenda);
- UC20 - Visualizar [anotações](../../base/requisitos/modelagem/lexicos/#lexico-anotacao);
- UC21 - Visualizar [eventos](../../base/requisitos/modelagem/lexicos/#lexico-evento);
- UC22 - Receber [notificações](../../base/requisitos/modelagem/lexicos/#lexico-notificacao) com informações da minha [criança](../../base/requisitos/modelagem/lexicos/#lexico-crianca);
- UC23 - Receber [relatórios](../../base/requisitos/modelagem/lexicos/#lexico-crianca) com o desempenho da minha [criança](../../base/requisitos/modelagem/lexicos/#lexico-crianca);

#### Descrição dos casos de uso significativos

- UC01 - Cadastrar [criança](../../base/requisitos/modelagem/lexicos/#lexico-crianca): este caso de uso é exclusivo do ator [administrador](../../base/requisitos/modelagem/lexicos/#lexico-administrador) e consiste em registrar uma [criança](../../base/requisitos/modelagem/lexicos/#lexico-crianca) dentro do sistema da aplicação com o objetivo de colocá-la no banco de dados, tornando essa [criança](../../base/requisitos/modelagem/lexicos/#lexico-crianca) uma [aluna](../../base/requisitos/modelagem/lexicos/#lexico-aluno) no [centro educacional](../../base/requisitos/modelagem/lexicos/#lexico-centro-educacional).

- UC02 - Gerenciar [turmas](../../base/requisitos/modelagem/lexicos/#lexico-turma): este caso de uso é exclusivo do ator [administrador](../../base/requisitos/modelagem/lexicos/#lexico-administrador) e consiste em fazer o gerenciamento das [turmas](../../base/requisitos/modelagem/lexicos/#lexico-turma). O [centro educacional](../../base/requisitos/modelagem/lexicos/#lexico-centro-educacional) pode possuir diversas divisões de [alunos](../../base/requisitos/modelagem/lexicos/#lexico-aluno) que estejam no mesmo nível educacional, o que podemos definir como [turmas](../../base/requisitos/modelagem/lexicos/#lexico-turma), e esse caso de uso trata justamente do gerenciamento de todas essas divisões por parte do [administrador](../../base/requisitos/modelagem/lexicos/#lexico-administrador).

- UC03 - Cadastrar [professor](../../base/requisitos/modelagem/lexicos/#lexico-professor): este caso de uso é exclusivo do ator [administrador](../../base/requisitos/modelagem/lexicos/#lexico-administrador) e consiste em registrar um [professor](../../base/requisitos/modelagem/lexicos/#lexico-professor) dentro do sistema da aplicação com o objetivo de dar-lhe permissão à funcionalidades na aplicação exclusivas do [professor](../../base/requisitos/modelagem/lexicos/#lexico-professor) e cadastrá-lo no sistema. 

- UC04 - Gerenciar [eventos](../../base/requisitos/modelagem/lexicos/#lexico-evento): este caso de uso é exclusivo do ator [administrador](../../base/requisitos/modelagem/lexicos/#lexico-administrador) e consiste em fazer o gerenciamento de [eventos](../../base/requisitos/modelagem/lexicos/#lexico-evento). Durante toda a temporada escolar, diversos [eventos](../../base/requisitos/modelagem/lexicos/#lexico-evento) podem acontecer. Para que [responsável](../../base/requisitos/modelagem/lexicos/#lexico-responsavel) e [professores](../../base/requisitos/modelagem/lexicos/#lexico-professor) tenham conhecimento desses [eventos](../../base/requisitos/modelagem/lexicos/#lexico-evento), o [administrador](../../base/requisitos/modelagem/lexicos/#lexico-administrador) pode fazer todo o gerenciamento com o objetivo de expô-los na aplicação.

- UC05 - Gerenciar [anotações](../../base/requisitos/modelagem/lexicos/#lexico-anotacao) sobre os [alunos](../../base/requisitos/modelagem/lexicos/#lexico-aluno): este caso de uso é exclusivo do ator [professor](../../base/requisitos/modelagem/lexicos/#lexico-professor) e consiste em fazer o gerenciamento das [anotações](../../base/requisitos/modelagem/lexicos/#lexico-anotacao) sobre os [alunos](../../base/requisitos/modelagem/lexicos/#lexico-aluno) de acordo com os acontecimentos diários observados pelo [professor](../../base/requisitos/modelagem/lexicos/#lexico-professor) no [centro educacional](../../base/requisitos/modelagem/lexicos/#lexico-centro-educacional).

- UC06 - Gerenciar [atividades](../../base/requisitos/modelagem/lexicos/#lexico-atividade) da [turma](../../base/requisitos/modelagem/lexicos/#lexico-turma): este caso de uso é exclusivo do ator [professor](../../base/requisitos/modelagem/lexicos/#lexico-professor) e consiste em fazer o gerenciamento de [atividades](../../base/requisitos/modelagem/lexicos/#lexico-atividade) da [turma](../../base/requisitos/modelagem/lexicos/#lexico-turma) com o objetivo de apresentar aos [responsáveis](../../base/requisitos/modelagem/lexicos/#lexico-responsavel) as [atividades](../../base/requisitos/modelagem/lexicos/#lexico-atividade) que foram pedidas aos [alunos](../../base/requisitos/modelagem/lexicos/#lexico-aluno) do [centro educacional](../../base/requisitos/modelagem/lexicos/#lexico-centro-educacional).

- UC07 - Efetuar login: este caso de uso pode ser feito pelos atores [professor](../../base/requisitos/modelagem/lexicos/#lexico-professor), [responsável](../../base/requisitos/modelagem/lexicos/#lexico-responsavel) e [administrador](../../base/requisitos/modelagem/lexicos/#lexico-administrador), e consiste em se conectar à aplicação por parte desses atores, utilizando um registro próprio com seu devido usuário e senha.

- UC08 - Verificar senha: este caso de uso pode ser feito pelos atores [professor](../../base/requisitos/modelagem/lexicos/#lexico-professor), [responsável](../../base/requisitos/modelagem/lexicos/#lexico-responsavel) e [administrador](../../base/requisitos/modelagem/lexicos/#lexico-administrador), e consiste na verificação da senha digitada por parte desses atores, para que possa se analisar se o seu registro inicial coincide com o digitado no momento. 

- UC09 - Exibir mensagem de erro: este caso de uso pode ser feito pelos atores [professor](../../base/requisitos/modelagem/lexicos/#lexico-professor), [responsável](../../base/requisitos/modelagem/lexicos/#lexico-responsavel) e [administrador](../../base/requisitos/modelagem/lexicos/#lexico-administrador) e consiste na exibição de uma mensagem de erro, caso a senha digitada no caso de uso 07 ([UC07](#visao-de-casos-de-uso)) não coincida com a senha registrada anteriormente.

- UC10 - Visualizar todas as minhas [turmas](../../base/requisitos/modelagem/lexicos/#lexico-turma): este caso de uso é exclusivo do ator [professor](../../base/requisitos/modelagem/lexicos/#lexico-professor) e consiste na visualização de todas as  [turmas](../../base/requisitos/modelagem/lexicos/#lexico-turma) por parte do [professor](../../base/requisitos/modelagem/lexicos/#lexico-professor) para que ele possa analisar todos os aspectos que envolvem uma  [turma](../../base/requisitos/modelagem/lexicos/#lexico-turma).

- UC11 - [Lançar presença](../../base/requisitos/modelagem/lexicos/#lexico-lancar-presenca) dos [alunos](../../base/requisitos/modelagem/lexicos/#lexico-aluno): este caso de uso é exclusivo para o ator [professor](../../base/requisitos/modelagem/lexicos/#lexico-professor) e consiste em confirmar a [presença](../../base/requisitos/modelagem/lexicos/#lexico-presenca) de [alunos](../../base/requisitos/modelagem/lexicos/#lexico-aluno) à aula.

- UC12 - Efetuar cadastro: este caso de uso é exclusivo para o ator [responsável](../../base/requisitos/modelagem/lexicos/#lexico-responsavel), onde apenas um [responsável](../../base/requisitos/modelagem/lexicos/#lexico-responsavel) pode realizar o seu cadastro na plataforma.

- UC13 - Conversar com o [centro educacional](../../base/requisitos/modelagem/lexicos/#lexico-centro-educacional): este caso consiste em um [responsável](../../base/requisitos/modelagem/lexicos/#lexico-responsavel) entrar em contato com um [professor](../../base/requisitos/modelagem/lexicos/#lexico-professor) ou [administrador](../../base/requisitos/modelagem/lexicos/#lexico-administrador) por meio do chat da plataforma.

- UC16 - Obter informações da minha [criança](../../base/requisitos/modelagem/lexicos/#lexico-crianca): o caso ocorre caso um [responsável](../../base/requisitos/modelagem/lexicos/#lexico-responsavel) queira visualizar as [presenças](../../base/requisitos/modelagem/lexicos/#lexico-presenca), as [atividades](../../base/requisitos/modelagem/lexicos/#lexico-atividade), a [agenda](../../base/requisitos/modelagem/lexicos/#lexico-agenda), as [anotações](../../base/requisitos/modelagem/lexicos/#lexico-anotacao) ou os [eventos](../../base/requisitos/modelagem/lexicos/#lexico-evento) de sua [criança](../../base/requisitos/modelagem/lexicos/#lexico-crianca).

- UC22 - Receber [notificações](../../base/requisitos/modelagem/lexicos/#lexico-notificacao) com informações da minha [criança](../../base/requisitos/modelagem/lexicos/#lexico-crianca): caso exista alguma informação nova da [criança](../../base/requisitos/modelagem/lexicos/#lexico-crianca) o [responsável](../../base/requisitos/modelagem/lexicos/#lexico-responsavel) deve ser notificado.

- UC23 - Receber [relatórios](../../base/requisitos/modelagem/lexicos/#lexico-relatorio) com o desempenho da minha [criança](../../base/requisitos/modelagem/lexicos/#lexico-crianca): neste caso o [responsável](../../base/requisitos/modelagem/lexicos/#lexico-responsavel) deve receber periodicamente [relatórios](../../base/requisitos/modelagem/lexicos/#lexico-relatorio) contendo informações sobre o desempenho de sua [criança](../../base/requisitos/modelagem/lexicos/#lexico-crianca).


## Visão Lógica

## Visão de Processos

## Visão de Implantação

## Visão de Implementação

## Visão de Dados

## Tamanho e Desempenho

## Qualidade

## Bibliografia

> - [1] Visões Arquiteturais. Disponível em <https://www.inf.ufpr.br/andrey/ci163/VisoesAl.pdf>. Acesso em 29 set. 2021.

## Versionamento

| Versão | Data | Modificação | Autor |
|:-:|--|--|--|
|1.0|29/09/2021| Abertura do documento e inclusão da introdução | Daniel Porto |
|x.x|05/10/2021 | Adição da visão dos casos de uso | Mateus O. Patrício e Gabriel Bonifácio |