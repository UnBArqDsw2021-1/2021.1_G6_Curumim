# GRASP - Padrões de Software para Atribuição de Responsabilidade Geral

Padrões GRASP são uma ajuda na hora de entender como desenhar um software orientado à objetos de maneira metódica, racional e explicável (LARMAN, 2004). Têm o intuito de tornar o código mais flexível, facilitando a manutenção e a extensibilidade.

## Criador


## Especialista
&emsp;&emsp;
Antes de definir exatamente o que é o "Especialista", é importante entender que o [criador](#criador), por exemplo, é um especialista, mas com um olhar focado em criação de instâncias. 
Por um outro lado, o padrão de projeto Especialista se preocupa em atribuir responsabilidades para alguma entidade mais especialista, seja mais especialista em instâncias ou não. O importante é que seja em um aspecto do sistema que há alguma entidade a fazer melhor aquilo, como por exemplo, em cadastrar uma [criança](../../base/requisitos/modelagem/lexicos/#lexico-crianca), [lançar uma presença](../../base/requisitos/modelagem/lexicos/#lexico-lancar-presenca), entre outros.

Alguns problemas foram identificados: falta de um princípio geral para atribuir responsabilidades a objetos e a necessidade de fazer escolhas sobre a atribuição de responsabilidades a entidades. Diante dessas dificuldades, veio a solução: iniciar declarando claramente a responsabilidade e atribuir uma responsabilidade de informação a uma entidade.

Um malefício claro desse padrão é quando a solução sugerida pelo especialista não é desejável, o que pode acontecer em algumas situações, mas os benefícios são inquestionáveis: baixo acoplamento, o encapsulamento da informação é mantido e a definição de entidades mais fáceis de entender e manter é encojarada.

## Controlador


## Invenção pura


## Alta Coesão


## Baixo Acoplamento


## Indireção


## Variações protegidas


## Polimorfismo



## Bibliografia

> - LARMAN, Craig. <b>Utilizando UML e Padrões</b>: Uma introdução à análise e ao projeto orientados a objetos e ao desenvolvimento iterativo. 3. ed. [S. l.: s. n.], 2004.
> - Videoaulas e materiais complementares presentes no moodle da disciplina Arquitetura e Desenho de Software. Disponível em https://aprender3.unb.br/course/view.php?id=8603. Acesso em: 03 set. 2021.
> - Padrões GRASP, UFU (Universidade Federal de Uberlândia). Disponível em http://www.facom.ufu.br/~bacala/ESOF/05a-Padr%C3%B5es%20GRASP.pdf. Acesso em: 03 set. 2021.
> - [Documento GRAPS do projeto Stock](https://unbarqdsw.github.io/2020.1_G12_Stock/#/Project/Estudos/GRASP);

## Versionamento
| Versão | Data | Modificação | Autor |
|--|--|--|--|
|1.0|01/09/2021| Abertura do documento | Mateus O. Patrício |
|1.1|03/09/2021| Adição do especialista | Gabriel Bonifácio |