[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-718a45dd9cf7e7f842a935f5ebbe5719a5e09af4491e668f4dbf3b35d5cca122.svg)](https://classroom.github.com/online_ide?assignment_repo_id=12217343&assignment_repo_type=AssignmentRepo)
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

---------------------------------------------------------------------------------------------------------------------
My response

$T(n) \in O(f(n)) \iff \exists c, n_0: T(n) \leq c \cdot f(n) \forall n \geq n_0$
$T(n) \in O(\log_{2} n)$ if and only if $\exists c, n_0: T(n) \leq c(\log_{2} n) \forall n \geq n_0$
$T(n) \in O(\log_{5} n) \iff \exists c, n_0: T(n) \leq c(\log_{5} n) \forall n \geq n_0$

Then using the property $(\log_{b} a) = (\frac{1}{(\log_{k} b)})(\log_{k} a)$ where k is any base, we can set up the following;

$T(n) \leq c(\frac{1}{(\log_{5} 2)})(\log_{5} n)$, $T(n) \leq c(\frac{1}{(\log_{2} 5)})(\log_{2} n)$

We can now let $c(\frac{1}{(\log_{5} 2)})$ and $c(\frac{1}{(\log_{2} 5)})$ = g and h respectively, where g and h are both constants.

We are left with;

$T(n) \leq g(\log_{5} n)$, $T(n) \leq h(\log_{2} n)$

Because the definition of $O$ says we can ignore constants;

$T(n) \in O(\log_{5} n)$, $T(n) \in O(\log_{2} n)$

Then

$\forall T(n) \in O(log_{3} n) \implies T(n) \in (\log_{3} n)$

and

$\forall T(n) \in O(log_{5} n) \implies T(n) \in (\log_{3} n)$

$\therefore O(\log_{3} n) = O(log_{5} n)$
