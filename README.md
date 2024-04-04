* ABOUT:
This repository showcases a practical application of data science in the Retail Industry using Multiple Linear Regression to derive valuable insights.
Included is a Case Study along with the corresponding source files (".xlsx") and code (".ipynb").

* CASE STUDY:
Utilizing transactional data from an event of a previous year, the case study addresses the following points:

  - Strategies for increasing sales in the category.
  - Weight analysis of each variable on sales.
  - Identification of variables requiring more emphasis.
  - Methods for predicting sales.
    
* INSIGHTS AFTER LINEAR REGRESSION:

Features	Weights
0	ANTIGDAD USUARIO (MESES) PROMEDIO	-0.06
1	SEMANA	-0.69
2	log_minses	6.39
3	CANAL DE COMPRA (MODA)_APP	0.17
4	MIEMBRO APP CLIENTEFIEL (MODA)_NO	0.31
5	ITEM DESC_CONS 1	-0.46
6	ITEM DESC_CONS 1 BDLE	-0.89
7	ITEM DESC_CONS 1 SLIM	0.82
8	ITEM DESC_CONS 2 BDLE	-0.47
9	ITEM DESC_CONS 2 SLIM	0.38
10	ITEM DESC_CONS 3	-0.28
11	ITEM DESC_CONS 3 BDLE	0.21
12	ITEM DESC_CONS 3 SLIM	-0.14
13	TIPO DE PAGO (MODA)_CREDITO	-0.88
Bias / Intercept : 22.62

> Interpretation of Weights:
  - Variables around 0 means close to no weight in our sales,
  - Neative variables mean the more that variable goes by our probability of sell decreases.
  - A positive value indicates the more that variable goes by our probability of sell increases.
  - We shouldn't focus that much on our "Canal de Compra_app", "Antiguedad(meses) promedio", "item desc_cons 3 slim".

> The Negatives:
- The more weeks go by our sales decrese. So we better capitalize on having better promos and agressive strategies in the first weeks.
- Why are our clients not using credit?, we don't have that much credit options as out competitors? this can be risky.
- The items Console 1 Bundle is likely to not be sold, is the category manager ok with this?. Are the competitors giving better price options?. Maybe better taxonomy/ keywords may improve our sales. 

> The Positives:
- The more minutes go by, our chances to sale increases. Let's capitalize in giving good crosselling and upselling options.
- Our items console 1 slim and console 2 slim are likely to be sold. Which means:
      - these items were key in the last event
      - are we having the same promotions than last year?
      -  what promos were used?
      -  Let's check what we did with these items the last time in terms of taxonomy and keywords.

> The Linear Regression Ecuation:
  Yhat = B0 + B1 X1 + Bn Xn
  yhat = 22.62 + (8*.06) + (3*.069) + (3.4*6.39) + (1*0.17) + (1*0.46)
- How to use it?,
 Suppose we want to predict sales for a user with an average of 8 months as a member, buying "Console 1" in week 3 of the event,
 with around 30 minutes in session via the App.
 Based on the linear regression equation, we expect to sell 46 pieces with a variability of 5 pieces, which means approximately between 41 and 51 pieces.


NOTE: Check the code for more info about how I came into this conclussion.
