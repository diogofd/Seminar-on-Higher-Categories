---
layout: post
title:  "Companion Note on Factorization Homology & Algebras"
date:   2023-05-18 01:30:03 +0000
categories: jekyll update
katex: True
excerpt_separator: <!--more-->
---

**Let me expand on some additional curiosities, examples and obsevations about Factorization Homology:**

### 1 - Actions of the Mapping Class Group
Take $$(\mathcal{S},\otimes)$$ to be a target symmetrix monoidal $$(\infty,1)$$-category, and consider $$A\colon \mathcal{D}\mathsf{isk}_2^{\mathsf{or}}\rightarrow \mathcal{S}$$ to be an (oriented) $$\mathbb{E}_2$$-algebra in $$\mathcal{S}$$. Then consider, for any genus $$g$$ oriented surface $$\Sigma_{g}$$, the Lie group $$\mathsf{Diff}^{+}(\Sigma_g)$$, of orientation-preserving diffeomorphisms of $$\Sigma_g$$. Not that this corresponds to the automorphisms of $$\Sigma_g$$ in $$\mathsf{M}\mathsf{fld}_{2}^{\mathsf{or}}$$, and therfore factorization homology furnishes a map 
$$\mathsf{Diff}^{+}(\Sigma_g)=\mathsf{hom}_{\mathcal{M}\mathsf{fld}_2^{\mathsf{or}}}(\Sigma_g,\Sigma_g) \rightarrow \mathsf{hom}_{\mathcal{S}}\Big(\int_{\Sigma_{g}}A,\int_{\Sigma_{g}}A\Big)$$
Taking connected components, we get an action of the mapping class group on $$\pi_0$$ of the object on the right hand side, and in the case that $$\mathcal{S}^{\otimes}=\mathsf{LinCat}_{\mathbb{k}}^{\times}$$, this recovers well-known actions on certain invariants of quantum groups.

### 2 - Pushforward Property
Factorization homology enjoys a Fubini-like property. This is often called the **pushforward property**. In its "simpler" guise it states that, for manifolds $$M^{m},N^{n}$$ (with superscript indicating dimension), we get the following equivalence 

$$\int_{M\times N}A \simeq \int_{M}\bigg(\int_{N\times \mathbb{R}^m}A\bigg)$$

To make sense of it, one should note that $$\int_{N\times \mathbb{R}^m}A$$ is an $$\mathbb{E}_m$$-algebra, much like we saw that $$\int_{M\times \mathbb{R}} A$$ was an $$\mathbb{E}_1$$-algebra. In its fancier, and evidently more general form, it says that given a map $$f\colon M^m \rightarrow N^n$$ which fibers over the interior and boundary of $$N$$, and for $$A$$ an $$\mathbb{E}_m$$-algebra, we get an equivalence 

$$\int_{N}f_{\ast}A \simeq \int_{M}A.$$ 

Where $$(f_\ast A)(U):=\int_{f^{-1}(U)}A$$. To recover the Fubini-looking identity we choose $$\pi_{M}\colon M\times N \rightarrow M$$, in this case $$f^{-1}(\mathbb{D}^m)=\mathbb{D}^m\times N$$, as expected.

### 3 - Factorization homology as ordinary homology
  
Factorization homology, in its version using $$\mathsf{Ch}_{\mathbb{Z}}^{\oplus}$$ as a target symmetric monoidal category, recovers "usual" homology of CW-complexes à la Eilenberg-Steenrod. Note that in this case $$\oplus$$ corresponds to the coproduct in the category, and as such forces any $$\mathbb{E}_n$$-algebra $$V\oplus V \rightarrow V$$ to be simple addition of chains.

We define the following chain complex 

$$\mathsf{C}_\ast(-;V):=\int_{-}V$$ 

and we call it "formal singular chains with coefficients in $$V$$". Consider the $$\otimes$$-excision axiom:

