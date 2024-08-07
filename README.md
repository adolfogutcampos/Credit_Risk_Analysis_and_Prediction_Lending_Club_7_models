Análisis y Predicción de Riesgo Crediticio de Lending Club

Github: adolfogutcampos

Linkedin: www.linkedin.com/in/adolfo-gutiérrez-campos-91a595131

# ⚡ 0.- Introducción

El análisis y predicción del riesgo crediticio es una tarea crucial en el ámbito financiero, ya que permite evaluar la probabilidad de que un prestatario cumpla con sus obligaciones crediticias. Este proceso se basa en un análisis exhaustivo de datos históricos y actuales para prever el comportamiento futuro de los prestatarios. 

En este documento, se aborda la predicción del riesgo crediticio utilizando un conjunto de datos proporcionado por LendingClub, una plataforma de préstamos entre particulares. El acceso a la base de datos se encuentra en el siguiente enlace:

https://www.kaggle.com/datasets/ethon0426/lending-club-20072020q1/data

En dicho enlace, se puede descargar los siguientes documentos:

- Loan_status_2007-2020Q3.csv          (Base de datos principal Base de datos original de 1,73 GB)

- LCDataDictionary.xlsx                (Descripción de las columnas de la base de datos principal)

# 🎯 1- Propósito del estudio

El principal objetivo de este estudio es desarrollar modelos de predicción de riesgo crediticio que puedan diferenciar eficazmente entre prestatarios que cumplirán con sus pagos ("Fully-Paid") y aquellos que no lo harán ("Default"). 

Para alcanzar este objetivo, se han implementado y comparado 7 modelos de Machine Learning, Deep Learning y Algoritmos Bio-Inspirados, cada uno con sus propias características y ventajas. Esto se ha plasmado en el siguiente documento en formato ipynb:

1_Prediccion_Riesgo_Crediticio_Lending_Club_2019_7_modelos.ipynb

Por otra parte, se ha realizado un EDA univariante y bivariante de varias características del dataset en el siguiente documento en formato ipynb:

2_Analisis_Riesgo_Crediticio_Lending_Club_EDA_2007_2020.ipynb

# 🏗 2.- Modelos para predicción crediticia y métricas

Construcción y evaluación de 7 modelos diferentes para la predicción del riesgo de crédito:

- 🌳 Modelo 1: Random Forest (Machine Learning)

- 🏔  Modelo 2: Gradient Boosting Classifier (Machine Learning) 

- 🖥️ Modelo 3: XGBoost (Machine Learning)

- 🧠 Modelo 4: Artificial Neural Networks (ANN) (Deep Learning)

- ⏳ Modelo 5: Long Short Memory Networks (LSTM) (Deep Learning)

- 🧬 Modelo 6: Genetic Algorithms (GA) (Algortimos Bio-Inspirados)

- ⚛️ Modelo 7: Particle Swarm Optimization (PSO) (Algoritmos Bio-Inspirados)

Tras haber elaborado los modelos, se ha identificado opciones de mejora para obtener mejores resultados en sus indicadores mediante:

- Ajuste de Hiperparámetros

- Ajuste de número de años en issue_d a más años

- Validación Cruzada

- Ensamblaje de Modelos (Ensemble)

# 📊 3.- Descripción de principales líneas del dataset

A partir del siguiente documento obtenido en el enlace de origen:

LCDataDictionary.xlsx

Se ha extraído las líneas más importantes del dataaset para la elaboración de los 7 modelos:

| No. | LoanStatNew               | Description                                                                 |
|-----|---------------------------|-----------------------------------------------------------------------------|
| 0   | loan_amnt                 | The listed amount of the loan applied for by the borrower.                  |
| 1   | term                      | The number of payments on the loan. Values are in months.                   |
| 2   | int_rate                  | Interest Rate on the loan.                                                  |
| 3   | installment               | The monthly payment owed by the borrower if the loan is funded.             |
| 4   | grade                     | LC assigned loan grade.                                                     |
| 5   | sub_grade                 | LC assigned loan subgrade.                                                  |
| 6   | emp_title                 | The job title supplied by the Borrower when applying for the loan.          |
| 7   | emp_length                | Employment length in years. Possible values are between 0 and 10.           |
| 8   | home_ownership            | The home ownership status provided by the borrower during registration.     |
| 9   | annual_inc                | The self-reported annual income provided by the borrower during registration.|
| 10  | verification_status       | Indicates if income was verified by LC, not verified, or if the income source was verified. |
| 11  | issue_d                   | The month which the loan was funded.                                        |
| 12  | loan_status               | Current status of the loan.                                                 |
| 13  | purpose                   | A category provided by the borrower for the loan request.                   |
| 14  | title                     | The loan title provided by the borrower.                                    |
| 15  | zip_code                  | The first 3 numbers of the zip code provided by the borrower in the loan application. |
| 16  | addr_state                | The state provided by the borrower in the loan application.                 |
| 17  | dti                       | A ratio calculated using the borrower’s total monthly debt payments on the total debt obligations, excluding mortgage and the requested LC loan, divided by the borrower’s self-reported monthly income. |
| 18  | earliest_cr_line          | The month the borrower's earliest reported credit line was opened.          |
| 19  | open_acc                  | The number of open credit lines in the borrower's credit file.              |
| 20  | pub_rec                   | Number of derogatory public records.                                        |
| 21  | revol_bal                 | Total credit revolving balance.                                             |
| 22  | revol_util                | Revolving line utilization rate, or the amount of credit the borrower is using relative to all available revolving credit. |
| 23  | total_acc                 | The total number of credit lines currently in the borrower's credit file.   |
| 24  | initial_list_status       | The initial listing status of the loan. Possible values are – W, F.         |
| 25  | application_type          | Indicates whether the loan is an individual application or a joint application with two co-borrowers. |
| 26  | mort_acc                  | Number of mortgage accounts.                                                |
| 27  | pub_rec_bankruptcies      | Number of public record bankruptcies.                                       |



