# Entropy
## Definition
随机变量$X$,样本空间 (alphabet)$\mathcal{X}$, 概率密度$p(x)$
Entropy:
$$H(X) = -\sum_{x\in \mathcal{X}}p(x)\log p(x)$$
- 非负，只和$p(x)$有关
- 均匀分布: $H(X) = \log |\mathcal{X}|$ (log size of $\mathcal{X}$)

$H(p)$和$H(\mathcal{X})$是一回事
-均匀分布最大化熵

## Joint Entropy

概率密度 $p(x,y)$
$$H(x,y) = -\mathbb{E}\log(X,Y) = -\sum_{x\in \mathcal{X}}\sum_{y\in \mathcal{Y}}p(x,y)\log p(x,y)$$
## ***(Average)*** Conditional Entropy

概率密度 $p(Y|X=x)$
$$H(Y|X) = -\mathbb{E}\log p(Y|X)$$

性质 
- Chain Rule
$$H(X|Y) + H(Y) = H(Y|X) + H(X) = H(X,Y)$$
- X, Y独立 $H(X,Y) = H(X) + H(Y)$
- Zero Entropy 

    X是Y的函数 $\leftrightarrow H(X,Y) = H(Y)\leftrightarrow H(X|Y)=0$

    
证明：

$\Rightarrow:$
$$X=g(Y) \rightarrow p(X|Y=y)=1 $$
$$H(X|Y) = \sum_{y\in\mathcal{Y}}p(y)\log p(X|Y=y) = 0$$

$\Leftarrow:$
$$H(X|Y) = \sum_{y\in\mathcal{Y}}p(y)\log p(X|Y=y) = 0$$
$p(y)$ is nonnegative
$$p(X|Y=y)=1 ,\forall y$$
Thus 
$$p(X|Y)=1$$
and
$$X = g(Y)$$