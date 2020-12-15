Consulta de franquias
=======================

Obs.: antes de consultar as franquias é necessário `Obter as configurações do formulário de risco`_

Serviço para obter as franquias de acordo com a configuração do formulário de risco.

As franquias, em cada produto E&O, variam de acordo com uma combinação de respostas à perguntas específicas do formulário de risco.
Por exemplo, em um determinado produto, as franquias são determinadas pela resposta à pergunta "atividade segurada"; em outros, elas podem ser determinadas por 
uma combinação das respostas dadas à "faturamento" e "atividade segurada".
Ainda, elas podem variar de acordo com a resposta dada à "atividade segurada" e uma determinada combinação de "categorias".

Há duas maneiras de identificar a correlação entre uma determinada franquia e um par pergunta-resposta do Formulário de risco:

Tomemos de exemplo, a seguinte lista de franquias

::

    "deductibles": [
        {
            "id": 1,
            "text": "8% dos prejuízos com mínimo de R$ 500,00",
            "amount": 8.0,
            "questionId": 28,
            "option": 1,
            "answers": [
                17
            ],
            "range": null,
            "questions": null
        },
        {
            "id": 2,
            "text": "10% dos prejuízos com mínimo de R$ 2.500,00",
            "amount": 10.0,
            "questionId": null,
            "option": 1,
            "answers": null,
            "range": null,
            "questions": [
                {
                    "questionId": 3,
                    "answers": [
                        4
                    ]
                },
                {
                    "questionId": 5,
                    "answers": [
                        4,
                        5,
                        6,
                        7,
                        8
                    ]
                }
            ]
        },
    ]

(1)  Caso a franquia dependa somente de uma pergunta, então deve-se olhar para os campos "questionId" e "answers".  No nosso exemplo acima, olhemos para a 
primeira franquia - de id: 1 - o campo "questionId" têm o valor 28 ao passo que o campo "answers" têm o valor [17], isto significa que, esta franquia - id: 1 - 
é aplicável à cotação, caso a pergunta 28 do formulário de risco seja respondida com o valor 17. 

(2) Caso a franquia dependa de mais de uma pergunta, então deve-se olhar para o campo "questions". De nosso exemplo, analisemos a segunda franquia - de id: 2 - em que 
o campo "questions" está preenchidda seguinte maneira: 

::

    {
        "questions": [{
            "questionId": 3,
            "answers": [4]
        }, 
        {
            "questionId": 5,
            "answers": [ 4, 5, 6, 7, 8]
        }]
    }


a interpretação do par pergunta-resposta que compõe o campo "questions" se dá como em (1), porém para a franquia ser aplicável é necessário avaliar a conjunção dos 
objetos que compõe o valor do campo. 
Na lista de franquias acima temos dois objetos: (a) o primeiro com "questionId": 3 e "answers": [4] e (b) o segundo com "questionId": 5 e "answers": [4,5,6,7,8], 
isto significa que, para a franquia - id: 2 - ser aplicável, a pergunta "3" do formulário de risco deve estar preenchida com o valor "4" e, ao mesmo tempo, 
a pergunta "5" deve estar preenchida com qualquer um dos valores configurados (4, 5, 6, 7 ou 8).

Dado isso, temos o necessário para a utilização do endpoint para obtenção de franquias.

**Endpoint**

::

    POST {{URL_AMBIENTE}}/operation/api/operations/get-deductibles 

**Request** 

No corpo da requisição, deve-se mandar o código da operação do produto sendo cotado e uma lista com pares pergunta-resposta de acordo com o  
preenchimento do formulário de risco envolvido em uma cotação específica. Só pares pergunta-resposta relevantes em relação às configurações - explicadas acima - 
deverão ser enviados. 

Suponhamos o seguinte cenário: 
(1) queremos fazer uma cotação do produto "dentistas PF";
(2) as franquias de dentista sejam condicionadas à pergunta "3" do formulário de risco.

Então, o objeto a ser enviado na requisição se parecerá com o seguinte: 

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

O exemplo acima significa que, estamos solicitando quais são as franquias aplicáveis ao produto "PROTECTOR_DENTISTAS_PF", em que a pergunta "3" do formulário
de risco está sendo respondida com a resposta "3".

**Response** 

A resposta do endpoint retornará todas as franquias aplicáveis ao produto nas condições especificadas no request.

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

Obter as configurações do formulário de risco 
===================================================

As configurações do formulário de risco podem ser obtidas através da seguinte URL:
::

    GET {{URL_AMBIENTE}}/quotation/api/operations/{{CODIGO_DO_PRODUTO}}

Produto (Código do produto)
    - Médicos PF (MDS_MEDICOS_PF)
    - Dentistas PF (PARTNER_DENTISTAS_PF)
    - Multiprofissionais PF (PARTNER_MULTIPROFFISIONAIS_PF)

As configurações de franquia são encontradas dentro da propriedade `deductibles` ao passo que as configurações do formulário de risco se encontram na propriedade `riskAnalysisForm`

Exemplo de retorno: 

::

    {
        riskAnalysisForm": {
            "questions": [
                {
                    "id": 1,
                    "code": "NOVO_SEGURADO",
                    "questionId": 1,
                    "text": "Você é um novo segurado ou renovação de outra companhia?",
                    "required": true,
                    "type": "RadioButton",
                    "defaultAnswer": "1",
                    "preAnswered": null,
                    "parentId": null,
                    "parentAnswerId": null,
                    "answers": [
                        {
                            "id": 1,
                            "text": "Novo"
                        },
                        {
                            "id": 2,
                            "text": "Renovação"
                        }
                    ],
                    "questions": null
                }
            (...)]
        },
        "deductibles": [
        {
            "id": 17,
            "text": "8% dos prejuízos com mínimo de R$ 500,00",
            "amount": 8.0,
            "questionId": 28,
            "option": 1,
            "answers": [
                17
            ],
            "range": null,
            "questions": null
        }
        (...)]
    }