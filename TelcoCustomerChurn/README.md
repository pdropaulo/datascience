# 📉 Telco Customer Churn Prediction

Este repositório contém a implementação de um algoritmo de **predição de churn de clientes** utilizando o famoso dataset **Telco Customer Churn**.  
O objetivo é analisar os principais fatores que levam um cliente a cancelar o serviço e aplicar técnicas de aprendizado de máquina para prever esse comportamento.

🔗 [Acesse o notebook no Google Colab](https://colab.research.google.com/drive/1ngfg8KfywfCvR6lK8OihtxKcZdvflFgE?usp=sharing)

---

## 📂 Estrutura do Projeto
- `notebook.ipynb`: notebook principal com a análise exploratória e a modelagem.
- `dataset`: dados utilizados (Telco Customer Churn - Kaggle).
- `readme.md`: este arquivo.

---

## 📊 Objetivos do Projeto
1. **Exploração dos dados (EDA)**:  
   - Analisar distribuição dos clientes a fim de entender a relação entre os atributos e como eles podem influenciar na tomada de decisões.  
   - Entender variáveis mais correlacionadas ao churn.
   - Uso de matriz de correlação para entender como essas variáveis se relacionam (após codificação dos dados, visto que a maioria dos atributos desse dataset são dados do tipo objeto).

 * Considerações:
 *  Contagem do atributo `tenure`: aqui foi considerado a quantidade de pessoas que passou mais tempo comprometida com a empresa em intervalos de 5 meses.   <img width="580" height="432" alt="tenure count" src="https://github.com/user-attachments/assets/6882cc4a-7a3f-4bca-9669-2b92d7a7c093" />

 *  

2. **Pré-processamento**:  
   - Tratamento de valores ausentes.
   - Exclusão de dados nulos, assumindo o risco de conter alguma informação pertinente (considerando que exclusão tem o fator risco elevado). 
   - Codificação de variáveis categóricas. Aqui, as variáveis categóricas, que são maioria no dataset, foram codificadas de forma que o processo one-hot encoding foi utilizado.  
   - `Normalização dos dados.` Etapa considerada primordial devido a grande diferença de intervalo entre os atributos, mas o teste inicialmente feito com a base do Telco Customer não usou a normalização. O motivo é comparar os resultados posteriormente.  

3. **Modelagem e Avaliação**:  
   - Teste de algoritmos de classificação.  
   - Comparação de métricas como **accuracy, precision, recall, F1-score**.  

---

## 🚀 Tecnologias Utilizadas
- Python 🐍
- Pandas, NumPy, Matplotlib, Seaborn (Análise e Visualização de Dados)
- Scikit-learn (Modelagem)
- Google Colab (Execução do projeto)

---

## 📈 Resultados
- Identificação das variáveis mais influentes no churn.  
- Comparação entre modelos de Machine Learning.  
- Avaliação da performance dos classificadores aplicados.  

---

## 🔮 Próximos Passos
- Testar algoritmos mais avançados (XGBoost, LightGBM).  
- Ajustar hiperparâmetros com **GridSearchCV/RandomizedSearchCV/Optuna**.  
- Implementar balanceamento de dados mais avançado (aqui considero implementar algo como SMOTE-ENN ou SMOTE TOMEK).  

---

## 📬 Contato
✉️ Pedro Paulo Rocha de Andrade  
🌐 https://www.linkedin.com/in/pdropaulora 
📌 https://www.linktr.ee/pdropaulo
📞 +55 (85) 98995-9274

---
