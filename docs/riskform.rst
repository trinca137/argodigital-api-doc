Formulário de risco
===========

Relação de perguntas x respostas do formulário de risco para cada produto E&O, diferenciados por Pessoa Física e Pessoa Jurídica.

Médicos - Pessoa Física
^^^^^^^^^^^^^^
Detalhamento do formulário de risco para o produto de Médicos Pessoa Física::

    [
      {
        "Id": 1,
        "Texto": "Você é novo segurado ou renovação de outra companhia?",
        "Obrigatório": "Sim",
        "Tipo": "Única escolha",
        "Respostas": [
          {
            "Id": 1,
            "Texto": "Novo"
          },
          {
            "Id": 2,
            "Texto": "Renovação"
          }
        ]
      },
      {
        "Id": 2,
        "IdQuestaoPai": 1,
        "IdRespostaQuestaoPai": [
          "2"
        ],
        "Texto": "Nome da Companhia Anterior",
        "Obrigatório": "Não",
        "Tipo": "Texto Livre"
      },
      {
        "Id": 3,
        "Tipo": "Única escolha",
        "Respostas": [
          {
            "Id": 2,
            "Texto": "Cirurgiões(Exceto Plástico), Anestesiologistas e Medicina Estética"
          },
          {
            "Id": 1,
            "Texto": "Sem Procedimentos Cirúrgicos"
          },
          {
            "Id": 3,
            "Texto": "Obstetras"
          }
        ]
      },
      {
        "Id": 4,
        "Texto": "Importância Segurada",
        "Obrigatório": "Sim",
        "Tipo": "Única escolha",
        "Respostas": [
          {
            "Id": 1,
            "Texto": "R$ 30.000,00"
          },
          {
            "Id": 2,
            "Texto": "R$ 50.000,00"
          },
          {
            "Id": 3,
            "Texto": "R$ 75.000,00"
          },
          {
            "Id": 4,
            "Texto": "R$ 100.000,00"
          },
          {
            "Id": 5,
            "Texto": "R$ 150.000,00"
          },
          {
            "Id": 6,
            "Texto": "R$ 200.000,00"
          },
          {
            "Id": 7,
            "Texto": "R$ 250.000,00"
          },
          {
            "Id": 8,
            "Texto": "R$ 300.000,00"
          },
          {
            "Id": 9,
            "Texto": "R$ 400.000,00"
          },
          {
            "Id": 10,
            "Texto": "R$ 500.000,00"
          },
          {
            "Id": 11,
            "Texto": "R$ 600.000,00"
          },
          {
            "Id": 12,
            "Texto": "R$ 700.000,00"
          },
          {
            "Id": 13,
            "Texto": "R$ 800.000,00"
          },
          {
            "Id": 14,
            "Texto": "R$ 900.000,00"
          },
          {
            "Id": 15,
            "Texto": "R$ 1.000.000,00"
          }
        ]
      },
      {
        "Id": 5,
        "Texto": "CRM",
        "Obrigatório": "Sim",
        "Tipo": "Texto Livre"
      },
      {
        "Id": 6,
        "Texto": "Você já sofreu qualquer tipo de reclamação extrajudicial, processo judicial civil, criminal ou ético administrativo por dano(s) causado(s) pela prestação de seus serviços nos últimos 5 anos?",
        "Obrigatório": "Sim",
        "Tipo": "Única escolha",
        "Respostas": [
          {
            "Id": 1,
            "Texto": "Nenhum"
          },
          {
            "Id": 2,
            "Texto": "1 sinistro"
          },
          {
            "Id": 3,
            "Texto": "2 sinistros"
          },
          {
            "Id": 4,
            "Texto": "3 sinistros ou mais"
          }
        ]
      },
      {
        "Id": 7,
        "IdQuestaoPai": 6,
        "IdRespostaQuestaoPai": [
          "2",
          "3",
          "4",
          "5",
          "6"
        ],
        "Texto": "Quantos sinistros nos últimos 12 meses?",
        "Obrigatório": "Sim",
        "Tipo": "Única escolha",
        "Respostas": [
          {
            "Id": 1,
            "Texto": "Nenhum"
          },
          {
            "Id": 2,
            "Texto": "1 sinistro"
          },
          {
            "Id": 3,
            "Texto": "2 sinistros ou mais"
          }
        ]
      },
      {
        "Id": 8,
        "Texto": "Você tem conhecimento de qualquer fato ou circunstância que possa gerar uma reclamação extrajudicial, processo judicial civil, criminal ou ético administrativo ou de qualquer tipo similar de pedIdo de reparação de dano(s) causados(s) pela prestação de seus serviços?",
        "Obrigatório": "Sim",
        "Tipo": "Única escolha",
        "Respostas": [
          {
            "Id": 1,
            "Texto": "Sim"
          },
          {
            "Id": 2,
            "Texto": "Não"
          }
        ]
      },
      {
        "Id": 9,
        "IdQuestaoPai": 8,
        "IdRespostaQuestaoPai": [
          "1"
        ],
        "Texto": "Nome dos Reclamantes",
        "Obrigatório": "Não",
        "Tipo": "Texto Livre"
      }
    ]

    

