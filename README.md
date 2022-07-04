# websites

这是对 $Github$ 的公式的测试

$$ x^2\equiv 0\pmod 6 $$

$$
\begin{align*}
x&=1+1 \\
&=x+2+2
\end{align*}
$$

$$
f(x)=\begin{cases}
x &\text{hello}\\
x+2+2 &\text{test}
\end{cases}
$$

# 阿佩里定理

## 简介

$\zeta(3)$ 是无理数。

## 证明

### 方法 1

对于每个非负整数 $n=0,1,2,\cdots $，定义有理函数

$$ R _ n:=\left( \dfrac{(t-1)\cdots (t-n)}{t(t+1)\cdots (t+n)} \right)^2 $$

定义 $D _ n$ 为 $1,2,\cdots ,n$ 的最小公倍数，并且 $D _ 0=1$。

引理 1：等式

$$ F _ n:=-\sum _ {t=1}^{\infty }R _ n^{\prime}(t)=u _ n\zeta(3)-v _ n \tag{1} $$

成立。其中 $u _ n\in \mathbb{Z}$，$D _ n^3v _ n\in \mathbb{Z}$。

证明：根据

$$
\dfrac{1}{t+k}\cdot\dfrac{1}{t+l}=\dfrac{1}{l-k}\cdot\left( \dfrac{1}{t+k}-\dfrac{1}{t+l} \right) \quad k\neq l
$$

注意到

$$
\dfrac{(t-1)\cdots (t-n)}{t(t+1)\cdots (t+n)}=\sum _ {k=0}^{n}\dfrac{(-1)^{n-k}\binom{n+k}{n}\binom{n}{k}}{t+k}
$$

则有公式

$$
R _ n(t)=\sum _ {k=0}^{n}\left( \dfrac{A _ {2k}^{(n)}}{(t+k)^2}+\dfrac{A _ {1k}^{(n)}}{t+k} \right)
$$

其中 $A _ {jk}=A _ {jk}^{(n)}$ 满足

$$
A _ {2k}=\binom{n+k}{n}^2\binom{n}{k}^2\in \mathbb{Z} \quad \text {且} \quad D _ nA _ {1k}\in \mathbb{Z} \quad k=0,1,\cdots ,n \tag{2}
$$

更进一步的

$$
\sum _ {k=0}^{n}A _ {1k}=\sum _ {k=0}^{n}\operatorname{Res} _ {t=-k}R _ n(t)=-\operatorname{Res} _ {t=\infty }R _ n(t)=0
$$

因为当 $t\rightarrow \infty $ 时，$R _ {n}(t)=O(t^{-2})$，则

$$
\begin{align*}
F _ n&=\sum _ {t=1}^{\infty}\sum _ {k=0}^{n}\left( \dfrac{2A _ {2k}}{(t+k)^3}+\dfrac{A _ {1k}}{(t+k)^2} \right) \\
&=\sum _ {k=0}^{n}\sum _ {l=k+1}^{\infty }\left( \dfrac{{2A _ {2k}}}{l^3}+\dfrac{A _ {1k}}{l^2} \right) \\
&=2\sum _ {k=0}^{n}A _ {2k}\left( \sum _ {l=1}^{\infty }-\sum _ {l=1}^{k} \right)\dfrac{1}{l^3}+\sum _ {k=0}^{n}A _ {1k}\left( \sum _ {l=1}^{\infty }-\sum _ {l=1}^{k} \right)\dfrac{1}{l^2}
\end{align*}
$$

有 $(1)$ 的形式，其中

$$
u _ n=2\sum _ {k=0}^{n}A _ {2k},\quad v _ n=2\sum _ {k=0}^{n}A _ {2k}\sum _ {l=1}^{k}\dfrac{1}{l^3}+\sum _ {k=0}^{n}A _ {1k}\sum _ {l=1}^{k}\dfrac{1}{l^2} \tag{3}
$$

最终，使用 $(2)$ 且

$$
D _ n^j\sum _ {l=1}^{k}\dfrac{1}{l^j}\in\mathbb{Z} \quad k=0,1,\cdots ,n\quad j=2,3
$$

我们推断出 $u _ n\in \mathbb{Z}$ 和 $D _ n^3v _ n\in \mathbb{Z}$。

因为

$$
R _ 0(t)=\dfrac{1}{t^2},\quad R _ 1(t)=\dfrac{1}{t^2}+\dfrac{4}{(t+1)^2}-\dfrac{4}{t}+\dfrac{4}{t+1}
$$

根据公式 $(3)$ 我们发现

$$
F _ 0=2\zeta(3) \text{且} F _ 1=10\zeta(3)-12 \tag{4}
$$

我们接下来定义一个有理函数 $S _ n(t):=s _ n(t)R _ n(t)$，其中

$$
s _ n(t):=4(2n+1)(-2t^2+t+(2n+1)^2) \tag{5}
$$

引理 2：对于每个 $n1,2,\cdot $，等式

$$
(n+1)^3R _ {n+1}(t)-(2n+1)(17n^2+17n+5)R _ n(t)+n^3R _ {n-1}(t)=S _ n(t+1)-S _ n(t) \tag{6}
$$

