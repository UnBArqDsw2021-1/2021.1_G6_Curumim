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

### Guardian

|Atributos | Propriedade | Tipo | Descrição |
|----------|-------------|------|-----------|
|IdGuardian|Chave primária|Inteiro|Indetificação do Responsável|
|Name|Obrigatório|String|Nome do Responsável|
|CPF|Obrigatório|String|CPF do Responsável|
|Email|Obrigatório|String| Email do  Responsável |
|Password|Obrigatório|String| Senha do  Responsável|
|Address|Obrigatório|String|  Endereço do  Responsável|

### Adm

|Atributos | Propriedade | Tipo | Descrição |
|----------|-------------|------|-----------|
|IdAdm|Chave primária|Inteiro|Indetificação do Administrador|
|Name|Obrigatório|String| Nome do Administrador |
|CPF|Obrigatório|String| CPF do Administrador|
|Email|Obrigatório|String|Email do Administrador |
|Password|Obrigatório|String| Senha do Administrador|
|Registration|Obrigatório|Inteiro| Registro do Administrador|

### Teacher

|Atributos | Propriedade | Tipo | Descrição |
|----------|-------------|------|-----------|
|IdTeacher|Chave primária|Inteiro|Indetificação do Professor|
|Name|Obrigatório|String| Nome do Professor|
|CPF|Obrigatório|String| CPF do Professor|
|Email|Obrigatório|String| Email do Professor|
|Password|Obrigatório|String| Senha do Professor|
|Registration|Obrigatório|Inteiro| Registro do Professor|

### Child

|Atributos | Propriedade | Tipo | Descrição |
|----------|-------------|------|-----------|
|IdChild|Chave primária|Inteiro| Indetificação da Criança|
|IdResponsavel|Chave estrangeira |Inteiro| Indetificação do Responsável|
|IdClass|Chave estrangeira|Inteiro| Indetificação da turma|
|Name|Obrigatório|String| Nome da Criança|
|Registration|Obrigatório|Inteiro| Registro da Criança|


### Class

|Atributos | Propriedade | Tipo | Descrição |
|----------|-------------|------|-----------|
|IdClass|Chave primária|Inteiro|Indetificação da turma|
|IdTeacher|Chave estrangeira|Inteiro[ ]| Indetificação do Professor |
|IdChild|Chave estrangeira|Inteiro[ ]| Indetificação da Criança| 
|Code|Obrigatório| String| Codigo da Turma|
|Capacity|Obrigatório|Inteiro| Capacidade da Turma|


### Event

|Atributos | Propriedade | Tipo | Descrição |
|----------|-------------|------|-----------|
|IdEvent|Chave primária|Inteiro|Indetificação do evento|
|IdAdm|Chave estrangeira|Inteiro|Indetificação do Administrador|
|IdClass|Chave estrangeira|Inteiro| Indetificação da Turma|
|Description|Obrigatório|String| Descrição do Evento|
|Title|Obrigatório|String| Titulo do Evento|
|Date|Obrigatório|Date| Data do Evento |


### Activity

|Atributos | Propriedade | Tipo | Descrição |
|----------|-------------|------|-----------|
|IdActivity|Chave primária|Inteiro|Identificação da atividade|
|IdTeacher|Chave estrangeira|Inteiro| Identificação do Professor|
|Title|Obrigatório|String| Titulo da Atividade|
|Description|Obrigatório|String| Descrição da Atividade|
|Date|Obrigatório|Date| Data da Atividade|

### Anotation

|Atributos | Propriedade | Tipo | Descrição |
|----------|-------------|------|-----------|
|IdAnotation|Chave primária|Inteiro| Identificação da anotação|
|IdTeacher|Chave estrangeira|Inteiro| Identificação do Professor|
|IdChild|Chave estrangeira|Inteiro| Identificação da Criança|
|Title|Obrigatório|String| Titulo da Anotação|
|Description|Obrigatório|String| Descrição da Anatoção|

### Board

|Atributos | Propriedade | Tipo | Descrição |
|----------|-------------|------|-----------|
|IdBoard|Chave primária|Inteiro|Identificação do mural|
|IdChild|Chave estrangeira|Inteiro| Identificação da Criança|
|IdAnotation|Chave estrangeira|Inteiro[ ]|Identificação da anotação|
|IdActivity|Chave estrangeira|Inteiro[ ]|Identificação da atividade|
|IdEvent|Chave estranfeira|Inteiro[ ]|Indetificação do evento|

