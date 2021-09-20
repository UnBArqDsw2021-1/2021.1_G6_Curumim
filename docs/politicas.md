# Políticas de Contribuição <br> <span class="rotulo-extra">Iniciativa Extra</span>

## Introdução
&emsp;&emsp;O presente documento visa apresentar as políticas que serão usadas no decorrer do projeto, detalhando as politicas de branches e seu fluxo de trabalho, [commits](https://github.com/UnBArqDsw2021-1/2021.1_G6_Curumim/commits/main), [issues](https://github.com/UnBArqDsw2021-1/2021.1_G6_Curumim/issues) e [pull requests](https://github.com/UnBArqDsw2021-1/2021.1_G6_Curumim/pulls).

## Política de Branches
&emsp;&emsp;É de suma importância que toda nova branch criada esteja devidamente atribuída a um [issue do projeto](https://github.com/UnBArqDsw2021-1/2021.1_G6_Curumim/issues).<br>
&emsp;&emsp;O produto que está sendo desenvolvido tem como versão inicial a **v0.0.0**.
### Fluxo de trabalho
#### Main
- Branch que contém o código mais estável da aplicação e em nível de produção;
- Existe penas uma branch main;
- Não é permitidos commits feitos diretamente na main;
- Deve aceitar mesclagens apenas de branches do tipo [hotfix](#hotfix) e [releases](#release);
- Na situação do repositório de documentação, deve aceitar mesclagem das branches do tipo [doc](#doc);
- Nome: main.

#### Develop
- Branch que contém a versão mais atualizada do código em nível de desenvolvimento;
- Existe apenas uma branch develop;
- Qualquer branch pode ser mesclada a develop;
- Nome: develop

#### Release
- Branch que representa um conjunto de funcionalidades, prontas para serem inseridas na [main](#main);
- Deve ser derivada da branch [develop](#develop);
- Deve ser mesclada a branch master e, se tiver sido alterada, a [develop](#develop) após a release ser concluída;
- Nenhuma funcionalidade pode ser inserida ao ambiente de produção fora de uma release;
- Deve aceita apenas Inserções de branches do tipo [bugfix](#bugfix);
- A cada nova release, a versão do produto deve ser modificada, acrescentando 1 ao número central;
- Deve ser marcada por uma 'tag' que represente o Número da Versão da release.
- Nome: release_v-xxx, onde xxx é o número da versão.
- Exemplo:
> Versão atual: 1.0.2<br>
> Nova release: release_v-1.1.2<br>
> Nova versão:  1.1.2  

#### Feature
- Branch direcionada ao desenvolvimento de uma nova funcionalidade do produto:
- Deve ser derivada da branch [develop](#develop);
- Deve ser mesclado de volta a branch [develop](#develop) e excluída do projeto após a funcionalidade ser desenvolvida;
- Nome: feature/USXXX_issueID_Nome-da-Feature, onde XXX é o número da Use story;
- Exemplo:
> feature/US999_42_cadastro

#### Doc
- Branch direcionada ao desenvolvimento de documentação;
- Deve ser derivada da branch [main](#main);
- Deve ser mesclado de volta a branch [main](#main) e excluída do projeto após a documentação;
- Nome: doc/issueID_Nome-do-artefato;
- Exemplo:
> doc/42_especificacao-suplementar

#### Bugfix
- Branch direcionada à implementação de soluções de bugs e erros encontrados numa [release](#release);
- Deve ser derivada da branch [release](#release);
- Deve ser mesclada a branch [release](#release) e excluída do projeto após a resolução do ponto abordado;
- Nome: bugfix/issueID_Nome-do-Bug.
- Exemplo:
> bugfix/42_erro-responsividade-pg-login

#### Hotfix
- Branch direcionada à implementação de soluções de bugs e erros emergentes encontrados em produção, na branch [main](#main);
- Deve ser derivada da branch [main](#main);
- Deve ser mesclada a branch [main](#main) e a [develop](#develop) e excluída do projeto após a resolução do ponto abordado;
- A cada novo hotfix, a versão do produto deve ser modificada, acrescentando 1 ao último número;
- Nome: hotfix/issueID_Nome-do-Bug_v-xxx, onde xxx é o novo número de versão.
- Exemplo:
> Versão atual: 1.0.2<br>
> Nova hotfix: hotfix/42_erro-autocompletar-pg-cadastro_v-1.0.3<br>
> Nova versão:  1.0.3 

## Política de Commits
- Mensagens devem ser em português, no gerúndio, e conter uma breve descrição do que foi feito;
- O commit deve apontar para os issues que está associado;
- Deve conter o tipo da branch em que se origina: feat para [feature](#feature), fix para [hotfix](#hotfix) ou [bugfix](#bugfix) e doc para [doc](#doc);
- Exemplos:

> feat(#xx) Alterando rotina de cadastro.<br>
> fix(#xx) Corrigindo e padronizando declaração de variáveis.<br>
> doc(#xx) Documentando a priorização.

- Deve ser usado o **Co-authored-by** para identificar o pareamento.
- Exemplo:

> feat(#xx) Alterando rotina de cadastro.<br>
> Co-authored-by: Fulano de Tal <<fulanodetal@github.com>>
https://github.com/UnBArqDsw2021-1/2021.1_G6_Curumim/blob/main/.github/ISSUE_TEMPLATE/template-basico.md
## Política de Issues
- Caso o issue esteja direcionado para o desenvolvimento de uma funcionalidade descrita no backlog, o título deve ser na forma: "USXX - Nome da história de usuário" onde XX representa o número da histíria de usuário:
> US42 - Eu, como usuário, desejo realizar login para utilizar a aplicação 
- Em geral, o nome do issue deve ser simples e descritivo;
- Devem ser seguidos os templates já definidos, [Bug Report](https://github.com/UnBArqDsw2021-1/2021.1_G6_Curumim/blob/main/.github/ISSUE_TEMPLATE/template-bug.md) ou [Template Básico](https://github.com/UnBArqDsw2021-1/2021.1_G6_Curumim/blob/main/.github/ISSUE_TEMPLATE/template-basico.md);
- Deve ser atribuído ao pipeline, o estado em que o issue se encontra no workflow. Será utilizado o workflow "Curumim" do ZenHub;
- Deve ser atribuído todos os assignees definidos para o issue;
- O issue deve ser marcado com todas a labels que são adequadas, para fins de rastreamento;
- O issue deve está atribuído a sprint e a milestone previstas para a sua execução;
- Deve ser adicionado ao issue, uma estimativa para a sua complexidade de execução;
- Quando o issue estiver direcionado para a implementação de uma histórias de usuário, deve ser atribuído o épico ao qual faz parte.

## Política de Pull Requests
- O título do Pull Request deve explicar o que está sendo inserido. Caso esteja vinculado com alguma história de usuário, indicar qual é na forma: "USXX - Nome da história de usuário" onde XX representa o número da história de usuário:
> US42 - Eu, como usuário, desejo realizar login para utilizar a aplicação 
- Os Pull requests devem seguir o template do repositório o qual deve ser preenchido pelo solicitante;
- Devem ser atribuídos dois ou mais revisores;
- Deve ser marcado com todas a labels que são adequadas, igualmente a issue correspondente;
- Deve conter a sprint e a milestone correspondente a execução das modificações;
- O Pull Request deve ser revisado e aceito por pelo menos duas pessoas;
- As pessoas responsáveis pelas revisões devem comentar seu parecer sobre as modificações feitas e, se necessário, solicitar as modificações cabíveis;
- Um Pull Request só deve ser aceito caso todos os critérios de aceitação, estipulados nas issues que ele está vinculado, sejam totalmente atendidos;
- Um Pull Request só deve ser aceito caso as modificações rodem sem erros, bugs ou mau funcionamento.

## Bibliografia
> - [Políticas de Contribuição do projeto Vamos Cuidar.](https://fga-eps-mds.github.io/2020.1-VC_Usuario/#/CONTRIBUTING)

- ## Versionamento
| Versão | Data | Modificação | Autor |
|:-:|--|--|--|
|1.0|03/08/2021| Abertura do documento | Daniel Porto |
|1.1|04/08/2021| Adição das políticas de issues e pull requests | Daniel Porto |
|1.2|17/09/2021| Atualização de informações de acordo com o feedback da entrega 1 | Gabriel Bonifácio |
|1.3|19/09/2021| Revisão por pares | Bruno Félix e Daniel Porto |