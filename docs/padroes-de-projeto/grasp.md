# GRASP - Padrões de Software para Atribuição de Responsabilidade Geral

Padrões GRASP são uma ajuda na hora de entender como desenhar um software orientado à objetos de maneira metódica, racional e explicável (LARMAN, 2004). Têm o intuito de tornar o código mais flexível, facilitando a manutenção e a extensibilidade.

## Criador


## Especialista


## Controlador


## Invenção pura


## Alta Coesão

&emsp;&emsp;No projeto de software, uma qualidade básica conhecida como coesão mede informalmente como funcionalidades relacionam as operações de um elemento de software e também mede quanto trabalho um elemento de software está realizando (LARMAN, 2004). A alta coesão é garantida quando atribui-se, de forma coerente, as responsabilidades de cada classe. Para manter a alta coesão é importante escolher uma arquitetura adequada para o seu produto e fazer uso do boas práticas de software.
 
&emsp;&emsp;Em termos de design de objeto, coesão (ou mais especificamente, coesão funcional) é uma medida de quão fortemente relacionadas e focadas as responsabilidades de um elemento estão. Um elemento com responsabilidades altamente relacionadas que não faz uma grande quantidade de trabalho tem alta coesão. Esses elementos incluem classes, subsistemas e assim por diante (LARMAN, 2004).

&emsp;&emsp;O padrão de Alta Coesão para ser aplicado possui uma dependência direta com a aplicação do padrão de [Baixo acoplamento](#baixo-acoplamento). Visto que estamos utilizando a arquitetura MVC como padrão, garantimos a alta coesão e que cada classe possua seus métodos e procedimentos específicos, facilitando a compreensão, o reuso e a manutenção, caso necessário.

## Baixo Acoplamento

&emsp;&emsp;Um dos grandes problemas relacionado ao planejamento de um grande projeto está atrelado a seguinte pergunta, "Como criar uma aplicação com baixa dependência, baixo impacto de mudança e maior reutilização?", pensado nisso, a literatura aborta o tema sobre design patterns, mais exatamente sobre os padrões GRASP.

&emsp;&emsp;Antes de falamos de [baixo acoplamento](#baixo-acoplamento), primeiro vamos falar de acoplamento, é uma forma medir o quão um elemento está conectado a outro elemento, tem conhecimento de outros elementos, ou depende de outros elementos. Depois de conhecer  oque é acoplamento fica mais fácil descrever oque é um [baixo acoplamento](#baixo-acoplamento), é um elemento que não depende de muitos outros elementos, somente o necessário, esses elementos incluem classes, subsistemas, sistemas e assim por diante.

&emsp;&emsp;Para deixa o contexto mais rico iremos falar sobre alto acoplamento, no  caso seria um elemento que depende de muitos outros elementos, assim acarretando alguns problemas já conhecido pela literatura.
   
* Mudanças nos elementos forçadamente devido a mudanças nos elementos relacionados.
* Dificuldades em entender os elementos isoladamente.
* Dificuldades em reutilizar elementos, porque seu uso requer o uso adicional de outros elementos.

&emsp;&emsp;Para responder a pergunta feita no início desse tópico, achamos a seguinte resposta, "Tentar balancear a atribuição de responsabilidade e dependência entre os elementos, para que tenham um [baixo acoplamento](#baixo-acoplamento)".

&emsp;&emsp;Pensado nisso a maioria das nossas decisões para nossa aplicação, foram munidas com esses princípios dita pela literatura, assim conseguimos chegar em um objetivo limpo e claro, norteado pelo GRASP.


## Indireção


## Variações protegidas


## Polimorfismo



## Bibliografia

> - LARMAN, Craig. <b>Utilizando UML e Padrões</b>: Uma introdução à análise e ao projeto orientados a objetos e ao desenvolvimento iterativo. 3. ed. [S. l.: s. n.], 2004.


## Versionamento
| Versão | Data | Modificação | Autor |
|--|--|--|--|
|1.0|01/09/2021| Abertura do documento | Mateus O. Patrício |
|1.1|03/09/2021| Adicionando tópico Alta coesão | João Pedro e Francisco Ferreira |
|1.2|04/09/2021| Adicionando tópico de baixo acoplamento | Francisco Ferreira e João Pedro |