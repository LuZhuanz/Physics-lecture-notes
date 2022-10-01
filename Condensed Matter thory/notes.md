# Condensed Matter Theory

## 1. From Particles to Fields

为了介绍场论的基本原理，我们首先考虑两个基本模型.第一个是对固体的一维近似模型(a one-dimensional “caricature” of a solid),第二个是自由传播的电磁场.

举例：一块典型的金属/导体可以用多体哈密顿量来描述: $H = H_e+H_i+Hei$,其中

$$
H_e = \sum_i\frac{\bf{P}^2_i}{2m}+\sum _{i<j}V_{ee}(\bf{r}_i-\bf{r}_j),
$$

$$
H_i = \sum_{I}\frac{\bf{P}^2_i}{2M} + \sum _{I<J}V_{ii}(\bf {R}_I-\bf{R}_J),
$$

$$
H_{ei} = \sum_{iI}V_{ei}(\bf{R}_{I}-\bf{r}_i).
$$

$H_e,H_i$和$H_{ei}$分别表示电子、离子和电子离子之间相互作用的动力学.像上式中的哈密顿函数含有丰富的动力学信息.我们不能像通常一样从基本的问题出发来解决这种多体问题，比如把所有成分的自由度处理为相同.

怎样建立对这些体系的分析模型呢？以下是一些基本原则.

1. **结构上的简化**： 在上式中的量并不需要被同时考虑.例如当我们考虑离子之间的关系时，电子之间的关系就可以忽略.同样，电子之间的相互作用大多是独立于离子的.
2. 在大多数情况下，我们对系统总的能谱不感兴趣，而是更关心体系在低能环境下的动力学.部分因为实际的需要，部分因为在低能状态下体系会呈现一些更为普遍的特征.
3. 对大部分我们关心的系统，它们的自由度都非常大( $N = \mathtt O (10^{23})$ ).然而这种庞大数目是一种优势，我们可以使用统计力学的概念和工具来解决问题.在如此大的数目下，统计误差会变得很小.
4. 凝聚态系统中会展现出很多内在的**对称性**.

在以下的内容里我们将会看到低能态动力学下的一些结论，与场论有关.

### 1.1 Classical harmonic chain: phonons

我们将离子视为经典的粒子,并且忽略与电子的关系,有  $H_e = H_ei = 0$的位置 $R_I \equiv \overline R_I = I_a$处于一个固定的有规律的位置.对于任何对平衡位置的偏移，都会产生势能的变化.在低能下，势能函数可以写成二次形.

简化后的哈密顿量可以写为

$$H = \sum _{I = 1}^{N}\left[\frac{P_I^2}{2M}+\frac{k_s}{2}(R_{I+1}-R_I-a)^2 \right]$$

与这个哈密顿量相关的拉格朗日函数为

$$L = T -U = \sum _{I = 1}^{N}\left[\frac{M\dot R_I^2}{2}-\frac{k_s}{2}(R_{I+1}-R_I-a)^2 \right]$$

在 $N$ 非常大的系统里，我们可以认为边界效应可以忽略，我们可以把原子链视为一个环.有边界条件 $R_{N+1}=R_1$.我们假设偏离是很小的( $|R_I(t)-\overline R_I|\ll a$),可以写作 $R_I(t) = \overline R_I + \phi_I(t) (\phi_{N+1} = \phi_1)$,有

$$L = \sum_{I=1}^{N}\left[\frac{M}{2}\dot \phi^2_I - \frac{k_s}{2}(\phi_{I+1}-\phi_I)^2 \right]$$

在 $N$ 非常大或者趋向于无穷时，问题将会得到极大简化，这也被称为 **连续极限**(continum limit)

在此极限下，可以使用泰勒展开来展开这些函数

