# 💳 Credit Risk Prediction — Previsão de Inadimplência com Machine Learning

<div align="center">

![Python](https://img.shields.io/badge/Python-3.10-blue)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-XGBoost-green)
![Status](https://img.shields.io/badge/Status-Concluído-success)
![Dataset](https://img.shields.io/badge/Dataset-Kaggle-orange)

</div>

---

# 📌 Visão geral

A inadimplência representa um dos principais riscos financeiros para bancos e fintechs. A capacidade de identificar clientes com maior probabilidade de inadimplência antes da concessão de crédito é essencial para reduzir perdas e melhorar a qualidade da carteira.

Este projeto desenvolve um modelo de Machine Learning capaz de prever a probabilidade de inadimplência com base em dados financeiros e comportamentais dos clientes.

---

# 🎯 Objetivo do projeto

Construir um modelo preditivo para classificar clientes quanto ao risco de inadimplência, permitindo apoiar decisões como:

- ✔ Aprovação ou recusa de crédito  
- ✔ Definição de limite de crédito  
- ✔ Ajuste de taxa de juros  
- ✔ Classificação de clientes por nível de risco  

---
# 📊 Dataset

Dataset utilizado: **Give Me Some Credit (Kaggle)**

Contém mais de **100.000 clientes** e variáveis como:

## Variáveis explicativas

- Idade  
- Renda mensal  
- Taxa de utilização de crédito  
- Taxa de endividamento  
- Histórico de atrasos  
- Número de linhas de crédito  
- Número de dependentes  

## Variável alvo

**Inadimplente_2anos**

- `0` → Não inadimplente  
- `1` → Inadimplente  

---
# 🔎 Análise Exploratória de Dados (EDA)

## Distribuição da inadimplência

<div align="center">
<img src="imagens/Percentual_de_inadimplencia.png" width="600">
</div>

### Insight

- O dataset é desbalanceado  
- A maioria dos clientes não é inadimplente  
- Isso exige atenção na avaliação do modelo  

---

## Histórico de atrasos vs inadimplência

<div align="center">
<img src="imagens/boxplot_atrasos.png" width="600">
</div>

### Insight

Clientes inadimplentes apresentam significativamente mais atrasos.

Esta é uma das variáveis mais importantes para prever risco.

---
## Uso de crédito vs inadimplência

<div align="center">
<img src="imagens/uso_credito.png" width="600">
</div>

### Insight

Quanto maior a utilização do limite de crédito, maior o risco de inadimplência.

---
# 🤖 Modelagem de Machine Learning

Foram treinados três modelos:

## Modelos utilizados

- Regressão Logística
- Random Forest
- XGBoost

## Métricas avaliadas

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC
- Matriz de Confusão

---

# 🏆 Melhor modelo: XGBoost

O modelo XGBoost apresentou o melhor desempenho geral.

## Vantagens observadas

- Melhor capacidade de separação das classes
- Melhor equilíbrio entre precision e recall
- Melhor performance geral

Também foi realizado ajuste de threshold para melhorar a detecção de inadimplentes.

---

# 📉 Matriz de Confusão

<div align="center">
<img src="imagens/matriz_confusao.png" width="500">
</div>

## Interpretação

- True Negative: clientes corretamente classificados como não inadimplentes  
- True Positive: clientes corretamente classificados como inadimplentes  
- False Positive: clientes classificados como inadimplentes, mas não são  
- False Negative: clientes classificados como não inadimplentes, mas são  

Insight principal:

O modelo apresenta boa capacidade de identificação de risco.

---

# 🧠 Feature Importance (Random Forest)

<div align="center">
<img src="imagens/feature_importance.png" width="600">
</div>

## Principais variáveis mais importantes

1. Taxa de utilização de crédito  
2. Taxa de endividamento  
3. Renda mensal  
4. Histórico de atrasos  
5. Idade  

## Insight

O comportamento financeiro é o principal fator de risco.

---

# 💼 Impacto de negócio

Este modelo pode ser utilizado para:

- Reduzir perdas financeiras
- Melhorar decisões de crédito
- Identificar clientes de alto risco
- Otimizar concessão de crédito
- Melhorar qualidade da carteira

---

# 🛠️ Tecnologias utilizadas

<div>

- Python  
- Pandas  
- NumPy  
- Matplotlib  
- Seaborn  
- Plotly  
- Scikit-learn  
- XGBoost  

</div>

---

# 🚀 Como executar o projeto
1. Clonar o repositório
git clone https://github.com/seuusuario/Inadimplencia_Credito.git
2. Entrar na pasta
cd Inadimplencia_Credito
3. Abrir o notebook
jupyter notebook notebooks/previsao_inadimplencia.ipynb

---

📈 Melhorias futuras

Deploy do modelo em API

Dashboard interativo

Ajuste fino de hiperparâmetros

Testes com outros algoritmos

---

👩‍💻 Autora

Deane Saraiva

Projeto desenvolvido para portfólio em Data Science.

---

⭐ Destaques do projeto

✔ Problema real de negócio
✔ Pipeline completo de Machine Learning
✔ Modelos avançados
✔ Interpretação de resultados
✔ Feature Importance
✔ Matriz de Confusão
✔ Ajuste de threshold

# 📁 Estrutura do projeto

```bash
credit-risk-prediction/

│
├── data/
│   ├── train.csv
│   └── test.csv
│
├── notebooks/
│   └── credit_risk_model.ipynb
│
├── imagens/
│   ├── distribuicao_inadimplencia.png
│   ├── boxplot_atrasos.png
│   ├── matriz_confusao.png
│   └── feature_importance.png
│
├── modelo/
│   └── modelo_xgboost.pkl
│
└── README.md
