Document 테스트
================
Issac Lee(이삭)
2016-12-17

한글은 지원이 되는가
====================

How to input math eqaution in this document
-------------------------------------------

Captain John $\\hat{\\lambda}=1.02$ Sheridan: You know, I just had a thought. You've been back and forth to your world so many
$$
\\int\_{0}^{12}\\frac{x\_{d}^{2}}{2}+y^{2}ds
$$

Consider the optimization problem

$$
\\begin{array}{cc}
minimize & f\_{0}\\left(x\_{1},x\_{2}\\right)\\\\
subject\\,to & 2x\_{1}+x\_{2}\\geq1\\\\
 & x\_{1}+3x\_{2}\\geq1\\\\
 & x\_{1}\\geq0,\\,x\_{2}\\geq0.
\\end{array}
$$
 For each of the following objective functions, find a solution of the problem. \#item dd
\begin{enumerate}
\item $f_{0}\left(x_{1},x_{2}\right)=x_{1}+x_{2}$
\item $f_{0}\left(x_{1},x_{2}\right)=-x_{1}-x_{2}$
\item $f_{0}\left(x_{1},x_{2}\right)=x_{1}$
\item $f_{0}\left(x_{1},x_{2}\right)=max\left\{ x_{1},x_{2}\right\} $
\item $f_{0}\left(x_{1},x_{2}\right)=x_{1}^{2}+9x_{2}^{2}$
\end{enumerate}\begin{description}
\item [{Sol.}] First, let us figure out the feasible set.
\end{description}\begin{center}
\includegraphics[width=6cm,height=6cm]{figure/Rplot}
\par\end{center}
times since you got here. How do I know you're the same Vorlon? Inside that encounter suit you could be anyone. Kosh Naranek: I have *always* been here. Captain John Sheridan: Oh, yeah? You said that about me too. Kosh Naranek: Yes. \[starts to walk away\] Captain John Sheridan: I really *hate* it when you do that. Kosh Naranek: \[turns around\] Good! Delenn: I am Grey. I stand between the candle and the star. We are Grey. We stand between the darkness and the light.

Lt. Corwin: Do we trust no-one then? Cmdr. Susan Ivanova: No, trust Ivanova, trust yourself, anybody else, shoot'em. Ta'Lon: Congratulations citizen G'Kar. You are now a religious icon. Susan Ivanova: So the next time we find out where the Shadows plan to strike, we can mine the area, and as soon as they come out of hyperspace... Citizen G'Kar: Then, as you so concisely say, Boom!

\subsection*{Problem 1. A simple problem}
Consider the optimization problem

$$
\\begin{array}{cc}
minimize & f\_{0}\\left(x\_{1},x\_{2}\\right)\\\\
subject\\,to & 2x\_{1}+x\_{2}\\geq1\\\\
 & x\_{1}+3x\_{2}\\geq1\\\\
 & x\_{1}\\geq0,\\,x\_{2}\\geq0.
\\end{array}
$$
 For each of the following objective functions, find a solution of the problem.
