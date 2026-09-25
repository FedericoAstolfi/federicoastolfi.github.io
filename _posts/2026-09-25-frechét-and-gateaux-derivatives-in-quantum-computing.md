---
title: Frechét and Gateaux derivatives in Quantum Computing
date: 2026-09-25T18:07:00
author: Federico Astolfi
categories: ''
---

Some topics in maths are just abstract as they are and they don't prove themselves useful to anything. It is just like it is. And this is okay, you can have it and crack your head on the most absurdly conundrums just for the sake of it. Some other times, in maths we can find beautifully formalized objects that are just perfectly shaped and sharped to be employed for applications. And if you ask me, quantum computing is a great application for the functional generalization of derivatives on _Banach spaces_: I am referring to the **Frechét** and **Gateaux** derivatives.

To make this concrete, for a functional $F$ on a Banach space, the **Gâteaux derivative** at $x$ in the direction $h$ is

$$ DF(x; h) = \lim_{t \to 0} \frac{F(x + t h) - F(x)}{t}, $$

whenever the limit exists. The **Fréchet derivative** is stronger: a bounded linear operator $A$ with $\lim_{\lVert h \rVert \to 0} \frac{\lVert F(x+h) - F(x) - A h \rVert}{\lVert h \rVert} = 0$.
