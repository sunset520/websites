# websites

# 希尔伯特-华林定理

## 简介

每个充分大的数都可以表示成有限个自然数 $k$ 次幂的和。

## 证明

### 方法 1

引入记号

$$
(x _ 1\pm x _ 2\pm \cdots \pm x _ h)^k=\sum _ {\varepsilon _ 2,\cdots ,\varepsilon _ h=\pm 1}(x _ 1+\varepsilon _ 2x _ 2+\cdots +\varepsilon _ hx _ h)^k
$$

定理 3.1：

$$
(x _ 1^2+x _ 2^2+x _ 3^2+x _ 4^2)^2=\dfrac{1}{6}\sum _ {1\leq i<j\leq 4}(x _ i+x _ j)^4+\dfrac{1}{6}\sum _ {1\leq i<j\leq 4}(x _ i-x _ j)^4
$$

是一个恒等式。每个非负整数至多是 $53$ 个整数的四次方的和，即

$$
g(4)\leq 53
$$

定理 3.2：

$$
(x _ 1^2+x _ 2^2+x _ 3^2+x _ 4^2)^3=\dfrac{1}{60}\sum _ {1\leq i<j<k\leq 4}(x _ i\pm x _ j\pm x _ k)^6+\dfrac{1}{30}\sum _ {1\leq i<j\leq 4}(x _ i\pm x _ j)^6+\dfrac{3}{5}\sum _ {1\leq i\leq 4}x _ i^6
$$

是一个恒等式。每个非负整数是有限个六次方的和。

定理 3.3：

$$
(x _ 1^2+x _ 2^2+x _ 3^2+x _ 4^2)^4=\dfrac{1}{840}(x _ 1\pm x _ 2\pm x _ 3 \pm x _ 4)^8+\dfrac{1}{5040}\sum _ {1\leq i<j<k\leq 4}(2x _ i\pm x _ j\pm x _ k)^8+\dfrac{1}{84}\sum _ {1\leq i<j\leq 4}(x _ i\pm x _ j)^8+\dfrac{1}{840}\sum _ {1\leq i\leq 4}(2x _ i)^6
$$

是一个恒等式。每个非负整数都是有限个八次幂的和。

我们先定义埃尔米特多项式 $H _ n(x)$

$$
H _ n(x)=\left( -\dfrac{1}{2} \right)^n\mathrm{e}^{x^2}\dfrac{\mathrm{d}^n}{\mathrm{d}x^n}\left( \mathrm{e}^{-x^2} \right)
$$

我们可以得到

$$
H _ 0(x)=1
$$

$$
H _ 1(x)=x
$$

$$
H _ 2(x)=x^2-\dfrac{1}{2}
$$

$$
H _ 3(x)=x^3-\dfrac{3}{2}x
$$

$$
H _ 4(x)=x^4-3x^2+\dfrac{3}{4}
$$

$$
H _ n^{\prime}(x)=2xH _ n(x)-2H _ {n+1}(x)
$$

则埃尔米特多项式满足递归关系

$$
H _ {n+1}(x)=xH _ {n}(x)-\dfrac{1}{2}H _ n^{\prime }(x)
$$

因此，$H _ n(x)$ 是具有有理系数的 $n$ 次一元多项式。且当 $n$ 为偶数时，$H _ n(x)$ 为偶多项式，反之为奇多项式。

引理 3.1：埃尔米特多项式 $H _ n(x)$ 有 $n$ 个不同的实数根。

证明：使用归纳法。当 $n=0,1$ 时显然成立。令 $n\geq 1$，假设引理对于 $n$ 是正确的。则 $H _ n(x)$ 有 $n$ 个不同的实根。这些根必定是单根。因此，存在

$$
\beta _ n<\cdots<\beta _ 2<\beta _ 1
$$

使得

$$
H _ n(\beta _ j)=0 \quad H _ n^{\prime}(\beta _ j)\neq 0 \quad (j=1,2,\cdots ,n)
$$

因为 $H _ n(x)$ 是 $n$ 次一元多项式，则有

$$
\lim _ {x \to \infty} H _ n(x)=\infty
$$

所以

$$
H _ {n}^{\prime }(\beta _ 1)>0
$$

由于 $H _ n^{\prime }(x)$ 的 $n-1$ 个根和 $H _ n(x)$ 的 $n$ 个根交错，则有

$$
(-1)^{j+1}H _ n^{\prime }(\beta _ j)>0 \quad (j=1,\cdots ,n)
$$

根据递归关系，有

$$
H _ {n+1}(\beta _ j)=\beta _ jH _ n(\beta _ j)-\dfrac{1}{2}H _ n^{\prime }(\beta _ j)=-\dfrac{1}{2}H _ n^{\prime }(\beta _ j)
$$

所以

$$
(-1)^jH _ {n+1}(\beta _ j)=\dfrac{(-1)^{j+1}}{2}H _ n^{\prime }(\beta _ j)>0
$$

因此，对于 $j=2,\cdots ,n$，$H _ {n+1}(x)$ 有零点 $\beta _ j^{\ast}$ 在 $(\beta _ j,\beta _ {j-1})$。由于 $\lim _ {x \to \infty} H _ {n+1}(x) = \infty $ 且 $H _ {n+1}(\beta _ 1)<0$。故 $H _ {n+1}(x)$ 有零点 $\beta _ 1^{\ast}>\beta _ 1$。如果 $n$ 是偶数，则 $H _ {n+1}(\beta _ n)>0$。因为 $n+1$ 是奇数，$\lim _ {x \to -\infty} H _ {n+1}(x)=-\infty $。这说明 $H _ {n+1}(x)$ 有零点 $\beta _ {n+1}^{\ast}<\beta _ {n}$。类似的，如果 $n$ 是奇数，也可以证明。故 $H _ {n+1}(x)$ 有 $n+1$ 个不同的实数零点。

引理 3.2：令 $n\geq 1$ 且 $f(x)$ 是 $n-1$ 次多项式，则有

