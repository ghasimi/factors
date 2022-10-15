# factors
Summary notes on factors.

## About factors

Factors explain part of the variations in the data, while the unexplained part is attributed to some random events. Formally:

$${R = \beta F + U}$$

$$\begin{bmatrix} 
  r1 \\
  \vdots \\
  rn   
\end{bmatrix} =
\begin{bmatrix} 
  b_{11} & \ldots & b_{1k} \\
  & \ddots & \\
  b_{n1} & \ldots & b_{nk} \\  
\end{bmatrix} 
\begin{bmatrix} 
  f_1 \\
  \vdots \\
  f_k   
\end{bmatrix} + 
\begin{bmatrix} 
  u_1 \\
  \vdots \\
  u_n
\end{bmatrix}$$

Where $R$ is a vector of target variable, $\beta$ is a matrix of factor exposures, $F$ is a vector of factors, and $U$ is a vector of residuals.

From one view, there are three groups of factor models:

1. Macro factors
2. Fundamental factors
3. Statistical factors


## Models

$R$: Excess return, i.e. return in excess of the risk free rate.

$R_m$: Excess return of the market.
__FF__: Fama-French 

Market model: 

${R =\alpha^{J} + {\beta_1}{R_m} + \epsilon}$ 


[Fama-French 3-factor](https://mba.tuck.dartmouth.edu/pages/faculty/ken.french/Data_Library/f-f_factors.html): 

${R =\alpha^{FF} + {\beta_1}{R_m} + {\beta_2}{HML} + {\beta_3}{SMB} + \epsilon}$ 


[Carhart 4-factor](https://en.wikipedia.org/wiki/Carhart_four-factor_model): 

${R =\alpha^{C} + {\beta_1}{R_m} + {\beta_2}{HML} + {\beta_3}{SMB} + {\beta_4}{UMD} + \epsilon}$ 


[Fama-French 5-factor](https://mba.tuck.dartmouth.edu/pages/faculty/ken.french/Data_Library/f-f_5_factors_2x3.html): 

${R =\alpha^{FF} + {\beta_1}{R_m} + {\beta_2}{HML} + {\beta_3}{SMB} + {\beta_4}{RBW} + {\beta_5}{CMA} + \epsilon}$ 

