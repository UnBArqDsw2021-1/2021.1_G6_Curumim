# GRASP - Padrões de Software para Atribuição de Responsabilidade Geral

Padrões GRASP são uma ajuda na hora de entender como desenhar um software orientado à objetos de maneira metódica, racional e explicável (LARMAN, 2004). Têm o intuito de tornar o código mais flexível, facilitando a manutenção e a extensibilidade.

## Criador

A instanciação de objetos é uma atividade comum em todo sistema orientado a objetos. Entender qual classe deve ser responsável por instanciar objetos reduz complexidade desnecessária do sistema.

Segundo Larman (2004), uma classe B deve ser responsável por criar instâncias de classe A se uma, ou quanto mais melhor, das seguintes afirmações se aplicarem:

- Instâncias de B contêm ou agregam instâncias de A;
- Instâncias de B gravam instâncias de A;
- Instâncias de B utilizam instâncias de A;
- Instâncias de B têm os dados necessários para iniciação das instâncias de A.

## Especialista


## Controlador


## Invenção pura


## Alta Coesão


## Baixo Acoplamento


## Indireção


## Variações protegidas


## Polimorfismo



## Bibliografia

> - LARMAN, Craig. <b>Utilizando UML e Padrões</b>: Uma introdução à análise e ao projeto orientados a objetos e ao desenvolvimento iterativo. 3. ed. [S. l.: s. n.], 2004.


## Versionamento
| Versão | Data | Modificação | Autor |
|--|--|--|--|
|1.0|01/09/2021| Abertura do documento | Mateus O. Patrício |
|1.1|01/09/2021| Adição da introdução e criador | Mateus O. Patrício |