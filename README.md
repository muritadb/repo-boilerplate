<h1 align="center">
  [NOME DO PROJETO]
</h1>


este repo, descricao aqui que faz parte [desse desafio]( LINK ) resto da descricao.

O projeto foi elaborado, exemplo para o repo [ - nesse vídeo -]().

## Tecnologias
 
- lista de tecnologias usadas no projeto

## Práticas adotadas

- exemplos de praticas
- SOLID, Testes automatizados, Uso de DTOs para a API, SASS etc

## Como Executar

### Localmente
- Clonar repositório git
- Construir o projeto:
```
instrucoes de como rodar o projeto
```
- Executar:
```
instrucoes de como executar o projeto
```

Exemplo: A API poderá ser acessada em [localhost:8080](http://localhost:8080).
O Swagger poderá ser visualizado em [localhost:8080/swagger-ui.html](http://localhost:8080/swagger-ui.html)

### Usando Docker

exemplo com docker para java

- Clonar repositório git
- Construir o projeto:
```
./mvnw clean package
```
- Construir a imagem:
```
./mvnw spring-boot:build-image
```
- Executar o container:
```
docker run --name place-service -p 8080:8080  -d place-service:0.0.1-SNAPSHOT
```

A API poderá ser acessada em [localhost:8080](http://localhost:8080).
O Swagger poderá ser visualizado em [localhost:8080/swagger-ui.html](http://localhost:8080/swagger-ui.html)

## API Endpoints

exemplo como documentar uma API

Para fazer as requisições HTTP abaixo, foi utilizada a ferramenta [httpie](https://httpie.io):

- POST /places
```
http POST :8080/places name="Place" state="State"

HTTP/1.1 200 OK
Content-Length: 129
Content-Type: application/json

{
    "createdAt": "2023-04-20T19:00:07.241632",
    "name": "Place",
    "slug": "place",
    "state": "State",
    "updatedAt": "2023-04-20T19:00:07.241632"
}
```

- GET /places/{id}
```
http :8080/places/1
HTTP/1.1 200 OK
Content-Length: 129
Content-Type: application/json

{
    "createdAt": "2023-06-07T14:45:39.693689",
    "name": "Place",
    "slug": "place",
    "state": "State",
    "updatedAt": "2023-06-07T14:45:39.693689"
} 
```

- GET /places?name=?
```
http :8080/places name==PLACE
HTTP/1.1 200 OK
Content-Type: application/json
transfer-encoding: chunked

[
    {
        "createdAt": "2023-06-07T14:45:39.693689",
        "name": "Place",
        "slug": "place",
        "state": "State",
        "updatedAt": "2023-06-07T14:45:39.693689"
    }
]
```

- PATCH /places/{id}
```
http PATCH :8080/places/1 name='New Name' state='New State'
HTTP/1.1 200 OK
Content-Length: 142
Content-Type: application/json

{
    "createdAt": "2023-06-07T14:45:39.693689",
    "name": "New Name",
    "slug": "new-name",
    "state": "New State",
    "updatedAt": "2023-06-07T14:53:21.671129345"
}
```