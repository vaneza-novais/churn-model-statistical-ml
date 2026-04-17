# Previsão de Churn em serviço de telecomunição
Esse projeto tem como objetivo investigar quais são as caracteristicas de clientes que optam pelo Churn no serviço em questão utilizando Modelagem Estatistica para entender a explicabilidade e Machine Learning para previsão.
O trabalho se encontra dividido em 3 etapas:

* Análise e diagnostico dos dados: compreensão dos dados, verificação de outliers e correlações
* Regressão Estatistíca: Aplicação de Logistic Regression para verificar e validar a relevância das variáveis e entender a linearidade dos dados através do resíduos
* Machine Learning: Aplicação de Logistic Regression, cross validation, Smote para balanceamento, Matriz de Confusão e feature importance
  
### Conclusão
De inicio, é essencial enfatizar a necessidade de entender a importancia de cada variável para Modelagem e Machine Learning, dado que o dataset original é disposto com muitas informações categóricas.  
Com isso, algumas variáveis foram eliminadas de ambas etapas e não impactaram negativamente no processo (conforme Residuo de Deviance) tornando possivel conluir que:
* As caractéristicas que mais influenciam no Churn são usuários que optam por: serviço de fibra otica, pagamento por cheque eletrônico e fatura eletrônica. Ou seja, usuários mais "digitais", que preferem praticidade.
* Quanto a previsão temos que, comparando o resultado da aplicação de Cross Validation com a não aplicação, os dados de treino apresentam um desbalanceamento para uma boa predição (poucos com Churn). Sendo necessário aplicar o balanceamento, que se mostrou seguro e resultou em um recall de 73%, ou seja, de 100 pessoas que realmente optaram por Churn, o modelo previu 73. Além disso, a variável com maior influencia sobre a predição correta de Churn, se manteve sendo usuários com serviço de fibra otica, seguido por usuários com fatura eletrônica e Streaming de Filmes, novamente, usuários mais "digitais". Em contrapartida, usuários que vão no sentido oposto de Churn são os que tem dependente e suporte tecnico, ou seja, familias preferem continuar com o serviço assim como aqueles que tem a suporte tecnico.

  **Sugestão para minimizar o Churn:**
  * Oferecer serviço tecnico gratuito para as pessoas detectadas previamente pelo modelo;
  * Oferecer planos familia, que tenham serviços para todas as idades;
  * Entender o que pode estar acontecendo com o servićo de fibra otica (sinal ruim, baixo alcance)

### Tecnologias Utilizadas
* Python (Pandas, NumPy, Matplotlib, Seaborn)
* Statsmodels (Regressão Estatística e Testes de Hipótese)
* Scikit-Learn (Machine Learning, Métricas e Validação)

### Melhorias Futuras (Previsão: junho/2026)
* Comparação entre modelos
* Gráfico de Calibração
