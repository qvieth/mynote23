# thesis
3 points:
I want report our team  and proposal:
We did contact the data provider and exchange information, we are ready to buy it
but before that i want to propose a new method, and make clear some idea:

As what i'm understanding that original paper trying to use Tail risk dependent structure analysis to model the dependence structure between variables in term of time series data, here their variables of interest were the indexes
the problem with using index is that calculating itselves is a complex method and the part we are facing problems are using market capitalization weighted average and share ratio divisor.

In the old way of calculating the index, we would need to manually divide the new share ratio every time there is a new listing or delisting in the market. Considering the current number of stocks being processed, which is approximately 400 companies,which still didn't count the delisted company. As for our current research knowledge we're still having no way how to find out the missing data for the delisted company. Therefore the process of calculating stock index would be too hard, even if we try to skip some process, the index computed by ourselves is still faulty and has its own limitation. So I propose an alternative approach for replace index using price simple weighted price return percentage.
 
Price Return = (Closing Price - Beginning Price) / Beginning Price * 100
Then we aggregate the price return using equal weighted average.

Price returns can still capture the price movement and volatility of the stock, which may be relevant for tail risk dependent structure analysis. And also it won't be affected by the stock split as in such event ,the adjustment typically affects both the adjusted opening price and the adjusted closing price of a stock. for example:
Day 1: company A | opening price: 100 | closing price: 120
Day 2: company A do 10-1 stock split | opening price: 11 closing price 11.3 |

If we do the price return in both date the price return for day 1 will be 20% while day 2 27%
in my old way of calculate the percentage of change, which you pointed out it would be wrong in the event of stock split as i did the subtract from day 2 closing price and day 1 closing price : 11.3 - 120
so a small and irrelevant question to what i'm proposing: if we still need market capitalization, can i use the new formular for the percentage of change and proceed to calculate the marketcap that old way?

as long as we carefully consider and describe the implications and limitations of using price returns alone. the end result may still valuable to the research community.

some advantage of this approach are: simplicty and feasibility, representativeness, data availability, time efficiency, the best thing for me is originality
its limitation: may not be a as robust as stock index for the representativeness.

I believe that using price return percentage as a weighting scheme for industry index calculation in the Vietnam stock market can offer advantages mentioned above despite its limitation. I hope to receive your advice and approval to proceed with this alternative approach for my thesis research dear professor.

## - we calculate marketcapitalization ourselves again but using my modified formula


 
 
 

Advantages of the Proposed Approach:

Simplicity and Feasibility: The proposed approach using price return percentage is simpler and more feasible compared to the original method of using market capitalization-based indexes, as it does not require additional data and complex calculations.
Representativeness: Price return percentage provides a comprehensive representation of industry performance, without biases towards larger or more established companies. This can give a meaningful measure of the overall dynamics of the industry.
Data Availability: Price return percentage data is typically available for a longer historical period, including for newer companies, addressing the issue of missing data that may arise with market capitalization-based indexes.
Time and Resource Efficiency: The proposed approach eliminates the cumbersome process of manually updating the index for new listings or delistings, which can be time-consuming and labor-intensive, especially with a large number of stocks to process (e.g., approximately 400 companies).
Originality and Innovation: The proposed approach demonstrates originality and innovation in research, showcasing critical thinking and novel solutions to research challenges.
Conclusion:

## variables
- propse a new method:
- tail risk dependent structure:
  - price return
  - price weighting


In our current way of calculating the index, we will have to divide the new share ratio "every time" their is new "listing or delisting" on the market, this way have to be done by finding out which new company have delisted or listed. consider the current number of stock we processing is about 400 companies. doing the dividing way will be too hard and time consuming.





VAR MODEL
11 real economy index and 1 fintech index

- In a VAR (Vector Autoregression) model, the variables are classified as either endogenous or exogenous.
- Endogenous variables(dependant variable), the variables that are being modeled and are affected by other variables in the system: here in our reserach it's the 11 real economy index
- Exogenous variables(independant variable), on the other hand, are variables that are not explained by the model and are assumed to influence the endogenous variables, but not be influenced by them. fintech index will be the exogenous variable in this case
- To estimate the VAR model, we also need to determine the appropriate lag order. One common method for selecting the optimal lag order is to compare the Akaike Information Criterion (AIC) and Bayesian Information Criterion (BIC) values for different lag orders. We estimated VAR models with varying lag orders ranging from 1 to 10, and computed the AIC and BIC values for each model. We then compared the AIC and BIC values to determine the optimal lag order that balances the goodness-of-fit and complexity of the model. The lag order with the lowest AIC and BIC values was selected as the optimal one for our VAR model.
- analyze result

