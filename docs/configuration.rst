Configurações
===========

Ambientes
^^^^^^^^^^^^^^
Na URL dos serviços, vamos encontrar o parametro {{URL_AMBIENTE}}, que deve ser substituido de acordo com o ambiente no qual serão feitas as requisições.

``Homolog`` https://azuh3-br-api-platform.azure-api.net

``Production`` https://argoseguros.azure-api.net


Credenciais
^^^^^^^^^^^^^^
Todas as requisições devem possuir dois parametros configurados no seu Header.

``Chave`` Chave recebida pelo parceiro para utilizar em todas as requisições feitas para a API

**Header**

::

    Key: Authorization | Value: application/json
    Key: Ocp-Apim-Subscription-Key | Value: {Chave}

.. Importante:: A ``Chave`` utilizada no parametro ``Ocp-Apim-Subscription-Key`` muda de acordo com a ``{{URL_AMBIENTE}}``
