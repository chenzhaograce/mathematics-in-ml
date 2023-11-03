
**Probability of a Single Data Point**:   
logistic regression model is:   
$P_w(y_i|x_i) = \sigma(w^T x_i)^{y_i} \times (1 - \sigma(w^T x_i))^{(1-y_i)}$

- When y_i = 1, it gives $\sigma(w^T x_i)$
- When y_i = 0, it gives $1 - \sigma(w^T x_i)$

**Likelihood for the Entire Dataset**:

$L(w) = \prod_{i=1}^{n} \sigma(w^T x_i)^{y_i} \times (1 - \sigma(w^T x_i))^{(1-y_i)}$

**Log-Likelihood**:

$\ell(w) = \sum_{i=1}^{n} [ y_i \log(\sigma(w^T x_i)) + (1 - y_i) \log(1 - \sigma(w^T x_i)) ]$

**Maximization vs. Minimization**:

$\mathcal{L}(w) = -\frac{1}{n} \sum_{i=1}^{n} [ y_i \log(\sigma(w^T x_i)) + (1 - y_i) \log(1 - \sigma(w^T x_i)]$   
This is precisely the formula you provided in the slide, separated into cases where \(y_i = 1\) and \(y_i = 0\).

By minimizing this negative log-likelihood, we're effectively maximizing the likelihood of observing the given training data under our model. 