$$
\int _ {-\infty }^{\infty}\mathrm{e}^{-x^2}H _ n(x)f(x)\mathrm{d}x=0
$$

证明：使用归纳法。如果 $n=1$ ，则 $H _ n(x)=x$ 且 $f(x)$ 是常数，令 $f(x)=a _ 0$，则

$$
\int _ {-\infty }^{\infty}\mathrm{e}^{-x^2}H _ n(x)f(x)\mathrm{d}x=a _ 0\int _ {-\infty }^{\infty}\mathrm{e}^{-x^2}x\mathrm{d}x=0
$$

现在假设引理对 $n$ 成立，令 $f(x)$ 作为次数至多为 $n$ 的多项式，则 $f^{\prime }(x)$ 是次数最多为 $n-1$ 的多项式。则有

$$
\begin{align*}
\int _ {-\infty }^{\infty}\mathrm{e}^{-x^2}H _ {n+1}(x)f(x)\mathrm{d}x&=\left( -\dfrac{1}{2} \right)^{n+1}\int _ {-\infty}^{\infty}\dfrac{\mathrm{d}^{n+1}}{\mathrm{d}x^{n+1}}(\mathrm{e}^{-x^2})f(x)\mathrm{d}x \\
&=\left( -\dfrac{1}{2} \right)^{n+1}\int _ {-\infty}^{\infty}\dfrac{\mathrm{d}^{n}}{\mathrm{d}x^{n}}(\mathrm{e}^{-x^2})f^{\prime}(x)\mathrm{d}x \\
&=\left( -\dfrac{1}{2} \right)\int _ {-\infty}^{\infty}\mathrm{e}^{-x^2}H _ n(x)f^{\prime}(x)\mathrm{d}x \\
&=0
\end{align*}
$$

证毕。

引理 3.3：对于 $n\geq 0$，

$$
c _ n=\dfrac{1}{\sqrt{\pi}}\int _ {-\infty }^{\infty }\mathrm{e}^{-x^2}x^n\mathrm{d}x=\begin{cases}
\dfrac{n!}{2^n(n/2)!} & n \text{是偶数} \\
0 & n \text{是奇数}
\end{cases}
$$

证明：使用归纳法。对于 $n=0$，有

$$
\int _ {-\infty}^{\infty }\mathrm{e}^{-x^2}\mathrm{d}x=\sqrt{\pi}
$$

可以得到 $c _ 0=1$。对于 $n=1$，根据奇函数的性质，$c _ 1=0$。

现在令 $n\geq 2$，且假设引理对 $n-2$ 成立，则有

$$
c _ n=\dfrac{1}{\sqrt{\pi}}\int _ {-\infty }^{\infty }\mathrm{e}^{-x^2}x^n\mathrm{d}x=\left(\dfrac{n-1}{2}\right)c _ {n-2}
$$

根据这个递推式我们可以完成证明。

引理 3.4：令 $n\geq 1$，令 $\beta _ 1,\cdots,\beta _ n$ 是 $n$ 个不同的实数，令 $c _ 0,c _ 1,\cdots ,c _ {n-1}$ 作为引理 3.3 中的数字，则线性方程组

$$
\sum _ {j=1}^{n}\beta _ j^kx _ j=c _ k \quad k=0,1,\cdots ,n-1
$$

有一个独一无二的解 $\rho _ 1,\cdots ,\rho _ n$。如果 $r(x)$ 是一个次数至多为 $n-1$ 的多项式，则

$$
\sum _ {j=1}^{n}r(\beta _ j)\rho _ j=\dfrac{1}{\sqrt{\pi}}\int _ {-\infty }^{\infty }\mathrm{e}^{-x^2}r(x)\mathrm{d}x
$$

证明：

该线性方程组的系数行列式可以写成范德蒙德行列式，根据范德蒙德行列式的性质知道该行列式不为零。所以原方程有唯一解。

令 $r(x)=\sum _ {k=0}^{n-1}a _ kx^k$，则有

$$
\begin{align*}
\sum _ {j=1}^{n}r(\beta _ j)\rho _ j &=\sum _ {j=1}^{n}\sum _ {k=0}^{n-1}a _ k\beta _ j^k\rho _ j \\
&=\sum _ {k=0}^{n-1}a _ k\sum _ {j=1}^{n}\beta _ j^k\rho _ j \\
&=\sum _ {k=0}^{n-1}a _ kc _ k \\
&=\dfrac{1}{\sqrt{\pi}}\sum _ {k=0}^{n-1}a _ k\int _ {-\infty }^{\infty }\mathrm{e}^{-x^2}x^k\mathrm{d}x \\
&=\dfrac{1}{\sqrt{\pi}}\int _ {-\infty }^{\infty }\mathrm{e}^{-x^2}r(x)\mathrm{d}x
\end{align*}
$$

引理 3.5：令 $n\geq 1$，令 $\beta _ 1,\cdots ,\beta _ n$ 作为埃尔米特多项式 $H _ n(x)$ 的 $n$ 个不同的根，令 $\rho _ 1,\cdots ,\rho _ n$ 作为引理 3.4 中的线性方程组的解。令 $f(x)$ 为次数最多为 $2n-1$ 的多项式，则

$$
\sum _ {j=1}^{n}f(\beta _ j)\rho _ j=\dfrac{1}{\sqrt{\pi }}\int _ {-\infty }^{\infty }\mathrm{e}^{-x^2}f(x)\mathrm{d}x
$$

证明：根据多项式的除法，存在次数至多为 $n-1$ 的多项式 $q(x)$ 和 $r(x)$ 使得

$$
f(x)=H _ n(x)q(x)+r(x)
$$

因为 $H _ n(\beta _ j) = 0 \quad j=1,\cdots,n$，有

$$
f(\beta  _ j)=H _ n(\beta _ j)q(\beta _ j)+r(\beta _ j)=r(\beta _ j)
$$

根据引理 3.4 和引理 3.2，有

