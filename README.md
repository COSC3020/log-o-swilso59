[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-718a45dd9cf7e7f842a935f5ebbe5719a5e09af4491e668f4dbf3b35d5cca122.svg)](https://classroom.github.com/online_ide?assignment_repo_id=12578174&assignment_repo_type=AssignmentRepo)
# Asymptotic Equivalences

In the lectures, we said that logarithms with different bases don't affect the
asymptotic complexity of an algorithm. Prove that $O(\log_{2} n)$ is the same as
$O(\log_{5} n)$. Use the mathematical definition of $O$ -- do a formal proof,
not just the intuition.

I have started with the formal definition of $O$ below. Add your answer to this
markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

$T(n) \in O(f(n)) \iff \exists c, n_0: T(n) \leq c \cdot f(n) \forall n \geq n_0$

To prove this, we will use the change of base formula for logarithms:

$\log_2(n) = \frac{\log_5(n)}{\log_5(2)}$

Now, substituting this into the inequality, we get:

$c_1 \cdot \frac{\log_5(n)}{\log_5(2)} \leq \log_5(n) \leq c_2 \cdot \frac{\log_5(n)}{\log_5(2)}$

Multiplying each term by $\log_5(2)$ (keeping in mind that $\log_5(2)$ is positive), we obtain:

$c_1 \cdot \log_5(n) \leq \log_5(n) \leq c_2 \cdot \log_5(n)$

Now, let $c_1 = 1$ and $c_2 = \log_5(2)$. This gives us:

$\log_5(n) \leq \log_5(n) \leq \log_5(2) \cdot \log_5(n)$

Since these inequalities hold for any $n$ greater than or equal to some $n_0$, we have shown that $O(\log_2(n))$ is indeed equivalent to $O(\log_5(n))$. Therefore, when analyzing the asymptotic complexity of algorithms, the choice of base does not affect the big O notation or the overall growth rate of the algorithm.
