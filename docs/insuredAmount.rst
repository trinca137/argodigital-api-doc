Consulta de Importância segurada
====================================

Serviço para obter as franquias de acordo com a configuração do formulário de risco.

As franquias, em cada produto E&O, variam de acordo com uma combinação de respostas à perguntas específicas do formulário de risco.
Por exemplo, em um determinado produto, as franquias são determinadas pela resposta à pergunta "atividade segurada"; em outros, elas podem ser determinadas por uma combinação das respostas dadas à "faturamento" e "atividade segurada".
Ainda, no caso de multiprofissionais, elas podem variar de acordo com a resposta dada à "atividade segurada" e uma determinada combinação de "categorias" que podem ser multiplamente selecionadas.

**Endpoint**

::

    POST {{URL_AMBIENTE}}/quotation/api/get-deductibles 

**Request** 

- `questionId` referentes à: 
   - `atividade segurada`: 3
   - `faturamento`: 5
   - `categorias` (multiprofissionais): 6

::

    {
        "questions": [
                {
                "questionId":"3",
                "answers":[3]
            }
        ],
        "operationCode":"PROTECTOR_DENTISTAS_PF"
    }

**Response** 

::

    [
        {
            "id":8,
            "text":"10% dos prejuízos com mínimo de R$ 500,00",
            "typeCode":null,
            "amount":10.0,
            "ratingTableCode":null,
            "ratingValueCode":null,
            "ratingTableId":4,
            "ratingValueId":1735,
            "questionId":3,
            "option":1,
            "answers":[3],
            "range":null,
            "questions":null,
            "priority":null,
            "order":null
        },
        {
            "id":7,
            "text":"10% dos prejuízos com mínimo de R$ 1.000,00",
            "typeCode":null,
            "amount":10.0,
            "ratingTableCode":null,
            "ratingValueCode":null,
            "ratingTableId":4,
            "ratingValueId":1088,
            "questionId":3,
            "option":2,
            "answers":[3],
            "range":null,
            "questions":null,
            "priority":null,
            "order":null
        },
        {
            "id":9,
            "text":"10% dos prejuízos com mínimo de R$ 3.500,00",
            "typeCode":null,
            "amount":10.0,
            "ratingTableCode":null,
            "ratingValueCode":null,
            "ratingTableId":4,
            "ratingValueId":1736,
            "questionId":3,
            "option":3,
            "answers":[3],
            "range":null,
            "questions":null,
            "priority":null,
            "order":null
        }
    ]