### EC

|Atributos | Propriedade | Tipo | Descrição |
|----------|-------------|------|-----------|
|IdEC|Chave primária|Inteiro|Identificação do Centro de Ensino|
|IdAdm|Chave estrangeira|Inteiro[ ]|Indetificação do administrador|
|IdTeacher|Chave estrangeira|Inteiro[ ]|Indetificação do professor|
|IdClass|Chave estrangeira|Inteiro[ ]|Indetificação da turma|
|Name|Obrigatório|String| Nome do Centro de Ensino|
|Adress|Obrigatório|String| Endereço do Centro  de Ensino|
|Description|Obrigatório|String| Descrição do Centro de Ensino|

### Report

|Atributos | Propriedade | Tipo | Descrição |
|----------|-------------|------|-----------|
|IdReport|Chave primária|Inteiro|Identificação do Relatório|
|IdAdm|Chave estrangeira|Inteiro|Indetificação do Rdministrador|
|Title|Obrigatório|String| Titulo do Relatório|
|Description|Obrigatório|String| Descriçaõ do Relatório|

## Relacionamentos
1. **RESPOSÁVEL** -- possui -- **CRIANÇA**: Um reponsável possui crianças e uma criança está atrelada a responsáveis.<br>
(Cardinalidade: n:m)

2. **ADMINISTRDOR** -- registra -- **TURMA**: Um administrador registra turmas e uma turma é registrada por uma adminstrador.<br>
(Cardinalidade: 1:n)

3. **ADMINISTRDOR** -- gera -- **RELTÓRIO**: Um administrador gera relatórios e um relatório é gerado por um administrador <br>
(Cardinalidade: 1:n)

4. **CENTRO DE ENSINO** -- possui -- **ADMINISTRADOR**: O centro de ensino possui ao menos um administrador e os administradores estão atrelados a um centro de ensino.<br>
(Cardinalidade: 1:n)

5. **CENTRO DE ENSINO** -- possui -- **PROFESSOR**: O centro de ensino possui professores e os professores possuem um centro de ensino.<br>
(Cardinalidade: 1:n)

6. **CENTRO DE ENSINO** -- possui -- **TURMA**: O centro de ensino possui turmas e as turmas possuem um centro de ensino. <br>
(Cardinalidade: 1:n)

7. **PROFESSOR** -- cria -- **ATIVIDADE**: Um professor cria atividades e uma atividade é criada por um professor. <br>
(Cardinalidade: 1:n)

8. **TURMA** -- contém-- **CRIANÇA**: Uma turma contém crianças e uma criança está contida em uma turma. <br>
(Cardinalidade: 1:n)

9. **TURMA** -- contém -- **PROFESSOR**: Uma turma contém professores e um professor está contido em turmas. <br>
(Cardinalidade: n:m)

10. **TURMA** -- participa -- **EVENTO**: Uma turma participa de eventos e um evento contém a participação das turmas. <br>
(Cardinalidade: n:m)

11. **TURMA** -- aplica -- **ATIVIDADE**: Uma turma aplica atividades e uma atividade é aplicada nas turmas. <br>
(Cardinalidade: n:m)

12. **CRIANÇA** -- possui -- **MURAL**: Uma criança possui um mural e um mural está atrelado a uma criança. <br>
(Cardinalidade: 1:1)

13. **MURAL** -- apresenta -- **EVENTO**: Um mural mostra os últimos eventos para a turma da criança e um evento está presente nos murais das crianças das turmas contempladas. <br>
(Cardinalidade: n:m)

14. **MURAL** -- apresenta -- **ATIVIDADE**: Um mural mostra as últimas atividades da turma da criança e uma atividade está presente nos murais das crianças. <br>
(Cardinalidade: n:m)

16. **MURAL** -- apresenta -- **ANOTAÇÃO**: Um mural mostra as últimas anotações da criança e uma anotação está presente em um mural. <br>
(Cardinalidade: 1:n)

## Conclusão
&emsp;&emsp;Tendo em vista as entidades e os relacionamentos aqui demonstrados, pode-se notar a necessidade de criação de tabelas associativas para melhor representar as relações de cardinalidade n:m apresentados nos relacionamentos 1, 9, 10, 11, 13 e 14. Além disso, nota-se que, pela cardinalidade do relacionamento 12, que a entidade Mural deve ser acoplada a entidade Criança, tendo seus atributos e relacionamentos transferidos.

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