GRANGER CAUSALITY TEST
The Granger causality test was used to investigate the direction and strength of causality between the fintech index and the 11 real economy indices, providing important insights into the potential spillover effects of fintech on the real economy.
To test for Granger causality between the fintech index and the 11 real economy indices, the following steps were carried out:

- The null hypothesis was selected based on the research question. In this case, the null hypothesis was that there is no Granger causality from the fintech index to any of the 11 real economy indices.
- An F-test of the null hypothesis was conducted using the lagged values of the variables in the VAR model. The VAR model included lagged values of all variables, including the fintech index and each of the 11 real economy indices.
- The F-test results were used to determine whether to reject or fail to reject the null hypothesis. If the p-value of the F-test was less than the chosen significance level (e.g., 0.05), the null hypothesis was rejected, indicating the presence of Granger causality from the fintech index to at least one of the 11 real economy indices.




## - methodology

- var, 3.2 garch, 3.5 covar model
-

### - var

Vector autoregression (VAR) is a statistical model used to capture the relationship between multiple quantities as they change over time. VAR is a type of stochastic process model. VAR models generalize the single-variable (univariate) autoregressive model by allowing for multivariate time series.

Like the autoregressive model, each variable has an equation modelling its evolution over time. This equation includes the variable's lagged (past) values, the lagged values of the other variables in the model, and an error term. VAR models do not require as much knowledge about the forces influencing a variable as do structural models with simultaneous equations. The only prior knowledge required is a list of variables which can be hypothesized to affect each other over time.

### granger causality test

As this paper investigate whether fintech(X) is useful in forcasting real economy(Y), it use Granger causality test to judge the promotion between one time series (fintech) and another(real economy).

A time series X is said to Granger-cause Y if it can be shown, usually through a series of t-tests and F-tests on lagged values of X (and with lagged values of Y also included), that those X values provide statistically significant information about future values of Y.

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

### - 3.2 garch

Generalized AutoRegressive Conditional Heteroskedasticity (GARCH) is a statistical model used in analyzing time-series data where the variance error is believed to be serially autocorrelated. GARCH models assume that the variance of the error term follows an autoregressive moving average process.

GARCH (p, q) model (where p is the order of the GARCH terms σ^2
and q is the order of the ARCH terms ϵ^2
) is a model which ϵ*t , the error terms, can be split into a stochastic piece z_t
and a time-dependent standard deviation σ_t characterizing the typical size of the terms so that ϵ_t = σ_t\*z_t
. The random variable z t is a strong white noise process while σ^2_t
is an ARMA process, i.e., σ^2_t = α_0 + ∑^q*(i = 1)α*i\*ϵ^2*(t−i)+∑^p*(i=1)β_i σ^2*(t−i)

### covar model

Karimalis et al. and Jiang et al. mentioned that given time
series X_A, X_B, the joint density function f(xA , xB ), the edge density function
f(xA ) and f(xB ), and the copula connection function between two nodes c, then the
conditional density function of time series X is

formula (11)

The joint distribution of the return series of the Fintech index and various real economy can be obtained using r-vine copula model. Later systematic risk between Fintech and industries will be measured based on the obtained joint distribution. the specific method are as follow

```latex
CoVaR^(A|B)_(alpha) = F^(A|B)_(1)*(alpha|VaR^beta_alpha), then solve the equation
formula (12)
```

the obtained x_A is the desired CoVar^(A|B)\_alpha
addtionally, deltaCoVaR^(A|B)\_alpha indicates the change of VaR in market A when market B is in extreme risk condition to is useful to improve the measurement of the risk spillover effect between A and B, . the specific expression is
deltaCoVaR^(A|B)\_alpha = CoVar(A|B)\_alpha - VaR^A_alpha

To remove the influence of dimension, it is necessary to standardize DCoVaR↵ to
obtain the accurate value of spillover risk more clearly and accurately, as follows.

formula(14)

### r-vine copula

