# Diagrama de Classes
 
## Introdução
 
&emsp;&emsp;O Diagrama de Classes é utilizado para representar e descrever a estrutura estática de classes do sistema, definindo os atributos, métodos e relacionamentos entre as classes. Além disso, fornece uma visão geral do comportamento estático do sistema, e pode ser utilizado como base para outros diagramas UML.

## Metodologia

&emsp;&emsp;O desenvolvimento do diagrama de classes levou em consideração as decisões de técnologias e estruturas que serão utilizadas no projeto. Sendo assim, o diagrama de classes aborda a representação das classes que serão desenvolvidas na API do projeto, a qual contará com arquitetura MVC.<br>
&emsp;&emsp;Portanto, foi focada a representação das entidades que compõem as camadas de modelos e controllers.<br>
&emsp;&emsp;É importante mencionar que os nomes das classes, de seus atributos e métodos foram representados em Inglês e no estilo CamelCase para que, desde já, seja feita uma padronização no que se refere ao que será implementado em código.

![Diagrama de classes](../../assets/imagens/diagrama-de-classes/Diagrama-de-classes.png)
 
<center>[Figura 1: Diagrama de classes](../../assets/imagens/diagrama-de-classes/Diagrama-de-classes.png)</center>
 
#### **Observações**:<br>
- Todos os atributos privados possuem métodos Getters e Setters, e não foram incluídos no diagrama para facilitar a visualização.
- A maioria dos métodos das classes controllers tem relação de dependencia com a classe AuthController, tais relações não foram incluídas no diagrama para facilitar a visualização.
 
## Bibliografia
> - UML Package Diagrams Overview. Disponível em: https://www.uml-diagrams.org/package-diagrams-overview.html. Acesso em: 13/08/2021.
> - Videoaulas e materiais complementares presentes no moodle da disciplina Arquitetura e Desenho de Software. Disponível em <https://aprender3.unb.br/course/view.php?id=8603>. Acesso em: 14 ago. 2021.

## Versionamento
| Versão | Data | Modificação | Autor |
| :-: | -- | -- | -- |
|0.1| 13/08/2021 | Criação do Diagrama de classes              |  Daniel Porto, Eliseu Kadesh  |
|1.0| 20/08/2021 | Abertura do Documento                       |  Eliseu Kadesh |
|1.1| 20/08/2021 | Adição da metodologia                       |  Daniel Porto  |
|2.0| 21/08/2021 | Correções no Diagrama de Classes            |  Eliseu Kadesh |
