# 群论课程笔记

## Introduction

1. 19th century：roots of polynomials.
2. 20th century: play a major role in physics.  the groups of diffeomorphism symmetries of manifolds.
3. since 1950s.  organize the zoo of subatomic particles,  formulate the Hamiltonian that governs interactions of elementary particles one must have some understanding of the theory of Lie algebras, Lie groups, and their representations.
4. late 20th and early 21st century.  essential in many areas of physics including atomic, nuclear, particle, and condensed matter physics.

### Equivalence Relations

> **Definition 1.1.1** Let X be any set. A binary relation ~ is an *equivalence relation* if $\forall a,b,c \in \bf{X}$
>
> 1. $a\sim a$
> 2. $a\sim b \Rightarrow b\sim a$
> 3. $a\sim b$ and $b\sim c \Rightarrow a\sim b$

**Example 1.1.1** ：$=$ 符合要求.
**Example 1.1.2** ：$\mathtt X = \mathbb A$, $a \sim b$,如果$a-b$为常数.

>**Definition 1.1.2** Let $\sim$ be an equivalence relation on $\mathtt X$. The *equivalence class* of an element $a$ is the subset 
>$$ [a]: =\{x \in \mathtt X: x\sim a\} \subset \mathtt X$$ 

### Groups:Basic Definitions and Examples

>**Definition 2.1** A group is a quartet $(G,\bf{m},\bf{I},e)$where
>1. G is a set.
>2. $\bf{m}: G × G \rightarrow G$ is a map, called the *group multiplication map*.
>3. $\bf{I}: G × G \rightarrow G$  is a map, called the *inverse map*.
>4. $e \in G$ is a distinguished element of G called the $identity \quad element$.

这些 $(G,\bf{m},\bf{I},e)$,需要满足以下的条件：
1. $\bf{m}$ is *associative*:对任意的$g_1,g_2,g_3 \in G$,有
   $$\bf{m}(\bf{m}(g_1,g_2),g_3) = \bf{m}(g_1,\bf{m}(g_2,g_3)) $$
2. $\forall g \in G \quad\quad \bf{m}(g,e) = \bf{m}(e,g) = g$
3. $\forall g \in G \quad\quad \bf{m}(\bf{I}(g),g) = \bf{m}(g,\bf{I}(g)) = e$
   
#### Remarks
1. 我们常常把$e$写作1，如果同时讨论超过一个群，我们把群$G$写作$1_G$.identity element 又常被称作 *unit element*,尽管*unnit*在环等场景中有其他的意思.
2. *monoid*(流形)具有映射关系$\bf{m} = M × M \rightarrow M$,如果有单位元$e \in M$起到*unital monoid*的作用（单位流形？），那么该流形就是一个群.
3. 还有很多更深的数学结构可以用来定义群.例如拓扑群，在其中的映射关系都是拓扑空间之间的连续映射.同样也可以定义李群.
4. 通常我们用$G$来表示$(G,\bf{m},\bf{I},e)$. 

>**Definition 2.4** Let $G_1,G_2$ be two groups. The *direct product* of $G_1,G_2$ is the set $G_1 × G_2$ with product:
>$$ \bf{m}_{G_1×G_2}\left( (g_1,g_2),(g'_1,g'_2)\right) = (\bf{m}_{G_1} (g_1,g'_1),\bf{m}_{G_2}(g_2,g'_2)) $$