Médicos - Pessoa Jurídica
^^^^^^^^^^^^^^
Detalhamento do formulário de risco para o produto de Médicos Pessoa Jurídica::

    [
      {
        "Id": 1,
        "Texto": "Você é novo segurado ou renovação de outra companhia?",
        "Obrigatório": "Sim",
        "Tipo": "Única escolha",
        "Respostas": [
          {
            "Id": 1,
            "Texto": "Novo"
          },
          {
            "Id": 2,
            "Texto": "Renovação"
          }
        ]
      },
      {
        "Id": 2,
        "IdQuestaoPai": 1,
        "IdRespostaQuestaoPai": [
          "2"
        ],
        "Texto": "Nome da Companhia Anterior",
        "Obrigatório": "Não",
        "Tipo": "Texto Livre"
      },
      {
        "Id": 3,
        "Texto": "Especialidade",
        "Obrigatório": "Sim",
        "Tipo": "Única escolha",
        "Respostas": [
          {
            "Id": 1,
            "Texto": "Home Care"
          },
          {
            "Id": 2,
            "Texto": "Clínica de Radiologia e Diagnóstico por Imagem"
          },
          {
            "Id": 3,
            "Texto": "Clínica de repouso, clínica psiquiátrica, clínica para tratamento dedependentes e riscos similares"
          },
          {
            "Id": 4,
            "Texto": "Transporte de pacientes"
          },
          {
            "Id": 5,
            "Texto": "Clínicas com cirurgia (exceto cirurgia plástica)"
          },
          {
            "Id": 6,
            "Texto": "Clínica sem cirurgia"
          },
          {
            "Id": 7,
            "Texto": "Clínicas de tratamento da dor e anestesiologia"
          },
          {
            "Id": 8,
            "Texto": "Laboratórios"
          },
          {
            "Id": 9,
            "Texto": "Clínicas de obstetrícia e reprodução humana"
          }
        ]
      },
      {
        "Id": 4,
        "Texto": "Importância Segurada",
        "Obrigatório": "Sim",
        "Tipo": "Única escolha",
        "Respostas": [
          {
            "Id": 1,
            "Texto": "R$ 100.000,00"
          },
          {
            "Id": 2,
            "Texto": "R$ 150.000,00"
          },
          {
            "Id": 3,
            "Texto": "R$ 200.000,00"
          },
          {
            "Id": 4,
            "Texto": "R$ 250.000,00"
          },
          {
            "Id": 5,
            "Texto": "R$ 300.000,00"
          },
          {
            "Id": 6,
            "Texto": "R$ 500.000,00"
          }
        ]
      },
      {
        "Id": 5,
        "Texto": "Faturamento",
        "Obrigatório": "Sim",
        "Tipo": "Única escolha",
        "Respostas": [
          {
            "Id": 1,
            "Texto": "R$ 50.000,00 - 100.000,00"
          },
          {
            "Id": 2,
            "Texto": "R$ 100.000,00 - 200.000,00"
          },
          {
            "Id": 3,
            "Texto": "R$ 200.000,00 - 300.000,00"
          },
          {
            "Id": 4,
            "Texto": "R$ 300.000,00 - 500.000,00"
          },
          {
            "Id": 5,
            "Texto": "R$ 500.000,00 - 1.000.000,00"
          },
          {
            "Id": 6,
            "Texto": "R$ 1.000.000,00 - 1.500.000,00"
          },
          {
            "Id": 7,
            "Texto": "R$ 1.500.000,00 - 2.000.000,00"
          },
          {
            "Id": 8,
            "Texto": "R$ 2.000.000,00 - 3.000.000,00"
          },
          {
            "Id": 9,
            "Texto": "R$ 3.000.000,00 - 5.000.000,00"
          },
          {
            "Id": 10,
            "Texto": "R$ 5.000.000,00 - 7.500.000,00"
          },
          {
            "Id": 11,
            "Texto": "R$ 7.500.000,00 - 10.000.000,00"
          }
        ]
      },
      {
        "Id": 6,
        "Texto": "Você já sofreu qualquer tipo de reclamação extrajudicial, processo judicial civil, criminal ou ético administrativo por dano(s) causado(s) pela prestação de seus serviços nos últimos 5 anos?",
        "Obrigatório": "Sim",
        "Tipo": "Única escolha",
        "Respostas": [
          {
            "Id": 1,
            "Texto": "Nenhum"
          },
          {
            "Id": 2,
            "Texto": "1 sinistro"
          },
          {
            "Id": 3,
            "Texto": "2 sinistros"
          },
          {
            "Id": 4,
            "Texto": "3 sinistros ou mais"
          }
        ]
      },
      {
        "Id": 7,
        "IdQuestaoPai": 6,
        "IdRespostaQuestaoPai": [
          "2",
          "3",
          "4",
          "5",
          "6"
        ],
        "Texto": "Quantos sinistros nos últimos 12 meses?",
        "Obrigatório": "Sim",
        "Tipo": "Única escolha",
        "Respostas": [
          {
            "Id": 1,
            "Texto": "Nenhum"
          },
          {
            "Id": 2,
            "Texto": "1 sinistro"
          },
          {
            "Id": 3,
            "Texto": "2 sinistros ou mais"
          }
        ]
      },
      {
        "Id": 8,
        "Texto": "Você tem conhecimento de qualquer fato ou circunstância que possa gerar uma reclamação extrajudicial, processo judicial civil, criminal ou ético administrativo ou de qualquer tipo similar de pedIdo de reparação de dano(s) causados(s) pela prestação de seus serviços?",
        "Obrigatório": "Sim",
        "Tipo": "Única escolha",
        "Respostas": [
          {
            "Id": 1,
            "Texto": "Sim"
          },
          {
            "Id": 2,
            "Texto": "Não"
          }
        ]
      },
      {
        "Id": 9,
        "IdQuestaoPai": 8,
        "IdRespostaQuestaoPai": [
          "1"
        ],
        "Texto": "Nome dos Reclamantes",
        "Obrigatório": "Não",
        "Tipo": "Texto Livre"
      }
    ]