$$\mathsf{C}_\ast(X_{1}\underset{X_1 \cap X_2}{\sqcup} X_2;V)\simeq \mathsf{C}_\ast(X_1;V)\underset{\mathsf{C}_\ast (X_1 \cap X_2;V)}{\bigotimes} \mathsf{C}_\ast(X_2;V)$$

In this case, the module structure has to be also given by addition i.e. this is the right $$\mathsf{C}_\ast(X_1\cap X_2;V)$$-module structure map

$$\mathsf{C}_\ast(X_1;V)\oplus \mathsf{C}_\ast(X_1\cap X_2;V)\xrightarrow{(-+-)} \mathsf{C}_\ast(X_1;V).$$

This means that the relative tensor product of modules is given by the coequalizer

$$\mathsf{coeq}\Big(\mathsf{C}_\ast(X_1;V)\oplus \mathsf{C}_\ast(X_1\cap X_2;V) \oplus \mathsf{C}_\ast(X_2;V) \substack{\longrightarrow\\[-1em] \longrightarrow \\} \mathsf{C}_\ast(X_1;V)\oplus \mathsf{C}_\ast(X_2;V)\Big)$$ 

where the top arrow is the right module structure map, and the bottom one the left-module structure map. We can recast in more familiar terms as the cokernel 

$$\mathsf{coker}\Big(\mathsf{C}_\ast(X_1\cap X_2;V)\xrightarrow{(x,-x)} \mathsf{C}_\ast(X_1;V)\oplus \mathsf{C}_\ast(X_2;V)\Big)$$. This is an injective map, and so all put together we get a short exact sequence of chain complexes 

$$0 \rightarrow \mathsf{C}_\ast(X_1\cap X_2;V) \xrightarrow{(x,-x)} \mathsf{C}_\ast(X_1;V)\oplus \mathsf{C}_\ast(X_2;V) \xrightarrow \mathsf{C}_\ast(X_1\cup X_2;V)\xrightarrow 0$$

and this can be seen as the Mayer-Vietoris sequence which "universally" characterizes singular homology. From this, we can then conclude that 

$$\int_X V$$

are actual singular chains in $$X$$ with coefficients in $$V$$, and $$\otimes$$-excision translates to Mayer-Vietoris.

### 4 - Where to look for $$\mathbb{E}_n$$-algebras?

1. Fix a base ring $$R$$, letting the target symmetric monoidal $$(\infty,1)$$-category be $$\mathcal{C}\mathsf{hain}_{R}^{\otimes_{R}^{\mathbb{L}}}$$ whose objects are chain complexes of $$R$$-modules, and whose symmetric monoidal structure is given by the derived tensor product $$\otimes_R ^{\mathbb{L}}$$. A commutative $$R$$-algebrea is an $$\mathbb{E}_n$$-algebra in $$\mathcal{C}\mathsf{hain}_{R}^{\otimes_{R}^{\mathbb{L}}}$$ for any $$n$$. More generally, a cdga (a commutative dg algebra) is an $$\mathbb{E}_n$$-alegbra for all $$n$$.

2. The Hochschild cochain complex of any associative algebra (or dg algebrea, or $$A_{\infty}$$-algebra) is an exmaple of an $$\mathbb{E}_2$$-algebra in $$\mathcal{C}\mathsf{hain}_{\mathbb{k}}^{\otimes_\mathbb{k}}$$. 


3. $$n$$-fold loop spaces are $$\mathbb{E}_n$$-algebras in $$\mathcal{T}\mathsf{op}^{\times}.$$

4. The free $$\mathbb{E}_n$$-algebra on one generator (in $$\mathcal{T}\mathsf{op}^{\times}$$) is $$\mathsf{Conf}(\mathbb{R}^n)$$ - the unordered configuration space of $$\mathbb{R}^n$$.

5. $$\mathbb{E}_n$$-algberas are also often constructed as deformations of commutative or cocommutative objects. The braided monoidal category of representations of the quantum group $$\mathsf{U}_q(\mathfrak{g})$$ is obtained by deforming a cocommutative Hopf algebra (the universal enveloping algebra of $$\mathfrak{g}$$).


## References:

1.
