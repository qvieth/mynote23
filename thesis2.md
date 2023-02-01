# thesis version 2

# dec 18 start

## purpose of the study

- chuyen len motivation
- tai sao dung model, giai quyet gi, bai reserach giai quyet van de gi,

## methodology

- viet cthuc ra thay vi anh
- explain vector Y_t va tat ca variable trong do
- hypothesis 0 va null
- garch(1,1)

# dec 18 end

- purpose of this study
- Fintech innovation has make the operation of the financial industry more efficient. It also advanced the sustainable development of the real economy. In the age of information technology, the growth of financial technology has become greater and and become the core pillar in the financial industry. not only financial technology has cause disruptive changes to the traditional financial mode, it's growth also correlate with financial industry's risk characteristics. Specifically, the innovation of financial products, the change of financing mode and the change of financial business model brought by fintech have greatly promoted the operational efficiency of the financial industry. Excessive innovation in the financial market has led to a significant increase in the complexity of financial products and financial transactions. Financial institutions together with non-financial institutions, have become increasingly close to each other in terms of equity and debt, business cooperation and penetration, forming a complex financial network structure, and the contagion characteristics of the systematic financial risk network have become more and more obvious. Risks from real economy are also transmitted to the financial system. in the age of modern and technology, demands for traditional products has become sluggish domestic and foreign markets has create pressure to enterprises as it remarkably reduced the profitability these enterprises. therefore, to maintain business operations, the high interest loan rate has increased the burden of the real economy, and the long-term “borrowing the new to repay the old” has add to the risks of fintech. Therefore, to analyze the risked spilled by fintech to real economy, we first conduct the Vector Auto Regression and granger causality test to see the interaction between fintech and real economy. Later to deal with the nonlinear relationship and deal with the high-dimensional-dependent structure faced by Copula, this paper establishes a GARCH–Vine–Copula model to study the tail risk and dynamic
  dependency between fintech and industries of the real economy in Vietnam.

- why use the model:
  - literature review of key paper

## var

## granger causality

this paper investigate whether fintech(X) is useful in forecasting real economy(Y) by using Granger causality test. Granger causality is used to judge the promotion between one time series and another. Here, the paper use structural vector auto-regression (SVAR) as principle for time series:

- provided X and Y's past information, variable X is useful to explain Y and considered to be the Granger cause of Y only if the prediction effect of Y is greater than that of Y alone.
- the test results are divided into 4 cases:
  - there is a one-way causal relationship from Y to X
  - there is a one-way causal relationship from X to Y
  - X and Y are cause and effect
  - there is no causal relationship between X and Y

where u1t and u2t are white noise; q and s are the lagging periods.
If the past information of X and Y is included, the prediction effect of variable Y is
better than that of Y alone, that is, variable X is helpful to explain the change of variable Y.
Therefore, variable X is considered to be the Granger cause of variable Y. The test results
are divided into the following four cases: (1) There is a one-way causal relationship from Y
to X; (2) There is a one-way causal relationship from X to Y; (3) X and Y are cause and effect;
(4) There is no causal relationship between X and Y

A time series X is said to Granger-cause Y if it can be shown, usually through a series of t-tests and F-tests on lagged values of X (and with lagged values of Y also included), that those X values provide statistically significant information about future values of Y.

-

## GARCH

## Covar

## R-vine copula model
