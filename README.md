# ENEM 2025 Mathematics Performance Analysis

[English](#english) | [Português](#português)

---

# English

## About the Project

This project presents an exploratory analysis of Mathematics performance in the **2025 Brazilian National High School Exam (ENEM)** using official microdata provided by **INEP**.

The project was developed as a practical application of **NumPy** to a large real-world dataset. The original results dataset contains more than **4.8 million records**, allowing NumPy concepts to be applied beyond small or artificial examples.

The analysis focuses on Mathematics scores and investigates their distribution, geographical differences, school characteristics, and municipality-level performance.

## Research Questions

The project investigates the following questions:

- How are Mathematics scores distributed in the ENEM 2025?
- How does mean Mathematics performance vary across exam states?
- How does mean Mathematics performance differ across school administrative dependency categories?
- How does mean Mathematics performance differ between urban and rural schools?
- Which exam municipalities present the highest mean Mathematics scores?

## Dataset

The analysis uses the official **ENEM 2025 Microdata**, published by the Brazilian National Institute for Educational Studies and Research Anísio Teixeira (**INEP**).

The main file used in this project is:

`RESULTADOS_2025.csv`

The original dataset contains:

- **4,810,772 records**
- **70 variables**

The raw dataset is not included in this repository due to its size. It can be obtained from the official INEP ENEM microdata repository.

## Data Preparation

The project uses NumPy to load, filter, and analyze the variables required for each stage of the analysis.

Missing Mathematics scores are identified using `np.isnan()`, and boolean masks are used to preserve the positional relationship between Mathematics scores and the corresponding geographical and school variables.

After removing missing Mathematics scores, **3,260,336 valid scores** remained for the main performance analysis.

## Analysis

The notebook includes:

- Dataset structure and variable selection
- Missing-value handling
- Descriptive statistics for Mathematics scores
- Score distribution by performance ranges
- Mathematics performance by exam state
- Mathematics performance by school administrative dependency
- Mathematics performance by school location
- Ranking of the 50 exam municipalities with the highest mean Mathematics scores

## Key Findings

The valid Mathematics scores had:

- **Mean:** 519.98
- **Median:** 500.00
- **Standard deviation:** 127.64
- **Minimum:** 0.00
- **Maximum:** 980.30

More than half of the valid scores were concentrated between **400 and 600 points**.

Substantial differences were observed across geographical and school-related categories.

Among school administrative dependency categories, the mean Mathematics scores were:

- **State:** 480.63
- **Municipal:** 532.26
- **Federal:** 586.95
- **Private:** 620.32

For school location:

- **Urban:** 516.27
- **Rural:** 465.96

### Performance by Exam State

Mathematics performance varied considerably across the Brazilian states where the exam was taken.

The highest mean scores were observed in **São Paulo (SP), Santa Catarina (SC), Rio Grande do Sul (RS), Minas Gerais (MG), and the Federal District (DF)**, while lower mean scores were observed in several states in the North and Northeast regions.

It is important to note that `SG_UF_PROVA` represents the state where the exam was taken and does not necessarily correspond to the participant's state of residence or schooling.

At the municipality level, **Veranópolis (RS)** presented the highest mean Mathematics score among the exam municipalities analyzed, followed by **Lajeado (RS)** and **Valinhos (SP)**.

These results are descriptive and should not be interpreted as evidence of causal relationships.

## NumPy Concepts Applied

This project provided practical experience with:

- NumPy arrays
- Array properties (`shape`, `size`, `ndim`, `dtype`)
- Indexing and slicing
- Boolean masks
- Boolean indexing
- Missing-value handling with `np.isnan()`
- Descriptive statistics
- Percentiles
- `np.unique()`
- `np.argsort()`
- Filtering and aggregation
- Alignment between multiple arrays

The project intentionally focuses on **NumPy** rather than higher-level data manipulation libraries in order to reinforce fundamental array operations.

## Limitations

Participant-level socioeconomic information could not be linked to the Mathematics results in the dataset used for this analysis.

Therefore, the observed performance differences could not be examined in relation to socioeconomic and demographic characteristics.

Additionally, the geographical analysis based on `SG_UF_PROVA` and `NO_MUNICIPIO_PROVA` refers to the **location where the exam was taken**, which does not necessarily correspond to the participant's place of residence or school.

Future analyses using datasets that allow socioeconomic and demographic variables to be linked to individual performance could provide a more comprehensive understanding of the observed patterns.

## Technologies

- Python
- NumPy
- Google Colab
- Jupyter Notebook

## Repository Structure

```text
enem-2025-mathematics-numpy/
│
├── enem_2025_mathematics_analysis.ipynb
└── README.md
```

## How to Run

1. Download the official ENEM 2025 microdata from INEP.
2. Extract the dataset and locate `RESULTADOS_2025.csv`.
3. Open `enem_2025_mathematics_analysis.ipynb` in Google Colab or Jupyter Notebook.
4. Update `results_path` in the notebook to point to the location of `RESULTADOS_2025.csv`.
5. Run the notebook cells in order.

---

# Português

## Sobre o Projeto

Este projeto apresenta uma análise exploratória do desempenho em Matemática no **Exame Nacional do Ensino Médio (ENEM) 2025**, utilizando os microdados oficiais disponibilizados pelo **INEP**.

O projeto foi desenvolvido como uma aplicação prática de **NumPy** em uma grande base de dados real. O arquivo original de resultados contém mais de **4,8 milhões de registros**, permitindo aplicar conceitos de NumPy para além de exemplos pequenos ou artificiais.

A análise concentra-se nas notas de Matemática e investiga sua distribuição, diferenças geográficas, características das escolas e desempenho por município de aplicação da prova.

## Perguntas de Pesquisa

O projeto investiga as seguintes questões:

- Como estão distribuídas as notas de Matemática no ENEM 2025?
- Como a média de Matemática varia entre os estados de aplicação da prova?
- Como a média de Matemática varia entre as diferentes dependências administrativas das escolas?
- Como o desempenho médio difere entre escolas urbanas e rurais?
- Quais municípios de aplicação da prova apresentam as maiores médias em Matemática?

## Base de Dados

A análise utiliza os **Microdados do ENEM 2025**, publicados pelo Instituto Nacional de Estudos e Pesquisas Educacionais Anísio Teixeira (**INEP**).

O principal arquivo utilizado no projeto é:

`RESULTADOS_2025.csv`

A base original contém:

- **4.810.772 registros**
- **70 variáveis**

A base bruta não está incluída neste repositório devido ao seu tamanho. Ela pode ser obtida no repositório oficial de microdados do ENEM disponibilizado pelo INEP.

## Preparação dos Dados

O projeto utiliza NumPy para carregar, filtrar e analisar as variáveis necessárias em cada etapa.

As notas ausentes de Matemática são identificadas utilizando `np.isnan()`, enquanto máscaras booleanas são utilizadas para preservar a correspondência entre as notas e suas respectivas informações geográficas e escolares.

Após a remoção das notas ausentes de Matemática, permaneceram **3.260.336 notas válidas** para a análise principal de desempenho.

## Análises Realizadas

O notebook inclui:

- Estrutura da base e seleção de variáveis
- Tratamento de valores ausentes
- Estatísticas descritivas das notas de Matemática
- Distribuição das notas por faixas de desempenho
- Desempenho em Matemática por estado de aplicação
- Desempenho por dependência administrativa da escola
- Desempenho por localização da escola
- Ranking dos 50 municípios de aplicação com maiores médias em Matemática

## Principais Resultados

As notas válidas de Matemática apresentaram:

- **Média:** 519,98
- **Mediana:** 500,00
- **Desvio padrão:** 127,64
- **Mínimo:** 0,00
- **Máximo:** 980,30

Mais da metade das notas válidas concentrou-se entre **400 e 600 pontos**.

Foram observadas diferenças relevantes entre categorias geográficas e escolares.

De acordo com a dependência administrativa da escola, as médias de Matemática foram:

- **Estadual:** 480,63
- **Municipal:** 532,26
- **Federal:** 586,95
- **Privada:** 620,32

Em relação à localização da escola:

- **Urbana:** 516,27
- **Rural:** 465,96

### Desempenho por Estado de Aplicação

O desempenho em Matemática apresentou variações consideráveis entre os estados brasileiros onde a prova foi realizada.

As maiores médias foram observadas em **São Paulo (SP), Santa Catarina (SC), Rio Grande do Sul (RS), Minas Gerais (MG) e Distrito Federal (DF)**, enquanto médias menores foram observadas em diversos estados das regiões Norte e Nordeste.

É importante observar que `SG_UF_PROVA` representa o estado onde a prova foi realizada e não necessariamente corresponde ao estado de residência ou escolarização do participante.

No nível municipal, **Veranópolis (RS)** apresentou a maior média de Matemática entre os municípios de aplicação analisados, seguida por **Lajeado (RS)** e **Valinhos (SP)**.

Esses resultados são descritivos e não devem ser interpretados como evidência de relações causais.

## Conceitos de NumPy Aplicados

O projeto proporcionou prática com:

- Arrays NumPy
- Propriedades de arrays (`shape`, `size`, `ndim`, `dtype`)
- Indexação e slicing
- Máscaras booleanas
- Indexação booleana
- Tratamento de valores ausentes com `np.isnan()`
- Estatísticas descritivas
- Percentis
- `np.unique()`
- `np.argsort()`
- Filtragem e agregação
- Alinhamento entre múltiplos arrays

O projeto utiliza **NumPy** de forma intencional, em vez de bibliotecas de manipulação tabular de nível mais alto, com o objetivo de consolidar os fundamentos das operações com arrays.

## Limitações

As informações socioeconômicas em nível individual não puderam ser vinculadas aos resultados de Matemática na base utilizada nesta análise.

Por isso, as diferenças observadas no desempenho não puderam ser analisadas em relação a características socioeconômicas e demográficas dos participantes.

Além disso, as análises geográficas baseadas em `SG_UF_PROVA` e `NO_MUNICIPIO_PROVA` referem-se ao **local de aplicação da prova**, que não corresponde necessariamente ao local de residência ou à escola do participante.

Análises futuras utilizando bases que permitam relacionar características socioeconômicas e demográficas ao desempenho individual poderão oferecer uma compreensão mais abrangente dos padrões observados.

## Tecnologias

- Python
- NumPy
- Google Colab
- Jupyter Notebook

## Estrutura do Repositório

```text
enem-2025-mathematics-numpy/
│
├── enem_2025_mathematics_analysis.ipynb
└── README.md
```

## Como Executar

1. Baixe os microdados oficiais do ENEM 2025 disponibilizados pelo INEP.
2. Extraia os arquivos e localize `RESULTADOS_2025.csv`.
3. Abra `enem_2025_mathematics_analysis.ipynb` no Google Colab ou Jupyter Notebook.
4. Altere `results_path` no notebook para o caminho onde está localizado `RESULTADOS_2025.csv`.
5. Execute as células do notebook em ordem.
