# Léxicos

## Introdução

&emsp;&emsp;Léxico é uma técnica de modelagem utilizada com o intuito de melhorar o entendimento sobre termos utilizados. Com o desenvolvimento dos artefatos se pode ter um entendimento mais rico e concreto do projeto e todas as terminologias usadas pelo grupo. Ao longo da [Design Sprint](../../../design-sprint/doc-design-sprint), ouve um constante aprendizado e aprimoramento do escopo do projeto e todas as palavras e frases que são cruciais na aplicação.

&emsp;&emsp;Este documento tem a finalidade de apresentar todos os léxicos levantados durante o desenvolvimento da wiki.

## Léxicos
&emsp;&emsp;A metodologia trabalhada nesse documento foi a **LAL - Léxico Ampliado da Linguagem**, trata-se de um método para descrever termos relacionados ao projeto.<br>
&emsp;&emsp;Cada léxico(termo) feito é estruturado segundo as seguintes definições:

- Número identificador do termo;<br>
- Nome do termo;<br>
- Classificação: Se o termo se for referente a um sujeito, objeto, verbo ou estado. Sujeito para os que se referem a atores que podem realizar ações, verbo para os termos que indicam ações, estado para os que indicam alguma condição temporária, e objeto para aqueles que não se encaixam em nenhum dos dois casos anteriores.<br>
- Noção: Significado e contexto do termo;<br>
- Impacto: Quais são os impactos referentes ao acontecimento do termo;<br>
- Sinônimos: Termos que têm o mesmo significado no projeto;<br>

&emsp;&emsp;Todos os léxicos estão organizados respeitando a seguinte tabela:

| Número Léxico | Nome do léxico |
| -- | -- |
| Classificação | |
| Noção | |
| Impacto | |
| Sinônimo | |

### Léxico - Responsável