$$
\begin{align*}
\sum _ {j=1}^{n}f(\beta _ j)\rho _ j&=\sum _ {j=1}^{n}r(\beta _ j)\rho _ j \\
&=\dfrac{1}{\sqrt{\pi}}\int _ {-\infty }^{\infty }\mathrm{e}^{-x^2}r(x)\mathrm{d}x \\
&=\dfrac{1}{\sqrt{\pi}}\int _ {-\infty }^{\infty }\mathrm{e}^{-x^2}H _ n(x)q(x)\mathrm{d}x +\dfrac{1}{\sqrt{\pi}}\int _ {-\infty }^{\infty }\mathrm{e}^{-x^2}r(x)\mathrm{d}x \\
&=\dfrac{1}{\sqrt{\pi}}\int _ {-\infty }^{\infty }\mathrm{e}^{-x^2}f(x)\mathrm{d}x
\end{align*}
$$

引理 3.6：令 $n\geq 1$，令 $\beta _ 1,\cdots ,\beta _ n$ 作为埃尔米特多项式 $H _ n(x)$ 的 $n$ 个不同的根，令 $\rho _ 1,\cdots ,\rho _ n$ 作为引理 3.4 中的线性方程组的解。则有

$$
\rho _ i>0 \quad i=1,\cdots,n
$$

证明：

因为

$$
H _ n(x)=\prod _ {j=1}^{n}(x-\beta _ j)
$$

则有，对于 $i=1,2,\cdots ,n$

$$
f _ i(x)=\left( \dfrac{H _ n(x)}{x-\beta _ i} \right)^2=\prod _ {j=1,j\neq i}^{n}(x-\beta _ j)^2
$$

是 $2n-2$ 次一元多项式使得对任意的 $x$，$f _ i(x)\geq 0$。因此

$$
\dfrac{1}{\sqrt{\pi}}\int _ {-\infty }^{\infty }\mathrm{e}^{-x^2}f _ i(x)\mathrm{d}x>0
$$

因为 $f _ i(\beta _ i)>0$ 且对于 $j\neq i$，$f _ i(\beta _ j)=0$，我们有

$$
\begin{align*}
f _ i(\beta _ i)\rho _ i&=\sum _ {j=1}^{n}f _ i(\beta _ j)\rho _ j \\
&= \dfrac{1}{\sqrt{\pi}}\int _ {-\infty }^{\infty }\mathrm{e}^{-x^2}f _ i(x)\mathrm{d}x \\
&>0
\end{align*}
$$

引理 3.7：令 $n\geq 1$，令 $c _ 0,c _ 1,\cdots ,c _ {n-1}$ 为引理 3.3 中的有理数。存在不同的有理数 $\beta _ 1^{\ast},\cdots ,\beta _ n^{\ast}$ 和正有理数 $\rho _ 1^{\ast},\cdots ,\rho _ n^{\ast}$ 使得

$$
\sum _ {j=1}^{n}(\beta _ j^{\ast})^k\rho _ j^{\ast}=c _ k \quad k=0,1,\cdots,n-1
$$

证明：

根据引理 3.4，对于任意的 $n$ 个数 $\beta _ 1,\cdots,\beta _ n$，$n$ 元线性方程组

$$
\sum _ {j=1}^{n}\beta _ j^kx _ j=c _ k \quad k=0,1,\cdots,n-1
$$

有独一无二的解 $(\rho _ 1,\cdots,\rho _ n)$。令 $\mathcal{R}$ 为满足 $\beta _ i\neq \beta _ j \quad (i\neq j)$ 的所有点 $(\beta _ 1,\cdots,\beta _ n)$ 的开集。令 $\Phi : \mathcal{R}\rightarrow \mathbb{R}^n$ 是将 $(\beta _ 1,\cdots ,\beta _ n)$ 映射到 $(\rho _ 1,\cdots ,\rho _ n)$。根据克拉姆法则，每个 $\rho _ j$ 可以表达为 $\beta _ 1,\cdots,\beta _ n$ 的有理函数，则函数有

$$
\Phi(\beta _ 1,\cdots,\beta _ n)=(\rho _ 1,\cdots,\rho _ n)
$$

是连续的。令 $\mathbb{R} _ {+}^{n}$ 是 $\mathbb{R}^{n}$ 的开子集且包含所有的点 $(x _ 1,\cdots ,x _ n)$ 满足 $x _ i>0 \quad (i=1,\cdots,n)$。根据引理 3.6，如果 $\beta _ 1,\cdots ,\beta _ n$ 是 $H _ n(x)$ 的 $n$ 个零点，则 $(\beta _ 1,\cdots ,\beta _ n)\in \mathcal{R}$ 且

$$
\Phi(\beta _ 1,\cdots,\beta _ n)=(\rho _ 1,\cdots,\rho _ n)\in \mathbb{R} _ {+}^{n}
$$

因为 $\mathbb{R} _ {+}^{n}$ 是 $\mathbb{R}^n$ 的一个开子集。这说明 $\Phi^{-1}(\mathbb{R} _ {+}^{n})$ 是 $(\beta _ 1,\cdots ,\beta _ n)$ 的一个在 $\mathcal{R}$ 中的开邻域。因为在 $\mathcal{R}$ 中有理坐标点是稠密的，这个邻域包含有有理点 $(\beta _ 1^{\ast},\cdots,\beta _ n^{\ast})$。令

$$
(\rho _ 1^{\ast},\cdots,\rho _ n^{\ast})=\Phi(\beta _ 1^{\ast},\cdots,\beta _ n^{\ast})\in \mathbb{R} _ {+}^{n}
$$

因为每个数字 $\rho _ i^{\ast}$ 都可以表示为具有有理系数的有理函数关于有理数 $\beta _ 1^{\ast},\cdots,\beta _ n^{\ast}$，这说明每个正数 $\rho _ i^{\ast}$ 都是有理数。

引理 3.8：令 $n\geq 1$，令 $c _ 0,c _ 1,\cdots,c _ {n-1}$ 为引理 3.3 中定义的数字，令 $\beta _ 1,\cdots,\beta _ n$ 为 $n$ 个不同的实数，令 $\rho _ 1,\cdots ,\rho _ n$ 为引理 3.4 线性方程组的解。对于每个正整数 $r$ 以及对于 $m=1,2,\cdots ,n-1$

