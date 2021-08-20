# Modelo entidade relacionamento

## Introdução

&emsp;&emsp;O Modelo de Entidade relacionamento também conhecido como MER, é um modelo conceitual usado para descrver as entidades em um domínio de negócio, assim listando suas caracteriscas e como elas se relacionam entre si. No geral esse modelo é utilizado para representar uma forma abstrata da estrutura que possuirá o banco de dados da aplicação.

## Metodologia
&emsp;&emsp;Para realizar essa especificação inicial do modelo, primeiramente foram definidas todas as entidades mais concretas que estarão presentes no banco de dados. Dessa forma, para cada entidade, foi preenchida uma tabela com as seguintes colunas:

- Atributos: todos os atributos necessários para representar uma instância da entidade;
- Propriedades: o que caracteriza aquele atributo, podendo ser uma chave primária, estrangeira, um atributo obrigatório ou opcional;
- Tipo: basicamnete se refere ao tip de dado do atiburo em questão;
- Descrição: uma breve explicação sobre o que o atributo representa.

&emsp;&emsp;Feito isso, foram descritas e analisadas as relações entre as entidades e suas respectivas cardinalidades. Sendo assim, ao final foi possível tecer conclusões sobre a modelagem do banco de dados de forma que possibilite uma representação gráfica coerente com o escopo do projeto e as necessidades do desenvolvimento.

## Entidades
&emsp;&emsp;A seguir estão descritas as entidades conforme citado anteriormente. Os nomes das entidades e seus atributos estarão em Inglês no padrão CamelCase para já iniciar e introduzir uma padronização do que será implementado no código.

### [Guardian](../../../base/requisitos/modelagem/lexicos/#lexico-responsavel)

