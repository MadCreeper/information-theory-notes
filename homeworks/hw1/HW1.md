Homework 1

DDL: Feb 23.

1. Show that $x\log x\to 0$, as $x\to 0$. 


   By L'Hospital's rule, 
   $$\lim_{x\rightarrow0}x\log x = \lim_{x\rightarrow0}\frac{\log x}{x^{-1}} = \lim_{x\rightarrow0}\log e\frac{x^{-1}}{-x^{-2}}=\lim_{x\rightarrow0}(-\log e)x=0$$



2. Show that $H(p) = -p\log p - (1-p)\log (1-p)$ is concave in $p\in [0,1]$.


   Let
   $$H_1(p)=-p\log p, H_2(p)=-(1-p)\log(1-p)$$
   $$\frac{d^2H_1}{dp^2}=-\log e \frac{1}{p} \lt 0$$
   So $H_1(p)$ is concave. Similarly  $H_2(p)$ is also concave. Thus $H(p) = H_1(p)+H_2(p)$ is concave.


3. Prove $H(X)\le\log |\mathcal{X}|$ via Lagrange multipler when $|\mathcal{X}|=3$
   
   $$
   \min f(x,y,z)=x\log x + y\log y + z\log z\\
   s.t \ \ x+y+z=1\\
   x,y,z\geq 0
   $$

   Consider its Lagrangian:
   $$
   g(x,y,z;\lambda) = f(x,y,z)-\lambda(x+y+z)
   $$
   (a). Compute $\nabla g$, i.e., the partial derivatives of $g$ with resepct to $x, y, z$; 

   (b). Let $\nabla  g = 0$, show that $x=y=z$. Thus, $\min f$ is attained only if $x=y=z$.
   

   (a)
   $$\nabla g =  
      \begin{pmatrix}
      \log x -\lambda + \log e \\
      \log y -\lambda+ \log e \\
      \log z -\lambda+ \log e
      \end{pmatrix}
   $$
   (b) Let $\nabla g = 0$, and we get
   $$\log x = \log y = \log z = \lambda - \log e$$
   Therefore the minimum is attained only if $x=y=z$.


4. Exercise **2.1, 2.2, 2.5, 2.7** in the textbook of Cover  

   2.1
   (a) 
   $$p(X=n) = (\frac{1}{2})^n$$
   $$H(X) = \sum_{n=0}^\infty -p(X=n)\log p(X=n) =\sum_{n=0}^\infty n (\frac{1}{2})^n = \frac{\frac{1}{2}}{(1-\frac{1}{2})^2} = 2$$
   (b) The n-th quesion is: Is $X$ in $S, S=\{n\}$?

      If $X=k$, then $n=k$.
      $$\mathbb E(n)=\mathbb E(X) = \sum_{n=1}^\infty n (\frac{1}{2})^n = 2 $$
      So the expected number of questions is $2$.

      $H(x)=2(bits)$, and one yes/no quesion gives $1$ bit of information, so it takes 2 questions in average to determine $X$. 
   
   2.2
   Let 
   $X \in \mathcal{X}, \mathcal{X}=\{x_1,x_2,\dots x_n\}$ and 
   $Y \in \mathcal{Y}, \mathcal{Y}=\{y_1,y_2,\dots y_m\}$
   
   (a) $y=2^x$ is a one-to-one funtion, so $n=m$.
   $$H(Y) =\sum_{i=1}^m-p(Y=y_i)\log p(Y=y_i) = \sum_{i=1}^n-p(X=x_i)\log p(X=x_i) = H(X)$$
   (b) For function $y=\cos x$, $n \geq m$. 
   
   So there exists $t_1, t_2, \dots, t_m$ such that $\cos x_{t_i} = y_i, i = 1,2,\dots, m$. 
   $$H(Y) =\sum_{i=1}^m-p(Y=y_i)\log p(Y=y_i) = \sum_{i=1}^m-p(X=x_{t_i})\log p(X=x_{t_i}) $$ 
   $$\leq \sum_{i=1}^n-p(X=x_i)\log p(X=x_i) = H(X)$$

   2.5
   $$H(Y|X) = \sum_{x \in \mathcal{X}}-p(x)H(Y|X=x) = 0$$
   For all $p(x) \gt 0$,
   $$H(Y|X=x)=\sum_{y\in \mathcal{Y}}-p(y|X=x) \log p(y|X=x) = 0$$
   For ang $y$, if $p(y|X=x) \gt 0$, $p(y|X=x)=1$
   
   So $Y$ is uniquely determined by $X$. i.e. $Y$ is a function of $X$.

   2.7 The counterfeit coin is either heavier or lighter, which can be represented with 1 bit. Suppose the $X$-th coin in $n$ coins is counterfeit. $X$ follows a uniform distribution. We have
   $$H(X) = -\sum_{k=1}^n p(X=k) \log p(X=k) = \log n$$
   The total information is $\tilde{H} = \log n +1$

   If the number of coins that remain to be tested is even, one weigh gives us $1$ bit of information (the balance can show 2 results).
   So
   $$\log n + 1 = k$$
   where $n = 2^m$.

   So the upper bound of $n$ is $2^{k-1}$.
   WRONG