$$
c _ m(x _ 1^2+\cdots +x _ r^2)^{m/2}=\sum _ {j _ 1=1}^{n}\cdots\sum _ {j _ r=1}^{n}\rho _ {j _ 1}\cdots \rho _ {j _ {r}}(\beta _ {j _ 1}x _ 1+\cdots +\beta _ {j _ r}x _ r)^m
$$

是一个恒等式。

证明：

$$
\begin{align*}
&\sum _ {j _ 1=1}^{n}\cdots\sum _ {j _ r=1}^{n}\rho _ {j _ 1}\cdots \rho _ {j _ {r}}(\beta _ {j _ 1}x _ 1+\cdots +\beta _ {j _ r}x _ r)^m \\
&=\sum _ {j _ 1=1}^{n}\cdots\sum _ {j _ r=1}^{n}\rho _ {j _ 1}\cdots \rho _ {j _ {r}}\sum _ {\mu _ 1+\cdots+\mu _ r=m, \mu _ i\geq 0}\dfrac{m!}{\mu _ 1!\cdots\mu _ r!}(\beta _ {j _ 1}x _ 1)^{\mu _ 1}\cdots(\beta _ {j _ r}x _ r)^{\mu _ r} \\
&=m!\sum _ {j _ 1=1}^{n}\cdots\sum _ {j _ r=1}^{n}\sum _ {\mu _ 1+\cdots+\mu _ r=m, \mu _ i\geq 0}\dfrac{x _ 1^{\mu _ 1}}{\mu _ 1!}(\beta _ {j _ 1}^{\mu _ 1}\rho _ {j _ 1})\cdots \dfrac{x _ r^{\mu _ r}}{\mu _ r!}(\beta _ {j _ r}^{\mu _ r}\rho _ {j _ r}) \\
&=m!\sum _ {\mu _ 1+\cdots+\mu _ r=m, \mu _ i\geq 0}\sum _ {j _ 1=1}^{n}\cdots\sum _ {j _ r=1}^{n}\prod _ {i=1}^{r}\dfrac{x _ i^{\mu _ i}}{\mu _ i!}(\beta _ {j _ i}^{\mu _ i}\rho _ {j _ i}) \\
&=m!\sum _ {\mu _ 1+\cdots+\mu _ r=m, \mu _ i\geq 0}\prod _ {i=1}^{r}\left( \dfrac{x _ i^{\mu _ i}}{\mu _ i!}\sum _ {j=1}^{n}\beta  _ {j}^{\mu _ i}\rho _ j \right) \\
&=m!\sum _ {\mu _ 1+\cdots+\mu _ r=m, \mu _ i\geq 0}\prod _ {i=1}^{r}\dfrac{c _ {\mu _ i}x _ i^{\mu _ i}}{\mu _ i!}
\end{align*}
$$

根据引理 3.3，如果 $m$ 是奇数，$c _ m=0$，且 $\mu _ 1+\cdots+\mu _ r=m$，则一定有某些 $\mu _ i$ 为奇数，则有

$$
\sum _ {j _ 1=1}^{n}\cdots\sum _ {j _ r=1}^{n}\rho _ {j _ 1}\cdots \rho _ {j _ {r}}(\beta _ {j _ 1}x _ 1+\cdots +\beta _ {j _ r}x _ r)^m=0
$$

如果 $m$ 是偶数，我们只需要考虑偶数部分，令 $\mu _ i=2v _ i$，

$$
\begin{align*}
&\sum _ {j _ 1=1}^{n}\cdots\sum _ {j _ r=1}^{n}\rho _ {j _ 1}\cdots \rho _ {j _ {r}}(\beta _ {j _ 1}x _ 1+\cdots +\beta _ {j _ r}x _ r)^m \\
&=m!\sum _ {2v _ 1+\cdots +2v _ r=m,v _ i\geq 0}\prod _ {i=1}^{r}\dfrac{c _ {2v _ i}x^{2v _ i}}{(2v _ i)!} \\
&=m!\sum _ {v _ 1+\cdots +v _ r=m/2,v _ i\geq 0}\prod _ {i=1}^{r}\dfrac{(2v _ i)!}{2^{2v _ i}v _ i!}\dfrac{x^{2v _ i}}{(2v _ i)!} \\
&=\dfrac{m!}{2^m}\sum _ {v _ 1+\cdots+v _ r=m/2,v _ i\geq 0}\prod _ {i=1}^{r}\dfrac{x _ i^{2v _ i}}{(v _ i)!} \\
&=\dfrac{m!}{2^m(m/2)!}(m/2)!\sum _ {v _ 1+\cdots+v _ r=m/2,v _ i\geq 0}\prod _ {i=1}^{r}\dfrac{(x _ i^2)^{v _ i}}{(v _ i)!} \\
&=c _ m\sum _ {v _ 1+\cdots+v _ r=m/2,v _ i\geq 0}\dfrac{(m/2)!}{v _ 1!\cdots v _ r!}(x _ 1^2)^{v _ 1}\cdots (x _ r^2)^{v _ r} \\
&=c _ m(x _ 1^2+\cdots +x _ r^2)^{m/2}
\end{align*}
$$

定理 3.4（希尔伯特恒等式）：对于每个 $k\geq 1$ 且 $r\geq 1$，存在一个整数 $M$ 和正有理数 $a _ i$ 和整数 $b _ {i,j}$，其中 $i=1,2,\cdots ,M$ 且 $j=1,2,\cdots ,r$ 使得

$$
(x _ 1^2+\cdots+x _ r^2)^k=\sum _ {i=1}^{M}a _ i(b _ {i,1}x _ 1+\cdots +b _ {i,r}x _ r)^{2k}
$$

