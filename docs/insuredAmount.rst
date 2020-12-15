Consulta de Importância segurada
====================================

Serviço para obter as importâncias seguradas de acordo com a configuração do formulário de risco.

As importâncias seguradas geralmente não possuem restrições salvo no produto "Multiprofissionais PF". 

**Endpoint**

::

    POST {{URL_AMBIENTE}}/operation/api/operations/get-insured-amount 

(1) Para os casos gerais, o request deverá ser realizado conforme o exemplo abaixo:

**Request** 

::

    {
        "OperationCode": "CODIGO_DO_PRODUTO", 
        "RatingTableId": 3,
        "Questions": []
    }


Produto (Código do produto)
    - Médicos PF (MDS_MEDICOS_PF)
    - Dentistas PF (PARTNER_DENTISTAS_PF)

(2) Para o caso de Multiprofissionais PF (PARTNER_MULTIPROFFISIONAIS_PF), as importâncias seguradas aplicáveis dependem da resposta dada à pergunta "Em qual categoria abaixo você se encaixa?" - id: 3 -  do formulário de risco. Segue abaixo a configuração desta pergunta:

::

    {
        "id": 3,
        "text": "Em qual categoria abaixo você se encaixa?",
        "answers": [{
                "id": 1,
                "text": "Audio, Vídeo e Fotografia"
            }, {
                "id": 2,
                "text": "Publicidade e Marketing"
            }, {
                "id": 3,
                "text": "Turismo"
            }, {
                "id": 4,
                "text": "Produção de Eventos e Entretenimento"
            }, {
                "id": 5,
                "text": "Consultoria em RH e Head Hunter",
            }, {
                "id": 6,
                "text": "Instituições e Profissionais de Ensino",
            }, {
                "id": 7,
                "text": "Notários Públicos e Registradores",
            }, {
                "id": 8,
                "text": "Jardinagem e Design de Interiores",
            }, {
                "id": 9,
                "text": "Salões de Beleza",
            }, {
                "id": 10,
                "text": "Empresas e Profissionais de Tecnologia",
            }, {
                "id": 11,
                "text": "Síndicos e Administradores de Condomínios"
            }
        ]
    }

Portanto, para obter as importâncias seguradas para "Salões de Beleza", por exemplo, o objeto "Questions" deve ser composto da seguinte forma:

::

    "Questions": [
        {
            "id": 3,
            "answers": [9]
        }
    ]

Para "Empresas e Profissionais de Tecnologia"

::

    "Questions": [
        {
            "id": 3,
            "answers": [10]
        }
    ]

e assim por diante. A requisição completa nestes casos têm o seguinte modelo:

::

    {
        "OperationCode": "PARTNER_MULTIPROFFISIONAIS_PF", 
        "RatingTableId": 3,
        "Questions": [
            {
                "id": 3,
                "answers": [10]
            }
        ]
    }

**Response** 

O endpoint deverá retornar uma lista de todas as importâncias seguradas aplicáveis ao cenário condizente com o request, seguindo o formato abaixo:

::

    [
        {
            "id": 1,
            "code": null,
            "text": "R$ 50.000,00",
            "documentText": null,
            "tooltip": null,
            "ratingValueId": "1399",
            "ratingValueCode": null,
            "answerConditions": [],
            "order": null
        }
    ]