The sigmoid function $\sigma(x)$ is defined as:

$sigma(x) = \frac{1}{1 + e^{-x}}$

Now, let's compute its derivative step by step:

**Step 1: Apply the Quotient Rule**

The derivative of a quotient in this case, \(1\) divided by $(1 + e^{-x})$ is given by the quotient rule, which states:

$\left( \frac{f}{g} \right)' = \frac{f'g - fg'}{g^2}$

Here, f(x) = 1 and $g(x) = 1 + e^{-x}$.

**Step 2: Compute \(f'(x)\) and \(g'(x)\)**

Since f(x) is a constant, its derivative f'(x) = 0.

To find g'(x), note that $g(x) = 1 + e^{-x}$. The derivative of a constant is 0, and the derivative of $e^{-x}$ with respect to x is $-e^{-x}$. Therefore:

$g'(x) = 0 - e^{-x} = -e^{-x}$

**Step 3: Apply the Derivative Values to the Quotient Rule**

Using the quotient rule from Step 1, with our computed derivatives from Step 2, we have:

$\sigma'(x) = \frac{0 \cdot (1 + e^{-x}) - 1 \cdot (-e^{-x})}{(1 + e^{-x})^2}$

**Step 4: Simplify the Expression**

Simplifying the numerator:

$\sigma'(x) = \frac{e^{-x}}{(1 + e^{-x})^2}$

**Step 5: Factor Out the Common Term**

The term $e^{-x}$ is common in both the numerator and the denominator, and the denominator can be expressed as $(1 + e^{-x})$ cdot $(1 + e^{-x})$. Factoring out $e^{-x}$ in the numerator gives us a term that looks like the original sigmoid function:

$\sigma'(x) = \frac{e^{-x}}{1 + e^{-x}} \cdot \frac{1}{1 + e^{-x}} = \sigma(x) \cdot \frac{1}{1 + e^{-x}}$

**Step 6: Recognize the Sigmoid Function in the Expression**

Notice that $\frac{1}{1 + e^{-x}}$ is $\sigma(x)$, and therefore:

$\sigma'(x) = \sigma(x) \cdot (1 - \sigma(x))$

Here's why: Recall that $\sigma(x) = \frac{1}{1 + e^{-x}}$, so $1 - \sigma(x)$ can be written as $1 - \frac{1}{1 + e^{-x}} = \frac{1 + e^{-x} - 1}{1 + e^{-x}} = \frac{e^{-x}}{1 + e^{-x}}$, which, when multiplied by $\sigma(x)$, gives us the above result.

**Final Derivative:**

The final derivative of the sigmoid function is thus:

$\sigma'(x) = \sigma(x) \cdot (1 - \sigma(x))$

This is a very useful result because it expresses the derivative of the sigmoid in terms of the sigmoid function itself. This property is particularly handy when computing gradients during the training of neural networks with sigmoid activation functions, as it simplifies the implementation and computation.