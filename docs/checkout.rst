Checkout
==================

Serviço para realizar o pagamento de um cotação.

``quotationCode``
    Identificador da cotação
``paymentOption`` 
    Seção referente as informações de pagamento

    ``paymentMethodId`` Define o tipo de pagamento (1 - Boleto, 2 - VISA, 3 - MASTERCARD)

    ``installmentNumber`` Número de parcelas

    ``cardNumber`` Número do cartão

    ``cardName`` Nome que consta no cartão

    ``cardExpirationDate`` Data de expieração do cartão (Formato: AAAA/MM/DD)

    ``cardSecurityCode`` Código de segurança do cartão (CVV)
    
``insuredData`` 
    Seção referente as informações do segurado da apólice (Devem ser as mesmas informadas no momento de realizar uma cotação).

    ``Name`` Nome

    ``Email`` E-mail

    ``Identity`` CPF/CNPJ do segurado

    ``gender`` Gênero (M ou F)

    ``birthDate`` Data de Nascimento (Formato: AAAA/MM/DD)

    ``phoneNumber`` Telefone (CVV)

    ``zipCode`` CEP

    ``address`` Endereço 

    ``number`` Número do endereço
    
    ``complement`` Complemento

    ``neighborhood`` Bairro

    ``state`` UF

    ``city`` Cidade

``brokerInfo`` 
    Seção referente as informações da corretora.

    ``cnpj`` CNPJ

    ``name`` Nome

    ``email`` E-mail

    ``susepNumber`` Número SUSEP

``pepData`` 
    Seção referente as informações de PEP. (Preencher somente se for uma pessoa exposta politicamente).

    ``PEP`` 'true' ou 'false'

    ``IDontWantToFillInTheInformation`` Se deseja preencher os campos seguintes? 'true' ou 'false'

    ``EstimatedPatrimony`` Patrimônio estimado

    ``FinantialSituation`` Situação financeira

    ``Profession`` Profissão

``PolicyData`` 
    Seção referente a dados da apólice (necessário somente para o produto de Depósito Recursal)

    ``operationCode`` Código da operação utilizada na cotação.


**Endpoint**

::

    POST {{URL_AMBIENTE}}/checkout/api/checkout/


**Resquest**

::

    {
        "quotationCode": "aa4e0649-782c-471a-a909-033d6d8ecee9",
        "paymentOption": {
            "paymentMethodId": "1",
            "installmentNumber": "12",
            "cardNumber": "0000000000000001",
            "cardName": "Laura Thais",
            "cardExpirationDate": "2019-08-04",
            "cardSecurityCode": "563"
        },
        "insuredData": {
            "Name": "Gabriel Maciel",
            "Email": "maciel@maciel.com",
            "Identity": "03088589059",
            "gender": "M",
            "birthDate": "1992-01-16",
            "phoneNumber": "51993193565",
            "zipCode": "94810040",
            "address": "Jose Feijo",
            "neighborhood": "PAsso do feijo",
            "number": "1337",
            "state": "RS",
            "city": "Alto Alegre",
            "complement": "teste"
        },
        "brokerInfo": {
            "cnpj": "01566248000187",
            "name": "Better de Americana Corretora de Seguros Ltda",
            "email": "par@trin.ca",
            "susepNumber": "1020220294"
        },
        "pepData": {
            "PEP": false,
            "IDontWantToFillInTheInformation": false,
            "EstimatedPatrimony": "",
            "FinantialSituation": "",
            "Profession": ""
        }
    }

**Response**

::

    {
        "documents": [
            {
                "id": 96940,
                "name": "E&O Templates",
                "url": "https://azuq2brapi.blob.core.windows.net/documents/1f8ca969-eb64-48b1-8e99-991c8684d929/0035202000000000057"
            }
        ],
        "certificateNumber": "0035202000000000057"
    }


.. Note:: Ao preencher as informações de 'pepData' no momento da cotação, ela passa por uma processo de moderação e o checkout só poderá ser realizado após a aprovação da mesma.
