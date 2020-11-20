| Data       | Versão | Descrição            | Autor(es)       |
| ---------- | ------ | -------------------- | --------------- |
| 24/10/2020 | 1.0 | Criação de documento com gofs do backend | Lucas Ganda, João Lucas Zarbiélli e João de Assis |
| 25/10/2020 | 1.1| Adição de imagens | Lucas Ganda, João Lucas Zarbiélli e João de Assis |
| 26/10/2020 | 1.2 | Adição de GOFs Front-end | Wictor Girardi |
| 26/10/2020 | 1.3 | Reestruturação | João Lucas Zarbiélli |
| 26/10/2020 | 1.4 | Agrupando os GoFs por tipo e adicionando imagens | João Lucas Zarbielli| 
| 19/11/2020 | 1.5 | Colocando exemplo de código no código proxy | André Freitas|
| 20/11/2020 | 1.6 | Retirando GOF Factory e adicionando Singleton e Decorator ao backend | João de Assis|  

# GOFS

## 1. Definição
Os GoF's (Gang of Four) são padrões de design que visão prover soluções para problemas comum no desenvolvimento de software. No caso de programação orientada à objetos, os GoF's se propõem a solucionar problemas de interação e geração de objetos, que podem ser aplicados a contexto de problemas reais.São ferramentas poderosas no desenvolvimento de softwares.

Os Padrões de Design Criacionais (Creational Patterns) abstraem a instanciação de objetos. Eles ajudam a criar um sistema independente de como seus objetos são criados, compostos e representados.

## 2. Tipos de Gof
Os gofs utilizados para a elaboração deste projeto podem ser separados em 3 tipos: Criacionais e Estruturais.

### 2.1 Gofs Criacionais:
#### 2.1.1 Definição
Os padrões criacionais fornecem vários mecanismos de criação de objetos, que aumentam a flexibilidade e reutilização de código já existente.

#### 2.1.2 GOFS Criacionais: BackEnd

##### 2.1.2.1 Singleton
<img src='./images/singleton.png'>
O Singleton é um padrão de projeto criacional que permite a você garantir que uma classe tenha apenas uma instância, enquanto provê um ponto de acesso global para essa instância.

Para o projeto utilizamos somente uma instância que realiza a conexão com o banco de dados, para garantir que tenhamos apenas uma conexão com o banco evitando problemas de duplicação de escrita e acesso ao banco.

Além disso, utilizamos o singleton para verificar se um usuário possui um token de login válido

<img src='./images/screenshot singleton.png'>

#### 2.1.3 GOFS Criacionais: FrontEnd
##### 2.1.3.1 Factory Method
O Flutter possui uma arquitetura chamada BLoC (Business Logic Component), a qual tem a função de separar a lógica de negócio da UI através do uso de Streams. Em suma, stream é uma fonte de eventos assíncronos.

Em termos práticos, essa arquitetura BLoC pode ser comparada com o padrão de projeto ‘factory method’.

#### 2.1.3.2 Singleton
No Front-End, usamos a classe Api como um singleton para fazer toda a comunição do front com o gateway, além de utilizar o singleton para lidar com informações de autenticação e utilizar o singleton nativo do flutter.

### 2.2 GOFS Estruturais
#### 2.2.1 Definição
Os padrões estruturais explicam como montar objetos e classes em estruturas maiores mas ainda mantendo essas estruturas flexíveis e eficientes.

### 2.2.2 GOFS Estruturais: BackEnd
##### 2.2.2.1 Proxy
<img src='./images/proxy.png'>
O Proxy é um padrão de projeto estrutural que permite que você forneça um substituto ou um espaço reservado para outro objeto. Um proxy controla o acesso ao objeto original, permitindo que você faça algo ou antes ou depois do pedido chegar ao objeto original. O proxy pode passar o pedido para o objeto de serviço somente se as credenciais do cliente coincidem com certos critérios (Proxy de Proteção).

