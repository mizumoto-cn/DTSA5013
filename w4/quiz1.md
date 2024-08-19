# Week 4 Quiz 1

## Quiz 1

![Question 1](./img/11.png)
![Question 2](./img/12.png)
![Question 3](./img/13.png)
![Question 4](./img/14.png)

以下是每道题目的整理和解答，包括不正确的多选选项的解答：

### 1. **Question 1**

**When compared to some common machine learning techniques, such as random forests, generalized additive models have the advantage of clearly showing the contribution of each predictor to the response.**

- **正确答案**: True
- **解答**: 广义加性模型（GAMs）的一个显著优势是，它能够清晰地展示每个预测变量对响应变量的贡献，这是与一些机器学习技术（如随机森林）相比的优势。GAMs 提供了易于解释的模型形式。

### 2. **Question 2**

**Generalized additive models can be thought of as a way to estimate nonlinear relationships between a response and several predictors simultaneously.**

- **正确答案**: True
- **解答**: GAMs 确实可以用于同时估计响应变量与多个预测变量之间的非线性关系。它们允许每个预测变量以平滑函数的形式单独影响响应变量。

### 3. **Question 3**

**Generalized additive models strike a nice balance between the interpretable, yet biased, linear model, and the extremely flexible, “black box” machine learning algorithms.**

- **正确答案**: True
- **解答**: GAMs 在可解释性和灵活性之间取得了良好的平衡。它们比线性模型更灵活，但又不像某些机器学习算法（如神经网络或随机森林）那样难以解释。

### 4. **Question 4**

**Which of the following are additive models?**

- **选项**:
  1. \(f(x_1, x_2) = \pi + \beta_1 e^{x_1} - 5x_2\) - **正确**
  2. \(f(x_1, x_2, x_3) = \beta_0 + \beta_1 \frac{e^{x_1}}{x_3} - \beta_2 5x_2\) - **错误**

3. \(f(x_1, x_2, x_3) = \beta_0 + \beta_1 \log(x_1 x_3^{\beta_2}) - \beta_2 5x_3\) - **正确** $log(x1 * x3^beta2) = log(x1) + beta2 * log(x3)$
4. \(f(x_1, x_2, x_3) = \beta_0 x_1 + \beta_1 x_1 + \cos(\pi x_2) + \beta_3 x_2^2 + x_1 x_2 + \sin^2(x_3)\) - **错误**
5. \(f(x_1, x_2, x_3) = \beta_0 x_1 + \beta_1 x_1 + \cos(\pi x_2) + \beta_3 x_2^2 + \sin^2(x_3)\) - **正确**

- **正确答案**: 选项 1 3 和 5
- **解答**: 加性模型是指响应变量是预测变量的加性组合，不允许预测变量之间的乘积项或复杂的非线性交互项。选项 1 和 5 是符合加性模型定义的，而选项 2和 4 含有非加性成分或交互项。

### 5. **Question 5**

**Additive models will work well when strong interactions between predictors exist.**

- **正确答案**: False
- **解答**: 加性模型假设每个预测变量对响应变量的影响是独立的。因此，当存在强交互效应时，加性模型可能无法很好地捕捉这些交互效应。

### 6. **Question 6**

**Generalized additive models have trouble incorporating non-normal (e.g., binomial) responses.**

- **正确答案**: False
- **解答**: GAMs 可以处理非正态响应变量（例如二项分布或泊松分布）的问题。这是通过使用适当的链接函数和分布族来实现的，因此这道题的答案是错误的。

### 7. **Question 7**

**Generalized additive models are typically more biased than standard linear regression models.**

- **正确答案**: False
- **解答**: GAMs 通常比标准线性回归模型更灵活，可以捕捉到更复杂的非线性关系，因此它们不一定会比线性模型有更高的偏差。这道题的答案是错误的。

### 8. **Question 8**

**Suppose that a response \(y\) is related nonlinearly to a (continuous) predictor \(x_1\), linearly to a (continuous) predictor \(x_2\), and linearly to a three-level factor \(x_3\). Then:**

- **选项**:
  1. For a one-unit increase in \(x_2\), the mean change in \(y\) is approximately 2.81, adjusting for other predictors. - **正确**
  2. This model includes interaction terms. - **错误**
  3. The mean change in \(y\) for one-unit increase in \(x_1\), adjusting for other predictors, depends on the value of \(x_1\). - **正确**
  4. For a one-unit increase in \(x_1\), the mean change in \(y\) is approximately 8.28, adjusting for other predictors. - **错误**

- **正确答案**: 选项 1 和 3
- **解答**:
  - 选项 1 是正确的，因为 \(x_2\) 的系数为 2.81，表示在控制其他预测变量后，\(x_2\) 增加一个单位，\(y\) 的均值增加约 2.81。
  - 选项 2 是错误的，因为模型没有包含交互项。
  - 选项 3 是正确的，因为 \(x_1\) 和 \(y\) 之间的关系是非线性的，意味着 \(x_1\) 对 \(y\) 的影响取决于 \(x_1\) 的具体值。
  - 选项 4 是错误的，因为 8.28 不是 \(x_1\) 增加一个单位时的均值变化，而是平滑函数 \(s(x1)\) 的有效自由度。

### 9. **Question 9**

根据问题中的描述，以及基于你之前提供的模型输出，以下是对每个选项的解答：

1. **For a one-unit increase in \(x_2\), the mean change in \(y\) is approximately 2.81, adjusting for other predictors.**

   - **正确**。模型中的线性项 \(x_2\) 的估计系数是 2.81405，表示在调整其他预测变量后，\(x_2\) 增加一个单位，\(y\) 的均值大约增加 2.81。

2. **This model includes interaction terms.**

   - **错误**。根据提供的模型公式 \(y \sim s(x1) + x2 + x3\)，该模型不包含交互项。模型中只有非线性项（\(s(x1)\)）和线性项（\(x2\) 和 \(x3\)），但没有交互项。

3. **The mean change in \(y\) for one-unit increase in \(x_1\), adjusting for other predictors, depends on the value of \(x_1\).**

   - **正确**。因为 \(x_1\) 是通过平滑函数 \(s(x1)\) 非线性建模的，所以 \(x_1\) 对 \(y\) 的影响取决于 \(x_1\) 的具体值。

4. **For a one-unit increase in \(x_1\), the mean change in \(y\) is approximately 8.28, adjusting for other predictors.**

   - **错误**。虽然 8.28 出现在模型输出中，但它是指平滑函数 \(s(x1)\) 的有效自由度（edf），而不是 \(x_1\) 增加一个单位时 \(y\) 的平均变化量。由于 \(x_1\) 与 \(y\) 的关系是非线性的，因此 \(x_1\) 增加一个单位时 \(y\) 的变化量是动态的，并不恒定。

因此，正确的选项是：

- **For a one-unit increase in \(x_2\), the mean change in \(y\) is approximately 2.81, adjusting for other predictors.**
- **The mean change in \(y\) for one-unit increase in \(x_1\), adjusting for other predictors, depends on the value of \(x_1\).**
