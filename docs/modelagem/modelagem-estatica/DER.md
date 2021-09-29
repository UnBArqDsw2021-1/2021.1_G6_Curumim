# Diagrama entidade relacionamento <br> <span class="rotulo-extra">Iniciativa Extra</span>

## Introdução
&emsp;&emsp;O Diagrama entidade relacionamento, também conhecido como DER, aborda uma forma de representar graficamente a modelagem do banco de dados. Basicamente, tem como objetivo organizar de forma conceitual e logica utilizando algum tipo de notação, as entiades que compõem o banco de dados e seus relacionamentos. Segundo Machado, Felipe Nery Rodrigues[[5]](#bibliografia), "O DER descreve a estrutura conceitual e lógica geral de um banco de dados."

## Metodologia
&emsp;&emsp;Para o desenvolvimento do diagrama conceitual, foi feita a leitura e análise do [MER](./MER.md) procurando elucidar graficamente as ideias contidas no artefato. Sendo assim, o diagrama conceitual possui descrito com as entidades, atributos e relacionamentos em Inglẽs, seguindo o padrão CamelCase de forma a já iniciar uma padronização do que será implementada em nível de código.<br>
&emsp;&emsp;Foi utilizada a ferramenta [Br Modelo](https://app.brmodeloweb.com) para a diagramação.

## Diagrama Conceitual

&emsp;&emsp;É um diagram que representa o modelo de forma mais próxima da realidade do usuário e com um alto nível de abstração.
Esse diagrama, juntamente ao [MER](./MER.md), devem ser tidos como base para a criação de um modelo lógico, o qual terá como foco a representação da forma de armazenamento dos dados no banco e também seus relacionamentos.
![foto](../../../assets/imagens/DER/der-conceitual-curumim.png)
<center>[Figura 1: Modelo Conceitual](../../../assets/imagens/DER/der-conceitual-curumim.png)</center>

## Bibliografia
> - [1] [Documento de Arquitetura do projeto Acácia](https://fga-eps-mds.github.io/2019.2-Acacia/#/architecture_document);
> - [2] [Documento de Arquitetura do projeto Ziguen](https://github.com/francisco1code/2020-1-Ziguen/blob/master/docs/wiki/Documento_arquitetura.md#4---Vis%C3%A3o-de-Dados);
> - [3] JOEL. Modelo Entidade Relacionamento (MER) e Diagrama Entidade-Relacionamento (DER). DevMedia, 2014. Disponível em: <https://www.devmedia.com.br/modelo-entidade-relacionamento-mer-e-diagrama-entidade-relacionamento-der/14332>. Acesso em: 18 ago. 2021.
> - [4] Introdução ao Modelo de Dados e seus níveis de abstração. SpaceProgrammer. Disponível em: <http://spaceprogrammer.com/bd/introducao-ao-modelo-de-dados-e-seus-niveis-de-abstracao/>. Acesso em 20 ago, 2021.
> - [5] Machado, Felipe Nery Rodrigues. Banco de dados: projeto e implementação, 4.ed, 2020. Disponível em: <https://books.google.com.br/books?hl=pt-BR&lr=&id=DZHODwAAQBAJ&oi=fnd&pg=PA1&dq=der+banco+de+dados&ots=aWdVsUVRQM&sig=PXCU8b35BhUNmworIpskEDbAb6c#v=onepage&q&f=false> Acesso em: 21/09/2021.

## Versionamento
| Versão | Data | Modificação | Autor |
| :-: | -- | -- | -- |
| 0.1 | 20/08/2021 | Criação diagrama conceitual | Daniel Porto, Francisco Emanoel |
| 1.0 | 20/08/2021 | Abertura do documento | Daniel Porto, Francisco Emanoel |
| 1.1 | 21/08/2021 | Revisão por pares | Mateus O. Patrício, Edson Soares |
| 1.2 | 21/09/2021 | Revisão feedback da professora |Edson Soares, Nilo Mendonça |