# Machine Learning Algorithms

In this project, the objective is to compare the performance of three distinct algorithms on a synthetic training set with the goal of learning a true vector w*. The dataset generation process involves first selecting a weight vector w* from a standard normal distribution and normalizing it to have a Euclidean norm of 1. Subsequently, a training set of size m is generated, consisting of random vectors x_i and binary labels y_i, where the labels are determined by a function incorporating the sigmoid function and a uniform distribution.

The three algorithms to be evaluated are as follows:
1. **Logistic Regression (Algorithm 1):**
   - Utilizes built-in methods for logistic regression.

2. **Gradient Descent (Algorithm 2):**
   - Trains a model of the form \( \sigma(w' \cdot x) \) with respect to square loss, using a custom implementation of gradient descent.
   - The loss function is \( \frac{1}{2}(\sigma(w' \cdot x) - y)^2 \), averaged over the training set.

3. **Stochastic Gradient Descent (Algorithm 3):**
   - Similar to Algorithm 2 but employs stochastic gradient descent.
   - During each iteration, the gradient is calculated at one random point from the training set.

The success measurement involves computing the Euclidean norm of the difference between the true weight vector w* and the output weight vector w' after training. This process is repeated multiple times for each value of m (50, 100, 150, 200, 250), and the results are averaged. The outcomes for all three algorithms are plotted, and the time taken for the entire experiment is recorded for each algorithm and value of m. The comparison aims to provide insights into the effectiveness and efficiency of these algorithms in learning the true vector w* on the synthetic training set.
