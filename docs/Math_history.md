# Une brève histoires des mathématiques 


## Contexte générale

Malgré les grandes avancées théoriques du XIXe siècle dans les domaines de l'électromagnétisme et de la thermodynamique, des questions fondamentales persistent au tournant du siècle, notamment l'explication des raies d'émission discrètes des atomes et la nature de l'effet photoélectrique.En 1921, Albert Einstein se voit attribuer le prix Nobel de physique pour son interprétation de l'effet photoélectrique (1905), formalisant la célèbre relation corpusculaire de l'énergie d'un photon : $E = h\nu$. Cette approche trouve un écho direct dans la condition de fréquence proposée dès 1913 par Niels Bohr :$$ h\nu_{nm} = E_n - E_m$$ où $n$ et $m$ désignent les nombres quantiques associés aux états stationnaires de l'atome.En 1924, Louis de Broglie bouleverse l'histoire de la physique en introduisant l'analogie formelle de la dualité onde-corpuscule [^1], résumée par sa relation fondamentale :$$ p = \frac{h}{\lambda} $$Si ces travaux fondateurs offrent une première approche quantitative de la quantification à l'échelle atomique (la « vieille théorie quantique »), ils se révèlent incapables de décrire de manière universelle les systèmes complexes. Notamment les effets Zeeman et Stark, qui traduisent le dédoublement des raies spectrales de l'atome lorsqu'il est soumis respectivement à un champ magnétique ou électrique externe restent incompris par la communauté scientifique. <div markdown="1" style="text-align: center;"> ![Photo de l'effet Zeeman, prise en 1896 par Pieter Zeeman.](https://upload.wikimedia.org/wikipedia/commons/3/32/ZeemanEffect.GIF?utm_source=fr.wikipedia.org&utm_campaign=parser&utm_content=thumbnail_unscaled) </div>

La discontinuité apparente des phénomènes naturels et les limites conceptuelles des modèles semi-classiques de Bohr-Sommerfeld — souvent accusés d'être construits de manière empirique ou ad hoc — génèrent de vives controverses. C'est de cette impasse que naîtront, par des voies formelles distinctes mais mathématiquement équivalentes, les deux piliers de la physique quantique moderne : la mécanique matricielle de Heisenberg, Born et Jordan, et la mécanique ondulatoire d'Erwin Schrödinger.

### La mécanique matricielle

En 1925 Heinsenberg s'interrésse par le problème des raies spectrales[^2] et procède par l'étude des fréquences des siganux lumineux émis ou absorbés par les atomes en posant un tableau. Actuellement l'on pourrait poser la matrice $(\nu_{nk})_{(n,k) \in \mathbb{N}^2}$ où les diagonales sont nulles car les électrons de valence ne peuvent pas passer de l'état $E_i \to E_i$ et $\nu_{nk} = \nu_{kn}$. Finalement il publie dans la même année un article qui bouleverse les modèles quantiques[^3] en donnant trois idées clées: 

1) Dans l'introduction apparaît pour la première fois la notion d'une observable [^4],  quoi qu'elle sera formalisée bien plus tard (PRECISER)(DONNER HYPER LIEN INTERNE AUX PRINCIPES)

2) Dans la partie des études cinématiques une nouvelle définition de la position $x(t)$ d'un électron qui orbite autour d'un noyau apparaît. Etant la position une fonction périodique la mécanique classique en donne une expression avec la série de Fourier: $$ x(t) = \sum_{\alpha = -\infty}^{+\infty} a_{\alpha}e^{i \alpha\omega_{n} t}$$ avec $n \in \mathbb{N}$ le mode de pulsation de l'électron. Comme la position $x$ n'est pas observable, Heisenberg propose de la remplacer par un objet mathématique qui reflète directement ce que l'on mesure : les transitions entre états stationnaires. Il propose d'interpréter la fréquence $\nu_{nk}$ comme la fréquence d'un signal lumineux (absorbé ou émis) par un atome, de considérer toutes les amplitudes possibles dans un tableau d'amplitudes $a_{nk}$ et étudier les positions en fonction d'un mode de pulsation $x_n(t)$

