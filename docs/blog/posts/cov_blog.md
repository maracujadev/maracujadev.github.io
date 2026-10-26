---
date: 2026-10-26
title: The Elegance of Variational Calculus
slug: variational-calculus
categories:
  - Math
---
# [WIP] The Elegance of Variational Calculus

What's the fastest path between two points? How do physicists know how light travels? 
A practical introduction to optimizing functionals.

<!-- more -->
## Prerequisites

If you'd like to read this text, you should be fluent in single variable calculus. 
Without knowing what a derivative or integral is, you probably won't get far here. 
The main results are in form of differential equations. Don't feel intimidated if you haven't had much contact with those.

## The Brachistochrone Problem
*Problem setup*

As you can see, using some basic physics and calculus, we can rearrange the problem of finding the optimal curve to optimizing the following function for a $y$ that gives the smallest $T[y]$.  
$T[y]=\int_{x_1}^{x_2} \frac{\sqrt{1+y'^2}}{\sqrt{2gy}}dx$  
For now, this might seem like just another complicated way to write the same problem. But bear with me, this will be our way to success later on. However, before being able to explore this problem better, we should take a brief sidetrack into the theory of so-called "Variational Calculus".

## Basics in Variational Calculus


The following section of this article will focus on proving the main result in Variational Calculus. 
Developing the "Euler-Lagrange Equation" will be the climax of this topic for most purposes. The result is highly elegant,
in fact deserving of the title as my personal favorite equation, but note that the derivation of it will be quite intense.
Make sure to take your time following the steps or possibly skim it if you don't feel well-versed in calculus. 

## Deriving the Euler-Lagrange Equation

In the following, we will try to establish a necessary condition for a function $f$ to be extremal considering a functional.
Remember that the condition is not sufficient, yet going from the entire function space to the solutions of a differential equation is highly useful for our studies.  
In the following, consider this shape of functional:

$$J[y]:=\int_{x_1}^{x_2} L(x,y(x),y'(x))dx$$

Here, $L(x,y(x),y'(x))$ shall be a given function that is at least twice continuously differentiable. The function $y$ is our independent variable. It shall be twice continuously differentiable and satisfy the boundary conditions $y(x_1)=y_1, y(x_2)=y_2$.
Now, we use a perturbation on our functional. That perturbation is a twice continuously differentiable function commonly denoted $\eta(x)$. The considered point/function where $J[y]$ reaches a local minimum/maximum shall be called $f$.
We are now dealing with a new function $H(\epsilon):=J[y+\epsilon\eta]$. Notice that to keep the edge conditions we need to set $\eta(x_1)=\eta(x_2)=0$.  
 This now means that
our new function $H(\epsilon)$ has a minimum at $\epsilon = 0$. This goes analogously to the standard method in single variable calculus. 
We can now say that 

$$H'(0)=\frac{dH}{d\epsilon}\Big|_{\epsilon=0}=\int_{x_1}^{x_2}\frac{dL}{d\epsilon}\Big|_{\epsilon=0}dx=0.$$

Consider $y=f+\epsilon\cdot\eta$ as a function of $\epsilon$. The term inside the integral can be replaced using the derivative of $L$ with respect to $\epsilon$. 

$$\frac{dL}{d\epsilon}=\frac{\partial L}{\partial y}\frac{dy}{d\epsilon}+\frac{\partial L}{\partial y'}\frac{dy'}{d\epsilon}=\frac{\partial L}{\partial y}\eta+\frac{\partial L}{\partial y'}\eta'$$

Notice that the last step follows directly from our definition for $\eta$ since $y=f+\epsilon\eta, y'=f'+\epsilon\eta'$ which means that $\frac{dy}{d\epsilon}=\eta$ and $\frac{dy'}{d\epsilon}=\eta'$.  
  
This result is highly valuable to us, as we can now rewrite our expression for the integral above.

$$\int_{x_1}^{x_2}\frac{dL}{d\epsilon}\Big|_{\epsilon=0}dx=\int_{x_1}^{x_2}\left( \frac{\partial L}{\partial f}\eta+\frac{\partial L}{\partial f'}\eta' \right)dx$$

Notice that $y$ becomes $f$ as we applied the condition $\epsilon=0$. Performing an integration by parts on this expression:

$$0=\int_{x_1}^{x_2}\left( \frac{\partial L}{\partial f}\eta+\frac{\partial L}{\partial f'}\eta' \right)dx = \int_{x_1}^{x_2}\frac{\partial L}{\partial f}\eta \; dx+ \frac{\partial L}{\partial f'}\eta\Big|_{x_1}^{x_2}-\int_{x_1}^{x_2}\eta\frac{d}{dx}\frac{\partial L}{\partial f'} \; dx$$

$$=\int_{x_1}^{x_2}\left( \frac{\partial L}{\partial f}\eta - \eta\frac{d}{dx}\frac{\partial L}{\partial f'} \right)dx$$

It becomes clear that the boundary term must vanish since we earlier defined that $\eta$ evaluated at both $x_1$ and $x_2$ has to be $0$.

We now have the result that for every perturbation $\eta$ of the function $f$:

$$ \int_{x_1}^{x_2}\left( \frac{\partial L}{\partial f} - \frac{d}{dx}\frac{\partial L}{\partial f'} \right)\eta \; dx =0$$

This can be finished off using the "Fundamental Lemma of Variational Calculus". 

## Solving the Brachistochrone Problem

## Applications of VC


