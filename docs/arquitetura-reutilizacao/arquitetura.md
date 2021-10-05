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
&emsp;&emsp;A visão lógica consiste na organização conceitual do projeto, podendo ser visualizado por meio do diagrama de classes, [pacotes](../modelagem/modelagem-estatica/diagrama-de-pacotes.md) e diagrama interação. O artefato de visão lógica é utilizado para mostrar o agrupamento das classes da arquitetura do sistema.

&emsp;&emsp;O projeto Curumim é estruturado no padrão MVC, o qual consiste em três camadas lógicas que interagem entre si. Aqui dividimos os pacotes em agrupamentos lógicos e apresentamos suas dependências entre eles.

### Back End
&emsp;&emsp;No back end contém a camada de controle, onde os componentes recebem requisições de componentes externos. Conforme o necessário, a camada de controle cuida das solicitações de requisições enviadas pela visão. Segundo os autores do artigo, Arquitetura de Software de Referência para Sistemas de Informação Governamentais. “Deve-se considerar que a camada de controle é responsável por colaborar com a camada de modelo.” (XI Brazilian Symposium on Information System, Goiânia, GO, Maio 26-29, 2015, p.81)[[]](#bibliografia)

&emsp;&emsp;As regras de negócios estão contidas na camada lógica da aplicação, com as classes de domínio do sistema, que contém os dados que serão persistidos no banco de dados. Essa é a camada de modelo da arquitetura utilizada no projeto Curumim.

### Front End
    Imagem
    PARÁGRAFO: explicar específico (View | gerar link pro artefato diagrama /#metodologia)


## Visão de Processos

## Visão de Implantação

## Visão de Implementação

## Visão de Dados

## Tamanho e Desempenho

## Qualidade

## Bibliografia

> - [1] Visões Arquiteturais. Disponível em <https://www.inf.ufpr.br/andrey/ci163/VisoesAl.pdf>. Acesso em 29 set. 2021.

> - [ ] SERRANO,Milene; SERRANO, Maurício; CALVACANTE,André Cruz. Arquitetura de Software deReferência para Sistemas de Informação Governamentais. In: XI Brazilian Symposium on Information System, Goiânia, Maio 26-29, 2015. Disponível em: <https://sol.sbc.org.br/index.php/sbsi/article/view/5886/5784>. Acesso em: 04/10/2021 
## Versionamento

| Versão | Data | Modificação | Autor |
|:-:|--|--|--|
|1.0|29/09/2021| Abertura do documento e inclusão da introdução | Daniel Porto |
|  1.1 |03/10/2021| Criação da estrutura Visão Lógica | Bruno Félix e Edson Soares |
| 1.2  |05/10/2021| Argumentação da Visão Lógica | Bruno Félix e Edson Soares |