证明：选择 $n>2k$，令 $\beta _ 1^{\ast},\cdots ,\beta _ n^{\ast},\rho _ 1^{\ast},\cdots ,\rho _ n^{\ast}$ 是引理 3.7 构造的有理数。则 $\beta _ 1^{\ast},\cdots ,\beta _ n^{\ast}$ 是互不相同的，$\rho _ 1^{\ast},\cdots ,\rho _ n^{\ast}$ 是正的。令 $m=2k$，根据引理 3.8，有

$$
c _ {2k}(x _ 1^2+\cdots +x _ r^2)^k=\sum _ {j _ 1=1}^{n}\cdots\sum _ {j _ r=1}^{n}\rho _ {j _ 1}^{\ast}\cdots \rho _ {j _ {r}}^{\ast}(\beta _ {j _ 1}^{\ast}x _ 1+\cdots +\beta _ {j _ r}^{\ast}x _ r)^{2k}
$$

令 $q$ 为 $\beta _ {j _ 1}^{\ast},\cdots ,\beta _ {j _ r}^{\ast}$ 的公共分母，则 $q\beta  _ j^{\ast}$ 是整数，且

$$
(x _ 1^2+\cdots +x _ r^2)^k=\sum _ {j _ 1=1}^{n}\cdots\sum _ {j _ r=1}^{n}\dfrac{\rho _ {j _ 1}^{\ast}\cdots \rho _ {j _ {r}}^{\ast}}{c _ {2k}q^{2k}}(q\beta _ {j _ 1}^{\ast}x _ 1+\cdots +q\beta _ {j _ r}^{\ast}x _ r)^{2k}
$$

就是希尔伯特恒等式。

引理 3.9：令 $k\geq 1$，如果存在正的有理数 $a _ 1,\cdots ,a _ M$ 使得每一个充分大的整数 $n$ 可以被写成如下形式

$$
n=\sum _ {i=1}^{M}a _ iy _ i^k
$$

其中 $x _ 1,\cdots ,x _ M$ 是非负整数，则华林问题对于指数 $k$ 成立。

证明：选择 $n _ 0$ 使得每个整数 $n\geq n _ 0$ 都可以表示称这样的形式。令 $q$ 是 $a _ 1,\cdots ,a _ M$ 的最小公共分母。则 $qa _ i\in \mathbb{Z}\quad i=1,\cdots ,M$ 且对于每个 $n\geq n _ 0$，$qn$ 是 $\sum _ {i=1}^{M}qa _ i$ 的非负 $k$ 次幂的和。因为每个整数都可以写成 $N\geq qn _ 0$ 可以写成 $N=qn+r$ 的形式，其中 $n\geq n _ 0,0\leq r\leq q-1$，这表明 $N$ 可以写成 $\sum _ {i=1}^{M}qa _ i+q-1$ 非负 $k$ 次幂。显然，每个非负整数 $N<qn _ 0$ 可以写成有限个 $k$ 次幂之和，所以华林问题对于 $k$ 成立。

令 $\sum _ {i=1}^{M}a _ ix _ i^k$ 是一个有着有理系数的 $k$ 次的固定形式。我们记 $n=\sum(k)$，如果存在非负整数 $x _ 1,\cdots ,x _ M$ 使得

$$
n=\sum _ {i=1}^{M}a _ ix _ i^k
$$

我们令 $\sum (k)$ 表示满足以上形式的所有数字。则有 $\sum (k)+\sum (k)=\sum (k)$，$\sum (2k)=\sum (k)$。引理 3.9 可以重新陈述如下，对于每个充分大的非负整数 $n$，如果 $n=\sum(k)$，华林问题在 $k$ 的情形下成立。

定理 3.5：如果华林问题对于 $k$ 成立，那么华林问题对于 $2k$ 也成立。

证明：我们用希尔伯特恒等式

$$
(x _ 1^2+\cdots +x _ 4^2)^{k}=\sum _ {i=1}^{M}a _ i(b _ {i,1}x _ 1+\cdots +b _ {i,4}x _ 4)^{2k}
$$

令 $y$ 作为一个非负整数。通过[拉格朗日四平方和定理](拉格朗日四平方和定理.md)，存在非负整数 $x _ 1,x _ 2,x _ 3,x _ 4$ 使得

$$
y=x _ 1^2+x _ 2^2+x _ 3^2+x _ 4^2
$$

所以

$$
y^k=\sum _ {i=1}^{M}a _ iz _ i^{2k}
$$

其中

$$
z _ i=b _ {i,1}x _ 1+\cdots +b _ {i,4}x _ 4
$$

是一个非负整数。这意味着

$$
y^k=\sum (2k)
$$

对于每一个非负整数 $y$ 成立。如果华林问题对于 $k$ 成立，每个非负整数都可以表示称有限个 $k$ 次幂的和，故每个非负整数都可以表示成有限个可以表示成 $\sum (2k)$ 形式的数的和。根据引理 3.9，华林问题在 $2k$ 时成立。

引理 3.10：令 $k\geq 2$ 且 $0\leq l\leq k$。存在正整数 $B _ {0,l},B _ {1,l},\cdots ,B _ {l-1,l}$ 只取决于 $k$ 和 $l$ 使得

$$
x^{2l}T^{k-l}+\sum _ {i=0}^{l-1}B _ {i,l}x^{2i}T^{k-i}=\sum (2k)
$$

对于所有的整数 $x$ 和 $T$ 满足 $x^2\leq T$。

证明：我们使用希尔伯特恒等式

$$
(x _ 1^2+\cdots +x _ 5^2)^{k+l}=\sum _ {i=1}^{M _ l}a _ i(b _ {i,1}x _ 1+\cdots +b _ {i,5}x _ 5)^{2k+2l}
$$

其中整数 $M _ l$ 和 $b _ {i,j}$ 和正有理数 $a _ i$ 只取决于 $k$ 和 $l$。令 $U$ 是非负整数。根据[拉格朗日四平方和定理](拉格朗日四平方和定理.md)，可以写成

$$
U=x _ 1^2+x _ 2^2+x _ 3^2+x _ 4^2
$$

其中 $x _ 1,x _ 2,x _ 3,x _ 4$ 非负。令 $x _ 5=x$。得到