3) La dernière idée clée réinterprète le produit de deux positions $x$ et $y$ données. En effet *la formule de Rydberg* donne directement *le principe de combinaison de Rydberg-Ritz*:
$$ \nu_{jk} = R_\nu(\frac{1}{j^2}-\frac{1}{k^2})  $$
$$ \nu_{jk} = \nu_{jm} + \nu_{mk}  $$

Cette dernière loi est vérifiée expérimentalement mais pose un problème théorique à Heinsenberg au moment de multiplier deux positions selon l'expression qu'il avait proposé.
$$ x_ny_n = \sum_{k} a_{nk}e^{i\omega_{nk}t} \sum_{m} b_{nm}e^{i\omega_{nm}t} = \sum_{k}\sum_{m} a_{nk}b_{nm}e^{i(\omega_{nk} + \omega_{nm})t} $$ 

Dans un cadre classique le produit de deux positions donne une troisième sous une expression équivalente, néanmoins d'après le *principe de recombinaison de Rydberg-Ritz* les deux pulsations d'onde ne peuvent pas se recombiner [^5]. Ceci donne une nouvelle condition sur les objets quantiques: les coefficients de Fourier et les pulsation des des objets quantiques sont liés de sorte que: $b_{nm} \to b_{km}$ et $\omega_{nm} \to \omega_{km}$ ce qui donne la loi classique: $$ x_ny_n = \sum_{m} c_{nm}e^{i\omega{nm}t} $$ avec $$ c_{nm} = \sum_{k} a_{nk}b_{km} $$

Le lecteur avisé reconnaîtra immédiatement le produit matriciel et pourra vérifier la non commutativité du produit $x_{n}y_{n}$, néanmoins Heisenberg n'en avait pas connaissance de cet objet[^6]. Born et Jordan tâcheront de formaliser cet objet[^7] avec un succès mitigé. D'une part le modèle matriciel décrit quantativement des systèmes comme l'oscillateur harmonique ou anharmonique, et donne la relation de commutation canonique: $pq-qp = \frac{h}{2\pi i }Id$. Néanmoins les modèles physiques jusqu'à maintenant employaient des objets moins abstraits, et les raisonnements étaient d'une toute autre nature.

### La mécanique ondulatoire

En 1925 Erwin Schrödinger fût frappé par le révolutionnaire article de De Broglie[^1] et il s'intéressa à la question de la quantification des niveaux d'énergies de l'électron dans le modèle de l'atome de Bohr Sommerfield. Néanmoins la *dualité onde corpuscule* serait vérifiée expérimentalement qu'en 1927, pour l'instant Schrödinger et son collègue Debye se montraient réticents: après tout 
*"on ne peut pas avoir d'ondes sans équation d'onde"*[^8]. Aussitôt ces deux derniers, dans un esprit de compétition décidèrent de cette équation d'onde, jusqu'à finalement la trouver en décembre de 1925 lors d'un séjour aux Alpes, accompagné de son amante. Schrödinger rejetait fortement la mécanique matricielle, étant trop abtraite pour bien décrire la physique, d'autant dire que la notion des *observables* signifiait une compréhension sur la nature radicalement différente à la sienne. C'est ainsi que, en s'inspirant des hypothèses physiques de De Broglie et des mathématiques propres à la mécanique Hamiltonienne classique, il parvient à formuler un modèle des orbitales de l'atome de l'Hydrogène[^9]. Son modèle écrasa, dans un premier temps, totalement celui proposé par Heisenberg: ce modèle décrivait les phénomènes à partir d'équations différentielles, un objet très parlant pour les physiciens. Schrödinger ne voulait pas révolutionner la physique quantique, mais restituer les modèles traditionnels dans un nouveau contexte. C'est pourquoi Heinsenberg et Schrödinger ne s'entendaient pas mal au début, mais des tensions croissantes ont atteintes une polémique entre Zürich et Göttingen. C'est en 1926 que Schrödinger lui même démontre l'équivalence entre ces deux modèles mathémiques[^10], mais sans jamais s'accorder avec la compréhension physique de Heinsenberg. 

