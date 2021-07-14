Proposta
==================

Criar proposta
^^^^^^^^^^^^^^

Serviço utilizado para gerar uma proposta a partir de uma cotação existente, anexando as fotos da Bike quando aplicável, e atualizando os dados pessoais do segurado.

``Identifier`` Código da Cotação.
   
``PersonalData`` 
    Seção referente as informações do segurado da apólice (Devem ser as mesmas informadas no momento de realizar uma cotação).

    ``Name`` Nome
    
    ``Email`` E-mail
    
    ``Identity`` CPF/CNPJ do segurado
    
    ``Gender``: Sexo - "M" para masculino, "F" para feminino
    
    ``PhoneNumber`` Telefone - "(XX) XXXXX XXXX"
    
    ``zipCode`` CEP
    
    ``address`` Endereço
    
    ``neighborhood`` Bairro
    
    ``number`` Número
    
    ``state``: UF
    
    ``city``: Cidade
    
    ``complement`` Complemento (opcional)
    
    ``secondaryDriverCPF`` CPF do Segundo Condutor - Apenas BIKES - Opcional
    
    ``secondaryDriverName`` Nome do Segundo Condutor - Apenas BIKES - Opcional,
    
    ``birthDate``: Data de Nascimento - "YYYY-MM-DDDD"

``pepData`` 
    Seção referente as informações de PEP. (Preencher somente se for uma pessoa exposta politicamente).

    ``PEP`` 'true' ou 'false'
    
    ``IDontWantToFillInTheInformation`` Se deseja preencher os campos seguintes? 'true' ou 'false'
    
    ``EstimatedPatrimony`` Patrimônio estimado
    
    ``FinantialSituation`` Situação financeira
    
    ``Profession`` Profissão


``Documents`` 
    Seção referente à lista de documentos da proposta. Ex.: Fotos da Bike (quando aplicável).
    
    ``Name`` Nome e extensão do arquivo
    
    ``File`` Arquivo - Base64 string
    
    ``FileType`` MIME type



``HasVoucher`` 'true' ou 'false', informar true caso não seja enviada a nota fiscal de bikes no nó ``Documents``
 

**Endpoint**

::

    POST {{URL_AMBIENTE}}/quotation/api/proposal
    
    
Exemplo
""""""""""""""""""

::

   {
       "Identifier": "{identifier da cotação}",
       //Dados do segurado
       "PersonalData": { 
           "name": "{Nome}",
           "identity": "{CPF/CNPJ}",
           "email": "{e-mail}",
           "gender": "{sexo - M para masculino, F para feminino}",
           "phoneNumber": "{Telefone (XX) XXXXX XXXX}",
           "zipCode": "{CEP}",
           "address": "{Endereço}",
           "neighborhood": "{Bairro}",
           "number": "{Número}",
           "state": "{UF}",
           "city": "{Cidade}",
           "complement": "{Complemento (opcional)}",
           "secondaryDriverCPF": "{CPF do Segundo Condutor - Apenas BIKES - Opcional}",
           "secondaryDriverName": "{Nome do Segundo Condutor - Apenas BIKES - Opcional}",
           "birthDate": "{Data de Nascimento - YYYY-MM-DDDD}"
       },
       //Dados de PEP
       "PEPData": {
           "PEP": false, //true se for Pessoa Exposta Politicamente
           "IDontWantToFillInTheInformation": false,
           "EstimatedPatrimony": "",
           "FinantialSituation": "",
           "Profession": "",
           "PhoneNumber": "(19) 99936 552",
           "Address": "Rua Missões, 500  - Vila Vista Alegre, Cachoeirinha - RS, 94945-410",
           "BirthDate": "1986-08-24T03:00:00.000Z"
       },
       //Fotos da Bike (quando aplicável)
       "Documents": [
           {
               //Foto da bike inteira
               "Name": "{Nome e extensão do arquivo}",
               "File": "{Arquivo - Base64}",
               "FileType": "{MIME type}"
           },
           {
               //Foto do grupo da bike
               "Name": "{Nome e extensão do arquivo}",
               "File": "{Arquivo - Base64}",
               "FileType": "{MIME type}"
           },
           {
               //Foto do número de série
               "Name": "{Nome e extensão do arquivo}",
               "File": "{Arquivo - Base64}",
               "FileType": "{MIME type}"
           },
           {
               //NF da bike (se informado na cotação que possui nota fiscal)
               "Name": "{Nome e extensão do arquivo}",
               "File": "{Arquivo - Base64}",
               "FileType": "{MIME type}"
           }
       ],
       "hasVoucher": false //Se possuir voucher (quando nao possuir a NF da Bike) enviar true
   }

.. Note:: A cotação do produto de bike está sempre sujeito a moderação, por tanto, após solicitar a cotação, acompanhe os status da moderação através do serviço de consulta de status da moderação no Fluxo Moderação :doc:`/moderation`.

**Response**

A estrutura de response é a mesma do endpoint para obter cotação, veja Cotação :doc:`/quotation`
