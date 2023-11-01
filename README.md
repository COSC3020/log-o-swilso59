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

We want to show that $O(\log_2(n))$ is equivalent to $O(\log_5(n))$ up to a constant factor, which means there exists a constant $c$ such that:

\[
\log_2(n) = c \cdot \log_5(n)
\]

To prove this, we will use the change of base formula for logarithms:

\[
\log_2(n) = \frac{\log_5(n)}{\log_5(2)}
\]

Now, let's set $c = \frac{1}{\log_5(2)}$, so we have:

\[
c = \frac{1}{\log_5(2)}
\]

Then, we can rewrite $\log_2(n)$ as:

\[
\log_2(n) = \frac{1}{\log_5(2)} \cdot \log_5(n)
\]

Now, if we multiply both sides by $\log_5(2)$, we get:

\[
\log_2(n) \cdot \log_5(2) = \log_5(n)
\]

Since $c$ is a constant $\left(\frac{1}{\log_5(2)}\right)$, we have shown that:

\[
\log_2(n) = c \cdot \log_5(n)
\]

This proves that $O(\log_2(n))$ is equivalent to $O(\log_5(n))$ up to a constant factor. Therefore, when analyzing the asymptotic complexity of algorithms, you can use either base 2 or base 5 logarithms interchangeably, and the choice of base does not affect the big O notation or the overall growth rate of the algorithm.
