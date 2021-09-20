# Padrões Emergentes

## Introdução

## Padrão Midleware



## Padrão MVC

### O que é MVC?

&emsp;&emsp;O mvc é um dos padroẽs arquiteturais mais famosos no mundo de desenvolvimento web, visto pela sua simplicidade organizacional, assim trazendo mais eficiência e otimização no tempo de velocidade feita em requisições pelo usuário. Com quase 5 décadas de formulação a arquitetura mvc é é basicamente dividida em 3 camadas, Model, View e Controller.

 * Model: Essa camada também é conhecida como business object model, ela é a principal responsável pela leitura e escrita de dados e principalmente pela validações. 

 * View: Essa camada que mais próxima do usuário, é a camada que ele se interage e recebe informações de forma visual.

 * Controller: A controller é responsável por fazer o intermédio das requisições da view com as respostas da model.

 ![MVC](../assets/imagens/padroes-emergentes/mvc.png)
<center>
[Figura 1 : MVC](../assets/imagens/padroes-emergentes/mvc.png)
</center>

### Aplicação do MVC no Curumim

&emsp;&emsp;Para o projeto Curumim foi adaptado o padrão MVC, essa decisão foi tomada por se tratar de um padrão de API REST, pesando nisso o grupo optou por separar a camada de view dentre a outras, assim a View é determinada pelo no client que faz essa renderização para o usuário da aplicação.


<center>

 ![MC](../assets/imagens/padroes-emergentes/mc.png)

[Figura 2: Organização das pastas da API](../assets/imagens/padroes-emergentes/mc.png)
</center>

<center>

 ![MODEL](../assets/imagens/padroes-emergentes/model.png)

[Figura 3: Exemplo da model User](../assets/imagens/padroes-emergentes/model.png)
</center>

<center>

 ![Authentication Controller](../assets/imagens/padroes-emergentes/controller.png)
<center>
[Figura 4: Exemplo da controller](../assets/imagens/padroes-emergentes/controller.png)
</center>



## Bibliografia

> - Zucher, Vitor. O que é padrão MVC? Entenda arquitetura de softwares!.Publicado em 17/07/2020. Disponível em: https://www.lewagon.com/pt-BR/blog/o-que-e-padrao-mvc. Acessado em 19/09/2021.

> - Ramos, Allan. O que é MVC?. Publicado em 26/02/2015. https://tableless.com.br/mvc-afinal-e-o-que/. Acessado em 19/09/2021.

> - Grupo Unigrade. Padrões Emergentes: API. Matéria de Arquitetura e Desenho de Software, 2019. Disponível em: https://ads-unigrade-2019-1.github.io/Wiki/dinamica05B/api/. Acesso em: 20/09/2021.


## Versionamento

| Versão | Data | Modificação | Autor |
|--|--|--|--|
|1.0|20/09/2021| Abertura do documento | Francisco |