Bikes
^^^^^^^^^^^^^^
Detalhamento do formulário de risco para o produto de Bikes::

    [
      {
        "Id": 1,
        "Texto": "Você é novo segurado ou renovação de outra companhia?",
        "Obrigatório": "Sim",
        "Tipo": "Única escolha",
        "Respostas": [
          {
            "Id": 1,
            "Texto": "Novo"
          },
          {
            "Id": 2,
            "Texto": "Renovação"
          }
        ]
      },
      {
        "Id": 2,
        "Texto": "Qual a sua profissão?",
        "Obrigatório": "Sim",
        "Tipo": "Texto Livre"
      },
      {
        "Id": 3,
        "Texto": "Modalidades que pedala?",
        "Obrigatório": "Sim",
        "Tipo": "Multipla escolha",
        "Respostas": [
          {
            "Id": 1,
            "Texto": "Estrada"
          },
          {
            "Id": 2,
            "Texto": "Triatlo"
          },
          {
            "Id": 3,
            "Texto": "Mountain Bike"
          },
          {
            "Id": 4,
            "Texto": "Downhill"
          }
        ]
      },
      {
        "Id": 4,
        "Texto": "Utilização da bike?",
        "Obrigatório": "Sim",
        "Tipo": "Multipla escolha",
        "Respostas": [
          {
            "Id": 1,
            "Texto": "Locomoção diária (trabalho, escola, etc)"
          },
          {
            "Id": 2,
            "Texto": "Lazer / Hobby"
          },
          {
            "Id": 3,
            "Texto": "Uso profissional"
          }
        ]
      },
      {
        "Id": 5,
        "Texto": "Participa de Competições?",
        "Obrigatório": "Sim",
        "Tipo": "Única escolha",
        "Respostas": [
          {
            "Id": 1,
            "Texto": "Sim"
          },
          {
            "Id": 2,
            "Texto": "Não"
          }
        ]
      },
      {
        "Id": 6,
        "Texto": "Treina em Assessoria Esportiva?",
        "Obrigatório": "Sim",
        "Tipo": "Única escolha",
        "Respostas": [
          {
            "Id": 1,
            "Texto": "Sim"
          },
          {
            "Id": 2,
            "Texto": "Não"
          }
        ]
      },
      {
        "Id": 7,
        "Texto": "Locais onde Pedala?",
        "Obrigatório": "Sim",
        "Tipo": "Multipla escolha",
        "Respostas": [
          {
            "Id": 1,
            "Texto": "Área Urbana"
          },
          {
            "Id": 2,
            "Texto": "Auto Estrada"
          },
          {
            "Id": 3,
            "Texto": "Campo ou Estradas de Terra"
          },
          {
            "Id": 4,
            "Texto": "Montanha"
          }
        ]
      },
      {
        "Id": 8,
        "Texto": "Frequência de Treino?",
        "Obrigatório": "Sim",
        "Tipo": "Única escolha",
        "Respostas": [
          {
            "Id": 1,
            "Texto": "1 a 2 vezes / semana"
          },
          {
            "Id": 2,
            "Texto": "3 a 5 vezes / semana"
          },
          {
            "Id": 3,
            "Texto": "Mais de 5 vezes"
          }
        ]
      },
      {
        "Id": 9,
        "Texto": "Descrição da Bicicleta",
        "Obrigatório": "Sim",
        "Tipo": "Texto Livre"
      },
      {
        "Id": 10,
        "Texto": "Local de Compra",
        "Obrigatório": "Sim",
        "Tipo": "Texto Livre"
      },
      {
        "Id": 11,
        "Texto": "Valor de Mercado",
        "Obrigatório": "Sim",
        "Tipo": "Decimal"
      },
      {
        "Id": 12,
        "Texto": "Número de Série",
        "Obrigatório": "Sim",
        "Tipo": "Texto Livre"
      },
      {
        "Id": 13,
        "Texto": "Bike Nova (0km)?",
        "Obrigatório": "Sim",
        "Tipo": "Única escolha",
        "Respostas": [
          {
            "Id": 1,
            "Texto": "Sim"
          },
          {
            "Id": 2,
            "Texto": "Não"
          }
        ]
      },
      {
        "Id": 14,
        "Texto": "Ano de Fabricação",
        "Obrigatório": "Sim",
        "Tipo": "Número"
      },
      {
        "Id": 15,
        "Texto": "Possui Nota Fiscal?",
        "Obrigatório": "Sim",
        "Tipo": "Única escolha",
        "Respostas": [
          {
            "Id": 1,
            "Texto": "Sim"
          },
          {
            "Id": 2,
            "Texto": "Não"
          }
        ]
      },
      {
        "Id": 16,
        "Texto": "Bike Original?",
        "Obrigatório": "Sim",
        "Tipo": "Única escolha",
        "Respostas": [
          {
            "Id": 1,
            "Texto": "Sim"
          },
          {
            "Id": 2,
            "Texto": "Não"
          }
        ]
      },
      {
        "Id": 17,
        "Texto": "Modificações - Quadro",
        "Obrigatório": "Não",
        "Tipo": "Texto Livre"
      },
      {
        "Id": 18,
        "Texto": "Modificações - Pedivela",
        "Obrigatório": "Não",
        "Tipo": "Texto Livre"
      },
      {
        "Id": 19,
        "Texto": "Modificações - Câmbio Traseiro",
        "Obrigatório": "Não",
        "Tipo": "Texto Livre"
      },
      {
        "Id": 20,
        "Texto": "Modificações - Selim",
        "Obrigatório": "Não",
        "Tipo": "Texto Livre"
      },
      {
        "Id": 21,
        "Texto": "Modificações - Mesa",
        "Obrigatório": "Não",
        "Tipo": "Texto Livre"
      },
      {
        "Id": 22,
        "Texto": "Modificações - Trocador Traseiro",
        "Obrigatório": "Não",
        "Tipo": "Texto Livre"
      },
      {
        "Id": 23,
        "Texto": "Modificações - Cubos",
        "Obrigatório": "Não",
        "Tipo": "Texto Livre"
      },
      {
        "Id": 24,
        "Texto": "Modificações - Pneus",
        "Obrigatório": "Não",
        "Tipo": "Texto Livre"
      },
      {
        "Id": 25,
        "Texto": "Modificações - Cor",
        "Obrigatório": "Não",
        "Tipo": "Texto Livre"
      },
      {
        "Id": 26,
        "Texto": "Modificações - Tamanho",
        "Obrigatório": "Não",
        "Tipo": "Texto Livre"
      },
      {
        "Id": 27,
        "Texto": "Modificações - Garfo",
        "Obrigatório": "Não",
        "Tipo": "Texto Livre"
      },
      {
        "Id": 28,
        "Texto": "Modificações - Freios",
        "Obrigatório": "Não",
        "Tipo": "Texto Livre"
      },
      {
        "Id": 29,
        "Texto": "Modificações - Câmbio Dianteiro",
        "Obrigatório": "Não",
        "Tipo": "Texto Livre"
      },
      {
        "Id": 30,
        "Texto": "Modificações - Canote",
        "Obrigatório": "Não",
        "Tipo": "Texto Livre"
      },
      {
        "Id": 31,
        "Texto": "Modificações - Guidão",
        "Obrigatório": "Não",
        "Tipo": "Texto Livre"
      },
      {
        "Id": 32,
        "Texto": "Modificações - Trocador Dianteiro",
        "Obrigatório": "Não",
        "Tipo": "Texto Livre"
      },
      {
        "Id": 33,
        "Texto": "Modificações - Rodas",
        "Obrigatório": "Não",
        "Tipo": "Texto Livre"
      },
      {
        "Id": 34,
        "Texto": "Modificações - Pedal",
        "Obrigatório": "Não",
        "Tipo": "Texto Livre"
      },
      {
        "Id": 35,
        "Texto": "Modificações - Número de Marchas",
        "Obrigatório": "Não",
        "Tipo": "Texto Livre"
      },
      {
        "Id": 36,
        "Texto": "Modificações - Clip",
        "Obrigatório": "Não",
        "Tipo": "Texto Livre"
      }
    ]


