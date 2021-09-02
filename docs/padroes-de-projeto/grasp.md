# GRASP - Padrões de Software para Atribuição de Responsabilidade Geral

&emsp;&emsp;Padrões GRASP são uma ajuda na hora de entender como desenhar um software orientado à objetos de maneira metódica, racional e explicável (LARMAN, 2004). Têm o intuito de tornar o código mais flexível, facilitando a manutenção e a extensibilidade.

## Criador


## Especialista


## Controlador


## Invenção pura


## Alta Coesão


## Baixo Acoplamento


## Indireção


## Variações protegidas


## Polimorfismo

&emsp;&emsp;Antes de definir o conceito de polimorfismo adotado pelos GRAPS é importante primeiro definir o conceito de polimorfismo. Ele se apresenta como um príncipio pelo o qual as subclasses de uma superpclasse conseguem chamar métodos, que apesar de apresentarem a mesma assinatura, se comportam de maneira diferente para cada classe derivada.<br>
&emsp;&emsp;Suponha que em determinada classe são utilizadas estruturas condicionais para determinar o comportamento em função do tipo de classe, esse tipo de método pode gerar diversos problemas para a manutenção do código, sendo assim o Polimmorfismo proposto pelos GRAPS sugere que a seleção do comportamento seja dado utilizando o polimorfismo, ou seja, a superclasse cria o método e as subclasses realizam a implementação do polimorfismo.


## Bibliografia

> - [Documento GRAPS do projeto QRodízio](https://unbarqdsw.github.io/2020.1_G10_QRodizio/design_patterns/grasps/grasps.html#grasps);
> - [Documento GRAPS do projeto Stock](https://unbarqdsw.github.io/2020.1_G12_Stock/#/Project/Estudos/GRASP);
> - LARMAN, Craig. <b>Utilizando UML e Padrões</b>: Uma introdução à análise e ao projeto orientados a objetos e ao desenvolvimento iterativo. 3. ed. [S. l.: s. n.], 2004.
> - MEDIUM. Padrões GRASP — Padrões de Atribuir Responsabilidades. Disponível em: <https://medium.com/@leandrovboas/padr%C3%B5es-grasp-padr%C3%B5es-de-atribuir-responsabilidades-1ae4351eb204>. Acesso em: 02 de set. 2021.
> - DEVMEDIA. Desenvolvimento com qualidade com GRASP. <https://www.devmedia.com.br/desenvolvimento-com-qualidade-com-grasp/28704>. Acesso em: 02 de set. 2021.


## Versionamento
| Versão | Data | Modificação | Autor |
|--|--|--|--|
|1.0|01/09/2021| Abertura do documento | Mateus O. Patrício |
|1.1|02/09/2021| Adição do polimorfismo | Nilo Mendonça |