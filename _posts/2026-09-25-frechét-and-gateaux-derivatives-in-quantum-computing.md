---
title: Fréchet and Gateaux derivatives in Quantum Computing
date: 2026-09-25T18:07:00
author: Federico Astolfi
categories: ''
published: false
---

Some topics in maths are just abstract as they are and they don't prove themselves useful to anything. It is just like it is. And this is okay, you can have it and crack your head on the most absurd conundrums just for the sake of it. Some other times, in maths we can find beautifully formalized objects that are just perfectly shaped and sharped to be employed for applications too. And if you ask me, quantum computing is a great application for the functional generalization of derivatives on _Banach spaces_: I am referring to the **Frèchet** and **Gateaux** derivatives.

---

## Inner products on $\mathbb{C}^N$

$$ \langle \varphi | \psi \rangle = \sum_{j=1}^{N} \overline{\varphi_j}\,\psi_j, \qquad \langle a\varphi|\psi\rangle = \bar a\,\langle\varphi|\psi\rangle, \qquad \langle\varphi|a\psi\rangle = a\,\langle\varphi|\psi\rangle $$

$$ (\varphi,\psi)_{\mathbb{R}} = \operatorname{Re}\langle\varphi|\psi\rangle, \qquad (\psi,\psi)_{\mathbb{R}} = \lVert\psi\rVert^2 $$

$$ \mathrm{d}F(\psi)[h] = \big(\nabla F(\psi),\,h\big)_{\mathbb{R}} = \operatorname{Re}\langle \nabla F(\psi) \,|\, h\rangle $$

## Fréchet / Gâteaux

$$ F(u+h) - F(u) = A\,h + o(\lVert h\rVert), \qquad A =: \mathrm{d}F(u) $$

$$ \frac{\lVert F(u+h)-F(u)-A h\rVert}{\lVert h\rVert} \xrightarrow[\lVert h\rVert\to 0]{} 0 $$

$$ \mathrm{d}_G F(u)[h] = \lim_{t\to 0}\frac{F(u+t h)-F(u)}{t} $$

$$ \mathrm{d}(G\circ F)(u)[h] = \mathrm{d}G(v)\big[\mathrm{d}F(u)[h]\big], \qquad v = F(u) $$

$$ \mathrm{d}F(u)[h] = \big(\nabla F(u),\,h\big) $$

$$ \lVert F(u)-F(v)\rVert \le \sup_{w\in[u,v]} \lVert \mathrm{d}_G F(w)\rVert_{\mathcal{L}}\;\lVert u-v\rVert $$

## Fidelity & expectation value

$$ q(z) = |z|^2, \qquad \mathrm{d}q(z)[w] = 2\operatorname{Re}(\bar z\,w) $$

$$ F_\varphi(\psi) = \big|\langle\varphi|\psi\rangle\big|^2 $$

$$ \mathrm{d}F_\varphi(\psi)[h] = 2\operatorname{Re}\!\big(\overline{\langle\varphi|\psi\rangle}\,\langle\varphi|h\rangle\big), \qquad \nabla F_\varphi(\psi) = 2\,\langle\varphi|\psi\rangle\,\varphi $$

$$ E_A(\psi) = \langle\psi|A\psi\rangle, \qquad \nabla E_A(\psi) = 2A\psi $$

$$ E_A(\psi+h) - E_A(\psi) = 2\operatorname{Re}\langle A\psi|h\rangle + \langle h|Ah\rangle $$

$$ \langle X, Y\rangle = \operatorname{tr}(X^\ast Y), \qquad F_G(W) = \frac{1}{N^2}\,\big|\operatorname{tr}(G^\ast W)\big|^2, \qquad \nabla F_G(W) = \frac{2}{N^2}\,\operatorname{tr}(G^\ast W)\,G $$

## Blocks

<div class="thm definition" markdown="1">
**Definition.** 
</div>

<div class="thm theorem" markdown="1">
**Theorem.** 
</div>

<div class="thm lemma" markdown="1">
**Lemma.** 
</div>

<div class="thm proposition" markdown="1">
**Proposition.** 
</div>

<div class="thm corollary" markdown="1">
**Corollary.** 
</div>

<div class="thm proof" markdown="1">
**Proof.** &nbsp; $\square$
</div>

<div class="thm remark" markdown="1">
**Remark.** 
</div>

<div class="thm example" markdown="1">
**Example.** 
</div>

## Useful formulas

$$ |\psi\rangle = \sum_j c_j\,|j\rangle, \qquad \langle\varphi|\psi\rangle = \sum_j \overline{\varphi_j}\,\psi_j, \qquad \langle\psi|\psi\rangle = \lVert\psi\rVert^2 = 1 $$

$$ \rho = |\psi\rangle\langle\psi|, \qquad \operatorname{tr}\rho = 1, \qquad \rho = \rho^\dagger \succeq 0 $$

$$ \langle A\rangle_\psi = \langle\psi|A|\psi\rangle = \operatorname{tr}(\rho A), \qquad (\Delta A)^2 = \langle A^2\rangle - \langle A\rangle^2 $$

$$ i\hbar\,\partial_t|\psi\rangle = H|\psi\rangle, \qquad |\psi(t)\rangle = U(t)\,|\psi(0)\rangle, \qquad U = e^{-iHt/\hbar} $$

$$ \dot\rho = -\frac{i}{\hbar}[H,\rho], \qquad [A,B] = AB - BA, \qquad \{A,B\} = AB + BA $$

$$ F(\varphi,\psi) = |\langle\varphi|\psi\rangle|^2, \qquad F(\rho,\sigma) = \Big(\operatorname{tr}\sqrt{\sqrt{\rho}\,\sigma\,\sqrt{\rho}}\,\Big)^2 $$

$$ \sigma_x = \begin{pmatrix}0&1\\1&0\end{pmatrix}, \quad \sigma_y = \begin{pmatrix}0&-i\\ i&0\end{pmatrix}, \quad \sigma_z = \begin{pmatrix}1&0\\0&-1\end{pmatrix}, \quad [\sigma_a,\sigma_b] = 2i\,\varepsilon_{abc}\,\sigma_c $$

$$
\begin{aligned}
E_A(\psi+h) - E_A(\psi)
&= \langle h|A\psi\rangle + \langle\psi|Ah\rangle + \langle h|Ah\rangle \\
&= 2\operatorname{Re}\langle A\psi|h\rangle + \langle h|Ah\rangle .
\end{aligned}
$$

$$
f(x) =
\begin{cases}
\;a & x \ge 0,\\
\;b & x < 0.
\end{cases}
$$
