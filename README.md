# roperacional-dados

Data package com dados do Armazém SIAFI que alimentam o Relatório Operacional

## Validações

Instale as dependências[^1] e para validação do data package completo execute:

```bash
frictionless validate datapackage.yaml
```

```
┏━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┳━━━━━━━┳━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┳━━━━━━━━━┓
┃ name                          ┃ type  ┃ path                                                           ┃ status  ┃
┡━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━╇━━━━━━━╇━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━╇━━━━━━━━━┩
│ alteracoes-orcamentarias      │ table │ data-raw/alteracoes_orcamentarias_2017.xlsx (multipart)        │ INVALID │
│ cota-item-data                │ table │ data-raw/cota-item-data_2017.xlsx (multipart)                  │ INVALID │
│ credito-inicial-autorizado    │ table │ data-raw/credito-inicial-autorizado_2014-2017.xlsx (multipart) │ INVALID │
│ execucao-itens-materiais      │ table │ data-raw/execucao-itens-materiais_2017.xlsx (multipart)        │ INVALID │
│ execucao                      │ table │ data-raw/execucao_2017-01.xlsx (multipart)                     │ INVALID │
│ receita                       │ table │ data-raw/receita_2017.xlsx (multipart)                         │ INVALID │
│ restos-pagar                  │ table │ data-raw/restos-pagar_2019-01_parte-1.xlsx (multipart)         │ INVALID │
│ tbl-aux_upg-desc              │ table │ data-raw/tbl-aux_upg-desc.xlsx                                 │ INVALID │
│ tbl-aux_acao-desc             │ table │ data-raw/tbl-aux_acao-desc.xlsx                                │ INVALID │
│ tbl-aux_acao-desc_rp          │ table │ data-raw/tbl-aux_acao-desc_RP.xls                              │ VALID   │
│ tbl-aux_agrupamento           │ table │ data-raw/tbl-aux_agrupamento.xls                               │ INVALID │
│ tbl-aux_elemento-item         │ table │ data-raw/tbl-aux_elemento-item.csv                             │ VALID   │
│ tbl-aux_natureza-desp-desc    │ table │ data-raw/tbl-aux_natureza-desp-desc.xls                        │ VALID   │
│ tbl-aux_objeto-processo-siafi │ table │ data-raw/tbl-aux_objeto-processo-siafi.csv                     │ INVALID │
│ tbl-aux_obra-desc             │ table │ data-raw/tbl-aux_obra-desc.xlsx                                │ INVALID │
│ tbl-aux_razao-social-desc     │ table │ data-raw/tbl-aux_razao-social-desc.xlsx                        │ INVALID │
│ tbl-aux_unidade-orcamentaria  │ table │ data-raw/tbl-aux_unidade-orcamentaria.csv                      │ VALID   │
│ reest_desp                    │ file  │ data-raw/reest_desp.xlsm                                       │ VALID   │
│ reest_rec                     │ file  │ data-raw/reest_desp.xlsm                                       │ VALID   │
└───────────────────────────────┴───────┴────────────────────────────────────────────────────────────────┴─────────┘
```

Também é possível realizar outros tipos de validação:

```bash
frictionless validate --resource-name receita datapackage.yaml # validação de um recurso específico
frictionless validate data-raw/receita_2017.xlsx # validação de um arquivo sem verificação de um table schema associado 
```

[^1]: Com `python -m pip install -r requirements.txt` de preferência em um ambiente virtual