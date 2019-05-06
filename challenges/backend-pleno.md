# Instruções

* Implemente o escopo abaixo, conforme os requisitos;
* Se não conseguir atender todo escopo mas quiser participar do processo mesmo assim, siga os próximos passos;
* Crie um repositório privado aqui no GitHub com seu teste;
* Dê acesso ao usuário `thiagohdeplima`;
* No repositório, crie um arquivo nomeado README.md contendo:
  * Uma breve descrição do projeto e como executá-lo;
  * Uma explicação do porque escolheu as ferramentas utilizadas;
  * Seu nome, e-mail e telefone para contato.

# Escopo

Crie o projeto e implementação sistemas que serão responsáveis por gerenciar:

* Empréstimos feitos através das nossas estações;
* As cobranças geradas em razão destes empréstimos.

As cobranças são realizadas de forma assíncrona, independente da resposta da API para o usuário. Um empréstimo pode possuir diversas cobranças.

_Uma vez que este teste não implementa uma aplicação de verdade, podemos considerar como cobrança a mera inserção de um registro de cobrança no banco de dados, relacionando-a com o empréstimo_.

# Requisitos

* Escolha livremente a `stack` desta implementação;
* Justifique suas escolhas no arquivo `README.md`;
* Implemente o sistema com os requisitos acima;
* Crie testes automatizados para sua aplicação.

# Diferenciais

Iremos considerar como diferenciadas aplicações que implementem, além do escopo especificado acima, os seguintes recursos:

* Criação de um container de Docker para a aplicação;
* Criação de um aquivo `docker-compose.yml` para toda stack da aplicação;
* Implemente o escopo usando a arquitetura de microsserviços;
* Comuniquem os microsserviços por meio de brokers como [RabbitMQ](https://www.rabbitmq.com/) ou mesmo [Redis](https://redis.io/topics/pubsub).
