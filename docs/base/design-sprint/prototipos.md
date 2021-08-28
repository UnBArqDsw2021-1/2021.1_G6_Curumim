# Prototipação

## Introdução

&emsp;&emsp;O [protótipo](../../requisitos/modelagem/lexicos/#lexico-prototipo) é utilizado para apresentar conceitos e funcionalidades de uma forma simples, com o objetivo de criar uma representação semi realística de algo para que seja possível interagir e testar com [usuários](../../requisitos/modelagem/lexicos/#lexico-usuario) reais. A sua principal função é descobrir problemas e oportunidades de melhorias antes de começar o desenvolvimento do produto, diminuindo o esforço gasto com os mesmos no futuro. Ele deve ser desenvolvido com base nos requisitos elicitados, e depois testado para validar se funciona conforme o esperado.<br>
&emsp;&emsp;Segundo Sommerville (2012), “um protótipo é uma versão inicial de um sistema de software, usado para demonstrar conceitos, experimentar opções de projeto e descobrir mais sobre o problema e suas possíveis soluções.”<br>
&emsp;&emsp;Já segundo BENYON (2011), "A utilização de protótipos é algo comum no ambiente de design e construção de software. Um protótipo é uma representação ou implementação concreta, porém parcial, do design de um sistema. É considerado a primeira e mais importante forma para envolver pessoas e clientes durante o processo de avaliação das ideias de design".

## Metodologia

&emsp;&emsp;Para a produção dos [protótipos](../../requisitos/modelagem/lexicos/#lexico-prototipo) o time decidiu que cada membro faria um [protótipo de baixa fidelidade](../../requisitos/modelagem/lexicos/#lexico-prototipo-de-baixa-fidelidade) de acordo com as funcionalidades e requisitos elicitados. Após a produção individual dos [protótipos](../../requisitos/modelagem/lexicos/#lexico-prototipo), o time se reuniu para decidir o que gostamos e não gostamos a partir da análise de todos os membros e produzimos um fluxograma do app. Esses [protótipos de baixa fidelidade](../../requisitos/modelagem/lexicos/#lexico-prototipo-de-baixa-fidelidade) serviram de inspiração para a criação do [protótipo de alta fidelidade](../../requisitos/modelagem/lexicos/#lexico-prototipo-de-alta-fidelidade), [protótipo](../../requisitos/modelagem/lexicos/#lexico-prototipo) este que será testado, de acordo com o nosso planejamento de avaliação, com [usuários](../../requisitos/modelagem/lexicos/#lexico-usuario) que se enquadrem nos perfis descritos nas personas.

#### Fluxograma
&emsp;&emsp;Fluxograma utilizado para ajudar na criação do [protótipo de alta fidelidade](../../requisitos/modelagem/lexicos/#lexico-prototipo-de-alta-fidelidade).
![fluxo-prototipo](https://user-images.githubusercontent.com/37383185/128437055-e4cec67c-a1a3-4c97-b751-62177bd17d6e.jpg)
<center>[Figura 1: Fluxograma da aplicação](https://user-images.githubusercontent.com/37383185/128437055-e4cec67c-a1a3-4c97-b751-62177bd17d6e.jpg)</center>


## Protótipos

### [Protótipo de Baixa Fidelidade](prototipo-baixa.md)

### [Planejamento da Avaliação do Protótipo de Alta Fidelidade](plan-test.md)

### [Protótipo de Alta Fidelidade](prototipo-alta.md)

## Resultados

&emsp;&emsp;Todas as pessoas que realizaram o teste se encaixavam em algum dos perfis descritos nas [personas](../requisitos/elicitacao/personas.md). As tarefas foram distribuídas da seguinte maneira:
- Para perfil de [administrador](../../requisitos/modelagem/lexicos/#lexico-administrador): Cadastrar uma [turma](../../requisitos/modelagem/lexicos/#lexico-turma), matricular um [aluno](../../requisitos/modelagem/lexicos/#lexico-aluno) e cadastrar um [evento](../../requisitos/modelagem/lexicos/#lexico-evento).
- Para perfil de [professor](../../requisitos/modelagem/lexicos/#lexico-professor): Cadastrar [atividade](../../requisitos/modelagem/lexicos/#lexico-atividade), [lançar presença](../../requisitos/modelagem/lexicos/#lexico-lancar-presenca) e abrir conversa com um [responsável](../../requisitos/modelagem/lexicos/#lexico-responsavel).
- Para perfil de [responsável](../../requisitos/modelagem/lexicos/#lexico-responsavel): Verificar as [atividades](../../requisitos/modelagem/lexicos/#lexico-atividade) da [criança](../../requisitos/modelagem/lexicos/#lexico-crianca), conversar com um [professor](../../requisitos/modelagem/lexicos/#lexico-professor) e acessar perfil do [centro educacional](../../requisitos/modelagem/lexicos/#lexico-centro-educacional).

&emsp;&emsp;Os resultado dos testes realizado no Usability Hub podem ser visualizados nos links a seguir:

- [Teste de usabilidade para perfil de administrador](https://app.usabilityhub.com/tests/9e02d61df442/results/e34c2ef6a0d6)
- [Teste de usabilidade para perfil de professor](https://app.usabilityhub.com/tests/90861625b53d/results/9e48eefddc3b)
- [Teste de usabilidade para perfil de responsável](https://app.usabilityhub.com/tests/28d7731ec8c2/results/d6372662f41c)

&emsp;&emsp;Para o questionário obtivemos o seguinte resultado:

&emsp;&emsp;Em uma escala de 1 a 5, onde 1 equivale a inútil e 5 a muito útil, qual é seu grau de utilidade da plataforma Curumim?
![image](https://user-images.githubusercontent.com/37383185/128441747-a079ac58-f9b8-4452-9a12-675bd364020a.png)
<center>[Figura 2: Respostas da pergunta 1](https://user-images.githubusercontent.com/37383185/128441747-a079ac58-f9b8-4452-9a12-675bd364020a.png)</center>

&emsp;&emsp;Em uma escala de 1 a 5, onde 1 equivale a muito fácil e 5 a muito difícil, avalie o grau de dificuldade na execução das tarefas?
![image](https://user-images.githubusercontent.com/37383185/128441793-eb8a5935-a957-4f9b-a5ab-ca1da12cecae.png)
<center>[Figura 2: Respostas da pergunta 2](https://user-images.githubusercontent.com/37383185/128441793-eb8a5935-a957-4f9b-a5ab-ca1da12cecae.png)</center>

&emsp;&emsp;Alguma sugestão de melhoria para a realização das tarefas?
![image](https://user-images.githubusercontent.com/37383185/128441858-d8da2a7c-8b30-4d4b-95f0-bf7ac8eb65e2.png)
<center>[Figura 3: Respostas da pergunta 3](https://user-images.githubusercontent.com/37383185/128441858-d8da2a7c-8b30-4d4b-95f0-bf7ac8eb65e2.png)</center>

&emsp;&emsp;Problemas de usabilidades descobertos:

| Onde ocorreu | descrição | sugestões de correção |
|--------------|-----------|-----------------------|
| Perfil do estudante | Algumas pessoas clicaram no nome ou no espaço em branco para abrir os detalhes das [atividades](../../requisitos/modelagem/lexicos/#lexico-atividade). | Abrir a descrição da [atividade](../../requisitos/modelagem/lexicos/#lexico-atividade) em toda a caixa além do botão de detalhes.|
| Home de [administrador](../../requisitos/modelagem/lexicos/#lexico-administrador) | Ao invés de clicar na aba de [turmas](../../requisitos/modelagem/lexicos/#lexico-turma) ou [eventos](../../requisitos/modelagem/lexicos/#lexico-evento) procuraram na barra lateral. | Adicionar opções que estão apenas na página inicial na barra lateral também.|
| Home de [professor](../../requisitos/modelagem/lexicos/#lexico-professor) | Algumas pessoas procuraram a aba de [presença](../../requisitos/modelagem/lexicos/#lexico-presenca) no menu lateral. | Adicionar opções que estão apenas na página inicial na barra lateral também.

## Bibliografia

> - [Documentação do protótipo do projeto Stock](https://unbarqdsw.github.io/2020.1_G12_Stock/#/Product/Prototipos);
> - [Documentação do protótipo do projeto SYA](https://unbarqdsw.github.io/2020.1_G11_SYA/#/prototipos/prototipo_alta);
> - Vantagens da prototipação no desenvolvimento de software: <https://www.treinaweb.com.br/blog/vantagens-da-prototipacao-no-desenvolvimento-de-software/>. Acesso em 04 ago. 2021.
> - SIMONE DINIZ JUNQUEIRO BARBOSA, BRUNO SANTANA DA SILVA, Interação Humano-Computador, 1a . Edição, Editora Campus, 2010.
> - FRANCISCO, Tatiane. Baixa, média ou alta fidelidade?. [S. l.], 2019. Disponível em <https://www.dextra.com.br/blog/baixa-media-ou-alta-fidelidade-conheca-as-diferencas-entre-os-tipos-de-prototipos/#:~:text=Prot%C3%B3tipo%20de%20m%C3%A9dia%20fidelidade,com%20os%20elementos%20da%20interface.>. Acesso em: 26 ago. 2021.
> - SOMMERVILLE, Ian. Engenharia de software. 9. ed. 2012.
> - BENYON, D. Interação humano-computador. 2. ed. São Paulo: Pearson Prentice Hall, 2011. 442 p.

## Versionamento
| Versão | Data | Modificação | Autor |
|--|--|--|--|
|1.0|30/07/2021| Abertura do documento | Daniel Porto |
|1.1|04/08/2021| Adição da introdução, metodologia e [protótipos](../../requisitos/modelagem/lexicos/#lexico-prototipo) | Mateus O. Patrício |
|1.2|05/08/2021| Adição do fluxograma | Mateus O. Patrício |
|1.3|06/08/2021| Adição de hiperlinks dos léxicos | Mateus O. Patrício |
|1.4|21/08/2021| Correção dos links dos léxicos | Gabriel Bonifácio |
| 1.5 | 26/08/2021 | Correções nos textos, referências e links com outros artefatos | Nilo Mendonça, Bruno Félix |
|1.6|28/08/2021|Revisão por pares|Daniel Porto, Mateus O. Patrício | 