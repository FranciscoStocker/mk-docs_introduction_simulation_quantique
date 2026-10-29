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

La mesure d'une grandeur physique $\mathcal{A}$ ne peut avoir pour résultat que l'une des valeurs propres de l'opérateur $\hat{A}$ qui lui est associé.


**Point mathématique**: Comme $\hat{A}$ est hermitien, le théorème spectrale généralisé sur les espaces de Hilbert nous assure que le spectre de $\hat{A}$ est une base orthogonale de $\mathcal{E}$.

Soit $(c_n)_{n \in \mathbb{N}}$ le spectre de $\hat{A}$ et $(\phi_n)_{n \in \mathbb{N}}$ la base composée des vecteurs propres associés. Ainsi $\forall \ket{\psi} \in \mathcal{E}, \exists (c_n)_{n \in \mathbb{N}} \in \mathbb{C}^{\mathbb{N}}, \ket{\psi} = \sum_{n = 1}^{\infty} c_n\ket{\phi_n}$ Alors la probabilité que le système soit à l'état $A_i$ est: $$ \mathcal{P}(A_n) = \frac{\vert{}\langle \phi_n \mid \psi \rangle\vert{}^2}{\langle \psi \mid \psi \rangle}$$

L'on nomme $c_n$ une *amplitude de probablité*, elle n'est d'ailleurs pas inteprétée physiquement, mais son module au carré correspond à une densité de probabilité.

## 4) Règle de Born

Pour un spectre discret, **non dégénéré**[^3], et pour une base spectrale orthonormée, l'on peut appliquer **la règle de Born**:
$\mathcal{P}(A_n) = \vert{} c_n\vert{} ^2$

Le système est dès lors non déterministe mais l'on peut calculer la *valeur moyenne* de l'opérateur $\hat{A}$ qui est donnée par la formule:
$$ \langle A \rangle = \langle \psi \vert{} \hat{A} \vert{} \psi \rangle = \sum_{n = 0}^{\infty} A_n\mathcal{P}(A_n) $$

Pour un spectre discret **dégénéré** l'on trouve des expressions équivalentes: $$ \mathcal{P}(A_n) = \sum_{n = 0}^{g_i-1}\vert{} c_i^n\vert{} ^2 $$ avec $g_i$ le degré de multiplicité du i-ème état propre

## 5) Réduction en paquets d'onde

La mesure perturbe le système physique de telle sorte que l'on refait la mesure, si le résultat de la mesure initiale est l'état $A_i$, on retrouve avec certitude $A_i$. Autrement dit immédiatement après la mesure de $A_i$, l'état du système est la projection normée de $\ket{\psi}$ sur le sous-espace propre associé à $A_i$, tel que:$$ \ket{\psi'} = \frac{\hat{P}_i\ket{\psi}}{\sqrt{\langle \psi \vert{} \hat{P}_i \vert{} \psi \rangle}}  $$

## 6) Equation de Schrödinger

L'évolution temporelle du système d'un état quantique, est régie par l'équation de Schrödinger: $$ i\hbar \frac{d}{dt}\ket{\Psi(t)} = \hat{H}(t)\ket{\Psi(t)} $$

[^1]: Plus d'informations dans Ayouz, M., Gillet, J.-M., Janolin, P.-E., & Kokoouline, V. (2020). Les fondamentaux de la mécanique quantique sous Python : Rappel de cours et exercices d'application avec programmes inclus. Ellipses.

[^2]: Un opérateur hermitien est un opérateur linéaire égal à son propre adjoint hermitien conjugué, si l'application est entre $\mathbb{R}$-espaces vectoriels, on dit qu'il est auto-adjoint. Autrement dit, $A$ est hermitien $\iff \hat{A} = \hat{A}^\dagger$

[^3]: Définition: à valeurs propres disctinctes. Explication mathématique: Le théorème de Wigner établit le lien fondamental : Toute dégénérescence du spectre d'un hamiltonien est associée à une symétrie de ce hamiltonien, plus précisément à la dimension des représentations irréductibles de son groupe de symétrie. Par exemple, pour une particule enfermée dans une boîte de potentiel infini 2D, la symétrie $x \leftrightarrow y$ provoque une dégénerescence du spectre. Physiquement au moins deux états ont la même énergie en un point de l'espace



