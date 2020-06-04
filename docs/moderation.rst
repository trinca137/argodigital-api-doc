Fluxo Moderação
===========

As cotações podem estar sujeitas a moderação, no fluxo de Produtos E&O (Médicos PF e PJ) para os casos de PEP e em todas as contratações de Bikes com ou sem PEP.


Consulta Status
^^^^^^^^^^^^^^

**Endpoint**

::

    GET {{URL_AMBIENTE}}/moderation/api/moderation/GetByQuotation?quotationIdentifier={Identificador da Cotação}


**Response**

::

    {
        "id": 415,
        "moderationProtocol": "202012300000000415",
        "status": 1,
        "createdAt": "2020-01-23T20:47:20.1962811",
        "moderationType": 2,
        "pepData": {
            "pep": true,
            "iDontWantToFillInTheInformation": false,
            "estimatedPatrimony": "Sem Renda",
            "finantialSituation": "Sem Patrimonio",
            "profession": "DEVELOPER"
        },
        "reasonsOfDisapproval": null
    }


Criar Moderação PEP
^^^^^^^^^^^^^^
Serviço para solicitar caso necessário uma moderação PEP.

``quotationIdentifier`` Identificador da cotação não qual deseja gerar uma moderação PEP

``ModerationType`` No caso de PEP deve ser sempre preenchido com: 2

``pepData`` 
    Seção referente as informações de PEP.

    ``PEP`` true ou false

    ``IDontWantToFillInTheInformation`` Caso queira informar os campos de PEP: ``true``, caso contrário: ``false`` 

    ``EstimatedPatrimony`` Patrimônio estimado

    ``FinantialSituation`` Situação financeira

    ``Profession`` Profissão

**Endpoint**

::

    POST {{URL_AMBIENTE}}/moderation/api/moderation/CreatePep


**Body**

::

    {  
        "Quotation":{
            "Identifier":"d815bf9d-b8bb-4dd6-af90-d3061a7eefb4"
        },
        "ModerationType":2,
        "PEPData": {  
            "PEP": true,
            "IDontWantToFillInTheInformation":false,
            "EstimatedPatrimony":"Sem Renda",
            "FinantialSituation":"Sem Patrimonio",
            "Profession":"DEVELOPER"
        }
    }

**Response**

::

    {
        "id": 415,
        "moderationProtocol": "202012300000000415",
        "status": 1,
        "createdAt": "2020-01-23T20:47:20.1962811+00:00",
        "moderationType": 2,
        "quotationIdentifier": "d815bf9d-b8bb-4dd6-af90-d3061a7eefb4"
    }



