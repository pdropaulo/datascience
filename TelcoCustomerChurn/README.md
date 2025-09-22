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
- Contagem do atributo `tenure`: aqui foi considerado a quantidade de pessoas que passou mais tempo comprometida com a empresa em intervalos de 5 meses.
<img width="580" height="432" alt="tenure count" src="https://github.com/user-attachments/assets/6882cc4a-7a3f-4bca-9669-2b92d7a7c093" />
- Contagem do atributo `monthlycharges`: aqui foi considerado a quantidade de pessoas que teve pagamento mensal em faixas de 5 unidades monetárias.  
<img width="580" height="432" alt="montly charges count" src="https://github.com/user-attachments/assets/0c8cea44-7e1e-4649-bcea-82f2564c4979" />
- Contagem do atributo `tenure` por idade do cliente, considerando ele ser maior ou não de 60: a ideia foi analisar se o fator idade é crucial para cancelamento do plano. A ideia de que pessoas com mais de 60 anos poderiam cancelar o plano se mostrou equivocada na medida em que o gráfico mostrou a ideia contrária, ou seja, as pessoas com menos de 60 anos eram as que mais cancelavam seus planos. Além disso, a distribuição é um tanto constante, não se aproximando do aspecto de uma distribuição normal (de Gauss).
<img width="580" height="432" alt="tenure-senior citizen count" src="https://github.com/user-attachments/assets/2622a480-5961-4c66-897e-96d3652a4205" />
- Contagem da variável `contrato` por atributo alvo `churn`: aqui foi verificado qual atributo de contrato foi primordial no cancelamento dos pacotes Telco. Nesse caso, considera-se que pacotes de plano mensal são mais suscetíveis a cancelamento de clientes.
<img width="580" height="432" alt="contract-churn count" src="https://github.com/user-attachments/assets/86af0c74-8065-4f39-b3e4-d670b1c32c1c" />
- Contade da variável `Payment Method` por atributo alvo `churn`: nesse caso, foi considerado descobrir qual método de pagamento seria mais fácil de ter cancelamento por conta dos clientes. Os métodos automáticos, ou seja, os que se renovam automaticamente, seja no crédito, seja no débito, levam a menos cancelamento.
<img width="580" height="556" alt="paymentmethod-churn count" src="https://github.com/user-attachments/assets/b39549f8-c96b-45cf-a379-a63e3305a3c2" />
- Pairplot: o pairplot considerou os atributos numéricos da base, o `tenure`, o `monthly charges` e o `total charges` para verificar como eles interagem entre si. Assim, foi possível descobrir que `tenure` e `total charges` têm variação positiva para ambas as classes, assim como ocorre com o `monthly charges` e o `total charges`. No entanto, o mesmo não ocorre com o `tenure` e o `monthly charges`, que não é possível verificar como as variáveis interagem.
<img width="820" height="741" alt="pairplot" src="https://github.com/user-attachments/assets/870e1373-a91b-430c-8ff8-d57ee2b81455" />
 


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
