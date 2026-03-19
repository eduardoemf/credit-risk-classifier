# 💳 Credit Risk Classifier

Este projeto apresenta um pipeline completo de machine learning para **classificação de risco de crédito**, com o objetivo de prever a probabilidade de um cliente se tornar inadimplente nos próximos dois anos.

A solução foi desenvolvida utilizando a base da competição *Give Me Some Credit*, disponível no Kaggle.

---

## 🎯 Business Problem

Instituições financeiras precisam tomar decisões rápidas e precisas sobre concessão de crédito. Um erro pode gerar:

- **Aprovar clientes de alto risco → prejuízo financeiro**
- **Negar bons clientes → perda de receita e market share**

O objetivo deste projeto é construir um modelo que estime:

> 📌 **Probabilidade de inadimplência de um cliente em até 2 anos**

Essa probabilidade pode ser usada para:
- Definir limites de crédito
- Ajustar taxas de juros
- Priorizar análises manuais
- Reduzir perdas financeiras

---

## 📊 Dataset

- Fonte: Kaggle — Give Me Some Credit  
- Link: https://www.kaggle.com/competitions/GiveMeSomeCredit/overview  
- Volume: ~250.000 clientes  
- Target: `SeriousDlqin2yrs` (0 = adimplente, 1 = inadimplente)

### Principais variáveis:

| Variável | Descrição 
|----------|----------
| **SeriousDlqin2yrs** | Indica inadimplência grave em até 2 anos (1 = sim, 0 = não) 
| **age** | Idade do cliente 
| **RevolvingUtilizationOfUnsecuredLines** | Percentual de uso do crédito rotativo 
| **NumberOfTime30-59DaysPastDueNotWorse** | Nº de atrasos entre 30–59 dias 
| **NumberOfTime60-89DaysPastDueNotWorse** | Nº de atrasos entre 60–89 dias 
| **NumberOfTimes90DaysLate** | Nº de atrasos >90 dias 
| **MonthlyIncome** | Renda mensal 
| **DebtRatio** | Relação dívida/renda 
| **NumberOfOpenCreditLinesAndLoans** | Total de linhas de crédito abertas 
| **NumberRealEstateLoansOrLines** | Nº de empréstimos imobiliários 
| **NumberOfDependents** | Nº de dependentes 

---

## ⚠️ Desafios do problema

Este dataset apresenta desafios reais de modelagem:

- **Desbalanceamento de classes** (poucos inadimplentes)
- **Valores ausentes** (ex: renda mensal)
- **Outliers extremos**
- **Possível data leakage em algumas variáveis**
- **Features altamente correlacionadas**

---

## 🏗️ Pipeline do Projeto

### 1. Data Cleaning
- Tratamento de valores ausentes
- Remoção/ajuste de outliers
- Validação de consistência dos dados

### 2. Análise Exploratória (EDA)
- Distribuição das variáveis
- Correlação entre features
- Análise da variável target
- Identificação de padrões de inadimplência

### 3. Feature Engineering
- Criação de novas variáveis
- Transformações (log, scaling)
- Agrupamentos e binning

### 4. Tratamento de Desbalanceamento
- Class weights
- Undersampling / Oversampling (ex: SMOTE)
- Comparação entre abordagens

### 5. Modelagem
Modelos avaliados:
- Logistic Regression (baseline)
- Random Forest
- Gradient Boosting (XGBoost / LightGBM)

### 6. Avaliação
Métricas utilizadas:
- ROC AUC
- Precision / Recall
- F1-score
- KS Statistic
- Curva ROC

---

## 📈 Resultados

> (Preencher após rodar os modelos)

| Modelo | ROC AUC | Recall | Precision |
|--------|--------|--------|----------|
| Logistic Regression | - | - | - |
| Random Forest | - | - | - |
| XGBoost | - | - | - |

---

## 🧠 Interpretabilidade

Para tornar o modelo utilizável em ambiente real:

- Feature importance
- SHAP values
- Análise de impacto das variáveis

Isso permite responder perguntas como:

> "Por que este cliente foi classificado como alto risco?"

---

## 🚀 Possíveis melhorias

- Validação temporal (simulando produção)
- Hyperparameter tuning (Optuna/Grid Search)
- Ensemble de modelos
- Calibração de probabilidades
- Deploy (API com FastAPI)
- Monitoramento de drift

---

## 🛠️ Tecnologias utilizadas

- Python
- Pandas / NumPy
- Scikit-learn
- XGBoost / LightGBM
- Matplotlib / Seaborn

---

## 📂 Estrutura do projeto
