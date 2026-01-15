
## The classical (frequentist) way


## The Bayesian way - thinking in probabilities
$P(parameters | data)$ - posterior - how likely each parameter value is after seeing a data
$P (data | parameters) $ - likelihood - how well the model (with this parameters) fits the data
$P(data)$ - prior - initial guess about the parameters value before looking at the data


## Example - guessing a cake recipe


Imagine you taste a cake:

- **prior**: before tasting I think "most cakes have 100-300 g sugar" (I give higher probability to that range)
- **Likelihood**: I taste the cake - it's very sweet. That means the likelihood of the data that cake is low sugar (100 g) is low, and is high for the large amount of sugar (300g)
- **posterior** - Mulptiply both - the final distribution peaks maybe near 250g sugar.


The **prior** only biases the result if the data are weak - low statistics, large uncertanties. If data are strong, the likelihood completely dominates and overwrites the prior.

Thats intentional - Bayesian explicitly combines the knowledge and evidence.

**Degeneracy** of parameters - if tow parameters can form different combination that lead to the same model prediction, so the data can not tell them apart clearly.

