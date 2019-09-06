# Instruções

1. Implemente o escopo abaixo conforme os requisitos;
2. Se não conseguir atender a todo o escopo mas quiser participar do processo mesmo assim, siga os próximos passos;
3. Crie um repositório privado aqui no GitHub com seu teste;
4. Dê acesso ao usuário `PauloDanielCarneiro`;
5. No repositório, crie um arquivo nomeado README.md com seu nome, e-mail e telefone para contato.

# Escopo

Precisamos que você construa uma API RESTful que permita a manipulação dos locais que possuem nossas estações, bem como suas respectivas estações.

Cada local pode possuir N estações, e uma estação só pode ser alocada em um local por vez. No caso da estação, o número de série é a chave primária da mesma no banco de dados.

Você deverá implementar os seguintes endpoints:

## Criação de local:

Endpoint: `POST /premises`

Corpo da requisição:

```json
{
  "name": "Meu edifício",
  "address": "R Iramaia, 36, Jardim Europa, São Paulo, SP"
}
```

Corpo da resposta:
```json
{
  "id": 123,
  "name": "Meu edifício",
  "address": "R Iramaia, 36, Jardim Europa, São Paulo, SP"
}
```

## Listagem de locais

Endpoint: `GET /premises`

Corpo da resposta:

```json
{
  "entries": [
    {
      "id": 123,
      "name": "Meu edifício",
      "address": "R Iramaia, 36, Jardim Europa, São Paulo, SP"
    },
    {
      "id": 321,
      "name": "Meu outro edifício",
      "address": "Rua José Mancini, Jardim Paulista, São Carlos, SP"
    }
  ]
}
```

## Criação de uma estação

Endpoint: `POST /v1/stations`

Corpo da requisição:

```json
{
  "serial": "12345",
  "premise_id": 123,
  "name": "Nome da máquina"
}
```

Corpo da resposta:

```json
{
  "serial": "12345",
  "premise_id": 123,
  "name": "Nome da máquina"
}
```

## Listagem de estações por locais

Endpoint: `GET /premises/:premise_id/stations`

Corpo da resposta:

```json
{
  "entries": [
    {
      "serial": "12345",
      "premise_id": 123,
      "name": "Nome da máquina"
    },
    {
      "serial": "54321",
      "premise_id": 123,
      "name": "Nome da outra máquina"
    }
  ]
}
```

# Requisitos

* A escolha do banco de dados é livre, use o que achar melhor;
* Caso saiba programar em Elixir, utilize o framework [Phoenix](https://phoenixframework.org);
* Caso não conheça Elixir, utilize Ruby com um dos microframeworks abaixo:
  * [Flask](http://flask.pocoo.org/)
  * [Sinatra](http://sinatrarb.com/)
  * [Grape](https://github.com/ruby-grape/grape)
  * [Spark](http://sparkjava.com/)
  * [Slim](https://www.slimframework.com/)
* Coloque a aplicação em um docker e, no readme, coloque as instruções para conseguir utilizar a aplicação
* Faça testes automatizados para tudo que for implementado;
* Utilize git-flow

# Diferenciais
* Quando usar bancos de dados relacionais, faça [migrations](https://medium.com/@juniorb2s/migrations-o-porque-e-como-usar-12d98c6d9269).
* Utilize boas práticas da linguagem escolhida. (Dica: Utilize softwares como rubocop em uma IDE ou editor de texto. Apesar de precisarem de um certo tempo para configurar eles fazem isso automaticamente por você)
