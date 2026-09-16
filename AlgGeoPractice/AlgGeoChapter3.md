---
layout: default
title: Practices in Chapter 2 of _Algebraic Geometry_ by R. Hartshorne (updating)
---
(v.1.1.1)

[Chapter 3: Cohomology](#chapter-3-cohomology)

[3.1: Derived Functors](#31-derived-functors)

[3.2: Cohomology of Sheaves](#32-cohomology-of-sheaves)

[3.3: Cohomology of a Noetherian Affine Scheme](#33-cohomology-of-a-noetherian-affine-scheme)

[3.4: Cech Cohomology](#34-cech-cohomology)

[3.5: The Cohomology of Projective Space](#35-the-cohomology-of-projective-space)

[3.6: Ext Groups and Sheaves](#36-ext-groups-and-sheaves)

[3.7: The Serre Duality Theorem](#37-the-serre-duality-theorem)

[3.8: Higher Direct Images of Sheaves](#38-higher-direct-images-of-sheaves)

[3.9: Flat Morphisms](#39-flat-morphisms)

[3.10: Smooth Morphisms](#310-smooth-morphisms)

[3.11: The Theorem on Formal Functions](#311-the-theorem-on-formal-functions)

[3.12: The Semicontinuity Theorem](#312-the-semicontinuity-theorem)

# Chapter 3: Cohomology

## 3.1: Derived Functors
There are no exercises for this sections. Although I think there should be. Weibel's, Maclane's, and Rotman's books all have excellent exercises on derived functors, there are also some in Vakil's book as well (Maybe I'll make a list of them). 
## 3.2: Cohomology of Sheaves

### 3.2.1

#### a)

Let $X = \A^1$ be the affine line over an infinite field $k$. Let $P,Q$ be distinct closed points of $X$, and let $U = X - P,Q$. Show that $H^1(X,\mathbb{Z}_U)\neq 0$.

_proof:_

Here $\mathbb{Z}\_U:=i\_!\mathbb{Z}$ the extension by zero of the constant sheaf outside of $U$. There is exact sequence
\\[
0\to \mathbb{Z}\_U\to \mathbb{Z}\to i\_P(\mathbb{Z})\plus i\_Q(mathbb{Z})\to 0
\\]
Here $i\_P(A)$ stand for the skycraper of $A$ at $P$.

We take the cohomology to get exact sequence.

\\[
0\to H^0(X,\mathbb{Z}\_U)\to \mathbb{Z}\xleftarrow{q} H^0(X,i\_P(\mathbb{Z})\oplus i\_Q(mathbb{Z}))=\mathbb{Z}\oplus \mathbb{Z}
\\ \to H^1(X,\mathbb{Z}\_U)\to 0
\\] The map $q$ takes $s\mapsto (s\|\_P, s\|\_Q)$, which is definitely not surjective.



## 3.3: Cohomology of a Noetherian Affine Scheme
## 3.4: Cech Cohomology
## 3.5: The Cohomology of Projective Space
## 3.6: Ext Groups and Sheaves
## 3.7: The Serre Duality Theorem
## 3.8: Higher Direct Images of Sheaves
## 3.9: Flat Morphisms
## 3.10: Smooth Morphisms
## 3.11: The Theorem on Formal Functions
## 3.12: The Semicontinuity Theorem
