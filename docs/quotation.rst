Cotação
==================


Obter cotação
^^^^^^^^^^^^^^
Serviço utilizado para se recuperar ou obter os dados de uma cotação utilizando o identificador único no retorno da cortação.

**Endpoint**

::

    GET {{URL_AMBIENTE}}/quotation/api/quotation?identifier=c051cb56-6b95-4741-9bc2-6caf9978252d


**Response**

::

    {
        "id": 4294,
        "identifier": "d815bf9d-b8bb-4dd6-af90-d3061a7eefb4",
        "proposalNumber": "4294000000020200035",
        "name": "teste teste",
        "email": "teste@teste.com",
        "identity": "68571561311",
        "riskAnalysis": {
            "NovoSegurado": "Novo",
            "NomedaCompanhiaAnterior": "",
            "Especialidade": "Sem Procedimentos Cirúrgicos",
            "ImportânciaSegurada": "75000.00",
            "CRM": "3213213213",
            "Sinistralidade": "Nenhum",
            "Númerodereclamações": "Nenhum",
            "ConhecimentoPréviodeFatos": "Não",
            "NomedosReclamantes": ""
        },
        "effectiveDate": "2020-01-24T03:00:00",
        "updatedAt": "2020-01-23T14:36:38.2384162",
        "validThrough": "2020-02-07T14:36:26.7382647",
        "moderationProtocol": "",
        "status": 7,
        "netValue": 438.56,
        "discount": 0,
        "paymentOptions": [
            {
            "type": "Ticket",
            "totalAmount": 470.93,
            "installments": [
                {
                "installmentNumber": 1,
                "totalInstallment": 470.93,
                "insterestValue": 0,
                "iof": 32.37,
                "totalValue": 470.93
                },
                {
                "installmentNumber": 2,
                "totalInstallment": 235.46,
                "insterestValue": 0,
                "iof": 32.37,
                "totalValue": 470.93
                },
                {
                "installmentNumber": 3,
                "totalInstallment": 156.98,
                "insterestValue": 0,
                "iof": 32.37,
                "totalValue": 470.93
                },
                {
                "installmentNumber": 4,
                "totalInstallment": 117.73,
                "insterestValue": 0,
                "iof": 32.37,
                "totalValue": 470.93
                }
            ]
            },
            {
            "type": "CreditCard",
            "totalAmount": 470.93,
            "installments": [
                {
                "installmentNumber": 1,
                "totalInstallment": 470.93,
                "insterestValue": 0,
                "iof": 32.37,
                "totalValue": 470.93
                },
                {
                "installmentNumber": 2,
                "totalInstallment": 235.46,
                "insterestValue": 0,
                "iof": 32.37,
                "totalValue": 470.93
                },
                {
                "installmentNumber": 3,
                "totalInstallment": 156.98,
                "insterestValue": 0,
                "iof": 32.37,
                "totalValue": 470.93
                },
                {
                "installmentNumber": 4,
                "totalInstallment": 117.73,
                "insterestValue": 0,
                "iof": 32.37,
                "totalValue": 470.93
                }
            ]
            }
        ],
        "totalAmount": 470.93,
        "installments": [
            {
            "installmentNumber": 1,
            "totalInstallment": 470.93,
            "insterestValue": 0,
            "iof": 32.37,
            "totalValue": 470.93
            },
            {
            "installmentNumber": 2,
            "totalInstallment": 235.46,
            "insterestValue": 0,
            "iof": 32.37,
            "totalValue": 470.93
            },
            {
            "installmentNumber": 3,
            "totalInstallment": 156.98,
            "insterestValue": 0,
            "iof": 32.37,
            "totalValue": 470.93
            },
            {
            "installmentNumber": 4,
            "totalInstallment": 117.73,
            "insterestValue": 0,
            "iof": 32.37,
            "totalValue": 470.93
            }
        ],
        "deductibles_New": [
            {
            "name": "Sem franquia",
            "coverages": [
                "Ressarcimentos especiais",
                "Despesas de defesa em ações judiciais, cíveis, criminais e processos administrativos",
                "Indenizações e acordos",
                "Honorários retidos",
                "Calúnia, injúria e difamação",
                "Omissão de socorro",
                "Infecção hospitalar",
                "Chefe de equipe ou diretor médico",
                "Cobertura extensiva para a pessoa jurídica",
                "Pagamentos suplementares",
                "Danos a Reputação",
                "Custas Emergenciais"
            ]
            }
        ],
        "operationId": 35,
        "operationCode": "PROTECTOR_MEDICOS_PF",
        "personalData": {
            "name": "teste teste",
            "firstName": "teste",
            "lastName": "",
            "identity": "68571561311",
            "email": "teste@teste.com",
            "gender": null,
            "birthDate": null,
            "phoneNumber": null,
            "zipCode": null,
            "address": null,
            "neighborhood": null,
            "number": null,
            "state": null,
            "city": null,
            "complement": null,
            "secondaryDriverCPF": null,
            "secondaryDriverName": null
        },
        "deductiblesAndCoverages": {
            "deductibles": [
            {
                "name": "Sem franquia",
                "coverages": [
                "Ressarcimentos especiais",
                "Despesas de defesa em ações judiciais, cíveis, criminais e processos administrativos",
                "Indenizações e acordos",
                "Honorários retidos",
                "Calúnia, injúria e difamação",
                "Omissão de socorro",
                "Infecção hospitalar",
                "Chefe de equipe ou diretor médico",
                "Cobertura extensiva para a pessoa jurídica",
                "Pagamentos suplementares",
                "Danos a Reputação",
                "Custas Emergenciais"
                ]
            }
            ],
            "lmiAndCoverages": [
            {
                "value": "75000.00",
                "coverages": [
                "Ressarcimentos especiais",
                "Despesas de defesa em ações judiciais, cíveis, criminais e processos administrativos",
                "Indenizações e acordos",
                "Honorários retidos",
                "Calúnia, injúria e difamação",
                "Omissão de socorro",
                "Infecção hospitalar",
                "Chefe de equipe ou diretor médico",
                "Cobertura extensiva para a pessoa jurídica",
                "Pagamentos suplementares",
                "Danos a Reputação",
                "Custas Emergenciais"
                ]
            }
            ],
            "netValueAndCoverages": [
            {
                "value": "470.93",
                "coverages": [
                "Ressarcimentos especiais",
                "Despesas de defesa em ações judiciais, cíveis, criminais e processos administrativos",
                "Indenizações e acordos",
                "Danos a Reputação",
                "Custas Emergenciais"
                ],
                "proponents": null
            },
            {
                "value": "NÃ£o hÃ¡ cobranÃ§a de prÃªmio",
                "coverages": [
                "Honorários retidos",
                "Calúnia, injúria e difamação",
                "Omissão de socorro",
                "Infecção hospitalar",
                "Chefe de equipe ou diretor médico",
                "Cobertura extensiva para a pessoa jurídica",
                "Pagamentos suplementares"
                ],
                "proponents": null
            }
            ]
        },
        "voucher": null,
        "deductibles": [
            "Sem franquia"
        ]
        }




