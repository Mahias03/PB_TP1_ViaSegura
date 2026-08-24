# Via Segura

Projeto individual desenvolvido por Matheus Afonso para o TP1 da disciplina de Projeto de Bloco — Inteligência Artificial Aplicada.

## Descrição

O Via Segura é uma aplicação demonstrativa desenvolvida em Python com Streamlit. O projeto busca facilitar a consulta e a interpretação dos dados de acidentes registrados em rodovias federais brasileiras.

Nesta primeira etapa, a aplicação apresenta o problema de negócio, os objetivos, os ODS relacionados, links úteis, indicadores e uma amostra dos dados da Polícia Rodoviária Federal.

## Problema de negócio

Os dados de acidentes em rodovias federais estão divididos em arquivos anuais e possuem muitas variáveis. Isso dificulta a consulta e a identificação de padrões por usuários sem conhecimento técnico em análise de dados.

## Objetivo

Desenvolver uma aplicação em Streamlit para organizar e apresentar dados de acidentes em rodovias federais, permitindo futuramente realizar análises por período, estado, município, rodovia, causa e gravidade.

## ODS relacionados

- ODS 3 — Saúde e Bem-Estar.
- ODS 11 — Cidades e Comunidades Sustentáveis.

## Fontes de dados

- [Dados Abertos da Polícia Rodoviária Federal](https://www.gov.br/prf/pt-br/acesso-a-informacao/dados-abertos/dados-abertos-da-prf)
- [Dicionário de Dados de Acidentes da PRF](https://www.gov.br/prf/pt-br/acesso-a-informacao/dados-abertos/dicionario-acidentes)
- [API de Localidades do IBGE](https://servicodados.ibge.gov.br/api/docs/localidades)

## Estrutura do projeto

- `01_business_understanding`: entendimento do problema e Project Charter.
- `02_data_ingest_understanding`: fontes, compreensão, preparação e amostra dos dados.
- `03_modeling`: planejamento da futura etapa de modelagem.
- `04_deployment`: planejamento da implantação da aplicação.
- `05_acceptance`: planejamento da validação e entrega final.
- `app.py`: aplicação demonstrativa em Streamlit.
- `requirements.txt`: lista das dependências necessárias.
- `.gitignore`: arquivos e pastas que não devem ser enviados ao GitHub.

## Como executar

Abra o terminal na pasta principal do projeto.

### 1. Criar o ambiente virtual

```powershell
py -m venv .venv
```

### 2. Ativar o ambiente no Windows

```powershell
.\.venv\Scripts\Activate.ps1
```

### 3. Instalar as dependências

```powershell
python -m pip install -r requirements.txt
```

### 4. Executar a aplicação

```powershell
python -m streamlit run app.py
```

Após a execução, a aplicação será aberta no navegador.

## Tecnologias utilizadas nesta etapa

- Python
- Pandas
- Streamlit
- Git
- GitHub

## Tecnologias previstas para as próximas etapas

- Requests para coleta de dados por API.
- BeautifulSoup para web scraping.
- Plotly para gráficos interativos.
- Machine Learning para análise da gravidade dos acidentes.
- Modelo de linguagem para geração de resumos automáticos.

## Situação atual

O TP1 apresenta uma demonstração inicial da aplicação. A coleta automatizada, o dashboard completo, a modelagem e a integração com uma LLM serão desenvolvidos nas próximas etapas.