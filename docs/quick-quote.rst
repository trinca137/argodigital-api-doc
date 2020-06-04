Simulação
==================


Realizar simulação - Depósito Recursal
^^^^^^^^^^^^^^

**Endpoint**

::

    POST {{URL_AMBIENTE}}/quotation/api/quotation/quick-quote

Serviço utilizado para solicitar simulação de Depósito Recursal

Headers da Requisição
""""""""""""""""""

``Content-Type`` application/json;v=2.0

``Ocp-Apim-Subscription-Key`` {{Chave}}

``Authorization`` Bearer {{Token}}

.. Note:: Para obter a {{Chave}}, consulte a página de :doc:`/configuration`. Para obter o {{Token}}, consulte a página de :doc:`/security`

Body da Requisição
""""""""""""""""""

``IdOperation`` Identificador da operação utilizada.

``RiskAnalysis`` 
    Seção referente as perguntas e respostas do respectivo formulário de risco

    ``questionId`` Id da questão
    ``answer`` Resposta da questão
    
``TakerData``
    Seção referente aos dados do tomador
    
    ``Cnpj`` CNPJ do tomador

``PolicyData``
    Seção referente a dados da apólice

    ``ContractName`` Nº do Processo
    ``Claimant`` Tribunal/Vara

**Exemplo Depósito Recursal**

::

    {
        "IdOperation": "50",
        "RiskAnalysis": 
        [
            {
                "questionId": "1",
                "answer": "123.45"
            },
            {
                "questionId": "2",
                "answer": "1"
            },
            {
                "questionId": "3",
                "answer": "5"
            },
            {
                "questionId": "4",
                "answer": "2020-04-23T03:00:00.000Z"
            },
            {
                "questionId": "5",
                "answer": "1"
            }
        ],
        "PolicyData": 
        {
            "ContractName": "123456789",
            "Claimant": "Teste Tribunal"
        },
        "TakerData": 
        {
            "Cnpj": "30291355000148"
        }
    }
  