Realizar cotação - Padrão
^^^^^^^^^^^^^^
Serviço utilizado para soliciatar cotação.


``IdOperation`` Identificador da operação utilizada.

``EffectiveDate`` Data de inicio da contratação (Formato: AAAA/MM/DD)

``RiskAnalysis`` 
    Seção referente as perguntas e respostas do respectivo formulário de risco

    ``questionId`` Id da questão
    ``answer`` Resposta da questão
    
``PersonalData`` 
    Seção referente as informações do segurado da apólice (Devem ser as mesmas informadas no momento de realizar uma cotação).

    ``Name`` Nome
    ``Email`` E-mail
    ``Identity`` CPF/CNPJ do segurado

``Documents`` 
    Seção utilizada apenas na cotação do produto de Bikes para as fotos da Bike e/ou Nota Fiscal.

    ``Name`` Nome do arquivo
    ``File`` Base64 do arquivo


**Endpoint**

::

    POST {{URL_AMBIENTE}}/quotation/api/quotation/


Exemplo E&O (Médicos PF)
""""""""""""""""""

::

    {
        "IdOperation": "35",
        "RiskAnalysis": [
            {
                "questionId": "1",
                "answer": "1"
            },
            {
                "questionId": "2",
                "answer": "2"
            },
            {
                "questionId": "3",
                "answer": "1"
            },
            {
                "questionId": "4",
                "answer": "3"
            },
            {
                "questionId": "5",
                "answer": "64121"
            },
            {
                "questionId": "6",
                "answer": "1"
            },
            {
                "questionId": "7",
                "answer": "1"
            },
            {
                "questionId": "8",
                "answer": "2"
            },
            {
                "questionId": "9",
                "answer": ""
            }
        ],
        "PersonalData": {
            "Name": "Test User",
            "Email": "argo@argo.com",
            "Identity": "00000000000"
        },
        "EffectiveDate": "2019-05-20"
    }

Exemplo Bikes
""""""""""""""""""

