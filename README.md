# Gatos API
![Python](https://img.shields.io/badge/python-%233776AB.svg?style=for-the-badge&logo=python&logoColor=white)&nbsp;
![FastAPI](https://img.shields.io/badge/FastAPI-005571?style=for-the-badge&logo=fastapi)&nbsp;

## Sobre o projeto

Uma API que gerência e consome dados de gatos para facilitar a integração de diversas plataformas no lado do cliente.

## Objetivo

disponibilizar o serviço para aplicações front-ends consumirem rota de consulta de dados.

## Dependências

- Python 3.10 ou superior
- PIP (Preferred Installer Program)
- FastAPI

## Preparação de ambiente

Instale as dependências em [requirements](requirements.txt) com:

```sh
pip install -r requirements.txt
```

Rode o projeto com:

```sh
py run.py
```

## Dica

Para visualizar os endpoints acesse este link no seu navegador após rodar o projeto

```sh
localhost:8000/docs
```

## Rotas

### /cat_question/gato/{id}
GET: Retorna o objeto gato pelo id com data de nascimento

```sh
{
    "id": 0,
    "nome": "Qualquer",
    "raca": "Qualquer",
    "idade": 0,
    "data_nascimento": "0000-00-00"
}
```

### /cat_question/gato
GET: retorna uma lista de gatos sem data de nascimento e sem idade

```sh
[
    {
        "id": 0,
        "nome": "Qualquer",
        "raca": "Qualquer", 
    }
]
```

### /cat_question/gatos-mais-velhos
GET: retorna lista dos gatos mais velhos

```sh
[
    {
        "id": 0,
        "nome": "Qualquer",
        "raca": "Qualquer",
        "idade": 0,
        "data_nascimento": "0000-00-00"
    },
    {
        "id": 0,
        "nome": "Qualquer",
        "raca": "Qualquer",
        "idade": 0,
        "data_nascimento": "0000-00-00"
    }
]
```

### /cat_question/buscar-gato?termo_busca=texto_de_busca
GET: retorna lista dos gatos pelo termo de busca por nome

```sh
[
    {
        "id": 0,
        "nome": "Qualquer",
        "raca": "Qualquer",
        "idade": 0
    },
    {
        "id": 0,
        "nome": "Qualquer",
        "raca": "Qualquer",
        "idade": 0
    }
]
```

### /cat_question/buscar-raca?termo_busca=texto_de_busca
GET: retorna lista dos gatos pelo termo de busca por raca

```sh
[
    {
        "id": 0,
        "nome": "Qualquer",
        "raca": "Qualquer",
        "idade": 0
    },
    {
        "id": 0,
        "nome": "Qualquer",
        "raca": "Qualquer",
        "idade": 0
    }
]
```