# factors
Summary notes on factors.

## Factor model

Factors explain part of the variations in the data, while the unexplained part is attributed to some random events (i.e. noise). Formally:

$${ \boldsymbol{r = BF + u}}$$

$${\boldsymbol{\bar{r} = B\mu }}$$

$${\boldsymbol{\sigma_{r}^2 = B \Sigma B' + D }}$$


Where

$$\boldsymbol{B} \text{: Matrix of factor exposures} $$

$$\boldsymbol{F} \text{: Vector of factors} $$

$$\boldsymbol{u} \text{: Vector of noise (unexplained) } $$


And

$$\boldsymbol{\mu} \text{: Vector of expected values of factors} $$

$$\boldsymbol{\Sigma} \text{: Covariance matrix of factors}$$

$$\boldsymbol{D} \text{: Diagonal matrix of unexplained variances}$$



Factor-based portfolio:

$${ r_p = \boldsymbol{w' r} }$$

$$
\bar{r_p} = \boldsymbol{w' B \mu}
$$

$$
\sigma_{r_p}^2 = \boldsymbol{w' B \Sigma B' w + w'Dw}
$$


Where $\boldsymbol{w}$ is the vector of weights. Expanded form with __n__ assets and __k__ factors:

$$\begin{bmatrix} 
  r_1 \\
  \vdots \\
  r_n   
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

$$
r_p = 
\begin{bmatrix} w_1 & \ldots & w_n \end{bmatrix}
\begin{bmatrix} 
  r_1 \\
  \vdots \\
  r_n   
\end{bmatrix}
$$


## The Three Types of Factor Models 

The literature often refers to the following three types of factor models:

1. __Macro__: Estimates _exposures_ $B$ by regressing the target variables $r$ on the time-series of known factors $F$. e.g. Estimating sensetivity of stocks to macroeconomic factors such as inflation or unemployment rate.

2. __Fundamental__: Estimates _factors_ $F$ using the cross-sectional regression of target variables $r$ on known exposures $B$. The known exposures are typically the attributes of the target variables. e.g. Size of companies (small, medium, and large cap) could be regarded as a factor. In this case, the market capitalization of each company is its _exposure_ to the size factor, while the factor needs to be estimated, by regressing the stock returns on the market cap data for a certain period.  

3. __Statistical__: Estimates both factors $F$ and exposures $B$ simultaneously, using statistical algorithms. 


## Classic factor models


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