As discussed by Hernandez et al. [39] and He and Li [40], the idea of the vine–copula
is to decompose the traditional multivariate copula into multiple pair copulas in the form
of vine graphic structure, making the model fit more simple and feasible, improving the
fitting accuracy, and making the model dispose of the limitation of only one copula function
in describing the dependent structure.
Before giving the definition of the vine, the tree is defined as a graph in which every
two nodes are connected by different edges. Based on this, the vine can be called a vine on
an n-dimensional variable when the following conditions are satisfied:
Condition 1: Vine = (T1 , . . . , Tm ).
Condition 2: T1 is a tree with N1 nodes and E1 edges on the vine structure. N1 = {1, 2, . . . , n}
is all nodes on the tree. The connection between nodes is the edge, and E1 represents
the set of all edges on the first layer tree.
Condition 3: Ti (i = 2, . . . , m) represents the ith tree on the vine except T1 , and N1 is the
node on T1 , which meets Ni 2 N1 [ E1 [ E2 [ E3 [ · · · [ Ei 1 .
The vine structure of an n-dimensional variable consists of n 1 trees. The ith tree
has n i + 1 nodes and n i edges, and the edge of one tree is used as a new node in the
next tree. Using the idea of rattan structure, high dimensional Copula functions can be
decomposed in different two-dimensional Copula to form different correlation structures,
in which R-vine is described as the actual dependency state between variables.
The R-vine structure of an n-dimensional variable can be composed of n 1 tree Ti
(i = 1, . . . , n 1). Assuming that there are n i + 1 nodes and n i edges on T1 , for the
remaining n 2 trees, the edges on Ti are transformed into new nodes of Ti+1 .

- The probability probabilitydensity densityfunction function of of the the R-vine R-vine Copula is

formula(9)

whereEEi iisisthe
theset
setof
alledges
edges on
on each
each layer
layer of
of the tree, e = jሺሻǡ
(e), k
(e)|D(e) is
edges,
edges,j(e),
j(e),k(e)
k(e)are
arethe
thecondition
conditionnodes
nodesat
atboth
both ends
ends of
of the
the edge,
edge, D(e) is the condition set,
and c୨ሺୣሻǡ୩ሺୣሻȁୈሺୣሻ
theconnection
connectionfunction
functionbetween
betweenthe
the two
two nodes.
nodes.
and
j(e),k(e)|D(eሺήǡήሻ
) (·, ·)isisthe
Figure11shows
showsan
anexample
exampleof
ofaasix-dimensional
six-dimensional R-vine
R-vine Copula
Copula tree
Figure
tree structure.
structure. In
In this
this
study,
the
R-vine
Copula
model
is
used
to
describe
the
dynamic
dependency
structure
study, the R-vine Copula model is used to describe the dynamic dependency structure
betweenindustries
industriesin
inthe
thereal
realeconomy
economy and
and Fintech.
Fintech. The
The steps
between
steps are
are as
as follows

- co phieu IT, consumer staples, financial
  - DGW, FPT, CMG, ELC
- create a graph, write words
- literature review
- big goals, mini goal
- AI
- crypto

- scribbr: how to structure your thesis https://www.youtube.com/watch?v=hxSD8VqgS6o

- https://dissertationtop.com/finance-dissertation-topics-examples/
- https://www.quora.com/What-is-a-list-of-20-thesis-topics-in-finance
- https://www.thoughtfulminds.org/top-100-finance-dissertation-topics-trending-in-the-year-2021/
- accounting

---

- Examples of the questions to ask during your first meeting with a potential supervisor:
  - How promising do you find my research topic?
  - Are there particular directions you think I should explore in developing a research question?
  - How often do you like to meet with advisees?
  - How many drafts are you willing to read? How many days do you require to read a draft?
  - [ ] What is your preferred method of maintaining regular contact?
  - [ ] Do you have any books or journal articles that you think I need to read before our next meeting?

what is fintech

how it gonna relate to ... economics, finance

what problem does it solve

what can we solve

- https://www.researchgate.net/publication/359056397_Fintech_and_Financial_Health_in_Vietnam_during_the_COVID-19_Pandemic_In-Depth_Descriptive_Analysis

  - This study investigates financial literacy, fintech adoption, and the impact of the COVID-19 crisis on the financial health of consumers in Vietnam
  - are found to be significantly correlated with fintech adoption in Vietnam
    - Perceived ease of use,
    - perceived usefulness,
    - trust, brand image,
    - government support,
    - user innovativeness,
    - and attitude
  - while financial literacy was found to be not significantly correlated with fintech adoption.
  - financial literacy
  - fintech adoption

- financial literacy
- financial health

- attend academic conference
- sample :
  broader range, after some reserach, narrow down, present in our next meeting

## fintech

- [youtube - More Recent Academic Fintech Research - Fintech and the New Financial Landscape](https://www.youtube.com/watch?v=vSrlD8OPLRI)
- https://www.youtube.com/results?search_query=fintech+research
