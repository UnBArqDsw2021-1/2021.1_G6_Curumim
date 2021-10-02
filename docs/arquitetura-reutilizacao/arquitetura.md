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

## Visão Lógica

## Visão de Processos

## Visão de Implantação

## Visão de Implementação

&emsp;&emsp;A visão de implementação se caracteriza como uma das cinco visões de arquitetura de um sistema e sua finalidade é captar as decisões de arquitetura tomadas para a implementação, buscando descrever como os artefatos de desenvolvimento estão organizados.<br>
&emsp;&emsp;Geralmente, a visão de implementação possui:

- Uma enumeração de todos os subsistemas no modelo de implementação;
- Diagramas de componentes que ilustram os susbsistemas, organizados em camadas e hierarquias;
- Ilustrações de dependências de importação entre subsistemas;

&emsp;&emsp;Sendo considerado extremamente útil em questões relacionadas a atribuição do trabalho de implementação a indivíduos e equipes, na avaliação da quantidade de código que será excluído, modificado ou desenvolvido e também para discursões a respeito de reutilização em larga escala e estratégias de release.

### Padrão MVC
#### Camadas

- Model: Essa camada na aplicação Curumim tem a responsabilidade de encapsular estados da aplicação, assim é possível tratar modificações de estado e notificações de estado;
- View: Essa segunda camada tem como objetivo apresentar a interface para o usuário, na aplicação Curumim ela é a principal responsável por mostrar informações da Model para a interface do cliente;
- Controller: Essa é camada que faz o intermédio entre as camadas View e Model, assim mapeando as ações do usuário na view para possíveis mudanças na Model;

#### Conclusão
&emsp;&emsp;Algumas literaturas ao falar do padrão MVC acabam abordando a aplicabilidade dessa arquitetura principalmente a aplicações web, visto sua facilidade e flexibilidade de interação e visualização de dados, além disso a arquitetura MVC trás alguns padrões já conhecidos como os:

- GRASPs(Indireções e Controller);
- GoFs Estruturais (Facade)
- GoFs Comportamentais (Observer)

&emsp;&emsp; Essa foi a principal arquitetura aplicada no projeto Curumim, visto sua eficiência e simplicidade, e por fim trazendo um código mais manutenível [[2]](#bibliografia). 

### API
&emsp;&emsp;API pode ser definida como um conjunto de protocolos e definições usados na integração e no desenvolvimento de softwares de aplicações, permitindo que uma solução ou serviço se comunique com outros produtos e serviços sem haver a necessidade de saber como eles foram implementados, simplificando assim o desenvolvimento de aplicações.<br>
&emsp;&emsp;No projeto Curumim o objetivo da divisão em camadas é possibilitar a reutilização da solução para diversas interfaces. Especificamente no back-end da aplicação a estrutura foi dividida em três componentes principais:

- Models: Assim como explicado no item anterior, tem a responsabilidade de encapsular os estados da aplicação;
- Controllers: Que realiza a ponte entre as Model e o cliente que consome a API;
- Middlewares: Que são representados por uma pipeline de processamentos, com funções pré-definidas que são handles, units e filters.

### Diagrama de camadas

&emsp;&emsp;Para melhor visualização das camadas da aplicação, foi elaborado um diagrama, composto pelas três principais camadas da aplicação:

- Client: Representa o [Front-end](../../base/requisitos/modelagem/lexicos/#front-end) , sendo implementado utilizando o React js;
- API: Representa o [Back-end](../../base/requisitos/modelagem/lexicos/#back-end), sendo implementado em Node js e utilizando o Express js;
- Database: Representa o banco de dados, utilizando o Postgresql;

<center>
![](../assets/imagens/arquitetura-reutilizacao/Diagrama-de-camadas.png)<br>
[Figura 1 - Diagrama de camadas](../assets/imagens/arquitetura-reutilizacao/Diagrama-de-camadas.png)
</center>

## Visão de Dados

## Tamanho e Desempenho

## Qualidade

## Bibliografia

> - [1] Visões Arquiteturais. Disponível em <https://www.inf.ufpr.br/andrey/ci163/VisoesAl.pdf>. Acesso em 29 set. 2021.
> - [2] O que é MVC?. Disponível em <https://www.treinaweb.com.br/blog/o-que-e-mvc>. Acesso em 02 de out. 2021
> - [3] UniGrade. Documento de Arquitetura de Software. Disponível em: <https://ads-unigrade-2019-1.github.io/Wiki/dinamica06/DAS/#7-visao-da-implementacao>. Acesso em 02 de out. 2021

## Versionamento

| Versão | Data | Modificação | Autor |
|:-:|--|--|--|
|1.0|29/09/2021| Abertura do documento e inclusão da introdução | Daniel Porto |
|1.2|02/10/2021| Criando tópico de visão de implementação | Francisco Ferreira e Nilo Mendonça|