$$
(x^2+U)^{k+l}=\sum _ {i=1}^{M _ l}a _ i(b _ ix+c _ i)^{2k+2l}
$$

其中数字 $M _ l,a _ i$，$b _ i=b _ {i,5}$ 只依赖于 $k$ 和 $l$。整数 $c _ i=b _ {i,1}x _ 1+\cdots +b _ {i,4}x _ 4$ 依赖于 $k,l,U$。因为 $l\leq k$，所以 $2l\leq k+l$。对等式左边进行微分

$$
\dfrac{\mathrm{d}^{2l}}{\mathrm{d}x^{2l}}((x^2+U)^{k+l})=\sum _ {i=0}^{l}A _ {i,l}x^{2i}(x^2+U)^{k-i}
$$

其中 $A _ {i,l}$ 是依赖于 $k,l$ 的正数。

对等式右边进行微分，有

$$
\begin{align*}
&\dfrac{\mathrm{d}^{2l}}{\mathrm{d}x^{2l}}\left(\sum _ {i=1}^{M _ l}a _ i(b _ ix+c _ i)^{2k+2l}\right) \\
&=\sum _ {i=1}^{M _ l}(2k+1)(2k+2)\cdots (2k+2l)b _ i^{2l}a _ i(b _ ix+c _ i)^{2k} \\
&=\sum _ {i=1}^{M _ l}a _ i^{\prime}(b _ ix+c _ i)^{2k} \\
&=\sum _ {i=1}^{M _ l}a _ i^{\prime}y _ i^{2k}
\end{align*}
$$

其中 $y _ i=\left| b _ ix+c _ i \right| $ 是一个非负整数且

$$
a _ i^{\prime}=(2k+1)(2k+2)\cdots (2k+2l)b _ i^{2l}a _ i
$$

是一个依赖于 $k,l$ 的非负有理数。则有，如果 $x$ 和 $U$ 是整数且 $U\geq 0$，则存在非负整数 $y _ 1,\cdots ,y _ M$ 使得

$$
\sum _ {i=0}^{l}A _ {i,l}x^{2i}(x^2+U)^{k-i}=\sum _ {i=1}^{M _ l}a _ i^{\prime}y _ i^{2k}
$$

令 $x$ 和 $T$ 是非负整数使得 $x^2<T$ ，因为 $A _ {l,l}$ 是一个正整数，则有 $x^2\leq A _ {l,l}T$，所以

$$
U=A _ {l,l}-x^2
$$

是一个非负整数。选择 $U$，我们有

$$
\begin{align*}
\sum _ {i=0}^{l}A _ {i,l}x^{2i}(x^2+U)^{k-i}&=\sum _ {i=0}^{l}A _ {i,l}x^{2i}(A _ {l,l}T)^{k-i} \\
&=\sum _ {i=0}^{l}A _ {i,l}A _ {l,l}^{k-i}x^{2i}T^{k-i} \\
&=A _ {l,l}^{k-l+1}\sum _ {i=0}^{l}A _ {i,l}A _ {l,l}^{l-i-1}x^{2i}T^{k-i} \\
&=A _ {l,l}^{k-l+1}\sum _ {i=0}^{l}B _ {i,l}x^{2i}T^{k-i}
\end{align*}
$$

其中 $B _ {l,l}=1$ 且

$$
B _ {i,l} = A _ {i,l}A _ {l,l}^{l-i-1}
$$

对于 $i=0,1,\cdots ,l-1$ 是正整数。令

$$
a _ i^{\prime}=\dfrac{a _ i^{\prime}}{A _ {l,l}^{k-l+1}}
$$

则有

$$
x^{2l}T^{k-l}+\sum _ {i=0}^{l-1}B _ {l,l}x^{2i}T^{k-i}=\sum _ {i=1}^{M _ l}a _ i^{\prime}y _ i^{2k}=\sum (2k)
$$

这就完成了证明。

定理 3.6：每个充分大的数都可以表示成有限个自然数 $k$ 次幂的和。

证明：使用归纳法。当 $k=1$ 时，显然成立。当 $k=2$ 时，根据[拉格朗日四平方和定理](拉格朗日四平方和定理.md)，成立。令 $k\geq 3$，假设对于所有的 $l<k$ 成立，则根据引理 3.5，对所有的 $2l$ 也成立。因此，存在一个整数 $r$，使得对每个非负整数 $n$，对于 $l=1,2,\cdots ,k-1$，等式

$$
n=x _ 1^{2l}+\cdots +x _ r^{2l}
$$

是成立的。（例如，我们可以选择 $r=\max\lbrace g(2l):l=1,2,\cdots,k-1 \rbrace$）。

令 $T\geq 2$。选择整数 $C _ 1,\cdots,C _ {k-1}$ 使得

$$
0\leq C _ l<T \quad l=1,\cdots ,k-1
$$

对于 $j=1,\cdots,r$ 和 $l=1,\cdots ,k-1$，存在非负整数 $x _ {j,l}$ 使得

$$
x _ 1^{2l}+\cdots +x _ r^{2l}=C _ {k-l}
$$

则

$$
x _ {j,l}^2\leq \sum _ {j=1}^{r}x _ {j,l}^{2i}\leq C _ {k-l}<T
$$

其中 $j=1,\cdots ,r$，$l=1,\cdots ,k-1$，$i=1,\cdots ,l$。根据引理 3.10，存在正整数 $B _ {i,l}$ 只取决于 $k,l$ 使得

$$
x _ {j,l}^{2l}T^{k-l}+\sum _ {i=0}^{l-1}B _ {i,l}x _ {j,l}^{2i}T^{k-i}=\sum (2k)=\sum (k)
$$

对于 $j=1,\cdots ,r$ 求和，有

$$
\begin{align*}
&C _ {k-l}T^{k-l}+\sum _ {i=0}^{l-1}B _ {i,l}T^{k-i}\sum _ {j=1}^{r}x _ {j,l}^{2i} \\
&=C _ {k-l}T^{k-l}+T^{k-l+1}\sum _ {i=0}^{l-1}B _ {i,l}T^{l-1-i}\sum _ {j=1}^{r}x _ {j,l}^{2i} \\
&=C _ {k-l}T^{k-l}+D _ {k-l+1}T^{k-l+1} \\
&=\sum (k)
\end{align*}
$$

