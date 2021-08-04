# Políticas de Contribuição

## Introdução
&emsp;&emsp;O presente documento visa apresentar as políticas que serão usadas no decorrer do projeto, detalhando as politicas de branchs e seu fluxo de trabalho, commits, issues e pull requests.

## Política de Branchs
&emsp;&emsp;É de suma importância que toda nova branch criada esteja devidamente atribuida a um issue do projeto<br>
&emsp;&emsp;O produto que está sendo desenvolvido tem como versão inicial **v0.0.0**.
### Fluxo de trabalho
#### Main
- Branch que contém o código mais estável da aplicação e em nível de produção;
- Existe penas uma branch main;
- Não é permitidos commits feitos diretamente na main;
- Deve aceitar mesclagens apenas de branches do tipo [hotfix](#hotfix) e [releases](#release);
- Na situação do repositório de documentação, deve aceitar mesclagem das branchs do tipo [doc](#doc);
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
- Deve ser marcada por uma 'tag' que representa o Número da Versão da release.
- Nome: release_v-xxx, onde xxx é o número da versão.
- Exemplo:
> Versão atual: 1.0.2<br>
> Nova release: release_v-1.1.2<br>
> Nova versão:  1.1.2  

#### Feature
- Branch direcionada ao desenvolvimento de uma nova funcionalidade do produto:
- Deve ser derivada da branch [develop](#develop);
- Deve ser mesclado de volta a branch [develop](#develop) e excluida do projeto após a funcionalidade ser desenvolvida;
- Nome: feature/USXXX_issueID_Nome-da-Feature, onde XXX é o número da Use story;
- Exemplo:
> feature/US999_42_cadastro

#### Doc
- Branch direcionada ao desenvolvimento de documentação;
- Deve ser derivada da branch [main](#main);
- Deve ser mesclado de volta a branch [main](#main) e excluida do projeto após a documentação;
- Nome: doc/issueID_Nome-do-artefato;
- Exemplo:
> doc/42_especificacao-suplementar

#### Bugfix
- Branch direcionada à implementação de soluções de bugs e erros encontrados numa [release](#release);
- Deve ser derivada da branch [release](#release);
- Deve ser mesclada a branch [release](#release) e excluida do projeto após a resolução do ponto abordado;
- Nome: bugfix/issueID_Nome-do-Bug.
- Exemplo:
> bugfix/42_erro-responsividade-pg-login

#### Hotfix
- Branch direcionada à implementação de soluções de bugs e erros emergentes encontrados em produção, na branch [main](#main);
- Deve ser derivada da branch [main](#main);
- Deve ser mesclada a branch [main](#main) e a [develop](#develop) e excluida do projeto após a resolução do ponto abordado;
- A cada novo hotfix, a versão do produto deve ser modificada, acrescentando 1 ao último número;
- Nome: hotfix/issueID_Nome-do-Bug_v-xxx, onde xxx é o novo numero de versão.
- Exemplo:
> Versão atual: 1.0.2<br>
> Nova hotfix: hotfix/42_erro-autocompletar-pg-cadastro_v-1.0.3<br>
> Nova versão:  1.1.3 

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

## Política de Issues

## Política de Pull Resquests

## Versionamento
| Versão | Data | Modificação | Autor |
|:-:|--|--|--|
|1.0|03/08/2021| Abertura do documento | Daniel Porto |