Depósito Recursal
^^^^^^^^^^^^^^^^^^
Detalhamento do formulário de risco para o produto Depósito Recursal::

    [
      {
        "Id": 1,
        "Texto": "Valor do Processo",
        "Obrigatório": "Sim",
        "Type": "Decimal"
      },
      {
        "Id": 2,
        "Texto": "Tipo de Recurso",
        "Obrigatório": "Sim",
        "Tipo": "Única escolha",
        "Respostas": [
          {
            "Id": 1,
            "Texto": "Recurso Ordinário"
          },
          {
            "Id": 2,
            "Texto": "Recurso de Revista"
          },
          {
            "Id": 3,
            "Texto": "Embargos"
          },
          {
            "Id": 4,
            "Texto": "Recurso Extraordinário"
          },
          {
            "Id": 5,
            "Texto": "Recurso em Ação Rescisória"
          },
          {
            "Id": 6,
            "Texto": "Agravo de Instrumento"
          }
        ]
      },
      {
        "Id": 3,
        "Texto": "Adicional CPC",
        "Obrigatório": "Sim",
        "Tipo": "Decimal",
        "Valores Possiveis": ["0", "5", "10", "15", "20", "25", "30"]
      },
      {
        "Id": 4,
        "Texto": "Início de Vigência",
        "Obrigatório": "Sim",
        "Type": "Data"
      },
      {
        "Id": 5,
        "Texto": "Prazo",
        "Obrigatório": "Sim",
        "Tipo": "Única escolha",
        "Respostas": [
          {
            "Id": 1,
            "Texto": "3 anos"
          },
          {
            "Id": 2,
            "Texto": "4 anos"
          },
          {
            "Id": 3,
            "Texto": "5 anos"
          }
        ]
      }
    ]