::

    {
        "IdOperation": 14,
        "RiskAnalysis": [
            {
                "questionId": 1,
                "answer": "1"
            },
            {
                "questionId": 2,
                "answer": "Desenvolvedor"
            },
            {
                "questionId": 3,
                "answer": "1"
            },
            {
                "questionId": 4,
                "answer": "1"
            },
            {
                "questionId": 5,
                "answer": "1"
            },
            {
                "questionId": 6,
                "answer": "1"
            },
            {
                "questionId": 7,
                "answer": "1"
            },
            {
                "questionId": 8,
                "answer": "1"
            },
            {
                "questionId": 9,
                "answer": "Texto Livre"
            },
            {
                "questionId": 10,
                "answer": "Texto Livre"
            },
            {
                "questionId": 11,
                "answer": "3000"
            },
            {
                "questionId": 12,
                "answer": "Texto Livre"
            },
            {
                "questionId": 13,
                "answer": "1"
            },
            {              
                "questionId": 14,
                "answer": "2016"
            },
            {
                "questionId": 15,
                "answer": "Texto Livre"
            },
            {
                "questionId": 16,
                "answer": "Texto Livre"
            },
            {
                "questionId": 17,
                "answer": "Texto Livre"
            },
            {
                "questionId": 18,
                "answer": "Texto Livre"
            },
            {
                "questionId": 19,
                "answer": "Texto Livre"
            },
            {
                "questionId": 20,
                "answer": "Texto Livre"
            },
            {
                "questionId": 21,
                "answer": "Texto Livre"
            },
            {
                "questionId": 22,
                "answer": "Texto Livre"
            },
            {
                "questionId": 23,
                "answer": "Texto Livre"
            },
            {
                "questionId": 24,
                "answer": "Texto Livre"
            },
            {
                "answer": "Texto Livre"
            },
            {
                "answer": "Texto Livre"
            },
            {
                "questionId": 27,
                "answer": "Texto Livre"
            },
            {
                "questionId": 28,
                "answer": "Texto Livre"
            },
            {
                "questionId": 29,
                "answer": "Texto Livre"
            },
            {
                "questionId": 30,
                "answer": "Texto Livre"
            },
            {
                "questionId": 31,
                "answer": "Texto Livre"
            },
            {
                "questionId": 32,
                "answer": "Texto Livre"
            },
            {
                "questionId": 33,
                "answer": "Texto Livre"
            },
            {
                "questionId": 34,
                "answer": "Texto Livre"
            },
            {
                "questionId": 35,
                "answer": "Texto Livre"
            },
            {
                "questionId": 36,
                "answer": "Texto Livre"
            }
        ],
        "PersonalData": {
            "Name": "Test User",
            "Email": "email@argo.com",
            "Identity": "00000000000"
        },
        "Documents": [
            {
                "Name": "bike.jpg",
                "File": "iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAYAAAAfFcSJAAAADUlEQVR42mP8/5+hHgAHggJ/PchI7wAAAABJRU5ErkJggg=="
            },
            {
                "Name": "bike1.jpg",
                "File": "iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAYAAAAfFcSJAAAADUlEQVR42mP8/5+hHgAHggJ/PchI7wAAAABJRU5ErkJggg=="
            },
            {
                "Name": "bike2.jpg",
                "File": "iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAYAAAAfFcSJAAAADUlEQVR42mP8/5+hHgAHggJ/PchI7wAAAABJRU5ErkJggg=="
            },
            {
                "Name": "bike3.jpg",
                "File": "iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAYAAAAfFcSJAAAADUlEQVR42mP8/5+hHgAHggJ/PchI7wAAAABJRU5ErkJggg=="
            }
        ]
    }

.. Note:: A cotação do produto de bike está sempre sujeito a moderação, por tanto, após solicitar a cotação, acompanhe os status da moderação através do serviço de consulta de status da moderação no :doc:`/moderation` 

**Exemplo Bikes**


**Endpoint**

::

    GET {{URL_AMBIENTE}}/quotation/api/quotation/get-voucher

**Response**

::

    {
        "identifier": "18dff6f3-9f1d-42e3-aec2-aa77a901afde",
        "voucher": "502B3Q"
    }

.. Note:: Serviço utilizado para contratações do produto Bikes quando necessário

Realizar cotação - Depósito Recursal
^^^^^^^^^^^^^^

**Endpoint**

::

    POST {{URL_AMBIENTE}}/quotation/api/quotation/

Serviço utilizado para solicitar cotação de Depósito Recursal

Headers da Requisição
""""""""""""""""""

``Content-Type`` application/json;v=2.0

``Ocp-Apim-Subscription-Key`` {{Chave}}

``Authorization`` Bearer {{Token}}

.. Note:: Para obter a {{Chave}}, consulte a página :doc:`/configuration`. Para obter o {{Token}}, consulte a página de :doc:`/security`

Body da Requisição
""""""""""""""""""

``IdOperation`` Identificador da operação utilizada.

``RiskAnalysis`` 
    Seção referente as perguntas e respostas do respectivo formulário de risco

    ``questionId`` Id da questão
    ``answer`` Resposta da questão
    
``PersonalData`` 
    Seção referente as informações do segurado da apólice (Reclamante).

    ``Name`` Nome
    ``Email`` E-mail
    ``Identity`` CPF/CNPJ do segurado

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
        },
        "PersonalData": 
        {
            "Name": "Teste Reclamante",
            "Email": "reclamante@email.com",
            "Identity": "28116682000111"
        }
    }
  