其中

$$
D _ {k-l+1}=\sum _ {i=0}^{l-1}B _ {i,l}T^{l-1-i}\sum _ {j=1}^{r}x _ {j,l}^{2i}
$$

且 $l=1,\cdots ,k-1$。整数 $D _ {k-l+1}$ 完全取决于 $k,l,T$，且 $C _ {k-l}$ 与 $C _ {k-i} \quad i\neq l$ 无关。令

$$
B^{\ast }=\max \lbrace B _ {i,l}:l=1,\cdots ,k-1 \quad i=0,1,\cdots ,l-1 \rbrace
$$

则有

$$
\begin{align*}
&0\leq C _ {k-l}T^{k-l}+D _ {k-l+1}T^{k-l+1} \\
&=C _ {k-l}T^{k-l}+\sum _ {i=0}^{l-1}B _ {i,l}T^{k-i}\sum _ {j=1}^{r}x _ {j,l}^{2i} \\
&<B^{\ast}(T^{k-l+1}+rT^k+\sum _ {i=1}^{l-1}T^{k-i+1}) \\
&=B^{\ast} (rT^k+T^{k-l+1}\sum _ {i=0}^{l-1}T^{i}) \\
&<B^{\ast}(rT^k+\dfrac{T^{k+1}}{T-1}) \\
&<(r+2)B^{\ast}T^k
\end{align*}
$$

因为 $T\geq 2$，所以 $T/(T-1)\leq 2$，令

$$
C _ k=D _ 1=0
$$

则有

$$
\sum _ {l=1}^{k-1}(C _ {k-l}T^{k-l}+D _ {k-l+1}T^{k-l+1})=\sum _ {l=1}^{k}(C _ l+D _ l)T^l=\sum (k)
$$

且

$$
0\leq \sum _ {l=1}^{k}(C _ l+D _ l)T^l<(k-1)(r+2)B^{\ast}T^k=E^{\ast}T^k
$$

其中整数

$$
E^{\ast}=(k-1)(r+2)B^{\ast}
$$

依赖于 $k$，和 $T$ 无关。如果选择

$$
T\geq E^{\ast}
$$

则有

$$
0\leq \sum _ {l=1}^{k}(C _ l+D _ l)T^l<E^{\ast}T^k<T^{k+1}
$$

将式子展开

$$
\sum _ {l=1}^{k}(C _ l+D _ l)T^l=E _ 1T+\cdots +E _ {k-1}T^{k-1}+E _ kT^k
$$

其中

$$
0\leq E _ i <E^{\ast} \quad i=1,\cdots ,k-1
$$

且

$$
0\leq E _ k <E^{\ast}
$$

用这种方式，对 $(k-1)$ 元组 $(C _ 1,\cdots,C _ {k-1})$ 在 $\lbrace 0,1,\cdots,T-1 \rbrace$ 的每一种选择都决定了 $(k-1)$ 元组 $(E _ 1,\ddots,E _ {k-1})$ 在 $\lbrace 0,1,\cdots,T-1 \rbrace$ 的选择。我们接下来证明这是一个双射。

证明是满射就足够了。令 $(E _ 1,\cdots,E _ {k-1})$ 是整数 $\lbrace 0,1,\cdots,T-1 \rbrace$ 的一个 $k-1$ 元组。存在一个简单的算法产生整数 $C _ 1,\cdots,C _ {k-1}\in \lbrace 0,1,\cdots,T-1 \rbrace$ 使得上式满足一些非负整数 $E _ k<E^{\ast}$。令 $C _ 1=E _ 1$ 且 $I _ 2=0$。因为 $D _ 1=0$，我们有

$$
(C _ 1+D _ 1)T=E _ 1T+I _ 2T^2
$$

整数 $C _ 1$ 决定整数 $D _ 2$。选择 $C _ 2\in \lbrace 0,1,\cdots ,T-1 \rbrace$ 使得

$$
C _ 2+D _ 2+I _ 2\equiv E _ 2 \mod T
$$

则有

$$
C _ 2+D _ 2+I _ 2=E _ 2+I _ 3T
$$

其中 $I _ 3$ 是整数，且

$$
\sum _ {l=1}^{2}(C _ l+D _ l)T^l=\sum _ {l=1}^{2}E _ lT+I _ 3T^3
$$

整数 $C _ 2$ 决定 $D _ 3$。选择 $C _ 3\in \lbrace 0,1,\cdots ,T-1 \rbrace$ 使得

$$
C _ 3+D _ 3+I _ 3\equiv E _ 3\mod T
$$

则

$$
C _ 3+D _ 3+I _ 3\equiv E _ 3+I _ 4T
$$

对于一些整数 $I _ 4$，且

$$
\sum _ {l=1}^{3}(C _ l+D _ l)T^l=\sum _ {l=1}^{3}E _ lT+I _ 4T^4
$$

令 $2\leq j\leq k-1$，且假设我们构造了整数 $I _ j$ 且

$$
C _ 1,\cdots ,C _ {j-1}\in \lbrace 0,1,\cdots ,T-1 \rbrace
$$

使得

$$
\sum _ {l=1}^{j-1}(C _ l+D _ l)T^l=\sum _ {l=1}^{j-1}E _ lT+I _ jT^j
$$

存在唯一的整数 $C _ j\in \lbrace 0,1,\cdots ,T-1 \rbrace$ 使得

$$
C _ j+D _ j+I _ j=E _ j \mod T
$$

则有

$$
C _ j+D _ j+I _ j=E _ j+I _ {j+1}T
$$

存在整数 $I _ {j+1}$，且

$$
\sum _ {l=1}^{j}(C _ l+D _ l)T^l=\sum _ {l=1}^{j}E _ lT+I _ {j+1}T^{j+1}
$$

