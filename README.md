# Análise Exploratória e Modelagem Preditiva Aplicadas à Detecção de Fraudes

Este projeto aplica técnicas de **Análise Exploratória de Dados (EDA)** e **Aprendizado de Máquina** para o problema de **detecção de fraudes em transações com cartão de crédito**, um cenário caracterizado por **dados altamente desbalanceados** e elevado custo associado a erros de classificação.

O trabalho explora padrões presentes nos dados, avalia diferentes modelos de classificação e investiga estratégias adequadas de avaliação para a **classe minoritária (fraudes)**, com foco em métricas e decisões que impactam diretamente a prevenção de perdas financeiras.

---

## 📊 Conjunto de Dados

O conjunto de dados é composto por transações financeiras anonimizadas, onde cada observação representa uma transação individual. As variáveis sensíveis foram transformadas por meio de técnicas de redução de dimensionalidade, preservando propriedades estatísticas relevantes.

Principais atributos:
- **V1 a V28** — variáveis transformadas (componentes principais)
- **Time** — tempo decorrido desde a primeira transação
- **Amount** — valor monetário da transação
- **Classe** — variável alvo:
  - `0`: transação legítima  
  - `1`: transação fraudulenta  

O dataset apresenta um **desbalanceamento extremo**, tornando a escolha de métricas e estratégias de modelagem um aspecto central do projeto.

---

## 🎯 Objetivos

Os principais objetivos deste projeto são:

- Realizar uma **Análise Exploratória de Dados (EDA)** para compreender a estrutura e os padrões do conjunto de dados
- Investigar o impacto do **desbalanceamento entre classes**
- Analisar variáveis-chave como **valor** e **tempo** das transações
- Visualizar a separação entre classes utilizando técnicas de redução de dimensionalidade
- Construir e comparar **modelos de classificação supervisionados**
- Avaliar o desempenho dos modelos com foco na **Classe 1 (fraude)**
- Investigar possíveis sinais de **overfitting**
- Fornecer insights que apoiem sistemas de **prevenção a fraudes**

---

## 🧪 Metodologia

### 🔹 Análise Exploratória de Dados (EDA)
- Inspeção inicial dos dados
- Análise do desbalanceamento da variável alvo
- Distribuição estatística das variáveis **Amount** e **Time**
- Visualização da separação entre classes por meio de **PCA**
- Análise de correlação com **mapa de calor (heatmap)**

### 🔹 Modelagem Preditiva
O problema foi tratado como uma **classificação binária**, com o treinamento e avaliação dos seguintes modelos:
- Árvore de Decisão
- Random Forest
- XGBoost

A avaliação foi realizada no conjunto de treino utilizando **validação cruzada estratificada**, com análise de diferentes **thresholds de decisão**.

---

## 📈 Avaliação de Desempenho

Devido ao desbalanceamento dos dados, a avaliação dos modelos priorizou métricas adequadas à classe minoritária:

- **Precision**
- **Recall**
- **F1-Score**
- **ROC-AUC**
- **PR-AUC**

Além disso, foi conduzida uma análise de **overfitting**, comparando o comportamento dos modelos e sua capacidade de generalização.

---

## 🏆 Principais Resultados

- Confirmação do **desbalanceamento severo** entre transações legítimas e fraudulentas
- Evidência de que métricas tradicionais, como acurácia, não são suficientes isoladamente
- Modelos baseados em ensembles apresentaram melhor desempenho na detecção de fraudes
- **Random Forest** mostrou bom equilíbrio entre desempenho e robustez
- **XGBoost** obteve métricas superiores para a Classe 1, especialmente em **PR-AUC**, exigindo maior cuidado com ajuste de hiperparâmetros

---

## 💡 Insights

- A escolha correta das métricas é essencial em problemas de fraude
- A definição do threshold de decisão impacta diretamente o custo do erro
- Baixa capacidade de generalização pode indicar overfitting, mesmo com métricas elevadas no treino
- A combinação de EDA e Machine Learning fornece subsídios importantes para a tomada de decisão

---

## 🛠️ Tecnologias Utilizadas

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- XGBoost
- Jupyter Notebook

---

## 📌 Conclusão

Este projeto demonstra como técnicas de **Ciência de Dados** podem ser aplicadas de forma eficaz à **detecção de fraudes financeiras**, destacando a importância da análise exploratória, da escolha adequada de métricas e da avaliação criteriosa de modelos em cenários de dados altamente desbalanceados.

---

👤 Autor

Cleiton Hentges

Projeto desenvolvido para fins de estudo, portfólio e aprimoramento em Ciência de Dados.
