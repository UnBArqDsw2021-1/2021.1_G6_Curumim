# Modelo entidade relacionamento


## Entidades

### Responsaveis

|Atributos | Propriedade | Tipo | Descrição |
|----------|-------------|------|-----------|
|IdResponsavel|Chave primária|Inteiro|Indetificação do administrador|
|Name|Obrigatório|String|        |
|Cpf|Obrigatório|String|         |
|Email|Obrigatório|String|       |
|Password|Obrigatório|String|      |
|Address|Obrigatório|String|       |

### Administrador

|Atributos | Propriedade | Tipo | Descrição |
|----------|-------------|------|-----------|
|IdAdm|Chave primária|Inteiro|Indetificação do administrador|
|Name|Obrigatório|String|        |
|Cpf|Obrigatório|String|       |
|Email|Obrigatório|String|    |
|Password|Obrigatório|String|    |
|Registration|Obrigatório|Inteiro|      |


### Professor

|Atributos | Propriedade | Tipo | Descrição |
|----------|-------------|------|-----------|
|IdProfessor|Chave primária|Inteiro|Indetificação do administrador|
|Name|Obrigatório|String||
|Cpf|Obrigatório|String||
|Email|Obrigatório|String||
|Password|Obrigatório|String||
|Registration|Obrigatório|Inteiro||


### Criança

|Atributos | Propriedade | Tipo | Descrição |
|----------|-------------|------|-----------|
|IdCrianca|Chave primária|Inteiro|Indetificação do administrador|
|IdResponsavel|Chave estrangeira |Inteiro|   |
|IdClass|Chave estrangeira |Inteiro|        |
|Name|Obrigatório|String|               |
|Registration|Obrigatório|Inteiro|         |


### Turma

|Atributos | Propriedade | Tipo | Descrição |
|----------|-------------|------|-----------|
|IdClass|Chave primária|Inteiro|Indetificação do administrador|
|IdTeacher|Chave estrangeira |Inteiro[ ]|      |
|IdChild|Chave estrangeira|Inteiro[ ]|         | 
|Code|Obrigatório| String |            |
|Capacity|Obrigatório||    |


### Evento

|Atributos | Propriedade | Tipo | Descrição |
|----------|-------------|------|-----------|
|IdEvento|Chave primária|Inteiro|Indetificação do administrador|
|IdAdm|Chave estrangeira|Inteiro|    |
|IdClass|Chave estrangeira |Inteiro|    |
|Description|Obrigatório|  |     |
|Title|Obrigatório|     |     |
|Date|Obrigatório|      |      |


### EventoTurma

|Atributos | Propriedade | Tipo | Descrição |
|----------|-------------|------|-----------|


### Atividade

|Atributos | Propriedade | Tipo | Descrição |
|----------|-------------|------|-----------|



### Anotação

|Atributos | Propriedade | Tipo | Descrição |
|----------|-------------|------|-----------|



### Mural

|Atributos | Propriedade | Tipo | Descrição |
|----------|-------------|------|-----------|


### Centro de Ensino

|Atributos | Propriedade | Tipo | Descrição |
|----------|-------------|------|-----------|


### Relatório

|Atributos | Propriedade | Tipo | Descrição |
|----------|-------------|------|-----------|



## Versionamento
| Versão | Data | Modificação | Autor |
| :-: | -- | -- | -- |
| 0.1 | 18/08/2021 | Criando documento MER | Daniel Porto, Francisco Emanoel  |




