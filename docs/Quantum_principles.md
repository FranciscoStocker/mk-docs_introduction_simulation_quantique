## 1) Principe de superposition[^1]

L'état quantique $\psi$ d'un système physique à l'instant $t$ est décrit par un *ket* noté $\ket{\psi}$ appartenant à l'espace d'états $\mathcal{E}$

**Exemple:**

Soit $\psi$ la fonction d'onde d'un qubit. Dans l'espace d'états $\mathcal{E}$ il existe une base $(\ket{0},\ket{1})$ et ainsi: $\exists (\alpha, \beta) \in \mathbb{C}^2, \ket{\psi} = \alpha\ket{0} + \beta\ket{1}$. $\psi$ est soumis à la superposition quantique des deux états $\ket{0}$ et $\ket{1}$

## 2) Principe de correspondance

Toute grandeur physique mesurable $\mathcal{A}$ est décrite par un observable à laquelle on associe un opérateur hermitien[^2] $\hat{A}$

**Relations de correspondace**:

Niels Bohr propose en 1923 la relation de correspondance, permettant d'exprimer des grandeurs physiques sous la forme suivante:

- **Observable position**: $\hat{r}:  \psi(\vec{r}, t) \to r \, \psi(\vec{r}, t)$

- **Observable Energie**: $\hat{E}: \psi(\vec{r},t) \to i\hbar \frac{\partial}{\partial t} \psi(\vec{r}, t)$

- **Observable impulsion** (quantité de mouvement):  $\hat{p}: \psi(\vec{r},t)\to -i\hbar \nabla\psi(\vec{r},t)$

- **Opérateur Energie cinétique** ($T=\frac{p^2}{2m}$)   $$ \hat{T}: \psi(\vec{r},t) \to -\frac{\hbar^2}{2m} \Delta\psi(\vec{r},t) $$

- **Opérateur moment cinétique** ($\vec{L} = \vec{r} \times \vec{p}$): $$ \hat{L} : \psi(\vec{r},t)\to  -i\hbar  r  \nabla \psi(\vec{r},t) $$

## 3) Principe de décomposition spectrale: 




[^1]: Plus d'informations dans Ayouz, M., Gillet, J.-M., Janolin, P.-E., & Kokoouline, V. (2020). Les fondamentaux de la mécanique quantique sous Python : Rappel de cours et exercices d'application avec programmes inclus. Ellipses.

[^2]: Un opérateur hermitien est un opérateur linéaire égal à son propre adjoint hermitien conjugué, si l'application est entre $\mathbb{R}$-espaces vectoriels, on dit qu'il est auto-adjoint. Autrement dit, $A$ est hermitien $\iff \hat{A} = \hat{A}^\dagger$