| L01 | Responsável |
| -- | -- |
| Classificação | Sujeito |
| Noção | - Ter uma ou mais crianças que estão matriculadas no [centro de ensino]().<br>- O [usuário](#lexico-usuario) que utiliza o sistema e tem acesso a funcionalidades desse perfil. |
| Impacto | - Pode se cadastrar e se validar no sistema;<br>- Pode entrar em contato com [professor](#lexico-professor)<br>- Pode visualizar os dados e as informações de suas [crianças](#lexico-crianca). |
| Sinônimo | - [Pai](#lexico-pai)<br> - [Usuário](#lexico-usuario) |

### Léxico - Protótipo

| L02 | Protótipo |
| -- | -- |
| Classificação | Objeto |
| Noção | - É um esboço em desenho ou em programa gráfico de como ficará o produto final. |
| Impacto | - O designer criou o protótipo.<br> - O stakeholder aprovou o protótipo. |
| Sinônimo | - Esboço |

### Léxico - Protótipo de baixa fidelidade

| L03 | Protótipo de baixa fidelidade |
| -- | -- |
| Classificação | Objeto |
| Noção | É um esboço em desenho contemplando funcionalidades de maneira simplista do produto final. |
| Impacto | - O time decidiu se reunir e cada membro fez um protótipo de baixa fidelidade;<br>- Com isso em mãos, o grupo pode discutir e criar o [Protótipo de alta fidelidade](#lexico-prototipo-de-alta-fidelidade). |
| Sinônimo | - [Protótipo](#lexico-prototipo) |

### Léxico - Protótipo de alta fidelidade

| L04 | Protótipo de alta fidelidade |
| -- | -- |
| Classificação | Objeto |
| Noção | - É uma representação interativa do produto. Esse tipo de protótipo representa o design final de forma fidedigna. |
| Impacto | - O protótipo de alta fidelidade foi desenvolvido na plataforma Figma;<br>- Principal base e influência do virá a ser o [Front End](#lexico-desenvolvimento-front-end) da aplicação.. |
| Sinônimo | - [Protótipo](#lexico-prototipo) |

### Léxico - Usuário

| L05 | Usuário |
| -- | -- |
| Classificação | Sujeito |
| Noção | - Pessoa que utiliza o sistema e se encaixa em alguma das personas definidas. |
| Impacto | - O usuário pode fazer login.<br> - O usuário pode gerar um [relatório](#lexico-relatorio).<br> - O usuário pode cadastrar uma [atividade](#lexico-atividade). |
| Sinônimo | - [Administrador](#lexico-administrador)<br> - [Professor](#lexico-professor)<br> - [Responsável](#lexico-responsavel)<br> - [Pai](#lexico-pai) |

### Léxico - Stakeholder

| L06 | Stakeholder |
| -- | -- |
| Classificação | Sujeito |
| Noção | - Partes interessadas, que devem estar de acordo com as decisões, no produto final. |
| Impacto | - Deve estar de acordo com o que está sendo produzido. <br> - Sua opinião é levada em consideração no desenvolvimento do projeto e do produto |
| Sinônimo | - Pessoa interessada no projeto. |

### Léxico -  Pai

| L07 | Pai |
| -- | -- |
| Classificação | Sujeito |
| Noção | - O [responsável](#lexico-responsavel) por uma ou mais [crianças](#lexico-crianca) que estão matriculadas no [centro de ensino](#lexico-centro-educacional).<br>- O [usuário](#lexico-usuario) que utiliza o sistema e tem acesso a funcionalidades desse perfil. |
| Impacto | - Podem se cadastrar e se validar no sistema;<br>- Podem entrar em contato com [professor](#lexico-professor)<br>- Pode visualizar os dados e as informações de suas [crianças](#lexico-crianca).|
| Sinônimo | - [Responsável](#lexico-responsavel) |

### Léxico -  Professor

| L08 | Professor |
| -- | -- |
| Classificação | Sujeito |
| Noção | - Pessoa responsável por gerir o ensino e organização de uma [turma](#lexico-turma) de [alunos](#lexico-aluno), criando e conduzindo as [atividades](#lexico-atividade), lançando [presença](#lexico-presenca) e comunicando com os [pais](#lexico-pai)/ [responsáveis](#lexico-responsavel).|
| Impacto | - Pode criar e gerenciar uma [atividade](#lexico-atividade);<br> - Pode [lançar presença](#lexico-lancar-presenca); O professor pode enviar anotações para um [aluno]().
| Sinônimo | |

### Léxico - Administrador

| L09 | Administrador |
| -- | -- |
| Classificação | Sujeito |
| Noção | - Pessoa que gerencia o [Centro Educacional](#lexico-centro-educacional) |
| Impacto | - Pode cadastrar uma [criança](#lexico-crianca);<br> - Pode cadastrar um [professor](#lexico-professor);<br> - Pode criar uma [turma](#lexico-turma); <br> - Pode criar e gerenciar um [evento](#lexico-evento). <br> |
| Sinônimo | - Gestor |

### Léxico -  Agenda

| L10 | Agenda |
| -- | -- |
| Classificação | Objeto |
| Noção | - Local onde o [professor](#lexico-professor) faz anotações |
| Impacto | - O [professor](#lexico-professor) anota informações sobre cada [aluno](#lexico-aluno) em sua respectiva agenda; <br> - Local que reunirá todas as [anotações](#lexico-anotacao) da [criança](#lexico-crianca). |
| Sinônimo | |

### Léxico -  Criança

| L11 | Criança |
| -- | -- |
| Classificação | Sujeito |
| Noção | - Os [alunos](#lexico-aluno) do [centro educacional](#lexico-centro-educacional) |
| Impacto | - Podem participar de [eventos](#lexico-evento)<br>- Podem realizar [atividades](#lexico-atividade). |
| Sinônimo | - [Aluno](#lexico-aluno) |

### Léxico - Notificação

| L12 | Notificação |
| -- | -- |
| Classificação | Objeto |
| Noção | - Mensagens enviadas pelo app com o intuito de alertar. |
| Impacto | - Os [responsáveis](#lexico-responsavel) irão receber notificações sobre novos eventos, [atividades](#lexico-atividade) e sobre a entrada e saída de suas [crianças](#lexico-crianca) |
| Sinônimo | |

### Léxico - Turma

| L13 | Turma |
| -- | -- |
| Classificação | Objeto |
| Noção | - Conjunto de [alunos](#lexico-aluno) que seguem o mesmo programa e possuem o mesmo [professor](#lexico-professor). |
| Impacto | - Os administradores as criarão e alocarão os [professores](#lexico-professor) e os [alunos](#lexico-aluno) nelas;<br>- O [professor](#lexico-professor) poderá criar [atividades](#lexico-atividade) para a turma. |
| Sinônimo | - Sala de aula |

### Léxico - Evento

| L14 | Evento |
| -- | -- |
| Classificação | Objeto |
| Noção | - Ações em grupo organizadas pelos [administradores](#lexico-administrador). |
| Impacto | - Os [administradores](#lexico-administrador) organizarão um momento coletivo para todas as [turmas](#lexico-turma) do [Centro Educacional](#lexico-centro-educacional).|
| Sinônimo | |

### Léxico - Presença

| L15 | Presença |
| -- | -- |
| Classificação | Objeto |
| Noção | - Marcador de frequência dos [alunos](#lexico-aluno). |
| Impacto | - Os [professores](#lexico-professor) marcaram as presenças dos [alunos](#lexico-aluno) na aplicação;<br> - Assim os [pais](#lexico-pai) e [responsáveis](#lexico-responsavel) poderão acompanhar a presença da [criança](#lexico-crianca). |
| Sinônimo | - Frequência |

### Léxico - Anotação

| L16 | Anotação |
| -- | -- |
| Classificação | Objeto |
| Noção | - Informações sobre o [aluno](). |
| Impacto | - As anotações estarão estarão dentro da agenda dos [alunos](#lexico-aluno); <br> - Será o jeito formal mais direto que um [professor](#lexico-professor) terá para informar algo ao [responsável](#lexico-responsavel). |
| Sinônimo | |

### Léxico - Relatório

| L17 | Relatórios |
| -- | -- |
| Classificação | Objeto |
| Noção | - Os [professores](#lexico-professor) disponibilizarão um relatório sobre os [alunos](#lexico-aluno). |
| Impacto | - Será disponibilizado no perfil do [aluno](#lexico-aluno) um relatório sobre ele; <br> - De tempos em tempos o [responsável](#lexico-responsavel) tera informações do [aluno](#lexico-aluno) de forma detalhada. |
| Sinônimo | |

### Léxico - Atividade

| L18 | Atividade |
| -- | -- |
| Classificação | Objeto |
| Noção | - Práticas desenvolvidas pelos [professores](#lexico-professor) para a realização dos [alunos](#lexico-aluno) no [Centro Educacional](#lexico-centro-educacional). |
| Impacto | - Os [professores](#lexico-professor) cadastram [atividades](#lexico-atividade) para suas [turmas](#lexico-turma) dentro da aplicação. |
| Sinônimo | - Práticas |

### Léxico - Educação

| L19 | Educação |
| -- | -- |
| Classificação | Objeto |
| Noção | - Ação ou efeito de educar, de aperfeiçoar as capacidades.  |
| Impacto | - O objetivo de um [centro educacional](#lexico-centro-educacional) é promover a educação das [crianças](#lexico-crianca).  |
| Sinônimo | - Pedagogia  |


### Léxico - Autenticação em duas etapas

| L20 | Autenticação em duas etapas |
| -- | -- |
| Classificação | Verbo |
| Noção | Torna necessário que o [usuário](#lexico-usuario) forneça além do login e senha, um código enviado pela aplicação para a autenticação no aplicativo |
| Impacto | O [usuário](#lexico-usuario) acessa a sua conta através dele |
| Sinônimo | Login |

### Léxico - Desenvolvimento Full-stack

| L21 | Full-stack |
| -- | -- |
| Classificação | Objeto |
| Noção | Desenvolvimento do código fonte do software que contempla todas todas as etapas de desenvolvimento, do inicio a entrega da funcionalidade |
| Impacto | Prática usada pelo desenvolvedor para escrever o código fonte  |
| Sinônimo | Etapas de desenvolvimento do software |

### Léxico - Desenvolvimento Front-end

| L22 | Front-end |
| -- | -- |
| Classificação | Objeto |
| Noção | Desenvolvimento do código fonte referente a parte visual, de contato direto com o [usuário](#lexico-usuario) final |
| Impacto | Prática usada pelo desenvolvedor para escrever o código fonte |
| Sinônimo | Interface da aplicação |


### Léxico - Baixar relatório

| L23 | Baixar relatório |
| -- | -- |
| Classificação | Verbo |
| Noção | O [responsável](#lexico-responsavel) clica para baixar o relatório sobre os dados da sua [criança](#lexico-crianca) |
| Impacto | O [responsável](#lexico-responsavel) recebe um relatório detalhado sobre os dados da sua [criança](#lexico-crianca) |
| Sinônimo | - |

### Léxico - Cadastrar Turma
| L24 | Cadastrar Turma |
| -- | -- |
| Classificação | Verbo |
| Noção | Cadastro de uma nova turma |
| Impacto | O administrador cadastra uma nova turma para poderem adicionar mais [crianças](#lexico-crianca) |
| Sinônimo | Registrar Turma |

### Léxico - Lançar presença 
| L25 | Lançar presença |
| -- | -- |
| Classificação | Verbo |
| Noção | Lançamento de presença para registrar presença no dia |
| Impacto | O [professor](#lexico-professor) lança presença, permitindo ao [responsável](#lexico-responsavel) a visualização dos dias que a [criança](#lexico-crianca) esteve ou não ausente |
| Sinônimo | Registrar presença, confirmar presença | |

### Léxico - Centro educacional

| L26 | Centro educacional |
| -- | -- |
| Classificação | - Objeto |
| Noção | - [Instituição](#lexico-instituicao) que aplica a utilização da plataforma. |
| Impacto | - As funcionalidade da plataforma giram em torno do dia a dia de um centro educacional; <br> - Promover a qualidade de [educação](#lexico-educacao) |
| Sinônimo | - Centro de ensino |

### Léxico - Aluno

| L27 | Aluno |
| -- | -- |
| Classificação | Sujeito |
| Noção | - As [crianças](#lexico-crianca) matriculadas no [centro educacional](#lexico-centro-educacional) |
| Impacto | - Os alunos podem participar de [eventos](#lexico-evento)<br>- Os alunos podem realizar [atividades](#lexico-atividade)|
| Sinônimo | - [Criança](#lexico-crianca) |

### Léxico - Instituição

| L28 | Instituição |
| -- | -- |
| Classificação | Sujeito |
| Noção | - Pessoa que responde pelo [centro educacional](#lexico-centro-educacional). |
| Impacto | - A instituição pode trocar mensagens com os [responsáveis](#lexico-responsavel).<br> - A instituição pode postar [eventos](#lexico-evento) que acontecerão. |
| Sinônimo | - [Administrador](#lexico-administrador) |

### Léxico - Mobile

| L29 | Mobile |
| -- | -- |
| Classificação | Objeto |
| Noção | - Aparelho celular utilizado pelo [usuário](#lexico-usuario). |
| Impacto | - Um dos locais pelo qual o aplicativo poderá ser acessado; <br> - [Usuário](#lexico-usuario) terá mais praticidade e facilidade em usar a aplicação. |
| Sinônimo | - Celular |

### Léxico - Notificar

| L30 | Notificar |
| -- | -- |
| Classificação | Verbo |
| Noção | Possibilita o [usuário](#lexico-usuario) a ser informado sem desvios ou perdas de informações. |
| Impacto | O [usuário](#lexico-usuario) recebe informações sobre [eventos](#lexico-evento) do [Centro Educacional](#lexico-centro-educacional). |
| Sinônimo | - Informar<br> - Sinalizar |

### Léxico - Bug

| L31 | Bug |
| -- | -- |
| Classificação | Objeto |
| Noção | - Causas de mal funcionamento do sistema |
| Impacto | - Os contribuidores do projeto podem relatar e corrigir eventuais bugs.|
| Sinônimo | |

### Léxico - Mural

| L32 | Mural |
| -- | -- |
| Classificação | Objeto |
| Noção | - Tela que mostra as últimas [atividades](#lexico-atividade), [eventos](#lexico-eventos) e [anotações](#lexico-anotacao) relacionados a uma [criança](#lexico-crianca). |
| Impacto | - Os [responsáveis](#lexico-responsavel) poderão acompanhar o cronograma da [criança](#lexico-crianca) no [centro educacional](#lexico-centro-educacional).|
| Sinônimo | |


## Bibliografia
> - SERRANO, Maurício; SERRANO, Milene; Requisitos - Aula 10.

## Versionamento

| Versão | Data | Modificação | Autor |
|--|--|--|--|
|1.0|06/08/2021| Criação do documento | Mateus O. Patrício |
|1.1|06/08/2021| Adição dos léxicos [L02](#lexico-prototipo), [L03](#lexico-prototipo-de-baixa-fidelidade), [L04](#lexico-prototipo-de-alta-fidelidade), [L05](#lexico-usuario) e [L06](#lexico-stakeholder) | Mateus O. Patrício |
|1.2|06/08/2021| Adição dos léxicos [L08](#lexico-professor), [L09](#lexico-administrador), [L12](#lexico-notificacao), [L13](#lexico-turma), [L14](#lexico-evento), [L18](#lexico-atividade) e [L19](#lexico-educacao) | Enzo Gabriel |
|1.3|06/08/2021| Adição dos léxicos [L01](#lexico-responsavel), [L07](#lexico-pai), [L26](#lexico-centro-educacional), [L27](#lexico-aluno) e [L31](#lexico-bug)| Daniel Porto |
|1.4|06/08/2021| Adição dos léxicos [L28](#lexico-instituicao), [L29](#lexico-mobile), [L30](#lexico-notificar) | João Pedro |
|1.5|06/08/2021| Adição dos léxicos [L23](#lexico-baixar-relatorio), [L24](#lexico-cadastrar-turma), [L25](#lexico-lancar-presenca) | Gabriel Bonifácio |
|1.6|06/08/2021| Adição dos léxicos [L10](#lexico-agenda), [L11](#lexico-crianca), [L15](#lexico-presenca), [L16](#lexico-anotacao), [L17](#lexico-relatorio) | Bruno Félix |
|1.7|06/08/2021| Adição dos léxicos [L20](#lexico-autenticacao-em-duas-etapas), [L21](#lexico-desenvolvimento-full-stack), [L22](#lexico-desenvolvimento-front-end) | Nilo Mendonça |
|1.8|06/08/2021| Adição de hiperlinks com léxicos| Daniel Porto |
|1.9|20/08/2021| Adição do léxico [L32](#lexico-mural)| Daniel Porto |
|2.0|28/08/2021| Incrementação da Introdução e dos Impactos dos Léxicos| Bruno Félix |
|2.1|28/08/2021|Revisão por pares|Daniel Porto, Mateus O. Patrício | 