# GRASP - Padrões de Software para Atribuição de Responsabilidade Geral

&emsp;&emsp;Padrões GRASP são uma ajuda na hora de entender como desenhar um software orientado a objetos de maneira metódica, racional e explicável (LARMAN, 2004). Têm o intuito de tornar o código mais flexível, facilitando a manutenção e a extensibilidade.

## Criador

&emsp;&emsp;A instanciação de objetos é uma atividade comum em todo sistema orientado a objetos. Entender qual classe deve ser responsável por instanciar objetos e reduzir a complexidade desnecessária do sistema.

&emsp;&emsp;Segundo Larman (2004), uma classe B deve ser responsável por criar instâncias de classe A se uma, ou quanto mais melhor, das seguintes afirmações se aplicarem:

- Instâncias de B contêm ou agregam instâncias de A;
- Instâncias de B gravam instâncias de A;
- Instâncias de B utilizam instâncias de A;
- Instâncias de B têm os dados necessários para iniciação das instâncias de A.

## Especialista
&emsp;&emsp;
Antes de definir exatamente o que é o "Especialista", é importante entender que o [criador](#criador), por exemplo, é um especialista, mas com um olhar focado em criação de instâncias. 

&emsp;&emsp;Por um outro lado, o padrão de projeto Especialista se preocupa em atribuir responsabilidades para alguma entidade mais especialista, seja mais especialista em instâncias ou não. O importante é que seja em um aspecto do sistema que há alguma entidade a fazer melhor aquilo, como por exemplo, em cadastrar uma [criança](../../base/requisitos/modelagem/lexicos/#lexico-crianca), [lançar uma presença](../../base/requisitos/modelagem/lexicos/#lexico-lancar-presenca), entre outros.

&emsp;&emsp;Alguns problemas foram identificados: falta de um princípio geral para atribuir responsabilidades a objetos e a necessidade de fazer escolhas sobre a atribuição de responsabilidades a entidades. Diante dessas dificuldades, veio a solução: iniciar declarando claramente a responsabilidade e atribuir uma responsabilidade de informação a uma entidade.

&emsp;&emsp;Um malefício claro desse padrão é quando a solução sugerida pelo especialista não é desejável, o que pode acontecer em algumas situações, mas os benefícios são inquestionáveis: [baixo acoplamento](#baixo-acoplamento), o encapsulamento da informação é mantido e a definição de entidades mais fáceis de entender e manter é encorajada.

## Controlador

&emsp;&emsp;O controlador funciona quase que como um mediador entre a interface de [usuário](../../base/requisitos/modelagem/lexicos/#lexico-usuario) e o sistema desenvolvido. Ele tem a responsabilidade de coordenar todas as operações solicitadas pelo usuário e verificar quem são os responsáveis por tais tarefas. No controlador, não há regras de negócio, sendo sua única tarefa, portanto, delegar e distribuir as atividades do sistema.

&emsp;&emsp;No nosso [diagrama de classes](../../modelagem/modelagem-estatica/diagrama-de-classes) podemos observar, que haverão alguns controladores dentro da aplicação. Como exemplo, temos:

- **UserController:**

![User Controller](../assets/imagens/GRASPs/user_controller.png)
<center>[Figura 1: Classe User Controller](../assets/imagens/GRASPs/user_controller.png)</center>

&emsp;&emsp;A classe **UserController** basicamente lida com tudo que pode envolver os [usuários](../../base/requisitos/modelagem/lexicos/#lexico-usuario) e distribui suas atividades para os devidos responsáveis.

## Invenção pura
&emsp;&emsp;O conceito de invenção pura aborda a utilização de soluções que não necessariamente se encaixam em algum padrão de projeto.
Com o objetivo de fortalecer a [alta coesão](#alta-coesao) e o [baixo acoplamento](#baixo-acoplamento), basicamente esse padrão consiste em atribuir um conjunto bem definido de responsabilidades para classes artificiais que não se encontram fundamentalmente no domínio do escopo do projeto.

&emsp;&emsp;Com base no [diagrama de classes](../../modelagem/modelagem-estatica/diagrama-de-classes) desenvolvido, esse padrão foi aplicado ao modelar as seguintes classes:

- **Authentication Controller:**

&emsp;&emsp;A classe **authController** foi modelada para conter a responsabilidade de aplicar todas as regras de autenticação do sistema. Basicamente todas as requisições do [usuário](../../base/requisitos/modelagem/lexicos/#lexico-usuario) serão direcionadas às rotas, as quais inicialmente invocarão os métodos da **authController**, para, somente se autorizado pelos mesmos, continuar para a aplicação das regras de negócio inicialmente requisitadas e, finalmente, retornar uma resposta para a camada de view.

![Authentication Controller](../assets/imagens/GRASPs/invencao_auth.png)
<center>[Figura 2: Classe authController](../assets/imagens/GRASPs/invencao_auth.png)</center>

- **Board:**

&emsp;&emsp;A classe [**Board**](../../base/requisitos/modelagem/lexicos/#lexico-mural) surgiu na necessidade de atribuir a responsabilidade de agrupar [atividades](../../base/requisitos/modelagem/lexicos/#lexico-atividade), [anotações](../../base/requisitos/modelagem/lexicos/#lexico-anotacao) e [eventos](../../base/requisitos/modelagem/lexicos/#lexico-evento) para a visualização por parte dos [responsáveis](../../base/requisitos/modelagem/lexicos/#lexico-responsavel). Essa classe tem sua validação na aplicação de regras específicas, como, por exemplo, a visualização de dados contidos nessas classes, em uma única tela, com a possibilidades de filtrar em um tipo de classe específica.

&emsp;&emsp;Tais funcionalidades estão especificadas na [US06](../../product-backlog/#US06) e podem ser melhor visualizadas no [protótipo de alta fidelidade](../../base/design-sprint/prototipo-alta/#prototipo-produzido).

![Board](../assets/imagens/GRASPs/invencao_board.png)
<center>[Figura 3: Classe Board](../assets/imagens/GRASPs/invencao_board.png)</center>

## Alta Coesão

&emsp;&emsp;No projeto de software, uma qualidade básica conhecida como coesão mede informalmente como funcionalidades relacionam as operações de um elemento de software e também mede quanto trabalho um elemento de software está realizando (LARMAN, 2004). A alta coesão é garantida quando atribui-se, de forma coerente, as responsabilidades de cada classe. Para manter a alta coesão é importante escolher uma arquitetura adequada para o seu produto e fazer uso de boas práticas de software.
 
&emsp;&emsp;Em termos de design de objeto, coesão (ou mais especificamente, coesão funcional) é uma medida de quão fortemente relacionadas e focadas as responsabilidades de um elemento estão. Um elemento com responsabilidades altamente relacionadas que não faz uma grande quantidade de trabalho tem alta coesão. Esses elementos incluem classes, subsistemas e assim por diante (LARMAN, 2004).

&emsp;&emsp;O padrão de Alta Coesão para ser aplicado possui uma dependência direta com a aplicação do padrão de [Baixo acoplamento](#baixo-acoplamento). Visto que estamos utilizando a arquitetura MVC como padrão, garantimos a alta coesão e que cada classe possua seus métodos e procedimentos específicos, facilitando a compreensão, o reuso e a manutenção, caso necessário.

## Baixo Acoplamento

&emsp;&emsp;Um dos grandes problemas relacionado ao planejamento de um grande projeto está atrelado a seguinte pergunta, "Como criar uma aplicação com baixa dependência, baixo impacto de mudança e maior reutilização?", pensado nisso, a literatura aborda o tema sobre design patterns, mais exatamente sobre os padrões GRASP.

&emsp;&emsp;Antes de falarmos de [baixo acoplamento](#baixo-acoplamento), primeiro vamos falar de acoplamento, é uma forma de medir o quão um elemento está conectado a outro elemento, tem conhecimento de outros elementos, ou depende de outros elementos. Depois de conhecer o que é acoplamento, fica mais fácil descrever o que é um [baixo acoplamento](#baixo-acoplamento). É um elemento que não depende de muitos outros elementos, somente o necessário, esses elementos incluem classes, subsistemas, sistemas e assim por diante.

&emsp;&emsp;Para deixar o contexto mais rico, iremos falar sobre alto acoplamento. No caso, seria um elemento que depende de muitos outros elementos, assim acarretando alguns problemas já conhecidos pela literatura.
   
* Mudanças nos elementos forçadamente devido a mudanças nos elementos relacionados.
* Dificuldades em entender os elementos isoladamente.
* Dificuldades em reutilizar elementos, porque seu uso requer o uso adicional de outros elementos.

&emsp;&emsp;Para responder a pergunta feita no início desse tópico, achamos a seguinte resposta, "Tentar balancear a atribuição de responsabilidade e dependência entre os elementos, para que tenham um [baixo acoplamento](#baixo-acoplamento)".

&emsp;&emsp;Pensando nisso, a maioria das nossas decisões para nossa aplicação, foram munidas com esses princípios ditos pela literatura, assim conseguimos chegar em um objetivo limpo e claro, norteado pelo GRASP.


## Indireção

&emsp;&emsp;Esse padrão se configura por atribuir responsabilidades de mediador a classes intermediárias entre outros componentes, objetos ou serviços com objetivo, também, de contribuir com a [alta coesão](#alta-coesao) e o [baixo acoplamento](#baixo-acoplamento).

&emsp;&emsp;**Camada Controller:** A indireção pode ser observada ao longo de todo o projeto simplesmente pela utilização da arquitetura **MVC**, visto que as classes contidas na camada de **controller** servem como mediadoras entre as camadas **view** e **model**. As classes controllers estão contidas nesse diretório.

&emsp;&emsp;**Middlewares:** Além disso, o nosso projeto utilizará middlewares que são classes utilizadas internamente na api, pelos controllers na execução das regras de negócio, de forma a desacoplar métodos e rotinas estratégicas. Os middlewares do projeto estão contidos nesse diretório.

## Variações protegidas
&emsp;&emsp;O padrão Variações protegidas se caracteriza por tentar manter possível o isolamento de componentes, sem fazer comunicações desnecessárias, buscando eliminar impactos indesejáveis de elementos em outros elementos. Portanto, aqui nós buscamos identificar pontos de variação ou instabilidade previsíveis e atribuir responsabilidades para criar uma interface estável em torno deles.

## Polimorfismo

&emsp;&emsp;Antes de definir o conceito de polimorfismo adotado pelos GRAPS é importante primeiro definir o conceito de polimorfismo. Ele se apresenta como um princípio pelo o qual as subclasses de uma superclasse conseguem chamar métodos, que apesar de apresentarem a mesma assinatura, se comportam de maneira diferente para cada classe derivada.

&emsp;&emsp;Suponha que em determinada classe são utilizadas estruturas condicionais para determinar o comportamento em função do tipo de classe, esse tipo de método pode gerar diversos problemas para a manutenção do código, sendo assim o Polimorfismo proposto pelos GRAPS sugere que a seleção do comportamento seja dado utilizando o polimorfismo, ou seja, a superclasse cria o método e as subclasses realizam a implementação do polimorfismo.

&emsp;&emsp;Como exemplo de polimorfismo adotado no projeto, temos a classe "UserController" com o método polimórfico "register".
<center>
	![polimorfismo](../assets/imagens/GRASPs/polimorfismo.png)<br>
	[Figura 4: Polimorfismo](../assets/imagens/GRASPs/polimorfismo.png)
</center>


## Bibliografia

> - [Documento GRAPS do projeto QRodízio](https://unbarqdsw.github.io/2020.1_G10_QRodizio/design_patterns/grasps/grasps.html#grasps);
> - [Documento GRAPS do projeto Stock](https://unbarqdsw.github.io/2020.1_G12_Stock/#/Project/Estudos/GRASP);
> - LARMAN, Craig. <b>Utilizando UML e Padrões</b>: Uma introdução à análise e ao projeto orientados a objetos e ao desenvolvimento iterativo. 3. ed. [S. l.: s. n.], 2004.
> - MEDIUM. Padrões GRASP — Padrões de Atribuir Responsabilidades. Disponível em: <https://medium.com/@leandrovboas/padr%C3%B5es-grasp-padr%C3%B5es-de-atribuir-responsabilidades-1ae4351eb204>. Acesso em: 02 de set. 2021.
> - DEVMEDIA. Desenvolvimento com qualidade com GRASP. <https://www.devmedia.com.br/desenvolvimento-com-qualidade-com-grasp/28704>. Acesso em: 02 de set. 2021.
> - Padrões GRASP, UFU (Universidade Federal de Uberlândia). Disponível em http://www.facom.ufu.br/~bacala/ESOF/05a-Padr%C3%B5es%20GRASP.pdf. Acesso em: 03 set. 2021.
> - [Documento GRAPS do projeto Stock](https://unbarqdsw.github.io/2020.1_G12_Stock/#/Project/Estudos/GRASP);
> - Videoaulas e materiais complementares presentes no moodle da disciplina Arquitetura e Desenho de Software. Disponível em <https://aprender3.unb.br/course/view.php?id=8603>. Acesso em: 27 jul. 2021.
> - Canal Vertice digital. Analise e Orientação a Objetos - Princípios do GRASP - Indirection ou Indireção. YouTube. Disponível em <https://www.youtube.com/watch?v=zPlAYo2E92o>. Acesso em: 02 set. 2021.
> - Canal Vertice digital. Analise e Orientação a Objetos - Princípios do GRASP - Pure Fabrication ou Invenção Pura. Disponível em <https://www.youtube.com/watch?v=4CteZ9144bw>. Acesso em: 02 set. 2021.
> - Canal Vertice digital. Analise e Orientação a Objetos - Princípios do GRASP - Controller ou Controlador. Disponível em <https://www.youtube.com/watch?v=CbB5Oy8eBzc>. Acesso em: 04 set. 2021.
> - Canal Vertice digital. Analise e Orientação a Objetos - Princípios do GRASP - Protected Variations ou Variações Protegidas. Disponível em <https://www.youtube.com/watch?v=AClwrkpYEG0>. Acesso em: 04 set. 2021.

## Versionamento
| Versão | Data | Modificação | Autor |
|--|--|--|--|
|1.0|01/09/2021| Abertura do documento | Mateus O. Patrício |
|1.1|01/09/2021| Adição da introdução e criador | Mateus O. Patrício |
|1.2|02/09/2021| Adição da invenção pura e indireção | Bruno Felix e Daniel Porto |
|1.3|02/09/2021| Adição do polimorfismo | Nilo Mendonça |
|1.4|03/09/2021| Adição do especialista | Gabriel Bonifácio |
|1.5|03/09/2021| Adicionando tópico Alta coesão | João Pedro e Francisco Ferreira |
|1.6|04/09/2021| Adicionando tópico de baixo acoplamento | Francisco Ferreira e João Pedro |
|1.7|04/09/2021| Adição da controlador e variações protegidas | Enzo Gabriel e Edson Araújo |
|1.8|11/09/2021| Correções no texto, versionamento e adição de "linkagem" de tópicos | Eliseu Kadesh
|1.9|14/10/2021| Padronização e correção ortográfica do documento | Bruno Felix e Nilo Mendonça |

