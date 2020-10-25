| Data       | Versão | Descrição            | Autor(es)       |
| ---------- | ------ | -------------------- | --------------- |
| 24/10/2020 | 0.1 | Criação de documento com gofs do backend | Lucas Ganda, João Lucas Zarbiélli e João de Assis |
| 25/10/2020 | 0.2| Adição de imagens | Lucas Ganda, João Lucas Zarbiélli e João de Assis |

# GOFS

## 1. Definição
Padrões de projeto são soluções típicas para problemas comuns em projeto de software. Eles são como plantas de obra pré fabricadas que você pode customizar para resolver um problema de projeto recorrente em seu código.

Durante a elaboração do projeto Cuponzim, foram definidos os seguintes GOFS

## 2. Tipos de Gof
Os gofs utilizados para a elaboração deste projeto podem ser separados em 3 tipos: Criacionais e Estruturais.
### 2.1 Gofs Criacionais:
#### 2.1.1 Definição
Os padrões criacionais fornecem vários mecanismos de criação de objetos, que aumentam a flexibilidade e reutilização de código já existente.

#### 2.1.2 GOFS Criacionais: BackEnd
##### 2.1.2.1 Factory Method
<img src='./images/factory.png'>
O Factory Method é um padrão criacional de projeto que fornece uma interface para criar objetos em uma superclasse, mas permite que as subclasses alterem o tipo de objetos que serão criados.

No backend foi utilizado o factory method durante a definição de entidades no banco de dados.

##### 2.1.2.2 Singleton
<img src='./images/singleton.png'>
O Singleton é um padrão de projeto criacional que permite a você garantir que uma classe tenha apenas uma instância, enquanto provê um ponto de acesso global para essa instância.

Para o projeto utilizamos somente uma instância que realiza a conexão com o banco de dados, para garantir que tenhamos apenas uma conexão com o banco evitando problemas de duplicação de escrita e acesso ao banco.


### 2.2 GOFS Estruturais
#### 2.2.1 Definição
Os padrões estruturais explicam como montar objetos e classes em estruturas maiores mas ainda mantendo essas estruturas flexíveis e eficientes.
#### 2.2.2 GOFS Estruturais: BackEnd
##### 2.2.2.1 Proxy
<img src='./images/proxy.png'>
O Proxy é um padrão de projeto estrutural que permite que você forneça um substituto ou um espaço reservado para outro objeto. Um proxy controla o acesso ao objeto original, permitindo que você faça algo ou antes ou depois do pedido chegar ao objeto original. O proxy pode passar o pedido para o objeto de serviço somente se as credenciais do cliente coincidem com certos critérios (Proxy de Proteção).

No backend foi utilizado a lógica de Proxy para limitar o acesso de algumas rotas estratégicas, onde o proxy verifica o nível de acesso do usuário atraves de JSON Web Token (JWT) e concede ou não o acesso a rota requisitada.


## 3. Referências 
Refactoring.guru. 2020. O Catálogo Dos Padrões De Projeto. [online] Disponível em : <https://refactoring.guru/pt-br/design-patterns/catalog> [Acessado 25 October 2020].