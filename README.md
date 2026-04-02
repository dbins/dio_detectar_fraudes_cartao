# 📊 Detecção de Fraude em Cartões de Crédito — Estudo Didático

Este projeto tem como objetivo demonstrar, de forma simples e prática, como diferentes modelos de Machine Learning podem ser utilizados para detectar fraudes em transações de cartão de crédito. Este foi um desafio proposto no bootcamp de Python para Análise e Automação de Dados feito pela DIO - Digital Innovation One. 

O dataset no formato CSV possui 284.809 registros e tem o tamanho de 144 mb. O link para baixar ele é este

https://storage.googleapis.com/download.tensorflow.org/data/creditcard.csv

O dataset utilizado contém transações rotuladas como:

* **0** → transação normal
* **1** → transação fraudulenta

Um dos principais desafios desse problema é o **desbalanceamento dos dados**, já que fraudes representam uma pequena fração do total.

---

## 🤖 Modelos utilizados

### 1. Regressão Linear

A Regressão Linear foi utilizada como ponto de partida.
Embora seja um modelo voltado para prever valores contínuos, ela pode ser adaptada para classificação simples usando um limite (threshold).

🔎 **Objetivo didático:**
Entender como um modelo básico se comporta em um problema de classificação.

⚠️ **Limitação:**
Não é adequada para classificação binária e tende a apresentar resultados pouco confiáveis nesse contexto.

---

### 2. Regressão Logística

A Regressão Logística é um modelo mais apropriado para problemas de classificação binária, como detecção de fraude.

🔎 **Vantagens:**

* Simples e eficiente
* Fácil interpretação
* Boa baseline para comparação

✅ **Uso recomendado:**
Primeiro modelo “correto” para esse tipo de problema.

---

### 3. Random Forest

O Random Forest é um modelo baseado em múltiplas árvores de decisão. Ele combina várias árvores para gerar uma previsão mais robusta.

🔎 **Vantagens:**

* Captura relações não-lineares
* Mais resistente a overfitting
* Boa performance geral

⚠️ **Observação:**
Pode ser mais lento para treinar, especialmente com grandes volumes de dados.

---

### 4. XGBoost

O XGBoost é um modelo avançado baseado em técnicas de boosting. Ele é amplamente utilizado em problemas reais e competições de Machine Learning.

🔎 **Vantagens:**

* Alta performance
* Excelente para dados tabulares
* Lida bem com desbalanceamento

🚀 **Destaque:**
Foi o modelo com melhor potencial de desempenho neste estudo.

---

## ⚖️ Técnica Extra: Balanceamento com SMOTE

Além dos modelos, foi utilizada a técnica **SMOTE (Synthetic Minority Over-sampling Technique)**.

🔎 **O que faz:**

* Cria exemplos sintéticos da classe minoritária (fraudes)
* Equilibra o dataset para melhorar o aprendizado

⚠️ **Cuidados:**

* Deve ser aplicado apenas nos dados de treino
* Pode gerar overfitting se usado incorretamente

---

## 📊 Conclusão

Este estudo mostra a evolução de modelos simples até técnicas mais avançadas:

* Modelos básicos ajudam a entender o problema
* Modelos mais complexos capturam melhor padrões de fraude
* Técnicas de balanceamento são essenciais em dados desbalanceados

💡 Em aplicações reais, modelos como **XGBoost**, aliados a ajustes finos e análise de métricas como *recall* e *ROC-AUC*, tendem a oferecer os melhores resultados.

---

## 🎯 Objetivo do Projeto

Este projeto tem caráter **didático**, com foco em:

* Comparar diferentes abordagens
* Entender o impacto do desbalanceamento
* Demonstrar boas práticas em Machine Learning

---

## 🚀 Próximos Passos (opcional)

* Ajuste de hiperparâmetros
* Uso de métricas avançadas (ROC-AUC, Precision-Recall)
* Teste com outros modelos (LightGBM, redes neurais)
* Deploy do modelo

---
