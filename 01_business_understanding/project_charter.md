# Project Charter — Via Segura

## 1. Título do projeto
#PROVISÓRIO
Via Segura: análise de acidentes em rodovias federais brasileiras.

## 2. Problema de negócio

A Polícia Rodoviária Federal disponibiliza dados sobre acidentes ocorridos nas rodovias federais brasileiras. Entretanto, esses dados estão divididos em arquivos anuais e possuem muitas variáveis, dificultando a consulta e a identificação de padrões por usuários sem conhecimento técnico.

O projeto busca facilitar o acesso e a interpretação dessas informações por meio de um dashboard interativo.

## 3. Objetivo geral

Desenvolver uma aplicação em Python com Streamlit para organizar e apresentar dados de acidentes em rodovias federais, permitindo analisar ocorrências por período, estado, município, rodovia, causa e gravidade.

## 4. Objetivos específicos

- Coletar e organizar os dados oficiais disponibilizados pela PRF.
- Padronizar estados e municípios utilizando dados do IBGE.
- Apresentar indicadores de acidentes, feridos e mortos.
- Permitir filtros por ano, estado, município e rodovia.
- Identificar as principais causas e tipos de acidentes.
- Gerar uma explicação automática dos resultados utilizando uma LLM.
- Disponibilizar as informações em um dashboard de fácil utilização.

## 5. Metas e indicadores de sucesso

| Meta | Indicador de sucesso |
|---|---|
| Integrar os dados da PRF de 2021 a 2025 | Todos os cinco anos carregados e organizados |
| Permitir a consulta dos dados | Filtros por ano, estado, município e rodovia funcionando |
| Apresentar os principais resultados | Indicadores de acidentes, feridos e mortos disponíveis |
| Facilitar a interpretação | Gráficos, tabelas e resumo textual apresentados sem erros |
| Garantir a execução da aplicação | Aplicação executada com o arquivo requirements.txt |

## 6. Público-alvo

O público-alvo é formado por cidadãos, motoristas, pesquisadores, estudantes e profissionais interessados em segurança viária. A aplicação também poderá auxiliar gestores públicos na consulta e interpretação dos dados.

## 7. ODS atendidos

### ODS 3 — Saúde e Bem-Estar

O projeto está relacionado ao ODS 3 por trabalhar com informações sobre mortes e lesões provocadas por acidentes de trânsito. A análise desses dados pode contribuir para a compreensão dos fatores associados às ocorrências.

### ODS 11 — Cidades e Comunidades Sustentáveis

O projeto também está relacionado ao ODS 11, que busca tornar os sistemas de transporte mais seguros e sustentáveis. O dashboard permitirá analisar informações relevantes para a segurança dos deslocamentos em rodovias federais.

## 8. Escopo do projeto

O projeto analisará acidentes registrados pela PRF em rodovias federais brasileiras entre 2021 e 2025. Serão considerados dados sobre localização, período, causa, tipo de acidente, condições da via, feridos e mortos.

Não fazem parte do escopo acidentes ocorridos exclusivamente em vias estaduais ou municipais, monitoramento em tempo real ou substituição das análises realizadas pelos órgãos responsáveis.

## 9. Stakeholders

- Responsável pelo projeto: Matheus Afonso.
- Fonte principal dos dados: Polícia Rodoviária Federal.
- Fonte de apoio geográfico: Instituto Brasileiro de Geografia e Estatística.
- Usuários: cidadãos, motoristas, pesquisadores, estudantes e gestores públicos.

## 10. Tecnologias previstas

- Python
- Pandas
- Streamlit
- Requests
- BeautifulSoup
- Plotly
- API de Localidades do IBGE
- Dados Abertos da PRF
- Modelo de linguagem para geração de resumos
- Git e GitHub