\begin{enumerate}
\item $f_{0}\left(x_{1},x_{2}\right)=x_{1}+x_{2}$
\item $f_{0}\left(x_{1},x_{2}\right)=-x_{1}-x_{2}$
\item $f_{0}\left(x_{1},x_{2}\right)=x_{1}$
\item $f_{0}\left(x_{1},x_{2}\right)=max\left\{ x_{1},x_{2}\right\} $
\item $f_{0}\left(x_{1},x_{2}\right)=x_{1}^{2}+9x_{2}^{2}$
\end{enumerate}\begin{description}
\item [{Sol.}] First, let us figure out the feasible set.
\end{description}\begin{center}
\includegraphics[width=6cm,height=6cm]{figure/Rplot}
\par\end{center}
The point where the two lines are crossed is $\\left(\\frac{2}{5},\\frac{1}{5}\\right)$.
\begin{enumerate}
\item When the objective function $f_{0}\left(x_{1},x_{2}\right)=x_{1}+x_{2}$,
the optimal is $\left(\frac{2}{5},\frac{1}{5}\right)$, is the only
point crossed with $\frac{3}{5}=x_{1}+x_{2}$, and optimal value $p^{\star}=\frac{3}{5}$. 
\begin{center}
\includegraphics[width=6cm,height=6cm]{figure/Rplot01}
\par\end{center}
\item When the objective function $f_{0}\left(x_{1},x_{2}\right)=-x_{1}-x_{2}$,
the problem is unbounded below since the objective function can have
$-\infty$.
\item When the objective function $f_{0}\left(x_{1},x_{2}\right)=x_{1}$,
there are infinite number of optimal points. The set of optimal points
$X_{opt}=\left\{ x\in\mathbb{R}^{2}:x_{1}=0,x_{2}\geq1\right\} $
and the optimal value is zero.
\item When the objective function $f_{0}\left(x_{1},x_{2}\right)=max\left\{ x_{1},x_{2}\right\} $,
the optimal point can be found by finding the point where the line
$x_{1}=x_{2}$ and $2x_{1}+x_{2}=1$ are crossed. $\left(\frac{1}{3},\frac{1}{3}\right)$
is the optimal point.
\begin{center}
\includegraphics[width=6cm,height=6cm]{figure/Rplot02}
\par\end{center}
\item When the objective function $f_{0}\left(x_{1},x_{2}\right)=x_{1}^{2}+9x_{2}^{2}$,
the point $\left(\frac{1}{2},\frac{1}{6}\right)$ is optimal. This
can be calculated by using the fact the gradient vector of $f_{0}$
should be equal to the normal vector of its tangent line. Thus,
\[
\nabla f_{0}\left(x_{1},x_{2}\right)=\left[\begin{array}{c}
2x_{1}\\
18x_{2}
\end{array}\right]
\]
is equal to $\left(1,3\right)$, which is the normal vector of $x_{1}+3x_{2}=1$.
\begin{center}
\includegraphics[width=6cm,height=6cm]{figure/Rplot03}
\par\end{center}
\end{enumerate}
\subsection*{Problem 2. Relaxation of Boolean LP}
In a Boolean linear program, the variable *x* is constrained to have components equal to zero or one:

$$
\\begin{array}{cc}
minimize & c^{T}x\\\\
subject\\,to & Ax\\preceq b\\\\
 & x\_{i}\\in\\left\\{ 0,1\\right\\} ,\\,i=1,...,n.
\\end{array}
$$
 In general, such problems are very difficult to solve, even though the feasible set is finite (containing at most 2<sup>*n*</sup> points). In a general method called relaxation, the constraint that be zero or one is replaced with the linear inequalities :
$$
\\begin{array}{cc}
minimize & c^{T}x\\\\
subject\\,to & Ax\\preceq b\\\\
 & 0\\leq x\_{i}\\leq1,\\,i=1,...,n.
\\end{array}
$$
 We refer to this problem as the LP relaxation of the Boolean LP. The LP relaxation is far easier to solve than the original Boolean LP.
\begin{enumerate}
\item Show that the optimal value of the LP relaxation is a lower bound
on the optimal value of the Boolean LP. What can you say about the
Boolean LP if the LP relaxation is infeasible?
\item It sometimes happens that the LP relaxation has a solution with $x_{i}\in\left\{ 0,1\right\} $.
What can you say in this case?
\end{enumerate}\begin{description}
\item [{Sol.}]~
\begin{enumerate}
\item The optimal value of the LP relaxation $p_{rlx}^{\star}$ is a lower
bound on the optimal value of the Boolean LP, $p^{\star}$. The optimal
point of the Boolean LP, $x$, satisfies,
\[
f_{0}\left(x\right)=c^{T}x=\sum_{i=1}^{n}c_{i}I_{\left\{ x_{i}=1\right\} }=p^{\star}.
\]
However, since the feasible set of the LP relaxation includes the
optimal point of the Boolean LP, $x$, the optimal value of the LP
relaxation $p_{rlx}^{\star}$ should be at least less than equal to
$p^{\star}$,
\[
p^{\star}=\sum_{i=1}^{n}c_{i}I_{\left\{ x_{i}=1\right\} }\geq\sum_{i=1}^{n}c_{i}x_{i}^{rlx}I_{\left\{ x_{i}^{rlx}>0\right\} }=p_{rlx}^{\star}.
\]
Thus, if the LP relaxation is infeasible, it means the Boolean LP
problem is also infeasible.
\item If that the LP relaxation has a solution with $x_{i}\in\left\{ 0,1\right\} $,
then we can say the optimal values of the two problems are same, $p^{\star}=p_{rlx}^{\star}$.
\end{enumerate}
\end{description}
\subsection*{Problem 3. Heuristic sub-optimal solution for Boolean LP}
This exercise builds on exercises 4.15 and 5.13 in Convex Optimization(textbook), which involve the Boolean LP
$$
\\begin{array}{cc}
minimize & c^{T}x\\\\
subject\\,to & Ax\\preceq b\\\\
 & x\_{i}\\in\\left\\{ 0,1\\right\\} ,\\,i=1,...,n.
