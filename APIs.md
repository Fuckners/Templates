# Nome da Api 

## Descrição
Descrição da sua API. "API RESTful para gestão de dados..."

## EndPoints

<!-- Método | rota -->
- ### POST /auth    
Descrição da rota    

#### Parâmetros    
parâmetro: descrição do parametro

<!-- exemplo de body de requisição -->
```json
{
    "perametro1": "exemploDadoParametro01",
    "parametro2": "exemploDadoParametro02"
}
```    

#### Respostas

<!-- vale lembrar que a parte de"_links" só é necessária caso você tenha implementado HATEOAS na sua API -->

<!-- status | descrição -->

##### 200 - OK!
```json
{
    "resposta": "conteudoDaResposta",
    "_links": [
        {
            "href": "http://localhost:8080/...",
            "method": "método",
            "ref": "nome_de_referencia"
        },
        {
            "href": "http://localhost:8080/...",
            "method": "metódo",
            "ref": "nome_de_referencia"
        }
    ]
}
```

##### 400 - Bad Request.
```json
{
    "err": "mensagem do erro 1."
}
```
```json
{
    "err": "mensagem do erro 2."
}
```

##### 401 - Unauthorized.
```json
{
    "err": "mensagem do erro."
}
```

##### 404 - Not Found.
```json
{
    "err": "mensagem do erro."
}
```

##### 500 - Internal Server Error.
```json
{
    "err": "mensagem do erro."
}
```

***

<!-- Método | rota -->
- ### GET /dados    
Descrição da rota 

#### Parâmetros    
Nenhum

#### Respostas
##### 200 - OK
```json
{
    "dados": [
        {
            "nomeDados01": "respostaDados01",
            "nomeDados01": "respostaDados02",
            "_links": [
                {
                    "href": "http://localhost:8080/...",
                    "method": "GET",
                    "ref": "nome_referência"
                },
                {
                    "href": "http://localhost:8080/...",
                    "method": "POST",
                    "ref": "nome_referência"
                },
                {
                    "href": "http://localhost:8080/...",
                    "method": "DELETE",
                    "ref": "nome_referência"
                }
            ]
        },
        {
            "nomeDados01": "respostaDados01",
            "nomeDados01": "respostaDados02",
            "_links": [
                {
                    "href": "http://localhost:8080/...",
                    "method": "GET",
                    "ref": "nome_referência"
                },
                {
                    "href": "http://localhost:8080/...",
                    "method": "POST",
                    "ref": "nome_referência"
                },
                {
                    "href": "http://localhost:8080/...",
                    "method": "DELETE",
                    "ref": "nome_referência"
                }
            ]
        },
        {
            "nomeDados01": "respostaDados01",
            "nomeDados01": "respostaDados02",
            "_links": [
                {
                    "href": "http://localhost:8080/...",
                    "method": "GET",
                    "ref": "nome_referência"
                },
                {
                    "href": "http://localhost:8080/...",
                    "method": "POST",
                    "ref": "nome_referência"
                },
                {
                    "href": "http://localhost:8080/...",
                    "method": "DELETE",
                    "ref": "nome_referência"
                }
            ]
        }
    ],
    "_links": [
        {
            "href": "http://localhost:8080/game",
            "method": "POST",
            "ref": "create_game"
        }
    ]
}
```

##### 404 - Not Found.
```json
{
    "err": "mensagem do erro."
}
```

***
<!-- Método | rota -->
- ### DELETE /dado/:id
Descrição da rota

#### Parametros
:id - id do dado que deseja deletar.    

##### Exemplos
`/dado/4`    
`/dado/25`

#### Respostas

##### 200 OK!
```json
{
    "_links": [
        {
            "href": "http://localhost:8080/...",
            "method": "GET",
            "ref": "nome_de_referencia"
        },
        {
            "href": "http://localhost:8080/...",
            "method": "POST",
            "ref": "nome_de_referencia"
        }
    ]
}
```

##### 400 Bad Request.
```json
{
    "err": "ID inválido."
}
```

##### 500 Internal Server Error.
```json
{
    "err": "mensagem de erro."
}
```

***

- ### PUT /dado/:id
Descrição da rota

#### Parametros
:id - id do dado que deseja editar.

parametro1: descrição parametro 1    
parametro2: descrição parametro 2    
parametro3: descrição parametro 3    
...

##### Exemplos
`/dado/4`    
`/dado/25`

#### Respostas

##### 200 OK!
```json
{
    "_links": [
        {
            "href": "http://localhost:8080/...",
            "method": "GET",
            "ref": "nome_de_referencia"
        },
        {
            "href": "http://localhost:8080/.../...",
            "method": "GET",
            "ref": "nome_de_referencia"
        },
        {
            "href": "http://localhost:8080/...",
            "method": "POST",
            "ref": "nome_de_referencia"
        }
    ]
}
```

##### 400 Bad Request.
```json
{
    "err": "mensagem do erro."
}
```
```json
{
    "err": "mensagem do erro."
}
```
```json
{
    "err": "mensagem do erro."
}
```

##### 404 Not Found.
```json
{
    "err": "mensagem do erro."
}
```

##### 500 Internal Server Erro.
```json
{
    "err": "mensagem do erro."
}
```
