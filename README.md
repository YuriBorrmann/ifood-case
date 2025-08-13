
# Projeto de Recomendação de Ofertas - iFood Case

Este projeto tem como objetivo construir um modelo de ranking de ofertas para recomendar as melhores promoções a clientes do iFood, maximizando a taxa de conversão.

## Estrutura do Repositório

O projeto está organizado da seguinte forma:

```
ifood-case/
├── data/                  # Datasets
│   ├── raw/               # Dados originais
│   └── processed/         # Dados processados
├── notebooks/             # Jupyter notebooks
│   ├── 1_data_processing.ipynb  # Notebook de processamento e análise exploratória
│   └── 2_modeling.ipynb          # Notebook de modelagem e avaliação do modelo
├── presentation/          # Slides para stakeholders
├── README.md
└── requirements.txt
```

---

## Como Executar o Projeto

Siga os passos abaixo para configurar o ambiente e reproduzir a análise e o modelo.

### 1. Pré-requisitos

Certifique-se de ter o **Python** e o **pip** instalados. Recomenda-se o uso de ambiente virtual para evitar conflitos de dependências.

### 2. Configurar o Ambiente Virtual

Crie e ative um ambiente virtual:

```bash
python -m venv venv
# No Linux ou macOS
source venv/bin/activate
# No Windows
venv\Scripts\activate
```

### 3. Instalar as Dependências

Instale as bibliotecas necessárias listadas no `requirements.txt`:

```bash
pip install -r requirements.txt
```

### 4. Estrutura de Pastas e Dados

```
data/raw/
├── offers.json
├── profile.json
└── transactions.json
```

### 5. Execução dos Notebooks

O projeto é dividido em dois notebooks Jupyter, que devem ser executados na ordem:

- `1_data_processing.ipynb`  
  - Abre os dados brutos.  
  - Realiza limpeza, pré-processamento e análise exploratória.  
  - Salva o dataset final processado em `data/processed/`.

- `2_modeling.ipynb`  
  - Carrega o dataset processado.  
  - Treina um modelo de ranking (LightGBM).  
  - Avalia a performance do modelo com métricas de ranking e conversão.  
  - Calcula o impacto esperado no negócio.

Para iniciar o Jupyter Notebook, execute:

```bash
jupyter notebook
```

E abra os notebooks pelo navegador, executando as células sequencialmente.

---

## Resultados Principais

- **Modelo de Ranking:** Treinado para recomendar as ofertas mais relevantes para cada cliente.
- **Métricas de Desempenho:** A análise de conversão e hit rate indica que o modelo melhora significativamente a eficácia das ofertas comparado à baseline.
- **Impacto Financeiro:** A aplicação das recomendações do modelo pode gerar aumento relevante na receita.

Para detalhes completos sobre a análise e os resultados, consulte os notebooks na pasta `notebooks/` e a apresentação na pasta `presentation/`.
