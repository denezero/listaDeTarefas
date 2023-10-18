# Aplicação de Lista de tarefas

Esta é uma aplicação Spring Boot que permite o cadastramento de tarefas.

## Requisitos

- Java 17 ou superior
- Maven
- Banco de dados

## Configuração

1. Clone o repositório:

   ```shell
   git clone https://github.com/denezero/listaDeTarefas
   ```

2. Configure o banco de dados editando o arquivo application.properties e fornecendo as configurações necessárias:

    ```properties
    spring.datasource.url=jdbc:h2:mem:todolist
    spring.datasource.username=admin
    spring.datasource.password=admin
    ```

3. Construa a aplicação:

    ```shell
    mvn clean install
    ```

4. Inicie a aplicação
    ```shell
        mvn spring-boot:run
    ```

A aplicação agora deve estar em execução em http://localhost:8080.


##  Modelo de Inserção em API

O modelo de inserção de usuário deve ser conforme abaixo:

```json
{
    "name": "Jose de Souza",
    "username": "jose",
    "password": "1234567890",
}
```
O modelo de inserção de uma tarefa deve ser conforme abaixo:
```json
{
    "description": "Limpar completamente o quarto e as gavetas",
    "title": "Limpar quarto",
    "priority": "ALTA",
    "startAt": "2023-10-04T10:30:00",
    "endAt": "2023-10-04T12:00:00",
    "idUser": "do1j2j12-3123xokd-0g93g349g-12d12r403"
}
```

### Notas

_startAt && endAt_ devem ser no formato  *yyyy-mm-ddTHH:mm:ss*
_idUser_ É fornecido pelo H2 no momento do post