成立。

证明：将上式两边同时除以 $R _ {n}(t)$ 验证两边则有

$$
(n+1)^3\left( \dfrac{t-n-1}{t+n+1} \right)^2-(2n+1)(17n^2+17n+5)+n^3\left( \dfrac{t+n}{t-n} \right)^2=s _ n(t+1)\left( \dfrac{t^2}{(t-n)(t-n+1)} \right)^2-s _ n(t)
$$

其中 $s _ n(t)$ 是 $(5)$ 中定义的。

引理 3：式 $(1)$ 满足差分方程

$$
(n+1)^3u _ {n+1}-(2n+1)(17n^2+17n+5)u _ n+n^3u _ n=0 \tag{7}
$$

其中 $n=1,2,\cdots $

证明：因为 $R _ n^{\prime}(t)=O(t^{-3})$ 且 $S _ n^{\prime }(t)=O(t^{-2})$，对 $(6)$ 差分并对 $t=1,2,\cdots $ 求和，我们得到等式

$$
(n+1)^3F _ {n+1}-(2n+1)(17n^2+17n+5)F _ n+n^3F _ {n-1}=S _ n^{\prime}(1)
$$

对于 $n\geq 1$，函数 $R _ n(t)$ 和 $S _ n(t)=s _ n(t)R _ n(t)$ 在 $t=1$ 处都有一个二阶零点。则对于 $n=1,2,\cdots $，$S _ n^{\prime}(1)=0$。

考虑另一个有理函数

$$
\widetilde{R} _ n(t):=n!^2(2t+n)\dfrac{(t-1)\cdots (t-n)(t+n+1)\cdots (t+2n)}{(t(t+1)\cdots (t+n))^4} \tag{8}
$$

对应的超几何级数

$$
\widetilde{F} _ {n}:=\sum _ {t=1}^{\infty }\widetilde{R} _ n(t) \tag{9}
$$

引理 4：对于每一个 $n=0,1,2,\cdots $ 有不等式

$$
0<\widetilde{F} _ n<20(n+1)^4(\sqrt{2}-1)^{4n} \tag{10}
$$

证明：因为对于 $t=1,2,\cdots ,n$，$\widetilde{R} _ n(t)=0$ 且对于 $t>n$ 可以推断有 $\widetilde{F} _ n>0$。

根据不等式

$$
\dfrac{1}{m}\dfrac{(m+1)^m}{m^{m-1}}=\left( 1+\dfrac{1}{m} \right)^m< e<\left( 1+\dfrac{1}{m} \right)^{m+1}=\dfrac{1}{m}\dfrac{(m+1)^{m+1}}{m^{m}}
$$

得出对于 $m=1,2,\cdots $，$(m+1)^m/m^{m-1}<em<(m+1)^{m+1}/m^m$。我们可以推出

$$
e^{-n}\dfrac{(m+n)^{m+n-1}}{m^{m-1}}<m(m+1)\cdots (m+n-1)<e^{-n}\dfrac{(m+n)^{m+n}}{m^m}
$$

因此，对于整数 $t\geq n+1$

$$
\begin{align*}
\widetilde{R} _ {n}(t)\dfrac{(t+n)^5}{(2t+n)(t+2n)}&=n!^2\dfrac{(t-1)\cdots (t-n)(t+n+1)\cdots (t+2n)}{(t(t+1)\cdots (t+n-1))^4} \\
&<(n+1)^{2(n+1)}\dfrac{t^{5t-4}(t+2n)^{t+2n}}{(t-n)^{t-n}(t+n)^{5(t+n)-4}}
\end{align*}
$$

则有

$$
\begin{align*}
\widetilde{R} _ {n}(t)\dfrac{t^4(t+n)}{(2t+n)(t+2n)(n+1)^2}
&<(n+1)^{2n}\dfrac{t^{5t}(t+2n)^{t+2n}}{(t-n)^{t-n}(t+n)^{5(t+n)}} \\
&=\left( 1+\dfrac{1}{n} \right)^{2n}e^{nf(t/n)}<e^2\left( \sup _ {\tau >1}e^{f(\tau)} \right)^n
\end{align*} \tag{11}
$$

其中

$$
f(\tau):=\log \dfrac{\tau^{5\tau}(\tau+2)^{\tau+2}}{(\tau-1)^{\tau-1}(\tau+1)^{5(\tau+1)}}
$$

方程

$$
f^{\prime}(\tau)\log \dfrac{\tau^{5}(\tau+2)}{(\tau-1)(\tau+1)^{5}}=0
$$

的唯一的满足 $\tau >1$ 的实数根 $\tau _ 0$ 是多项式

$$
\tau^5(\tau+2)-(\tau-1)(\tau+1)^5=-\left( \tau+\dfrac{1}{2} \right)\left( 2\left( \tau+\dfrac{1}{2} \right)^4-5\left( \tau+\dfrac{1}{2} \right)^2 -\dfrac{7}{8}\right)
$$

的零点。则有