|Atributos | Propriedade | Tipo | Descrição |
|----------|-------------|------|-----------|
|IdGuardian|Chave primária|Inteiro|Indetificação do [Responsável](../../../base/requisitos/modelagem/lexicos/#lexico-responsavel)|
|Name|Obrigatório|String|Nome do [Responsável](../../../base/requisitos/modelagem/lexicos/#lexico-responsavel)|
|CPF|Obrigatório|String|CPF do [Responsável](../../../base/requisitos/modelagem/lexicos/#lexico-responsavel)|
|Email|Obrigatório|String| Email do  [Responsável](../../../base/requisitos/modelagem/lexicos/#lexico-responsavel) |
|Password|Obrigatório|String| Senha do  [Responsável](../../../base/requisitos/modelagem/lexicos/#lexico-responsavel)|
|Address|Obrigatório|String|  Endereço do  [Responsável](../../../base/requisitos/modelagem/lexicos/#lexico-responsavel)|

### [Adm](../../../base/requisitos/modelagem/lexicos/#lexico-administrador)

|Atributos | Propriedade | Tipo | Descrição |
|----------|-------------|------|-----------|
|IdAdm|Chave primária|Inteiro|Indetificação do [administrador](../../../base/requisitos/modelagem/lexicos/#lexico-administrador)|
|Name|Obrigatório|String| Nome do [administrador](../../../base/requisitos/modelagem/lexicos/#lexico-administrador) |
|CPF|Obrigatório|String| CPF do [administrador](../../../base/requisitos/modelagem/lexicos/#lexico-administrador)|
|Email|Obrigatório|String|Email do [administrador](../../../base/requisitos/modelagem/lexicos/#lexico-administrador) |
|Password|Obrigatório|String| Senha do [administrador](../../../base/requisitos/modelagem/lexicos/#lexico-administrador)|
|Registration|Obrigatório|Inteiro| Registro do [administrador](../../../base/requisitos/modelagem/lexicos/#lexico-administrador)|

### [Teacher](../../../base/requisitos/modelagem/lexicos/#lexico-professor)

|Atributos | Propriedade | Tipo | Descrição |
|----------|-------------|------|-----------|
|IdTeacher|Chave primária|Inteiro|Indetificação do [professor](../../../base/requisitos/modelagem/lexicos/#lexico-professor)|
|Name|Obrigatório|String| Nome do [professor](../../../base/requisitos/modelagem/lexicos/#lexico-professor)|
|CPF|Obrigatório|String| CPF do [professor](../../../base/requisitos/modelagem/lexicos/#lexico-professor)|
|Email|Obrigatório|String| Email do [professor](../../../base/requisitos/modelagem/lexicos/#lexico-professor)|
|Password|Obrigatório|String| Senha do [professor](../../../base/requisitos/modelagem/lexicos/#lexico-professor)|
|Registration|Obrigatório|Inteiro| Registro do [professor](../../../base/requisitos/modelagem/lexicos/#lexico-professor)|

### [Child](../../../base/requisitos/modelagem/lexicos/#lexico-crianca)

|Atributos | Propriedade | Tipo | Descrição |
|----------|-------------|------|-----------|
|IdChild|Chave primária|Inteiro| Indetificação da [criança](../../../base/requisitos/modelagem/lexicos/#lexico-crianca)|
|IdResponsavel|Chave estrangeira |Inteiro| Indetificação do [responsável](../../../base/requisitos/modelagem/lexicos/#lexico-responsavel)|
|IdClass|Chave estrangeira|Inteiro| Indetificação da [turma](../../../base/requisitos/modelagem/lexicos/#lexico-turma)|
|Name|Obrigatório|String| Nome da [criança](../../../base/requisitos/modelagem/lexicos/#lexico-crianca)|
|Registration|Obrigatório|Inteiro| Registro da [criança](../../../base/requisitos/modelagem/lexicos/#lexico-crianca)|


### [Class](../../../base/requisitos/modelagem/lexicos/#lexico-turma)

|Atributos | Propriedade | Tipo | Descrição |
|----------|-------------|------|-----------|
|IdClass|Chave primária|Inteiro|Indetificação da [turma](../../../base/requisitos/modelagem/lexicos/#lexico-turma)|
|IdTeacher|Chave estrangeira|Inteiro[ ]| Indetificação do [professor](../../../base/requisitos/modelagem/lexicos/#lexico-professor)|
|IdChild|Chave estrangeira|Inteiro[ ]| Indetificação da [criança](../../../base/requisitos/modelagem/lexicos/#lexico-crianca)| 
|Code|Obrigatório| String| Codigo da [turma](../../../base/requisitos/modelagem/lexicos/#lexico-turma)|
|Capacity|Obrigatório|Inteiro| Capacidade da [turma](../../../base/requisitos/modelagem/lexicos/#lexico-turma)|

### [Event](../../../base/requisitos/modelagem/lexicos/#lexico-evento)

|Atributos | Propriedade | Tipo | Descrição |
|----------|-------------|------|-----------|
|IdEvent|Chave primária|Inteiro|Indetificação do [evento](../../../base/requisitos/modelagem/lexicos/#lexico-evento)|
|IdAdm|Chave estrangeira|Inteiro|Indetificação do [administrador](../../../base/requisitos/modelagem/lexicos/#lexico-administrador)|
|IdClass|Chave estrangeira|Inteiro| Indetificação da [turma](../../../base/requisitos/modelagem/lexicos/#lexico-turma)|
|Description|Obrigatório|String| Descrição do [evento](../../../base/requisitos/modelagem/lexicos/#lexico-evento)|
|Title|Obrigatório|String| Titulo do [evento](../../../base/requisitos/modelagem/lexicos/#lexico-evento)|
|Date|Obrigatório|Date| Data do [evento](../../../base/requisitos/modelagem/lexicos/#lexico-evento) |

### [Activity](../../../base/requisitos/modelagem/lexicos/#lexico-atividade)

|Atributos | Propriedade | Tipo | Descrição |
|----------|-------------|------|-----------|
|IdActivity|Chave primária|Inteiro|Identificação da [atividade](../../../base/requisitos/modelagem/lexicos/#lexico-atividade)|
|IdTeacher|Chave estrangeira|Inteiro| Identificação do [professor](../../../base/requisitos/modelagem/lexicos/#lexico-professor)|
|Title|Obrigatório|String| Titulo da [atividade](../../../base/requisitos/modelagem/lexicos/#lexico-atividade)|
|Description|Obrigatório|String| Descrição da [atividade](../../../base/requisitos/modelagem/lexicos/#lexico-atividade)|
|Date|Obrigatório|Date| Data da [atividade](../../../base/requisitos/modelagem/lexicos/#lexico-atividade)|

### [Anotation](../../../base/requisitos/modelagem/lexicos/#lexico-anotacao)

|Atributos | Propriedade | Tipo | Descrição |
|----------|-------------|------|-----------|
|IdAnotation|Chave primária|Inteiro| Identificação da [anotação](../../../base/requisitos/modelagem/lexicos/#lexico-anotacao)|
|IdTeacher|Chave estrangeira|Inteiro| Identificação do [professor](../../../base/requisitos/modelagem/lexicos/#lexico-professor)|
|IdChild|Chave estrangeira|Inteiro| Identificação da [criança](../../../base/requisitos/modelagem/lexicos/#lexico-crianca)|
|Title|Obrigatório|String| Titulo da [anotação](../../../base/requisitos/modelagem/lexicos/#lexico-anotacao)|
|Description|Obrigatório|String| Descrição da [anotação](../../../base/requisitos/modelagem/lexicos/#lexico-anotacao)|

### [Board](../../../base/requisitos/modelagem/lexicos/#lexico-mural) 

|Atributos | Propriedade | Tipo | Descrição |
|----------|-------------|------|-----------|
|IdBoard|Chave primária|Inteiro|Identificação do [mural](../../../base/requisitos/modelagem/lexicos/#lexico-mural)|
|IdChild|Chave estrangeira|Inteiro| Identificação da [criança](../../../base/requisitos/modelagem/lexicos/#lexico-crianca)|
|IdAnotation|Chave estrangeira|Inteiro[ ]|Identificação da [anotação](../../../base/requisitos/modelagem/lexicos/#lexico-anotacao)|
|IdActivity|Chave estrangeira|Inteiro[ ]|Identificação da [atividade](../../../base/requisitos/modelagem/lexicos/#lexico-atividade)|
|IdEvent|Chave estranfeira|Inteiro[ ]|Indetificação do [evento](../../../base/requisitos/modelagem/lexicos/#lexico-evento)|

### [EC](../../../base/requisitos/modelagem/lexicos/#lexico-centro-educacional)

|Atributos | Propriedade | Tipo | Descrição |
|----------|-------------|------|-----------|
|IdEC|Chave primária|Inteiro|Identificação do [centro educacional](../../../base/requisitos/modelagem/lexicos/#lexico-centro-educacional)|
|IdAdm|Chave estrangeira|Inteiro[ ]|Indetificação do [administrador](../../../base/requisitos/modelagem/lexicos/#lexico-administrador)|
|IdTeacher|Chave estrangeira|Inteiro[ ]|Indetificação do [professor](../../../base/requisitos/modelagem/lexicos/#lexico-professor)|
|IdClass|Chave estrangeira|Inteiro[ ]|Indetificação da [turma](../../../base/requisitos/modelagem/lexicos/#lexico-turma)|
|Name|Obrigatório|String| Nome do [centro educacional](../../../base/requisitos/modelagem/lexicos/#lexico-centro-educacional)|
|Adress|Obrigatório|String| Endereço do [centro educacional](../../../base/requisitos/modelagem/lexicos/#lexico-centro-educacional)|
|Description|Obrigatório|String| Descrição do [centro educacional](../../../base/requisitos/modelagem/lexicos/#lexico-centro-educacional)|

### [Report](../../../base/requisitos/modelagem/lexicos/#lexico-relatorio) 

|Atributos | Propriedade | Tipo | Descrição |
|----------|-------------|------|-----------|
|IdReport|Chave primária|Inteiro|Identificação do [relatório](../../../base/requisitos/modelagem/lexicos/#lexico-relatorio)|
|IdAdm|Chave estrangeira|Inteiro|Indetificação do [administrador](../../../base/requisitos/modelagem/lexicos/#lexico-administrador)|
|Title|Obrigatório|String| Titulo do [relatório](../../../base/requisitos/modelagem/lexicos/#lexico-relatorio)|
|Description|Obrigatório|String| Descriçaõ do [relatório](../../../base/requisitos/modelagem/lexicos/#lexico-relatorio)|

## Relacionamentos
1. [**RESPOSÁVEL**](../../../base/requisitos/modelagem/lexicos/#lexico-responsavel) -- possui -- [**CRIANÇA**](../../../base/requisitos/modelagem/lexicos/#lexico-crianca): Um [reponsável](../../../base/requisitos/modelagem/lexicos/#lexico-responsavel) possui [crianças](../../../base/requisitos/modelagem/lexicos/#lexico-crianca) e uma criança está atrelada a [responsáveis](../../../base/requisitos/modelagem/lexicos/#lexico-responsavel).<br>
(Cardinalidade: n:m)

2. [**ADMINISTRDOR**](../../../base/requisitos/modelagem/lexicos/#lexico-administrador) -- registra -- [**TURMA**](../../../base/requisitos/modelagem/lexicos/#lexico-turma): Um [administrador](../../../base/requisitos/modelagem/lexicos/#lexico-administrador) registra [turmas](../../../base/requisitos/modelagem/lexicos/#lexico-turma) e uma [turma](../../../base/requisitos/modelagem/lexicos/#lexico-turma) é registrada por uma [administrador](../../../base/requisitos/modelagem/lexicos/#lexico-administrador).<br>
(Cardinalidade: 1:n)

3. [**ADMINISTRDOR**](../../../base/requisitos/modelagem/lexicos/#lexico-administrador) -- gera -- [**RELATÓRIO**](../../../base/requisitos/modelagem/lexicos/#lexico-relatorio): Um [administrador](../../../base/requisitos/modelagem/lexicos/#lexico-administrador) gera [relatórios](../../../base/requisitos/modelagem/lexicos/#lexico-relatorio) e um [relatório](../../../base/requisitos/modelagem/lexicos/#lexico-relatorio) é gerado por um [administrador](../../../base/requisitos/modelagem/lexicos/#lexico-administrador).<br>
(Cardinalidade: 1:n)

4. [**CENTRO EDUCACIONAL**](../../../base/requisitos/modelagem/lexicos/#lexico-centro-educacional) -- possui -- [**ADMINISTRADOR**](../../../base/requisitos/modelagem/lexicos/#lexico-administrador): O [centro educacional](../../../base/requisitos/modelagem/lexicos/#lexico-centro-educacional) possui ao menos um [administrador](../../../base/requisitos/modelagem/lexicos/#lexico-administrador) e os [administradores](../../../base/requisitos/modelagem/lexicos/#lexico-administrador) estão atrelados a um [centro educacional](../../../base/requisitos/modelagem/lexicos/#lexico-centro-educacional).<br>
(Cardinalidade: 1:n)

5. [**CENTRO EDUCACIONAL**](../../../base/requisitos/modelagem/lexicos/#lexico-centro-educacional) -- possui -- [**PROFESSOR**](../../../base/requisitos/modelagem/lexicos/#lexico-professor): O [centro educacional](../../../base/requisitos/modelagem/lexicos/#lexico-centro-educacional) possui [professores](../../../base/requisitos/modelagem/lexicos/#lexico-professor) e os [professores](../../../base/requisitos/modelagem/lexicos/#lexico-professor) estão atrelados a um [centro educacional](../../../base/requisitos/modelagem/lexicos/#lexico-centro-educacional).<br>
5. [**CENTRO EDUCACIONAL**](../../../base/requisitos/modelagem/lexicos/#lexico-centro-educacional) -- possui -- [**PROFESSOR**](../../../base/requisitos/modelagem/lexicos/#lexico-professor): O [centro educacional](../../../base/requisitos/modelagem/lexicos/#lexico-centro-educacional) possui [professores](../../../base/requisitos/modelagem/lexicos/#lexico-professor) e os [professores](../../../base/requisitos/modelagem/lexicos/#lexico-professor) estão atrelados a um [centro educacional](../../../base/requisitos/modelagem/lexicos/#lexico-centro-educacional).<br>
5. [**CENTRO EDUCACIONAL**](../../../base/requisitos/modelagem/lexicos/#lexico-centro-educacional) -- possui -- [**PROFESSOR**](../../../base/requisitos/modelagem/lexicos/#lexico-professor): O [centro educacional](../../../base/requisitos/modelagem/lexicos/#lexico-centro-educacional) possui  [professores](../../../base/requisitos/modelagem/lexicos/#lexico-professor) e os  [professores](../../../base/requisitos/modelagem/lexicos/#lexico-professor) estão atrelados a um [centro educacional](../../../base/requisitos/modelagem/lexicos/#lexico-centro-educacional).<br>
(Cardinalidade: 1:n)

6. [**CENTRO EDUCACIONAL**](../../../base/requisitos/modelagem/lexicos/#lexico-centro-educacional) -- possui -- [**TURMA**](../../../base/requisitos/modelagem/lexicos/#lexico-turma): O [centro educacional](../../../base/requisitos/modelagem/lexicos/#lexico-centro-educacional) possui [turmas](../../../base/requisitos/modelagem/lexicos/#lexico-turma) e as [turmas](../../../base/requisitos/modelagem/lexicos/#lexico-turma) possuem um [centro educacional](../../../base/requisitos/modelagem/lexicos/#lexico-centro-educacional). <br>
(Cardinalidade: 1:n)

7. [**PROFESSOR**](../../../base/requisitos/modelagem/lexicos/#lexico-professor) -- cria -- [**ATIVIDADE**](../../../base/requisitos/modelagem/lexicos/#lexico-atividade): Um professor cria [atividades](../../../base/requisitos/modelagem/lexicos/#lexico-atividade) e uma [atividade](../../../base/requisitos/modelagem/lexicos/#lexico-atividade) é criada por um [professor](../../../base/requisitos/modelagem/lexicos/#lexico-professor). <br>
(Cardinalidade: 1:n)

8. [**TURMA**](../../../base/requisitos/modelagem/lexicos/#lexico-turma) -- contém-- [**CRIANÇA**](../../../base/requisitos/modelagem/lexicos/#lexico-crianca): Uma [turma](../../../base/requisitos/modelagem/lexicos/#lexico-turma) contém [crianças](../../../base/requisitos/modelagem/lexicos/#lexico-crianca) e uma [criança](../../../base/requisitos/modelagem/lexicos/#lexico-crianca) está contida em uma [turma](../../../base/requisitos/modelagem/lexicos/#lexico-turma). <br>
(Cardinalidade: 1:n)

5. [**CENTRO EDUCACIONAL**](../../../base/requisitos/modelagem/lexicos/#lexico-centro-educacional) -- possui -- [**PROFESSOR**](../../../base/requisitos/modelagem/lexicos/#lexico-professor): O [centro educacional](../../../base/requisitos/modelagem/lexicos/#lexico-centro-educacional) possui [professores](../../../base/requisitos/modelagem/lexicos/#lexico-professor) e os [professores](../../../base/requisitos/modelagem/lexicos/#lexico-professor) estão atrelados a um [centro educacional](../../../base/requisitos/modelagem/lexicos/#lexico-centro-educacional).<br>
9. [**TURMA**](../../../base/requisitos/modelagem/lexicos/#lexico-turma) -- contém -- [**PROFESSOR**](../../../base/requisitos/modelagem/lexicos/#lexico-professor): Uma [turma](../../../base/requisitos/modelagem/lexicos/#lexico-turma) contém [professores](../../../base/requisitos/modelagem/lexicos/#lexico-professor) e os [professores](../../../base/requisitos/modelagem/lexicos/#lexico-professor) estão contidos em [turmas](../../../base/requisitos/modelagem/lexicos/#lexico-turma). <br>
(Cardinalidade: n:m)

10. [**TURMA**](../../../base/requisitos/modelagem/lexicos/#lexico-turma) -- participa -- [**EVENTO**](../../../base/requisitos/modelagem/lexicos/#lexico-evento): Uma [turma](../../../base/requisitos/modelagem/lexicos/#lexico-turma) participa de [eventos](../../../base/requisitos/modelagem/lexicos/#lexico-evento) e um [evento](../../../base/requisitos/modelagem/lexicos/#lexico-evento) contém a participação das [turmas](../../../base/requisitos/modelagem/lexicos/#lexico-turma). <br>
(Cardinalidade: n:m)

11. [**TURMA**](../../../base/requisitos/modelagem/lexicos/#lexico-turma) -- aplica -- [**ATIVIDADE**](../../../base/requisitos/modelagem/lexicos/#lexico-atividade): Uma [turma](../../../base/requisitos/modelagem/lexicos/#lexico-turma) aplica [atividades](../../../base/requisitos/modelagem/lexicos/#lexico-atividade) e uma [atividade](../../../base/requisitos/modelagem/lexicos/#lexico-atividade) é aplicada nas [turmas](../../../base/requisitos/modelagem/lexicos/#lexico-turma). <br>
(Cardinalidade: n:m)

12. [**CRIANÇA**](../../../base/requisitos/modelagem/lexicos/#lexico-crianca) -- possui -- [**MURAL**](../../../base/requisitos/modelagem/lexicos/#lexico-mural) : Uma [criança](../../../base/requisitos/modelagem/lexicos/#lexico-crianca) possui um [mural](../../../base/requisitos/modelagem/lexicos/#lexico-mural) e um [mural](../../../base/requisitos/modelagem/lexicos/#lexico-mural) está atrelado a uma [criança](../../../base/requisitos/modelagem/lexicos/#lexico-crianca). <br>
(Cardinalidade: 1:1)

13. [**MURAL**](../../../base/requisitos/modelagem/lexicos/#lexico-mural)  -- apresenta -- [**EVENTO**](../../../base/requisitos/modelagem/lexicos/#lexico-evento): Um [mural](../../../base/requisitos/modelagem/lexicos/#lexico-mural) mostra os últimos [eventos](../../../base/requisitos/modelagem/lexicos/#lexico-evento) para a [turma](../../../base/requisitos/modelagem/lexicos/#lexico-turma) da [criança](../../../base/requisitos/modelagem/lexicos/#lexico-crianca) e um [evento](../../../base/requisitos/modelagem/lexicos/#lexico-evento) está presente nos [murais](../../../base/requisitos/modelagem/lexicos/#lexico-mural) das [crianças](../../../base/requisitos/modelagem/lexicos/#lexico-crianca) das [turmas](../../../base/requisitos/modelagem/lexicos/#lexico-turma) contempladas. <br>
(Cardinalidade: n:m)

14. [**MURAL**](../../../base/requisitos/modelagem/lexicos/#lexico-mural)  -- apresenta -- [**ATIVIDADE**](../../../base/requisitos/modelagem/lexicos/#lexico-atividade): Um [mural](../../../base/requisitos/modelagem/lexicos/#lexico-mural) mostra as últimas [atividades](../../../base/requisitos/modelagem/lexicos/#lexico-atividade) da [turma](../../../base/requisitos/modelagem/lexicos/#lexico-turma) da [criança](../../../base/requisitos/modelagem/lexicos/#lexico-crianca) e uma [atividade](../../../base/requisitos/modelagem/lexicos/#lexico-atividade) está presente nos [murais](../../../base/requisitos/modelagem/lexicos/#lexico-mural) das [crianças](../../../base/requisitos/modelagem/lexicos/#lexico-crianca). <br>
(Cardinalidade: n:m)

16. [**MURAL**](../../../base/requisitos/modelagem/lexicos/#lexico-mural)  -- apresenta -- [**ANOTAÇÃO**](../../../base/requisitos/modelagem/lexicos/#lexico-anotacao): Um [mural](../../../base/requisitos/modelagem/lexicos/#lexico-mural) mostra as últimas [anotações](../../../base/requisitos/modelagem/lexicos/#lexico-anotacao) da [criança](../../../base/requisitos/modelagem/lexicos/#lexico-crianca) e uma [anotação](../../../base/requisitos/modelagem/lexicos/#lexico-anotacao) está presente em um [mural](../../../base/requisitos/modelagem/lexicos/#lexico-mural). <br>
(Cardinalidade: 1:n)

## Conclusão
&emsp;&emsp;Tendo em vista as entidades e os relacionamentos aqui demonstrados, pode-se notar a necessidade da criação de tabelas associativas para melhor representar as relações de cardinalidade n:m apresentados nos relacionamentos 1, 9, 10, 11, 13 e 14. Além disso, nota-se que, pela cardinalidade do relacionamento 12, que a entidade Mural deve ser acoplada a entidade [criança](../../../base/requisitos/modelagem/lexicos/#lexico-crianca), tendo seus atributos e relacionamentos transferidos.

## Bibliogarafia
> - [Documento de Arquitetura do projeto Acácia](https://fga-eps-mds.github.io/2019.2-Acacia/#/architecture_document);
> - [Documento de Arquitetura do projeto Ziguen](https://github.com/francisco1code/2020-1-Ziguen/blob/master/docs/wiki/Documento_arquitetura.md#4---Vis%C3%A3o-de-Dados);
> - JOEL. Modelo Entidade Relacionamento (MER) e Diagrama Entidade-Relacionamento (DER). DevMedia, 2014. Disponível em: <https://www.devmedia.com.br/modelo-entidade-relacionamento-mer-e-diagrama-entidade-relacionamento-der/14332>. Acesso em: 18 ago. 2021.

## Versionamento
| Versão | Data | Modificação | Autor |
| :-: | -- | -- | -- |
| 0.1 | 18/08/2021 | Definição de entidades e relacionamentos | Daniel Porto, Francisco Emanoel  |
| 1.0 | 18/08/2021 | Abertura do documento e adição da Metodologia, das entidades, dos relacionamentos e da conclusão | Daniel Porto, Francisco Emanoel  |
| 1.1 | 19/08/2021 | Adicionando descrição das entidades e a introdução do documento | Daniel Porto, Francisco Emanoel  |
| 1.2 | 20/08/2021 | Adição dos léxicos | Daniel Porto |