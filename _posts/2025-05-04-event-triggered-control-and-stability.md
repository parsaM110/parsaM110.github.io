---
title: Event Triggered Control and Stability
date: 2025-05-04 11:02:00 +0800
categories: [Control Theory]
tags: []
author: parsa
math: true
image:
  path: assets/headers/2025-05-03-control-theory.png
  alt: Control Theory
---

## Introduction

the idea of event triggered system is that we instead of online feedback , define a policy and update the feedback signal based on that policy, the gain we get is mostly computational although it can also gives us other gains too.

## prelimanaries

consider a state space system like:

$$
\dot{x} = Ax + Bu \underset{\implies}{u = kx(t)} \dot{x} = (A-Bk)x \; \text{input feedback}
$$

$$
V(x) = {x(t)}^T(t)Px(t) > 0 \implies P > 0 \text{Lyapunov stability}
$$

$$
\dot{V(x)} = \dot{x(t)^T}Px(t) + x(t)^TP\dot{x(t)} < 0
$$

$$
\underset{\implies}{state space} {x(t)}^T (A+BK)
$$