\\end{array}
$$
 with optimal value *p*<sup>⋆</sup>. Let *x*<sup>*r**l**x*</sup> be a solution of the LP relaxation
$$
\\begin{array}{cc}
minimize & c^{T}x\\\\
subject\\,to & Ax\\preceq b\\\\
 & 0\\preceq x\\preceq1.
\\end{array}
$$
 so *L* = *c*<sup>*T*</sup>*x*<sup>*r**l**x*</sup> is a lower bound on *p*<sup>⋆</sup>. The relaxed solution *x*<sup>*r**l**x*</sup> can also be used to guess a Boolean point $\\hat{x}$, by rounding its entries, based on a threshold *t* ∈ \[0,1\]:
$$
\\hat{x}\_{i}=\\begin{cases}
1 & x\_{i}^{rlx}\\geq t\\\\
0 & o.w.,
\\end{cases}
$$
 for *i* = 1, ..., *n*.

Evidently $\\hat{x}$ is Boolean (i.e., has entries in ${ 0,1} $). If it is feasible for the Boolean LP, i.e., if $A\\hat{x}\\preceq b$, then it can be considered a guess at a good, if not optimal, point for the Boolean LP. Its objective value, $U=c^{T}\\hat{x}$, is an upper bound on *p*<sup>⋆</sup>. If *U* and *L* are close, then $\\hat{x}$ is nearly optimal; specifically, $\\hat{x}$ cannot be more than (*U*−*L*)-suboptimal for the Boolean LP. This rounding need not work; indeed, it can happen that for all threshold values, is infeasible. But for some problem instances, it can work well. Of course, there are many variations on this simple scheme for (possibly) constructing a feasible, good point from *x*<sup>*r**l**x*</sup>.

Finally, we get to the problem. Generate problem data using

``` r
n <- 100;
m <- 300;
x <- rep(0, n);
A <- matrix(runif(n*m), nrow = m, ncol = n);
b <- A %*% rep(1,n) / 2;
c <- -runif(n)
```

Find a solution of the relaxed LP and examine its entries.
\begin{description}
\item [{Sol.}] We will use $\mathtt{R}$ package named $\mathtt{lpSolveAPI}$.
The $\mathtt{lpSolveAPI}$, first, create a variable for containing
the information of problem and second the update of the information
can be done by the following codes:

```r
library(lpSolveAPI)
my.lp <- make.lp(m, n)
for (i in 1:n){
    # update constraints
    set.column(my.lp, i, A[,i])
}
# update inequalities of constraints
set.constr.type(my.lp, rep("<=", m))

# setting right-hand side values in constraints
set.rhs(my.lp, b)

# setting objective function                
set.objfn(my.lp, c)

# setting bounds for decision variables
# x_i's are real valued number between 0 and 1.
set.bounds(my.lp, lower = rep(0,n), upper = rep(1,n), columns = c(1:n))
solve(my.lp)
```

```
## [1] 0
```

\end{description}
After updating the information to solve the optimization problem, use the `s``o``l``v``e` commend to calculate the solution.

The return value 0 illustrates that the problem is feasible. The optimal point and optimal value can be obtained by using `g``e``t``.``v``a``r``i``a``b``l``e``s` and `g``e``t``.``o``b``j``e``c``t``i``v``e`.

``` r
optp <- get.variables(my.lp)
L <- get.objective(my.lp)
length(optp[optp>0])
```

    ## [1] 56

``` r
length(optp[optp==1])
```

    ## [1] 29

``` r
L
```

    ## [1] -34.61292

