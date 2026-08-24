# Data Summary Report — Via Segura

## 1. Objetivo do documento

Este documento apresenta o primeiro levantamento das fontes e dos dados que serão utilizados no projeto Via Segura. O projeto utilizará dados sobre acidentes em rodovias federais brasileiras e informações geográficas dos municípios.

## 2. Fonte principal — Polícia Rodoviária Federal

- Instituição: Polícia Rodoviária Federal — PRF
- Fonte: https://www.gov.br/prf/pt-br/acesso-a-informacao/dados-abertos/dados-abertos-da-prf
- Base: Boletim de Acidente de Trânsito — BAT
- Formato: CSV disponibilizado em arquivo ZIP
- Organização: acidentes agrupados por ocorrência
- Período previsto: 2021 a 2025
- Atualização informada: mensal
- Forma de obtenção: download e, futuramente, web scraping dos links disponíveis na página da PRF

A base agrupada por ocorrência foi escolhida porque cada linha representa um acidente. Isso evita a repetição que poderia ocorrer na base agrupada por pessoa.

## 3. Dados da PRF que serão utilizados

| Dado | Tipo esperado | Objetivo de uso |
|---|---|---|
| id | Inteiro | Identificar cada ocorrência |
| data_inversa | Data | Analisar a evolução dos acidentes |
| dia_semana | Texto | Comparar acidentes por dia da semana |
| horario | Horário | Identificar períodos com mais ocorrências |
| uf | Texto | Filtrar e comparar os estados |
| br | Inteiro | Identificar a rodovia federal |
| km | Decimal | Localizar o trecho da ocorrência |
| municipio | Texto | Filtrar e comparar os municípios |
| causa_acidente | Texto | Identificar as principais causas |
| tipo_acidente | Texto | Analisar os tipos de acidente |
| classificacao_acidente | Texto | Analisar a gravidade da ocorrência |
| fase_dia | Texto | Comparar ocorrências durante o dia e a noite |
| condicao_metereologica | Texto | Analisar as condições meteorológicas |
| tipo_pista | Texto | Comparar acidentes por tipo de pista |
| tracado_via | Texto | Analisar características do traçado |
| pessoas | Inteiro | Contabilizar pessoas envolvidas |
| mortos | Inteiro | Calcular o número de mortes |
| feridos_leves | Inteiro | Contabilizar feridos leves |
| feridos_graves | Inteiro | Contabilizar feridos graves |
| feridos | Inteiro | Calcular o total de feridos |
| veiculos | Inteiro | Contabilizar veículos envolvidos |
| latitude | Decimal | Representar as ocorrências geograficamente |
| longitude | Decimal | Representar as ocorrências geograficamente |

## 4. Fonte complementar — IBGE

- Instituição: Instituto Brasileiro de Geografia e Estatística — IBGE
- Fonte: https://servicodados.ibge.gov.br/api/docs/localidades
- Formato: JSON
- Forma de obtenção: API REST
- Objetivo: obter códigos e nomes oficiais de estados, municípios e regiões brasileiras

A API do IBGE será utilizada para padronizar as localidades presentes nos dados da PRF e permitir a organização dos filtros geográficos.

## 5. Tratamentos previstos

Os principais tratamentos inicialmente previstos são:

- converter datas e horários para formatos apropriados;
- padronizar nomes de estados e municípios;
- converter colunas numéricas;
- tratar valores ausentes;
- remover registros duplicados, caso existam;
- verificar categorias com grafias diferentes;
- identificar registros sem latitude ou longitude;
- juntar os dados dos diferentes anos;
- criar variáveis auxiliares, como ano, mês e período do dia.

## 6. Qualidade e limitações dos dados

Os dados dependem do registro realizado pela PRF e representam apenas ocorrências em rodovias federais atendidas pelo órgão. Portanto, não representam todos os acidentes de trânsito ocorridos no Brasil.

Também poderão existir valores ausentes, diferenças de preenchimento e mudanças entre os arquivos anuais. Essas situações serão verificadas durante a etapa de exploração e tratamento.

O ano de 2026 não será utilizado inicialmente, pois ainda está em andamento e sua comparação com anos completos poderia produzir interpretações incorretas.

## 7. Amostra dos dados

Para a aplicação demonstrativa do TP1, será utilizada uma pequena amostra dos dados de acidentes de 2025 agrupados por ocorrência.

A amostra ficará armazenada em:

`02_data_ingest_understanding/data/amostra_acidentes.csv`

Essa amostra será apresentada em uma tabela na aplicação Streamlit.

## 8. Uso futuro dos dados

Nas próximas etapas, os dados poderão ser utilizados para:

- criação de indicadores e gráficos;
- análise temporal e geográfica;
- identificação de padrões de acidentes;
- comparação entre estados, municípios e rodovias;
- criação de um modelo de classificação da gravidade;
- geração de resumos automáticos utilizando uma LLM.