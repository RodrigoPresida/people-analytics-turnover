# People Analytics — Análise e Predição de Turnover

Estudo analítico sobre os fatores que levam colaboradores a deixar uma empresa, usando o dataset IBM HR Analytics. O projeto vai do perfil dos funcionários até um modelo preditivo de Machine Learning com estimativa de impacto financeiro.

## Estrutura do Projeto

```
people-analytics-turnover/
│
├── notebooks/
│   ├── 01_eda_perfil_colaboradores.ipynb   # Quem são os colaboradores?
│   ├── 02_analise_turnover.ipynb           # Por que eles saem?
│   └── 03_modelo_predicao.ipynb            # Quem está em risco?
│
├── data/
│   └── raw/                               # Dataset IBM HR (baixar do Kaggle)
│
├── requirements.txt
└── README.md
```

## Notebooks

### 01 — Perfil dos Colaboradores
Análise exploratória do headcount: composição demográfica, distribuição salarial por departamento, tempo de casa e taxa de turnover por nível de cargo.

**Principais achados:**
- Taxa geral de turnover de 16,1% — acima do limite saudável de 15%
- Profissionais júnior têm o maior risco de saída
- Salário médio de quem sai é sistematicamente menor dentro do mesmo departamento

### 02 — Análise dos Fatores de Turnover
Investigação das variáveis que mais se associam à decisão de sair: horas extras, satisfação, equilíbrio trabalho-vida, tempo sem promoção e viagens.

**Principais achados:**
- Quem faz horas extras tem ~3x mais chance de sair
- Baixa satisfação com o trabalho dobra a taxa de turnover
- Diagnóstico de ausência de crescimento: turnover cresce com o tempo sem promoção

### 03 — Modelo Preditivo de Turnover
Random Forest treinado para identificar colaboradores em risco, com feature importance para priorizar ações de RH e estimativa de impacto financeiro do turnover.

**Resultados:**
- ROC-AUC ≈ 0.83 (validação cruzada 5-fold)
- Top fatores: salário, horas extras, satisfação e tempo de casa
- Custo estimado de turnover: entre USD 6M e USD 24M para 237 saídas

## Como Reproduzir

```bash
# 1. Clone o repositório
git clone https://github.com/RodrigoPresida/people-analytics-turnover.git
cd people-analytics-turnover

# 2. Instale as dependências
pip install -r requirements.txt

# 3. Baixe o dataset
# Acesse: https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset
# Salve o CSV em: data/raw/ibm_hr_attrition.csv

# 4. Execute os notebooks na ordem
jupyter notebook
```

## Dataset

**IBM HR Analytics Employee Attrition & Performance**
- Fonte: [Kaggle](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset)
- 1.470 colaboradores, 35 variáveis
- Variável alvo: `Attrition` (Yes/No)

## Stack

| Ferramenta | Uso |
|---|---|
| Python 3.12 | Linguagem principal |
| Pandas | Manipulação de dados |
| Plotly | Visualizações interativas |
| Scikit-learn | Modelo preditivo (Random Forest) |

## Autor

**Rodrigo Presida**  
Estudante de Ciência de Dados — último semestre  
[LinkedIn](https://www.linkedin.com/in/rodrigopresida) · [GitHub](https://github.com/RodrigoPresida)