La question la plus intriguante sur la mécanique ondulatoire concerne la nature de la fonction d'onde notée $\psi$. En effet Schrödinger pensait que la fonction d'onde avait un caractère matériel ou encore physique, mais qu'est-ce qui ondulait exactement? Dans quel milieu? L'interprétation de $\psi$ fût discutée, d'autant dire que, sous forme de moquerie un petit quatrain humoristique lui était dédié[^11]: 

                                          Erwin ne cesse de calculer
                                          Avec son psi ondulatoire,
                                          Mais à quoi ça peut ressembler
                                          Ca, on aimerait le savoir

C'est le propre Heisenberg celui qui en donne l'interprétation de $\psi $approuvée jusqu'à maintenant, i.e celle d'interpréter le carré de son module comme une densité de probabilités. La fonction d'onde se révela finalement encore plus abstraite au moment d'appliquer le même raisonnement que celui de l'atome d'hydrogène à des atomes ayant plusieurs électrons de valence, comme l'Hélium. En effet Schrödinger considérait une fonction d'onde par électron de valence, ce qui était mathématiquement contradictoire. Ainsi l'on impose que la fonction d'onde représente les deux électrons au même temps, ce qui signifie considérer une fonction d'onde qui se déplace en un espace de 6 dimensions. (les degrés de liberté de chaque atome). Ce problème là rendit tout à fait impossible d'interpréter la fonction d'onde comme une onde physique.



[^1]: Louis De Broglie. Recherches sur la théorie des quanta. PhD thesis, Migration-université en cours d'affectation, 1924

[^2]: Kumar, M., & Sigaud, B. (Trad.). (2011). Le grand roman de la physique quantique : Einstein, Bohr… et le débat sur la nature de la réalité (B. Sigaud, Trad.). JC Lattès. (Ouvrage original publié en 2008, Quantum), p274

[^3]:Werner Heisenberg. Über quantentheoretische umdeutung kinematischer und mechanischer beziehungen. In Original Scientific Papers Wissenschaftliche Originalarbeiten, pages 382–396. Springer, 1985.


[^4]: *ibid*: "It is known that one can raise the serious objection to the formal rules that are
generally employed in quantum theory for the calculation of observable quantities (e.g.,
energy in the hydrogen atom) that those rules of calculation are obtained essentially as
constituent relations between quantities that cannot be observed, in principle (such as,
e.g., the position or orbital period of the electron), so those rules will obviously lack any
intuitive physical foundation if one would not like to continue to maintain the hope that
those up-to-now unobservable quantities might perhaps be made experimentally
accessible at some later point. That hope could be regarded as justified if the stated rules
were applied to a certain unlimited domain of quantum-theoretical problems in an
intrinsically consistent way."
[^5]: Vous pouvez voir une démonstration complète sur la vidéo "This is how Heisenberg created quantum mechanics: step-by-step guide", Dr. Jorge S. Diaz,  https://youtu.be/oVzzIkkYGY8

[^6]: Manjit Kumar, Op.cit. p.280 : "Heinsenberg se plagnit qu'il ne savait même pas ce que c'était une matrice"

[^7]: Born, M., & Jordan, P. (1925). Zur Quantenmechanik. Zeitschrift für Physik, 34, 858–888. https://doi.org/10.1007/BF0132853

[^8]: Manjit Kumar, Op.cit. p.296

[^9]: Schrödinger, E. (1926). Quantisierung als Eigenwertproblem. Annalen der Physik, 384(4), 361–376. https://doi.org/10.1002/andp.19263840404

[^10]: Erwin Schrödinger. (1926). Sur les rapports qui existent entre la mécanique quantique de Heisenberg-Born-Jordan et la mienne.  Annalen der Physik, 79(4).

[^11]: Manjit Kumar, Op.cit. p.307