The result shows that the number of decision variable chosen was , and among these variables, there are variables are not integer, which makes the optimal point infeasible in Boolean LP. Since the optimal value of relaxation LP is a lower bound of the optimal value of Boolean LP, we set the variable `L` = *c*<sup>*T*</sup>*x*<sup>*r**l**x*</sup>=.

Now, we will find out the best approximation of the optimal point of LP. To find it, we need to calculate the upper bound $U=c^{T}\\hat{x}$ first. Carry out threshold rounding for 100 values of *t*, uniformly spaced over \[0,1\]. For each value of *t*, calculate $\\hat{x}$ from above and keep the the objective value $c^{T}\\hat{x}$ and the maximum constraint violation $max\\left(A\\hat{x}-b\\right)$. The best approximation of the optimal point of the LP can be obtained by finding the $\\hat{x}$ which makes the gap of (*U*−*L*) to be a minimum.

The following code is used for finding $\\hat{x}$:

``` r
t <- rep(seq(0, 1, length.out = 100),100)
t <- t(matrix(t, nrow = 100, ncol = 100))
optp <- matrix(optp, nrow = 100, ncol = 100)
x_hat <- optp - t
x_hat[x_hat>=0] <- 1
x_hat[!x_hat>=0] <- 0 
```

The last two lines of code implement the classification

$$
\\hat{x}\_{i}=\\begin{cases}
1 & x\_{i}^{rlx}\\geq t\\\\
0 & o.w.,
\\end{cases}
$$
 for each *t*. Next, the maximum constraint violation $max\\left(A\\hat{x}-b\\right)$ and the gap between *U* − *L* can be calculated as follows:

``` r
b <- matrix(b, nrow = 300, ncol = 100)
error <- A %*% x_hat-b
maxerror <- apply(error, 2, max)
U <- c(t(c) %*% x_hat)
gap <- U - L
best_x_hat <- x_hat[,min(which(maxerror<0))]
```

The best approximation of the optimal point of LP, $\\hat{x}\_{best}$,should not only make the gap to be minimum, but also be feasible in LP. In other words, $\\hat{x}\_{best}$ should not violate the constraints; $max\\left(A\\hat{x}\_{best}-b\\right)\\leq0$. Thus, the last line of code determine $\\hat{x}\_{best}$ under the constraints, and the optimal value of the Boolean LP, $\\hat{p}^{\\star}$, is approximately equal to . This approximation fairly good because the gap between *U* − *L* was . <img src="kubetest_files/figure-markdown_github/unnamed-chunk-6-1.png" style="display: block; margin: auto;" />

Figures
=======

``` r
plot(1:10)
```

<img src="kubetest_files/figure-markdown_github/unnamed-chunk-7-1.png" style="display: block; margin: auto;" />

### Level 3

Commander Jeffrey David Sinclair: Everyone lies, Michael. The innocent lie because they don't want to be blamed for something they didn't do and the guilty lie because they don't have any other choice. Lt. Corwin: Do we trust no-one then? Cmdr. Susan Ivanova: No, trust Ivanova, trust yourself, anybody else, shoot'em. Susan Ivanova: If I live through this without completely losing my mind, it will be a miracle of Biblical proportions.

Lt. Corwin: \[aside\] Well, there goes my faith in the Almighty. \[Opening narration, season 3\] Susan Ivanova: The Babylon Project was our last, best hope for peace. It failed. But in the year of the Shadow War, it became something greater: our last, best hope for victory. The year is 2260. The place - Babylon 5. Alfred Bester: Being a telepath means you're special and rare and valuable.

#### Level 4

Delenn: We are star stuff. We are the universe made manifest trying to figure itself out.

Captain John Sheridan: If more of our so-called leaders would walk the same streets as the people who voted them in, live in the same buildings, eat the same food instead of hiding behind glass and steel and bodyguards, maybe we'd get better leadership and a little more concern for the future.

Captain John Sheridan: If more of our so-called leaders would walk the same streets as the people who voted them in, live in the same buildings, eat the same food instead of hiding behind glass and steel and bodyguards, maybe we'd get better leadership and a little more concern for the future. Kosh Naranek: Understanding is a three-edged sword. Alfred Bester: Much as it might offend their sense of perspective, not everything is about Babylon 5.
