---
layout: post
title:  "On (co)Cartesian Fibrations"
date:   2023-05-15 01:30:03 +0000
categories: jekyll update
katex: True
excerpt_separator: <!--more-->
---

Let's start by enunciating a recurring idea in mathematics: *objects do not exist in isolation, but tend to occur in families*. This might sound a bit vague at first blush, so let us consider the case of covering spaces/maps 

$$E \xrightarrow{f} B$$

which can be thought of as a **family** of sets parameterized by a space $$B$$: these assemble as the following collection of sets $$\{F^{-1}(b)\}_{b\in B}$$, where for each point $$b\in B$$, the fiber $$f^{-1}(b)\subset E$$ is a set.

This construction furnishes an isomorphism 

$$\mathsf{Cov}(B)\simeq [B,\mathcal{S}\mathsf{et}^{\simeq}]$$

from the set of covering spaces of $$B$$ and the set of homotopy classes of maps $$B\rightarrow \mathcal{S}\mathsf{et}^{\simeq}$$.

We should then ask ourselves: If $$\mathcal{B}$$ is a "space" whose morphisms are not all invertible - that is if $$\mathcal{B}$$ is an $$\infty$$-category -, then what, exactly is classified by a map $$\mathcal B \rightarrow \mathcal{S}\mathsf{et}$$? 
