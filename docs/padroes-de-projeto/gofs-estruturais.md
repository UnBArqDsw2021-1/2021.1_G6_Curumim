# GOFs Estruturais

## Adapter

&emsp;&emsp;Adpter é um padrão de projeto, que tem como objetivo converter a interface de uma classe em outra interface para o cliente. Os Adapters permitem que classes trabalhem juntas, mesmo que estejam em interfaces incompatíveis.

&emsp;&emsp;Algums problemas que o Adapter pode solucionar:

- Reutilização de interfaces;
- Incompatibilidade de interfaces;
  
&emsp;&emsp;No contexto do nosso projeto, temos um exemplo de Adapter nas models da nossa aplicação, que é criada a partir da biblioteca sequelize do nodejs, e essas models funcionam como uma ponte entre o banco de dados e o app. Com isso o app fica completamente independente de qual banco de dados será utilizado.

![Exemplo de Adapter - Model Adm](../assets/imagens/gofs-adapters/adapters-model-adm.png)
<center>[Figura 1: Exemeplo de Adapter - Adm](../assets/imagens/gofs-adapters/adapters-model-adm.png)</center>

![Exemplo de Adapter - Controller Teste](../assets/imagens/gofs-adapters/adapters-controller.png)
<center>[Figura 2: Exemeplo de Adapter - Adm](../assets/imagens/gofs-adapters/adapters-controller.png)</center>

## Bibliografia

> - LARMAN, Craig. <b>Utilizando UML e Padrões</b>: Uma introdução à análise e ao projeto orientados a objetos e ao desenvolvimento iterativo. 3. ed. [S. l.: s. n.], 2004.

> - The GoF Design Patterns Reference. Disponível em: [http://www.w3sdesign.com/](http://www.w3sdesign.com/)

## Versionamento
| Versão | Data | Modificação | Autor |
|--|--|--|--|
|1.0|10/09/2021| Abertura do documento | João Pedro |
|1.1|10/09/2021| Adicionando topico Composite | João Pedro, Eliseu Kadesh |
|1.2|13/09/2021| Adicão do Adapter | Eliseu Kadesh
