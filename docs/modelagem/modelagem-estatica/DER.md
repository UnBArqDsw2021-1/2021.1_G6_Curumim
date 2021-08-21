# Diagrama entidade relacionamento

## Introdução
&emsp;&emsp;O Diagrama entidade relacionamento, também conhecido como DER, aborda uma forma de representar gráficamente a modelagem do banco de dados. Basicamente, tem como objetivo organizar de forma conceitual e logica utilizando algum tipo de notação, as entiades que compõem o banco de dados e seus relacionamentos.

## Metodologia
&emsp;&emsp;Para o desenvolvimento do diagrama conceitual, foi feita a leitura e analise do [MER](./MER.md) procurando elucidar gráficamente as ideias contidas no artefato. Sendo assim, o diagrama conceitual possui descrito com as entidades, atributos e relacionamentos em Inglẽs, senguindo o padrão CamelCase de forma a já iniciar uma padronização do que será implementada em nível de código.<br>
&emsp;&emsp;Foi utilizada a ferramenta [Br Modelo](https://app.brmodeloweb.com) para a diagramação.

## Diagrama Conceitual

&emsp;&emsp;É um diagram que representa o modelo de forma mais próxima da realidade do usuário e com um alto nível de abstração.
Esse diagrama, juntamente ao [MER](./MER.md), devem ser tidos como base para a criação de um modelo lógico, o qual terá como foco a representação da forma de armazenamento dos dados no banco e também seus relacionamentos.
![foto](../../../assets/imagens/DER/der-conceitual-curumim.png)
<center>[Figura 1: Modelo Conceitual](../../../assets/imagens/DER/der-conceitual-curumim.png)</center>

## Bibliografia
> - [Documento de Arquitetura do projeto Acácia](https://fga-eps-mds.github.io/2019.2-Acacia/#/architecture_document);
> - [Documento de Arquitetura do projeto Ziguen](https://github.com/francisco1code/2020-1-Ziguen/blob/master/docs/wiki/Documento_arquitetura.md#4---Vis%C3%A3o-de-Dados);
> - JOEL. Modelo Entidade Relacionamento (MER) e Diagrama Entidade-Relacionamento (DER). DevMedia, 2014. Disponível em: <https://www.devmedia.com.br/modelo-entidade-relacionamento-mer-e-diagrama-entidade-relacionamento-der/14332>. Acesso em: 18 ago. 2021.
> - Introdução ao Modelo de Dados e seus níveis de abstração. SpaceProgrammer. Disponível em: <http://spaceprogrammer.com/bd/introducao-ao-modelo-de-dados-e-seus-niveis-de-abstracao/>. Acesso em 20 ago, 2021.

## Versionamento
| Versão | Data | Modificação | Autor |
| :-: | -- | -- | -- |
| 0.1 | 20/08/2021 | Criação diagrama conceitual | Daniel Porto, Francisco Emanoel |
| 1.0 | 20/08/2021 | Abertura do documento | Daniel Porto, Francisco Emanoel |