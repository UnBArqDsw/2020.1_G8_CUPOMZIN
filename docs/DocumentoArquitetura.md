# Documento de Arquitetura de Software


# Histórico de versão

| Data       | Versão | Descrição                                          | Participantes                                                                   |
| ---------- | ------ | -------------------------------------------------- | ------------------------------------------------------------------------------- |
| 27/09/2020 | 1.0    | Criação do documento | João de Assis|
| 26/10/2020 | 1.1    | Adicionando TypeOrm as tecnologias utilizadas | João de Assis|
| 16/11/2020 | 1.2    | Adicionando diagramas e atualizando tecnologias | Lucas Ganda | 
<br/>

## 1. Introdução
Este documento visa especificar de forma básica alguns tópicos referentes ao Documento de Arquitetura que será desenvolvido no decorrer da disciplina.

## 2. Tecnologias utilizadas
### 2.1. Front End
* ### 2.1.1. Flutter
    Flutter é o kit de ferramentas de interface do usuário do Google para criar aplicativos belos e compilados nativamente para dispositivos móveis, Web e desktop a partir de uma única base de código. É um framework que possui como linguagem base o Dart

* ### 2.1.2. React.js
    O React é uma biblioteca JavaScript de código aberto com foco em criar interfaces de usuário em páginas web. É mantido pelo Facebook, Instagram, outras empresas e uma comunidade de desenvolvedores individuais.

### 2.2. Back End
* ### 2.2.1. Express
    O Express é um framework para aplicações web em Node.js. Pequeno e flexível, fornecendo um conjunto robusto de recursos para aplicativos web e mobile.

* ### 2.2.2 TypeORM
    O TypeORM é um módulo avançado de gerenciamento de relações de objeto que é executado no Node. js. Como o nome indica, o TypeORM deve ser usado com o TypeScript.

### 2.3. Banco de Dados
* ### 2.3.1. PostgreSQL
    PostgreSQL é um poderoso sistema de banco de dados relacional de objetos de código aberto, com mais de 30 anos de desenvolvimento ativo, que ganhou uma forte reputação de confiabilidade, robustez de recursos e desempenho.

## 3. Abordagem Arquitetural
* ### Microsserviços
    Microsserviços são um tipo de arquitetura de software que consiste em construir aplicações desmembrando-as em serviços independentes. Estes serviços se comunicam entre si usando APIs e promovem grande agilidade em times de desenvolvimento.

No produto cuponzim:

* Fale conosco:  bloco responsável pela comunicação de usuários com os desenvolvedores do cuponzim

* Loja: bloco responsável por guardar e administrar as informações sobre as lojas, bem como seu login e cadastron

* Promoções: serviço responsável por administrar os lançamentos de promoções

* Cupom: serviço responsável pela validação, resgate e exclusão de cupons

* Cliente: bloco responsável por guardar e administrar as informações sobre os clientes, bem como seu login e cadastro

* Comunicação entre os serviços

    Comunicação entre os serviços será feita por meio de uma API Gateway, a qual será responsável por fazer o intermédio entre os microsserviços por meio de métodos do protocolo HTTP.

Para maiores informações, recomenda-se a leitura do [Diagrama de Contexto](DiagramadeContexto.md)
## 4. Restrições e metas arquiteturais

|     Metas      |                                                                            |
| :------------: | :------------------------------------------------------------------------: |
| Escalabilidade |                       A aplicação deve ser escalável                       |
|   Segurança    | A aplicação deve tratar de forma de segura os dados sensíveis dos usuários |
|     Deploy     |                A aplicação deve possuir deploy automatizado                |


|  Restrições   |                                                                |
| :-----------: | :------------------------------------------------------------: |
| Conectividade |   É necessária a conexão com internet para utilização do App   |
|  Plataforma   |         A aplicação terá suporte para Android e iOS         |
|    Público    |  A aplicação será desenvolvida voltada ao público brasileiro   |
|   Linguagem   |      A aplicação será desenvolvida em português do Brasil      |
|    Equipe     |             A equipe possui 5 integrantes              |
|     Prazo     | O escopo proposto deve ser terminado até o final da disciplina |

## 5. Referências

Para melhor entendimento do documento recomenda-se a leitura dos seguintes diagramas elaborados:

* [Diagrama de Contexto](DiagramadeContexto.md)
* [Diagrama de Casos de Uso](DiagramaCasosDeUso.md)


Referências utilizadas:
- DONG, Tao. **Flutter**. [S. l.], 2019. Disponível em: https://medium.com/flutter. Acesso em: 27 set. 2020.
- MALLAWAARACHCHI, Vijini. **10 Common Software Architectural Patterns in a nutshell**. [S. l.], 2017. Disponível em: https://towardsdatascience.com/10-common-software-architectural-patterns-in-a-nutshell-a0b47a1e9013. Acesso em: 27 set. 2020.
- **NODE.JS**. In: WIKIPÉDIA, a enciclopédia livre. Flórida: Wikimedia Foundation, 2019. Disponível em: <https://pt.wikipedia.org/w/index.php?title=Node.js&oldid=55592828>. Acesso em: 27 set. 2020.
- PANT, Prabhu. **A complete guide to PostgreSQL**. [S. l.], 2018. Disponível em: https://medium.com/@heyPrabhu/a-complete-guide-to-postgresql-e4d1cefb9866. Acesso em: 27 set. 2020.
- RICHARDSON, Chris. **Pattern**: Decompose by subdomain. [S. l.]. Disponível em: https://microservices.io/patterns/decomposition/decompose-by-subdomain.html. Acesso em: 27 set. 2020.
- RICHARDSON, Chris. **What are microservices?**. [S. l.]. Disponível em: https://microservices.io/index.html. Acesso em: 27 set. 2020.
- WAYNER, Peter. **The top 5 software architecture patterns**: how to make the right choice. [S. l.]. Disponível em: https://techbeacon.com/app-dev-testing/top-5-software-architecture-patterns-how-make-right-choice. Acesso em: 27 set. 2020.