No backend foi utilizado a lógica de Proxy para limitar o acesso de algumas rotas estratégicas, onde o proxy verifica o nível de acesso do usuário atraves de JSON Web Token (JWT) e concede ou não o acesso a rota requisitada.

Pode-se ver que aqui a lógica proxy sendo utilizada no retorno do JWT no login, e o mesmo sendo necessário em requisições.
<img src='./images/proxylogin.png'>
<img src='./images/proxycodigo.png'>

##### 2.2.2.2 Decorator
<img src='./images/decorator.png'>
O Decorator é um padrão de projeto estrutural que permite que você acople novos comportamentos para objetos ao colocá-los dentro de invólucros de objetos que contém os comportamentos.

No backend utilizamos decorator para definir as entidades do banco de dados.

Todas as classes de entidade são originadas a partir de uma unica classe Entity, e através de decorators passamos as tabelas que serão geradas no banco
<img src='./images/screenshot decorator.png'>


### 2.3 GOFS Comportamentais
#### 2.3.1 Definição 
Estes padrões são voltados aos algoritmos e a designação de responsabilidades entre objetos.

### 2.2.2 GOFS Comportamentais: FrontEnd
#### 2.2.2.1 Memento
<img src='./memento.png'>
<br>
O Memento é um padrão de projeto comportamental que permite que você salve e restaure o estado anterior de um objeto sem revelar os detalhes de sua implementação. 

O Flutter usa o padrão memento na pilha de navegação.

#### 2.2.2.2 Chain of Responsibility
<img src='./chain.png'>
<br>
A intenção deste padrão é evitar o acoplamento do remetente de uma solicitação ao seu receptor, ao dar a mais de um objeto a oportunidade de tratar essa solicitação. Encadear os objetos receptores, passando a solicitação ao longo da cadeia até que um objeto a trate.

Nesse padrão cada objeto receptor possui uma lógica descrevendo os tipos de solicitação que é capaz de processar e como passar adiante aquelas que requeiram processamento por outros receptores. A delegação das solicitações pode formar uma árvore de recursão, com um mecanismo especial para inserção de novos receptores no final da cadeia existente.

Dessa forma, fornece um acoplamento mais fraco por evitar a associação explícita do remetente de uma solicitação ao seu receptor e dar a mais de um objeto a oportunidade de tratar a solicitação.

Um exemplo da aplicação desse padrão é o mecanismo de herança nas linguagens orientadas a objeto: um método chamado em um objeto é buscado na classe que implementa o objeto e, se não encontrado, na superclasse dessa classe, de maneira recursiva.

#### 2.2.2.3 State
<img src='./state.png'>
<br>
O State é um padrão de projeto comportamental que permite que um objeto altere seu comportamento quando seu estado interno muda. Parece como se o objeto mudasse de classe.


O Flutter por default vem com a arqitetura Lifting State Up (Vanilla), o qual é uma derivação do state. Todas as variáveis dentro da classe fazem parte do estado do widget. Nisso, quando alguma delas é alterada no setState(), toda a aplicação é renderizada.

#### 2.2.2.4 Strategy
<img src='./strategy.png'>
<br>
O Strategy é um padrão de projeto comportamental que permite que você defina uma família de algoritmos, coloque-os em classes separadas, e faça os objetos deles intercambiáveis.


A BaseScreen é o padrão que toda tela deve seguir, ela possui o contexto para o resto da página Widget body, e como toda tela no flutter herda de Widget existe a garantia de que esse contexto sempre existirá.


## 3. Referências 
Refactoring.guru. 2020. O Catálogo Dos Padrões De Projeto. [online] Disponível em : <https://refactoring.guru/pt-br/design-patterns/catalog> [Acessado 25 October 2020].
Padrões de Projetos em Dart<https://medium.com/flutterando/implementando-padr%C3%B5es-de-projetos-em-dart-parte-1-d604f6038460> [Acessado 25 October 2020].
025 – Padrão de Projeto STATE – Design Pattern do FLUTTER<http://davesbalthazar.com.br/025-padrao-de-projeto-state-design-pattern-do-flutter/> [Acessado 25 October 2020].