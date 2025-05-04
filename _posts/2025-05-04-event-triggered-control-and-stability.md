---
title: Event Triggered Control and Stability
date: 2025-05-04 11:02:00 +0800
categories: [Control Theory]
tags: []
author: parsa
math: true
image:
  path: assets/headers/2025-05-04-event-triggered-control-and-stability.png
  alt: Control Theory
---

## Introduction

the idea of event triggered system is that we instead of online feedback , define a policy and update the feedback signal based on that policy, the gain we get is mostly computational although it can also gives us other gains too.

## prelimanaries

consider a state space system like:

$$
\dot{x} = Ax + Bu \underset{u = kx(t)}{\implies} \dot{x} = (A-Bk)x \quad \text{input feedback}
$$

$$
V(x) = {x(t)}^TPx(t) > 0 \implies P > 0 \quad \text{Lyapunov stability}
$$

$$
\dot{V(x)} = \dot{x(t)^T}Px(t) + x(t)^TP\dot{x(t)} < 0
$$

$$
\underset{state space}{\implies} {x(t)}^T (A+BK)^T P x(t) + x^T(t)P(A+BK)x(t) < 0 
$$

$$
\implies x^T(t)\underbrace{[\left (A+BK)^TP + P(A+BK) \right]}_{N.O.} x(t) < 0
$$

$$
stability condition :
\begin{cases} 
      P > 0 \\ 
      (A+BK)^TP+ P(A+BK) < 0\\
   \end{cases}
$$
