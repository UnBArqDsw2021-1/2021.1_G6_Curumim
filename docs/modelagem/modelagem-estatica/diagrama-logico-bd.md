# Diagrama lógico do banco de dados <br> <span class="rotulo-extra">Iniciativa Extra</span>

## Introdução
&emsp;&emsp; O modelo lógico é o resultado ou produto da conversão de um modelo conceitual para um determinado tipo de banco de dados, ou conforme Heuser, “Um modelo lógico é uma descrição de um banco de dados no nível de abstração visto pelo usuário do sistema gerenciador.

## Metodologia
&emsp;&emsp;Primeiramente foi realizada a revisão dos artefatos [MER](../modelagem-estatica/MER.md) e [DER](../modelagem-estatica/DER.md) que foram previamente desenvolvidos, pois estes documentos são utilizados como base para os demais processos de modelagem do banco de dados.
Depois de algumas discussões durante a construção do modelo lógico, foi observado que algumas questões nos artefatos da modelagem conceitual, poderiam ser adaptados durante essa etapa e com isso definir de maneira coerente a modelagem lógica.<br>
&emsp;&emsp;Foi utilizada a ferramenta [Br Modelo](http://www.sis4.com/brmodelo/) na versão desktop para a construção do diagrama.

## Diagrama Lógico
&emsp;&emsp;O diagrama lógico representa de forma gráfica a modelagem lógica do banco de dados, geralmente utilizando a notação UML. Este modelo possui um nível de abstração menor que o [DER](../modelagem-estatica/DER.md), já que o diagrama lógico define as relações e atributos das tabelas no banco de dados, adaptando-os especificamente para o banco de dados escolhido,  que no caso do projeto será um banco de dados PostgreSQL.

&emsp;&emsp;
![foto](../../../assets/imagens/diagrama-logico-bd/diagrama-logico-bd-curumim.png)
<center>[Figura 1: Diagrama Lógico](../../../assets/imagens/diagrama-logico-bd/diagrama-logico-bd-curumim.png)</center>

## Bibliografia
> - []();
> - []();

## Versionamento
| Versão | Data | Modificação | Autor |
| :-: | -- | -- | -- |
| 0.1 | 25/08/2021 | Discussão sobre o [MER](../modelagem-estatica/MER.md) e [DER](../modelagem-estatica/DER.md) | Edson Soares e Eliseu Kadesh |
| 0.2 | 27/08/2021 | Desenvolvimento do diagrama lógico | Edson Soares e Eliseu Kadesh |
| 0.3 | 27/08/2021 | Discussão para reajustar a modelagem | Edson Soares, Eliseu Kadesh, Daniel Porto |
| 1.0 | 30/08/2021 | Abertura do documento | Edson Soares, Eliseu Kadesh |