# Diário-de-bordo
# Análise de Corridas - info_transportes.csv

Este projeto tem como objetivo processar os dados do arquivo info_transportes.csv, que contém registros de corridas realizadas por um aplicativo de transporte privado. A análise agrupa as corridas por data de início e gera uma nova tabela chamada info_corridas_do_dia, contendo estatísticas relevantes para o time de negócio entender o comportamento dos usuários.

O arquivo de entrada info_transportes.csv possui as seguintes colunas:

- DATA_INICIO (formato: "mm-dd-yyyy HH")
- DATA_FIM (formato: "mm-dd-yyyy HH")
- CATEGORIA (Negócio ou Pessoal)
- LOCAL_INICIO
- LOCAL_FIM
- PROPOSITO (ex: Reunião, Voltar para casa, etc.)
- DISTANCIA (em milhas)

## Objetivo:

Criar uma nova tabela  com os dados agregados por dia (yyyy-MM-dd), contendo as colunas:

| Coluna              | Descrição                                                           |
|---------------------|---------------------------------------------------------------------|
| DT_REFE           | Data de referência (DATA_INICIO convertida para o formato yyyy-MM-dd) |
| QT_CORR           | Quantidade total de corridas do dia                                 |
| QT_CORR_NEG       | Corridas com a categoria "Negócio"                                  |
| QT_CORR_PESS      | Corridas com a categoria "Pessoal"                                  |
| VL_MAX_DIST       | Maior distância percorrida                                          |
| VL_MIN_DIST       | Menor distância percorrida                                          |
| VL_AVG_DIST       | Distância média das corridas                                        |
| QT_CORR_REUNI     | Corridas com o propósito "Reunião"                                  |
| QT_CORR_NAO_REUNI | Corridas com propósito diferente de "Reunião"                       |

## Ferramentas Utilizadas

- Pyspark
- Databricks


  
##  Como Executar? 

1. Abra o notebook info_transportes.ipynb no Jupyter ou Databricks
2. Execute as células na ordem para importar, tratar e visualizar os dados
3. A tabela final será exibida ao final do notebook
