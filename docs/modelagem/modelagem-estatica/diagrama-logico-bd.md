# Diagrama lógico do banco de dados <br> <span class="rotulo-extra">Iniciativa Extra</span>
 
## Introdução
&emsp;&emsp; O modelo lógico é o resultado ou produto da conversão de um modelo conceitual para um determinado tipo de banco de dados, ou conforme Heuser, “Um modelo lógico é uma descrição de um banco de dados no nível de abstração visto pelo [usuário](/2021.1_G6_Curumim/base/requisitos/modelagem/lexicos/#lexico-usuario) do sistema gerenciador."
 
## Metodologia
&emsp;&emsp;Primeiramente foi realizada a revisão dos artefatos [MER](../modelagem-estatica/MER.md) e [DER](../modelagem-estatica/DER.md) que foram previamente desenvolvidos, pois estes documentos são utilizados como base para os demais processos de modelagem do banco de dados.
Depois de algumas discussões durante a construção do modelo lógico, foi observado que algumas questões nos artefatos da modelagem conceitual, poderiam ser adaptados durante essa etapa e com isso definir de maneira coerente a modelagem lógica.<br>
&emsp;&emsp;Foi utilizada a ferramenta [Br Modelo](http://www.sis4.com/brmodelo/) na versão desktop para a construção do diagrama.
 
## Diagrama Lógico
&emsp;&emsp;O diagrama lógico representa de forma gráfica a modelagem lógica do banco de dados, geralmente utilizando a notação UML. Este modelo possui um nível de abstração menor que o [DER](../modelagem-estatica/DER.md), já que o diagrama lógico define as relações e atributos das tabelas no banco de dados, adaptando-os especificamente para o banco de dados escolhido,  que no caso do projeto será um banco de dados [PostgreSQL](https://www.postgresql.org/).

### Versão 1.0
&emsp;&emsp;
![Diagrama lógico do Banco de Dados](../../assets/imagens/diagrama-logico-bd/diagrama-logico-bd-curumin-v1.png)
<center>[Figura 1: Diagrama lógico do Banco de Dados V1](../../assets/imagens/diagrama-logico-bd/diagrama-logico-bd-curumin-v1.png)</center>

### Versão 2.0
&emsp;&emsp;A seguir temos a segunda versão do diagrama lógico do banco de dados, com algumas mudanças após a modelagem física<br>
&emsp;&emsp;Nessa versão, o nome das tabelas foram alteradas para o plural, por questões de padronização, foram também simplificadas algumas tabelas, como por exemplo a tabela [Teacher](../../../base/requisitos/modelagem/lexicos/#lexico-professor), e a tabela [Adm](../../../base/requisitos/modelagem/lexicos/#lexico-administrador) que agora foram substituida por outra tabela Professional, que possui uma string indicando o tipo do profissional. Também foi simplificada as tabelas [Activity](../../../base/requisitos/modelagem/lexicos/#lexico-atividade) e [Event](../../../base/requisitos/modelagem/lexicos/#lexico-evento) para uma única tabela Projects, que indica também através de uma string que tipo de projeto se trata.

&emsp;&emsp;
![Diagrama lógico do Banco de Dados](../../assets/imagens/diagrama-logico-bd/diagrama-logico-bd-curumin-v2.png)
<center>[Figura 2: Diagrama lógico do Banco de Dados v2](../../assets/imagens/diagrama-logico-bd/diagrama-logico-bd-curumin-v2.png)</center>

 
#### **Legenda dos simbolos**:<br>
- Chave preta: Chave primária
- Chave verde: Chave estrangeira
 
#### **Observações**:<br>
- As tabelas [Adm](../../../base/requisitos/modelagem/lexicos/#lexico-administador), [Teacher](../../../base/requisitos/modelagem/lexicos/#lexico-professor) e [Guardian](../../../base/requisitos/modelagem/lexicos/#lexico-responsavel), cada uma possuem uma chave primária que também é uma chave estrangeira que faz referência a tabela [User](../../../base/requisitos/modelagem/lexicos/#lexico-usuario), que será a tabela que possui de fato as informações pessoais de cada tipo de [usuário](../../../base/requisitos/modelagem/lexicos/#lexico-usuario), e um identificar de qual tipo é aquele [usuário](../../../base/requisitos/modelagem/lexicos/#lexico-usuario).
- O [Board](../../../base/requisitos/modelagem/lexicos/#lexico-mural) que antes estava presente no [MER](../modelagem-estatica/MER.md) e [DER](../modelagem-estatica/DER.md), pela sua cardinalidade em relação a tabela [Child](../../../base/requisitos/modelagem/lexicos/#lexico-crianca) seria adequado que fosse incorporada a tabela [Child](../../../base/requisitos/modelagem/lexicos/#lexico-crianca), porém depois de alguns debates e análises, foi evidenciado que os atributos presentes na tabela [Board](../../../base/requisitos/modelagem/lexicos/#lexico-mural) não teriam utilidade no desenvolvimento, e deixaria a tabela [Child](../../../base/requisitos/modelagem/lexicos/#lexico-crianca) com muita informação desnecessariamente, por isso o [Board](../../../base/requisitos/modelagem/lexicos/#lexico-mural) acabou ficando de fora da modelagem final.
 
 
## Bibliografia
> - Vídeo aula : Modelagem de dados - modelo conceitual, lógico e físico. Disponível em: <https://www.youtube.com/watch?v=8CkMX2qXgdY>. Acesso em: 25 ago, 2021;
> - HEUSER, Carlos Alberto. Projeto de Banco de Dados, Porto Alegre: Instituto de informática da UFRGS, Sagra Luzzato, 2001 Série livros didáticos n.º 4. Acesso em: 30 ago, de 2021;
> - brModelo: FERRAMENTA DE MODELAGEM CONCEITUAL DE BANCO DE DADOS. Disponível em:
<http://www.fernandozaidan.com.br/ined/bd/outros/brModelo.pdf>. Acesso em: 30 ago, 2021;
 
 
## Versionamento
| Versão | Data | Modificação | Autor |
| :-: | -- | -- | -- |
| 0.1 | 25/08/2021 | Discussão sobre o [MER](../modelagem-estatica/MER.md) e [DER](../modelagem-estatica/DER.md) | Edson Soares e Eliseu Kadesh |
| 0.2 | 27/08/2021 | Desenvolvimento do diagrama lógico   | Edson Soares e Eliseu Kadesh |
| 0.3 | 27/08/2021 | Discussão para reajustar a modelagem | Edson Soares, Eliseu Kadesh, Daniel Porto |
| 1.0 | 30/08/2021 | Abertura do documento          | Edson Soares, Eliseu Kadesh |
| 1.1 | 30/08/2021 | Adição de link para o léxicos  | Eliseu Kadesh |
| 1.2 | 30/08/2021 | Revisão por pares              | Gabriel Bonifácio, Francisco Ferreira |
| 1.3 | 30/08/2021 | Alterações no diagrama e novas observações | Eliseu Kadesh |
| 2.0 | 19/09/2021 | Adição da segunda versão do diagrama | Eliseu Kadesh |
| 2.1 | 19/09/2021 | Revisão por pares | Daniel Porto, Edson Soares |