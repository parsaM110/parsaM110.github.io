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

## preliminaries

consider a state space system like:

$$
\dot{x} = Ax + Bu \underset{u = kx(t)}{\implies} \dot{x} = (A+Bk)x \quad \text{input feedback}
$$

$$
V(x) = {x(t)}^TPx(t) > 0 \implies P > 0 \quad \text{Lyapunov stability}
$$

$$
\dot{V}(x) = \dot{x}^T(t)Px(t) + x^T(t)P\dot{x(t)} < 0
$$

$$
\underset{\text{state space}}{\implies} {x(t)}^T (A+Bk)^T P x(t) + x^T(t)P(A+Bk)x(t) < 0 
$$

$$
\implies x^T(t)\underbrace{[\left (A+Bk)^TP + P(A+Bk) \right]}_{N.O.} x(t) < 0
$$

$$
\text{stability condition} :
\begin{cases} 
      P > 0 \\ 
      (A+Bk)^TP+ P(A+Bk) < 0\\
   \end{cases}
$$

## Event-Based

$$
u = kx(\tau) \implies \dot{x(t)} = Ax(t) + Bkx(\tau)
$$

$$
\dot{V}(x) = \dot{x}(t)^TPx(t) + x(t)^TP\dot{x}(t) < 0
$$

$$
\dot{V}(x) = x^T(\tau) (Bk)^TPx(t) + x^T(t)PBkx(\tau) + x(t)A^TPx(t) + x^T(t)PAx(t) < 0
$$

by defining error singal, we have:
$$
e(t) = x(t) - x(\tau) \implies x(\tau) = x(t) - e(t) 
$$

$$
\implies x^T(t)[\left (A+Bk)^TP + P(A+Bk) \right] x(t) - e(t)^T(Bk)^TPx(t) - x^T(t)PBkx(t) < 0
$$