$$
\tau _ 0=-\dfrac{1}{2}+\sqrt{\dfrac{5}{4}+\sqrt{2}}
$$

因此

$$
\sup _ {\tau>1}f(\tau)=f(\tau _ 0)=f(\tau _ 0)-\tau _ 0f^{\prime}(\tau _ 0)=2\log (\tau _ 0+2)+\log (\tau _ 0-1)-5\log (\tau _ 0+1)=4\log (\sqrt{2}-1)
$$

继续估计 $(11)$，有

$$
\widetilde{R} _ {n}(t)\dfrac{t^4(t+n)}{(2t+n)(t+2n)}<e^2(n+1)^2(\sqrt{2}-1)^{4n} \tag{12}
$$

最终，我们使用 $(12)$ 估计 $(10)$

$$
\begin{align*}
\widetilde{F} _ n&=\sum _ {t=n+1}^{\infty }\widetilde{R} _ n(t)<e^2(n+1)^2(\sqrt{2}-1)^{4n}\sum _ {t=n+1}^{\infty }\dfrac{(2t+n)(t+2n)}{t^4(t+n)}\\
&<e^2(n+1)^2(\sqrt{2}-1)^{4n}\sum _ {t=n+1}^{\infty }\left( \dfrac{2}{t^5}+\dfrac{5n}{t^4}+\dfrac{2n^2}{t^3} \right) \\
&\leq e^2(n+1)^2(2\zeta(5)+5n\zeta(4)+2n^2\zeta(3))(\sqrt{2}-1)^{4n}<20(n+1)^4(\sqrt{2}-1)^{4n}
\end{align*}
$$

这就完成了证明。

$$
\begin{align*}
\widetilde{S} _ n(t):=&\dfrac{\widetilde{R} _ n(t)}{(2t+n)(t+2n-1)(t+2n)}\cdot (-t^6-(8n-1)t^5+(4n^2+27n+5)t^4 \\
&+2n(67n^2+71n+15)t^3+(358n^4+339n^3+76n^2-7n-3)t^2 \\
&+(384n^5+396n^4+97n^3-29n^2-17n-2)t \\
&+n(153n^5+183n^4+50n^3-30n^2-22n-4))
\end{align*} \tag{13}
$$

引理 5：对于 $n=1,2,\cdots $，等式

$$
(n+1)^3\widetilde{R} _ {n+1}(t)-(2n+1)(17n^2+17n+5)\widetilde{R} _ n(t)+n^3\widetilde{R} _ {n-1}(t)=\widetilde{S} _ n(t+1)-\widetilde{S} _ n(t) \tag{14}
$$

成立。

证明：两边同时除以 $\widetilde{R} _ n(t)$ 验证。

引理 6:对于 $n=1,2,\cdots $，$(9)$ 满足差分方程 $(7)$。

证明：因为当 $t\rightarrow \infty $，$n\geq 1$ 时，$\widetilde{R} _ n^(t)=O(t^{-5})$ 且 $\widetilde{S} _ n(t)=O(t^{-2})$，对 $(14)$ 在 $t=1,2,\cdots $ 求和，我们得到等式

$$
(n+1)^3\widetilde{F} _ {n+1}-(2n+1)(17n^2+17n+5)\widetilde{F} _ n+n^3\widetilde{F} _ {n-1}=-\widetilde{S} _ n^{\prime}(1)
$$

对于 $n\geq 1$，函数 $(8)$ 和 $(13)$ 在 $t=1$ 处都有一个零点。则对于 $n=1,2,\cdots $，$\widetilde{S} _ n^{\prime}(1)=0$。

引理 7：对于 $n=0,1,2,\cdots $，$(1)$ 和 $(9)$ 时一致的。

证明：因为 $F _ n$ 和 $\widetilde{F} _ n$ 都满足同样的二阶差分方程 $(7)$，我们验证 $F _ 0=\widetilde{F} _ 0$ 且 $F _ 1=\widetilde{F} _ 1$。直接计算表明

$$
\widetilde{R} _ 0(t)=\dfrac{2}{t^3},\quad \widetilde{R} _ 1(t)=-\dfrac{2}{t^4}+\dfrac{2}{(t+1)^4}+\dfrac{5}{t^3}+\dfrac{5}{(t+1)^3}-\dfrac{5}{t^2}+\dfrac{5}{(t+1)^2}
$$

因此 $\widetilde{F} _ 0=2\zeta(3)$ 且 $\widetilde{F} _ 1=10\zeta (3)-12$

假设 $\zeta =p/q$，其中 $p$ 和 $q$ 时正整数。则使用 $D _ n<3^n$，我们推断，对于每个 $n=0,1,2,\cdots $，整数 $qD _ n^3F _ n=D _ n^3u _ np-D _ n^3v _ nq$ 满足估计

$$
0<qD _ n^3F _ n<20q(n+1)^43^{2n}(\sqrt{2}-1)^{4n} \tag{15}
$$

然而这是不可能的，因为对于充分大的整数 $n$，式子左边是一个正整数，式子右边却比 $1$ 小。

因此，$\zeta(3)$ 是无理数。
