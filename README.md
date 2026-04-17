# People Analytics — Análise e Predição de Turnover

![Status](https://img.shields.io/badge/status-concluído-brightgreen)
![Python](https://img.shields.io/badge/Python-3.12+-blue?logo=python)
![Plotly](https://img.shields.io/badge/Plotly-interativo-blueviolet?logo=plotly)
![ML](https://img.shields.io/badge/ML-Random%20Forest-orange?logo=scikit-learn)
![Dados](https://img.shields.io/badge/dados-IBM%20HR%20Analytics-lightgrey)

Estudo analítico sobre os fatores que levam colaboradores a deixar uma empresa. O projeto vai do perfil dos funcionários até um modelo preditivo de Machine Learning com estimativa de impacto financeiro.

> *"Turnover não é um problema de salário isolado — é um problema de condições de trabalho que o salário não compensa sozinho."*

---

## Motivação

Esse projeto faz parte de uma série de People Analytics desenvolvida como portfólio. A pergunta central é a mais cara para qualquer área de RH: **quem está prestes a sair — e o que fazer antes que isso aconteça?**

Os dados do IBM HR Analytics permitem investigar essa pergunta com profundidade: 1.470 colaboradores, 35 variáveis, e uma variável-alvo clara. O modelo resultante transforma um problema reativo em uma decisão preventiva.

---

## Notebooks

| # | Notebook | Descrição | Status |
|---|---|---|---|
| 01 | `01_eda_perfil_colaboradores.ipynb` | Composição demográfica, distribuição salarial por departamento, tempo de casa e taxa de turnover por nível de cargo | ✅ |
| 02 | `02_analise_turnover.ipynb` | Fatores associados à saída: horas extras, satisfação, equilíbrio trabalho-vida, tempo sem promoção e viagens | ✅ |
| 03 | `03_modelo_predicao.ipynb` | Random Forest com feature importance, validação cruzada e estimativa de impacto financeiro | ✅ |

---

## Principais Achados

| Achado | Valor |
|---|---|
| Taxa geral de turnover | **16,1%** — acima do limite saudável de 15% |
| Impacto de horas extras | **~3× mais chance** de sair |
| Impacto de satisfação baixa | **dobra** a taxa de turnover |
| ROC-AUC do modelo | **0,83** (validação cruzada 5-fold) |
| Custo estimado das 237 saídas | **USD 6M–24M** em substituição |
| Cargo de maior risco | **Júnior** — menor salário e menor perspectiva de crescimento |

> O principal preditor não é o salário em si — é a combinação de salário baixo, horas extras e ausência de crescimento percebido.

---

## Conclusões

| Fator | Impacto | Recomendação |
|---|---|---|
| Horas extras | ~3× mais risco de saída | Monitorar frequência; custo de substituição supera o custo de ajuste |
| Satisfação no trabalho | Nota baixa dobra o turnover | eNPS e pesquisas de clima regulares capturam o sinal cedo |
| Tempo sem promoção | Risco cresce progressivamente | Trilhas de carreira claras reduzem a sensação de estagnação |
| Nível de cargo | Júnior tem maior risco | Onboarding e acompanhamento próximo nos primeiros 2 anos |
| Salário | Principal preditor do modelo | Revisões salariais periódicas comparadas ao mercado |

**Impacto financeiro:** as 237 saídas representam entre USD 6M e USD 24M em custo de substituição. Reter um colaborador de alto risco custa entre 5% e 20% desse valor.

---

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

---

## Dataset

| Base | Fonte | Variáveis |
|---|---|---|
| IBM HR Analytics Employee Attrition & Performance | [Kaggle](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset) | 1.470 colaboradores, 35 variáveis — alvo: `Attrition` (Yes/No) |

---

## Stack

| Ferramenta | Uso |
|---|---|
| Python 3.12 | Linguagem principal |
| Pandas | Manipulação de dados |
| Plotly | Visualizações interativas |
| Scikit-learn | Modelo preditivo (Random Forest) |

---

## Autor

**Rodrigo Cruz dos Santos**
[LinkedIn](https://www.linkedin.com/in/rodrigopresidati) · [GitHub](https://github.com/RodrigoPresida)
