| Data       | Versão | Descrição            | Participantes                                                     |
| ---------- | ------ | -------------------- | ----------------------------------------------------------------- |
| 01/09/2020 | 1.0    | Criação do documento | João de Assis, Lucas Ganda, João Lucas Zarbiélli e Wictor Girardi |

# Contribuindo com o projeto

Coisas nas quais você pode ajudar:

- [Documentação](#documentação)
- [Criação de novas features](#criação-de-novas-features)
- [Issues](#issues)
- [Bugs](#bugs)
  - [Sugestões de melhoria](#sugestões-de-melhoria)

## Fluxo de trabalho

Todos os contribuidores do projeto devem seguir os seguintes passos:

1.  Puxe uma _branch_ com base na _branch_ _development_
2.  Nomeie a _branch_ conforme as [políticas de branches](#politicas-de-branches)
3.  Trabalhe nas suas mudanças nesta branch
4.  Crie um pull request para o repositório
5.  A integração contínua irá verificar as suas alterações
6.  Um mantenedor do projeto irá avaliar e realizar o merge da sua contribuição

## Desenvolvendo

1. Clone o repositório

```bash
git clone https://github.com/UnBArqDsw/2020.1_G8_CUPONZIM.git
```

2. Abra o projeto [2020.1-Cuponzim](https://github.com/UnBArqDsw/2020.1_G8_CUPONZIM.git) no editor de texto de sua preferência
3. Faça as suas contribuições

## Politicas de Branches

As _branches_ devem ser nomeadas conforme o que será desenvolvido:

- Para novas **_features_**, a _branch_ deverá ser nomeada seguindo o seguinte padrão:

```
feature/usx
```

em que 'X' é a US da _issue_.

- Para **correção de _bugs_**, a _branch_ deverá ser nomeada seguindo o seguinte padrão:

```
bug/id
```

em que 'id' é o número que identifica a _issue_ no GitHub.

- Para **pequenas correções**, a _branch_ deverá ser nomeada seguindo o seguinte padrão:

```
hotfix/id
```

em que 'id' é o número que identifica a _issue_ no GitHub.

- Para **envio de documentação**, a _branch_ deverá ser nomeada seguindo o seguinte padrão:

```
docs/nome
```

em que 'nome' é o nome do artefato.

## Políticas de _Commits_

Os _commits_ devem ser atômicos e a mensagem do _commit_ deve ser clara e objetiva e no idioma português.

## Documentação

Mais documentação é algo que você pode contribuir de forma simples:

1. Clone o repositório

```bash
git clone https://github.com/UnBArqDsw/2020.1_G8_CUPONZIM.git
```

2. Acesse a pasta docs

```bash
cd 2020.1-Cuponzim
```

3. Edite ou crie novas documentações e salve-as na pasta correspondente

## Criação de novas features

Para a criação de novas features, siga os seguintes passos:

1. Crie uma issue com o template de _feature_
2. Insira _labels_ que estejam relacionados com a _issue_ criada
3. Aguarde o feedback de algum mantenedor que irá validar a _feature_ sugerida
4. Caso o _feedback_ for positivo, dê _assign_ da _issue_ para você mesmo
5. Inicie o desenvolvimento
6. No pull request, faça o _link_ do _pull request_ com a _issue_ criada previamente
7. Aguarde a resposta do _pull request_

## Issues

Você pode contribuir criando novas _issues_ ou corrigindo _issues_ existentes

#### _Bugs_

Caso encontre algum bug no projeto, sinta-se à vontade para criar uma _issue_ nos reportando:

1. Crie a _issue_ seguindo o template de **Reportar _Bugs_**
2. Insira _labels_ que estejam relacionados com a _issue_ criada
3. Aguarde _feedback_ de um mantenedor

#### Sugestões de melhoria

Caso tenha alguma sugestão de melhoria ou _feature_ siga os seguintes passos:

1. Crie a _issue_ seguindo um dos templates disponíveis no campo de criação da _issue_
2. Insira _labels_ que estejam relacionados com a _issue_ criada
3. Aguarde _feedback_ de um mantenedor
4. Caso queira contribuir com a implementação, verifique os passos para a [criação de novas features](#criacao-de-novas-features)

## Atribuição

Este documento é uma adaptação do artefato do projeto [opsdroid](https://github.com/opsdroid/opsdroid), acessado em 07 de setembro de 2020.
