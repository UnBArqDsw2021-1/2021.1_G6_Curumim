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

- UC01 - Cadastrar criança
- UC02 - Gerenciar turmas
- UC03 - Cadastrar professor
- UC04 - Gerenciar eventos
- UC05 - Gerenciar anotações sobre os alunos
- UC06 - Gerenciar atividades da turma
- UC07 - Efetuar login
- UC08 - Verificar senha
- UC09 - Exibir mensagem de erro
- UC10 - Visualizar todas as minhas turmas
- UC11 - Lançar presença dos alunos
- UC12 - Efetuar cadastro
- UC13 - Conversar com o centro educacional
- UC14 - Conversar com os administradores
- UC15 - Conversar com os professores da turma da minha criança
- UC16 - Obter informações da minha criança
- UC17 - Visualizar presenças
- UC18 - Visualizar atividades
- UC19 - Visualizar agenda
- UC20 - Visualizar anotações
- UC21 - Visualizar eventos
- UC22 - Receber notificações com informações da minha criança
- UC23 - Receber relatórios com o desempenho da minha criança


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