通过归纳法可以产生一个独一无二的整数序列 $C _ 1,\cdots ,C _ {k-1}\in \lbrace 0,1,\cdots ,T-1 \rbrace$ 使得

$$
\sum _ {l=1}^{k-1}(C _ l+D _ l)T^l=\sum _ {l=1}^{k-1}E _ lT+I _ {k}T^{k}
$$

因为 $C _ k=0$ 且 $C _ {k-1}$ 决定 $D _ k$，我们有

$$
0\leq \sum _ {l=1}^{k}(C _ l+D _ l)T^l=\sum _ {l=1}^{k-1}E _ lT^l+(D _ k+I _ k)T^k=\sum _ {l=1}^{k}E _ lT^l<E^{\ast}T^k
$$

其中 $D _ k+I _ k=E _ k$。因为

$$
0\leq \sum _ {l=1}^{k-1}E _ lT^l<T^k
$$

则有

$$
0\leq E _ k<E^{\ast}
$$

且

$$
\sum _ {l=1}^{k-1}E _ lT^l+E^{\ast}T^k<(1+E^{\ast})T^k\leq 2E^{\ast}T^k
$$

考虑到

$$
\sum _ {l=1}^{k}E _ lT^l=\sum _ {l=1}^{k}(C _ l+D _ l)T^l=\sum (k)
$$

因为 $E^{\ast}$ 只依赖于 $k$ 而不是 $T$，则有

$$
(E^{\ast}-E _ k)T^k=\sum (k)
$$

则有

$$
\sum _ {l=1}^{k-1}E _ lT^l+E^{\ast}T^k=\sum (k)
$$

对于每个 $(k-1)$ 元组 $(E _ 1,\cdots ,E _ {k-1})$，其中 $E _ l\in \lbrace 1,1,\cdots ,T-1 \rbrace$。选择整数 $T _ 0>5E^{\ast}$ 使得

$$
4(T+1)^k\leq 5T^k T\geq T _ 0 \text{对于所有的} T\geq T _ 0
$$

我们应该证明如果 $T\geq T _ 0$，$(F _ 0,\cdots ,F _ {k-1})$ 是任何的 $k$ 元组整数 $\lbrace 0,1,\cdots ,T-1 \rbrace$，则有

$$
F _ 0+F _ 1T+\cdots +F _ {k-1}T^{k-1}+4E^{\ast}T^l=\sum (k)
$$

令 $E _ 0^{\prime}\in \lbrace 0,1,\cdots ,T-1 \rbrace$，有

$$
\begin{align*}
E _ 0^{\prime}(T+1)+E^{\ast}(T+1)^k&<(T+1)^2+E^{\ast}(T+1)^k\\
&\leq (1+E^{\ast})(T+1)^k \\
&\leq 2E^{\ast}(T+1)^k
\end{align*}
$$

同时，我们有

$$
E _ 0^{\prime}(T+1)+E^{\ast}(T+1)^k=\sum (k)
$$

对于每个选择

$$
E _ 0^{\prime} ,E _ 1,\cdots ,E _ {k-1} \in \lbrace 0,1,\cdots,T-1 \rbrace
$$

我们有

$$
\begin{align*}
F^{\ast}&=(E _ 1T+\cdots +E _ {k-1}T^{k-1}+E^{\ast}T^k)+(E _ 0^{\prime}(T+1)+E^{\ast}(T+1)^k) \\
&=(E _ 0^{\prime}+E^{\ast})+(E-1+E _ 0^{\prime}+kE^{\ast})T+\sum _ {l=2}^{k-1}\left(E _ l+\binom{k}{l}E^{\ast}\right)T^l+2E^{\ast}T^k \\
&=\sum (k)
\end{align*}
$$

进一步的有

$$
0\leq F^{\ast}<4E^{\ast}(T+1)^k\leq 5E^{\ast}T^k<T^{k+1}
$$

因为 $4(T+1)^k\leq 5T^k$ 且 $T\geq T _ 0>5E^{\ast}$。所有的 $k$ 个数

$$
F _ 0,F _ 1,\cdots,F _ {k-1}\in \lbrace 0,1,\cdots ,T-1 \rbrace
$$

我们可以使用算法得到 $F _ k$ 和

$$
E _ 0^{\prime} ,E _ 1,\cdots ,E _ {k-1}\in \lbrace 0,1,\cdots ,T-1 \rbrace
$$

使得

$$
\begin{align*}
&F _ 0+F _ 1T+\cdots +F _ {k-1}T^{k-1}+F _ kT^k \\
&=E _ 1T+\cdots +E _ {k-1}T^{k-1}+E^{\ast}T^k+E _ 0^{\prime}(T+1)+E^{\ast}(T+1)^k \\
&=\sum (k)
\end{align*}
$$

且 $F _ k$ 是整数满足

$$
0\leq F _ k<5E^{\ast}
$$

加上 $(5E^{\ast}-F _ k)T^k=\sum (k)$，有

$$
F _ 0+F _ 1T+\cdots +F _ {k-1}T^{k-1}+5E^{\ast}T^k=\sum (k)
$$

对于所有的 $T\geq T _ 0$ 且 $F _ 0,\cdots F _ {k-1}$ 的所有的选择。这证明了如果 $T\geq T _ 0$ 且

$$
5E^{\ast}T^k\leq n< (5E^{\ast}+1)T^k
$$

则 $n=\sum (k)$。

存在一个整数 $T _ 1\geq T _ 0$ 使得

$$
5E^{\ast}(T+1)^k < (5E^\ast+1)T^k \text{对于所有的} T\geq T _ 1
$$

则如果 $T\geq T _ 1$ 且

$$
5E^{\ast}T^k\leq n< (5E^{\ast}+1)T^k
$$

则有 $n=\sum (k)$。

因为对于每个整数 $n\geq 5E^{\ast}T _ 1^k$ 在一些 $T\geq T _ 1$ 满足上述不等式，我们有

$$
n=\sum (k) \text{对于所有的} n\geq 5E^{\ast}T _ 1^k
$$

根据引理 3.9 可知华林问题对于 $k$ 成立。