$$ \phi_I \rightarrow a^{1/2}\phi(x)|_{x=Ia}, \phi_{I+1}-\phi_I \rightarrow a^{3/2}\partial_x\phi(x)|_{x = Ia},\sum_{I=1}^N\rightarrow \frac{1}{a}\int_{0}^{L}dx,$$

其中 $L = Na$ .拉格朗日函数可以写为

$$ L[\phi] = \int_{0}^{L} dx \mathfrak{L} (\phi,\partial_x\phi,\dot\phi),\mathfrak{L}(\phi,\partial_x\phi,\dot\phi) = \frac{m}{2}\dot\phi^2-\frac{k_sa^2}{2}(\partial_x\phi)^2$$

#### INFO
$\phi$ 就是一种“场”.场是一个光滑的映射

$$ \phi: M \rightarrow T,z \rightarrow \phi(z)$$

从一个特定的流形 $M$ ,一般被称为"base manifold",映射到一个 "target" 或者 "field manifold" $T$.

**拉格朗日密度(Lagrangian density)** 是[能量]/[长度]的量纲.类似的,我们有连续形式的运动方程

$$ S[\phi] = \int dt \,L[\phi] = \int \int_{0}^{L}dx\, \mathfrak{L}(\phi,\partial_x\phi,\dot\phi).$$

虽然哈密顿函数已经包含了系统的全部信息，但是我们仍然不能了解它的具体行为.为了从函数中获得准确的物理信息，我们需要得到他的运动方程(equationsn of motion).

我们让 $\phi(x,t) \rightarrow \phi(x,t) +\epsilon\eta(x,t)$ ,并且使得其展开式的第一项为0，则有

$$ S[\phi+\epsilon\eta]-S[\phi] = -\int dt \int_{0}^{L} dx(m\dot\phi\dot\eta - k_sa^2\partial_x\phi\partial_x\eta) + O(\epsilon^2)$$

对其分步积分，则有

$$ \lim_{\epsilon \rightarrow 0} \frac{1}{\epsilon}(S[\phi +\epsilon\eta]-S[\phi])=-\int dt \int_0^Ldx(m\ddot\phi-k_sa^2\partial^2_x\phi)\eta \neq 0 $$

由于是变分，积分号内为0，得到波动方程

$$(m\partial^2_t - k_sa^2\partial^2_x) = 0$$

这个方程的一般形式解为 $\phi_{+}(x-vt)+\phi_{-}(x+vt)$ 其中 $v = a\sqrt{k_s/m}$

#### *Hamiltonian formulation*

解释能量问题. 考虑拉格朗日密度,定义

$$ \pi (x) \equiv \frac{\partial(\phi,\partial_x\phi, \dot\phi)}{\partial\dot\phi(x)}$$

为与 $\phi$ 有关的**canonical momentum**.和 $\phi$ 一样，动量 $\pi$ 也是一个连续的自由度. 

哈密顿密度由Legendre变换定义

$$ H(\phi,\partial_x\phi,\pi) =\left(\pi\dot{\phi}-\mathfrak{L}(\phi,\partial_x\phi,\dot\phi) \right)\mid_{\dot{\phi}=\dot{\phi}(\phi,\pi)}$$

#### EXERCISE

Verify that the transition $L → H$ is a straightforward continum generalization of the Legendre transformation of the N-particle Lagrangian L($\{\phi_I\}, \{\dot\phi_I \}$).






### 1.2 Functional analysis and variational principles

$$ F[f+\epsilong]-F[f] = \epsilon\doteqDF_f[g]+ \mathfrak{O}(\epsilon^2)$$

其中 $DF_f$ 为线性函数， $\epsilon$ 为小的参数.

### 1.3  Maxwell’s equations as a variational principle

### 1.4 Quantum chain

### 1.5 Quantum electrodynamics

### 1.6 Noether’s theorem

### 1.7 Summary and outlook

### 1.8 Problems


## 2 Second quantization

本章节介绍并应用了二次量子化的方法.这种方法支撑了多体量子力学理论.