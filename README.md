# Events

Este é um projeto de demonstração para um sistema de gerenciamento de eventos utilizando Spring Boot. O objetivo deste projeto é permitir a criação, visualização e inscrição em eventos. Este projeto foi desenvolvido durante a NLW Connect da Rocketseat.

## Tecnologias Utilizadas

- **Java 21**: Linguagem de programação utilizada.
- **Spring Boot 3.4.2**: Framework para desenvolvimento de aplicações Java.
- **Spring Data JPA**: Para interação com o banco de dados.
- **MySQL**: Sistema de gerenciamento de banco de dados utilizado.
- **Maven**: Gerenciador de dependências e construção do projeto.

## Funcionalidades

- **Gerenciamento de Eventos**: Criação e listagem de eventos.
- **Inscrições**: Usuários podem se inscrever em eventos e visualizar rankings de inscrições.
- **API REST**: O projeto expõe uma API REST para interação com as funcionalidades.

## Estrutura do Projeto

### Estrutura do Projeto

- `src/`
	: Diretório principal do projeto.
- `main/`
	: Contém o código-fonte principal do aplicativo.
- `java/`
	: Diretório que armazena o código Java.
- `br/com/nlw/events/`
	: Pacote principal do projeto.
- `controller/`
	: Controladores que gerenciam as requisições HTTP e a lógica de negócios.
- `dto/`
	: Objetos de Transferência de Dados utilizados para comunicação entre camadas.
- `exception/`
	: Classes de exceção personalizadas para tratamento de erros.
- `model/`
	: Modelos que representam as entidades do sistema.
- `repo/`
	: Repositórios que gerenciam a persistência de dados.
- `service/`
	: Serviços que contêm a lógica de negócios do aplicativo.
- `resources/`
	: Contém arquivos de configuração, como `application.properties`.
- `test/`
	: Contém testes automatizados do aplicativo.


## Como Executar o Projeto

1. **Clone o repositório**:
   ```bash
   git clone https://github.com/HermannDouglas/events
   cd events
   ```

2. **Configure o banco de dados**:
   - Crie um banco de dados MySQL chamado `db_events`.
   - Atualize as credenciais no arquivo `src/main/resources/application.properties`.

3. **Execute o projeto**:
   ```bash
   ./mvn spring-boot:run
   ```

## Endpoints da API

- `POST /events`: Cria um novo evento.
- `GET /events`: Retorna todos os eventos.
- `GET /events/{prettyName}`: Retorna um evento específico pelo nome amigável.
- `POST /subscription/{prettyName}`: Inscreve um usuário em um evento.
- `GET /subscription/{prettyName}/ranking`: Retorna o ranking de inscrições para um evento.

