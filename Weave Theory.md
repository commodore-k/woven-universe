
## Overview

This documents the Canon Weave Theory. However, it is up to the Allkin of the Aether Weave and the Humans of the Terrum Weave to figure this out. This system hides in it an arms race, the Gods are ahead in understanding but lost to the Blood Madness. Humans are way behind but they are starting to get a foot in this race. Beings of other weaves can control and mutate other weaves, and they can thus destroy other weaves. If the humans discover the truth, and develop the means, they may decide tearing the Aether Weave, and thus killing their once-thought immortal gods may assure their survival. But the Allkin, lost in their Blood Maddness, don't want to perish, and certainly don't want to loose access to blood. But they are divided with Dura, and thus cannot mutate the Terrum Weave to better feed this drug. And after discovering they can live by proxy in the Terrum Weave, they have a stake in the Terrum Weave. In this grimdark world, it will be an immovable object vs an unstoppable force, both sides have their objectives, whether they know it or not, and neither will ever be able to fully complete it.

This document is written as if the blood-life humans in the far future unraveled all this. So this theory and the notation is what should be plucked from and used by them as they learn it in any Woven Universe literacy.

---

## 1. Notation

| Math                                      | ASCII   | Object                                                                                                                                                                                                                                                                       |
| ----------------------------------------- | ------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| $\mathfrak{f}$                            | `f`     | **Fyber** — the sole universal substrate                                                                                                                                                                                                                                     |
| $\gamma$                                  | `y`     | **Wyrd strand** (achiral)                                                                                                                                                                                                                                                    |
| $\lambda$                                 | `n`     | **Warp strand** ($+$ chirality)                                                                                                                                                                                                                                              |
| $\nu$                                     | `u`     | **Weft strand** ($-$ chirality)                                                                                                                                                                                                                                              |
| $\Omega$                                  | `S`     | **Strand Set**: $\{\,\gamma,\, \lambda,\, \nu\, \}$                                                                                                                                                                                                                          |
| $\mathcal{W}$                             | `W`     | **Weave**: made from $\lambda$ and $\nu$ Strands                                                                                                                                                                                                                             |
| $\chi$                                    | `x`     | **Intersection**: one warp–weft crossing in a weave                                                                                                                                                                                                                          |
| $\rho$                                    | `p`     | **Strand Segment**: A segment of a Warp Strand xor Weft Strand between two adjacent intersections on a Weave $\mathcal{W}$. see [A4 - Weave Segments](Weave%20Theory.md#Weave%20Segments) for definition details.                                                            |
| $\operatorname{\#}_\mu(\theta)$           | `#_m`   | **Embodiment Pattern**: A function that determines the pair of warp segments set and weft segments set that represent a thing $\theta$ that exists within the Weave $\mathcal{W}$ at some moment $\mu$.                                                                      |
| $\psi$                                    | `c`     | **Braid**: braiding of all 3 universal strands                                                                                                                                                                                                                               |
| $\mathcal{K}$                             | `K`     | infinite alphabet of distinct **knot identities**                                                                                                                                                                                                                            |
| $\mathcal{L},\,\mathcal{H},\,\mathcal{B}$ | `L,H,B` | knot **classes**: **L**oop, **H**itch, **B**end (strict subsets of)                                                                                                                                                                                                          |
| $a$                                       | `a`     | **agent**: one that can interact with the $\lambda$, $\nu$, and $\gamma$ strands                                                                                                                                                                                             |
| $\iota_{\theta}$                          | `i`     | **identity knot** this is merely short hand to represent the warp-loop-knot $\lambda\ell$ that was tied around a weft segment $\nu\rho$ in some Weave $\mathcal{W}$ that imbues identity for a thing $\theta$ (often an agent $a$) that the weft segment $\nu\rho$ embodies. |
| $\alpha$                                  | —       | a **Wyrd Aspect**                                                                                                                                                                                                                                                            |
| $\varphi$                                 | `phi`   | the **Wyrd Function** — the (undivined) map from a compound's network to its Aspect                                                                                                                                                                                          |
| $\mathcal{U}$                             | `U`     | the whole **Woven Universe**                                                                                                                                                                                                                                                 |
| $\bowtie$                                 | `><`    | **Match** — the sole connection relation (same id, opposite chirality)                                                                                                                                                                                                       |
| $\hookrightarrow$                         | `-->`   | **Hitch Knot Tying** operator e.g. $a \hookrightarrow b \Rightarrow \text{a hitched to b}$                                                                                                                                                                                   |
| $\looparrowright$                         | `==>`   | **Loop Knot Tying** operator e.g. $a \looparrowright b \Rightarrow \text{a looped around b}$                                                                                                                                                                                 |
| $\leftrightharpoons$                      | `<->`   | **Bend Knot Tying** operator e.g. $a \leftrightharpoons b \Rightarrow \text{a and b bended}$                                                                                                                                                                                 |

---
## 2. The Woven Axioms

The irreducible truths. Everything in §3–§6 is derived from these.

### A1: Substrate & Plasticity
*Fyber* $\mathfrak{f}$ is the fundamental substrate of the Woven Universe. Fyber is *plastic* so any deformation imparted on it persists.

### A2: Wyrdness
*Fyber* $\mathfrak{f}$ tends to naturally bunch into **achiral** *Wyrd Strands* $\gamma$.

### A3: Strand Chirality
A *Wyrd Strand* may be twisted into one of two things: A *Warp Strand* $\lambda$ which has a positive chirality, or a *Weft Strand* $\nu$ which has a negative chirality to it; and by [the first axiom](Weave%20Theory.md#A1%20Substrate%20&%20Plasticity) the change is permanent.

**Strand-classes** (by chirality of the tying strand): $\sigma \in \{\lambda, \nu, \gamma\}$.

**Twisting.** Fiber bunches into $\gamma$; twisting fixes chirality:

$$\operatorname{twist}_{+}(\gamma) = \lambda \qquad \operatorname{twist}_{-}(\gamma) = \nu$$
### A4: Weave
A *Weave* $\mathcal{W}$ is woven from the *Warp* and *Weft* strands **only**.
#### Weave Construction
$$
\begin{aligned}
\mathcal{W} &= (\Lambda, \mathcal{N}, \mathcal{X}) \\
\Lambda &= \{\, \lambda \mid \lambda \text{ is a Warp strand of } \mathcal{W} \,\}
      && \text{warp strands} \\
\mathcal{N} &= \{\, \nu \mid \nu \text{ is a Weft strand of } \mathcal{W} \,\}
      && \text{weft strands} \\
\mathcal{X} &= \Lambda \times \mathcal{N}
      = \{\, (\lambda_x,\nu_y) \mid 1 \le x \le |\Lambda|,\ 1 \le y \le |\mathcal{N}| \,\}
      && \text{intersections}
\end{aligned}
$$
#### Weave Intersections
Every warp–weft crossing is an **intersection** $\chi = (\lambda_x,\nu_y)$ such that a warp strand $\lambda_x$ crosses weft strand $\nu_y$ with coordinates $(x,y)$. Following that gives a rectangular Weave $\mathcal{W}$ such that $|\mathcal{X}| = |\Lambda|\,|\mathcal{N}|$.
#### Weave Segments
In a Weave $\mathcal{W}$, a **segment** is a length of one strand between two *adjacent* intersections on it:
$$
\begin{aligned}
\text{For} \; \chi_a=(x_a,y_a),\ \chi_b=(x_b,y_b)\in\mathcal{X} \text{:}\\

\text{Warp segment} \Rightarrow \ \lambda\rho_i \ =\ \lambda_{\chi_a\chi_b} \  &\iff x_a = x_b \ \wedge\ |y_a - y_b| = 1 \ \wedge\ \lambda\rho_i \in \mathcal{Q} \\

\text{Weft segment} \Rightarrow \ \nu\rho_i \ =\ \nu_{\chi_a\chi_b} \ &\iff y_a = y_b \ \wedge\ |x_a - x_b| = 1 \ \wedge\ \nu\rho_i \in \mathcal{P}
\end{aligned}
$$
The set of all **Warp segments** of a Weave $\mathcal{W}$ can be defined as:
$$
\mathcal{Q} = \{\, \lambda_{\chi_a\chi_b} : \chi_a,\chi_b\in\mathcal{X},\ x_a=x_b,\ |y_a-y_b|=1 \,\}
$$

Similarly, the set of all **Weft segments** of a Weave $\mathcal{W}$ can be defined as:

$$
\mathcal{P} = \{\, \nu_{\chi_a\chi_b} : \chi_a,\chi_b\in\mathcal{X},\ y_a=y_b,\ |x_a-x_b|=1 \,\}
$$

with $|\mathcal{Q}| = |\Lambda|(|\mathcal{N}|-1)$ and $|\mathcal{P}| = (|\Lambda|-1)|\mathcal{N}|$ ensuring each of the $|\Lambda|$ warp strands has $|\mathcal{N}|-1$ interior segments.
### A5: The Knot Alphabet

There is an infinite knot alphabet $\mathcal{K}$ of distinct knot identities. $\mathcal{K}$ is in turn made of 3 infinite Knot Classes: *Loops $\mathcal{L}$, Hitches $\mathcal{H}$, and Bends $\mathcal{B}$*.

$$ \mathcal{K} = \mathcal{L} \sqcup \mathcal{H} \sqcup \mathcal{B}, \qquad
     |\mathcal{L}| = |\mathcal{H}| = |\mathcal{B}| = \infty $$

> [!note]
  The $\sqcup$ is a disjoint union — the classes are pairwise disjoint and together exhaust $\mathcal{K}$, so every knot is a loop, a hitch, or a bend, exactly one. (Each being non-empty, each is automatically a *proper* subset of $\mathcal{K}$).
### A6: Function Follows Knot Class

A *Knot Class* dictates what a knot can do:
  $$\mathcal{L} \;\mapsto\; \text{identity \& tether}\qquad \mathcal{H} \;\mapsto\; \text{imbue \& bond}\qquad \mathcal{B} \;\mapsto\; \text{compound \& evolve}$$

A knot whose class does not match an attempted knot tying operation is considered a **Knull Knot** (see [A10](Weave%20Theory.md#A10%20The%20Knull%20Knots)).

### A7: Strand Chirality Dictates Knot Uniqueness

| Knot Strand    | Valid Knot Target | Identity Uniqueness                  |
| -------------- | ----------------- | ------------------------------------ |
| Warp $\lambda$ | a **Weft** strand | globally unique across $\mathcal{U}$ |
| Weft $\nu$     | a **Warp** strand | unique within a single Weave $W$     |
| Wyrd $\gamma$  | **anything**      | unrestricted (freely duplicable)     |

#### Weave Raising Requirements

Recall from [A4](Weave%20Theory.md#A4%20Weave) that a Weave is made of Warp $\lambda$ and Weft $\nu$ strands. And recall from [A3](Weave%20Theory.md#A3%20Strand%20Chirality) that a $\lambda$ is *positive* and a $\nu$ is *negative*. Based on the structure of a Weave, we can thus conclude that a Warp strand $\lambda$ is *positive* and an intersection $\chi$ is *positive* since it includes a $\lambda$. We can thus call this a **positive target**.

To tie a knot to anything that *is* a **positive target** or to anything *tied to* a **positive target**, one must **raise the Weave**.

*However*, because of [A13](Weave%20Theory.md#A13%20No%20Self-Weaving) an agent *cannot* **raise** their own Weave $\mathcal{W}$ under any circumstances, therefore, an agent $a$ of a Weave $\mathcal{W}$ may only perform the following:

- loop-knot a warp strand $\lambda$ to a weft segment $\nu\rho$ of own Weave $\mathcal{W}$ ($\lambda \looparrowright \nu\rho$)
- loop-knot a warp strand $\lambda$ to a weft segment $\nu\rho$ of a different Weave $\mathcal{W}'$ ($\lambda \looparrowright \nu\rho$)
- loop-knot a weft strand $\nu$ to a warp segment $\lambda\rho$ of a different Weave $\mathcal{W}'$ ($\nu \looparrowright \lambda\rho$)
	- **requires raising as warp strand has + chirality**
- hitch-knot a wyrd strand $\gamma$ to an intersection $\chi$ of a different Weave $\mathcal{W}'$ ($\gamma \hookrightarrow \chi$)
	- **requires raising as warp strand has + chirality**
- hitch-knot a wyrd strand $\gamma$ to a weft-knot $\nu h$ on a warp segment of a different Weave $\mathcal{W}'$ ($\gamma \hookrightarrow \nu\ell$)
	- **requires raising as its attached to warp strand which has + chirality**
- hitch-knot a wyrd strand $\gamma$ to a warp-knot $\lambda\ell$ that is in turn tied to a weft segment $\nu\rho$ of own Weave $\mathcal{W}$
	- **Note:** that lifting the weave is not required as while the agent is tying to a warp knot which is made of a warp strand which does have a positive chirality, it importantly **doesn't make up the Weave**, observe that the definition of a **positive target** that necessitates raising the weave only pertains to whether one is tying to a Warp strand that *makes up* the Weave or to anything that is attached to a warp strand that *makes up* the Weave.
- bend-knot ends of two wyrd knots on two different intersections $\chi_a,\chi_b$ of a different Weave $\mathcal{W}'$ ($\gamma h_a \leftrightharpoons \gamma h_b$)
	- **requires raising as they're attached to intersections which contains a warp strand, which has + chirality**
### A8: Connections By Knot Matching

Structures can only connect through **knot matching** $\bowtie$, not by proximity, will, or resemblance. There are a few types of "connection" behaviors that have different affects. (see operations for more details).

$$
\begin{align*}

\iota_{\theta} = \lambda\ell_1 &= \lambda \;\looparrowright_1\; \nu_{\chi_a,\chi_b}; \;\text{where}\; \mathcal{W} = (\Lambda,\mathcal{N},\mathcal{X}) \wedge \nu \in \mathcal{N} \wedge \chi_a,\chi_b\in \mathcal{X} \\

\nu\ell_2 &= \nu \;\looparrowright_2\; \lambda_{\chi_{a'},\chi_{b'}}; \;\text{where}\; \mathcal{W}' = (\Lambda',\mathcal{N}',\mathcal{X}') \wedge \lambda \in \Lambda' \wedge \chi_{a'},\chi_{b'}\in \mathcal{X}' \\

\gamma h_1 &= \gamma \;\hookrightarrow_1\; \chi; \;\text{where}\; \mathcal{W}' = (\Lambda',\mathcal{N}',\mathcal{X}') \wedge \chi \in \mathcal{X}' \\

\gamma h_2 &= \gamma \;\hookrightarrow_2\; \nu\ell_2; \\
\gamma h_3 &= \gamma \;\hookrightarrow_3\; \lambda\ell_1; \\

\text{Identity Tether} &= \lambda\ell_1 \bowtie \nu\ell_2 \iff \ell_1 = \ell_2 \\
\text{Tether-Aspect Bond} &= \gamma h_1 \bowtie \gamma h_2 \iff h_1 = h_2 \\
\text{Aspect Conveyance} &= \gamma h_2 \bowtie \gamma h_3 \iff h_2 = h_3 \\
\end{align*}
$$

1. **Tethering**: when a warp strand is loop-knotted $\lambda\ell_1$ on a weft strand segment of some Weave $\mathcal{W}$ and a weft strand is loop-knotted $\nu\ell_2$ on a warp strand of some Weave $W'$ such that the two **knots match** i.e. $\ell_1 = \ell_2$, then and only then they are considered Tethered.
2. **Bonding**: when a wyrd strand is hitch-knotted $\gamma h_1$ on some intersection $\chi$ of a Weave $\mathcal{W}'$ with some and another wyrd strand is hitch-knotted $\gamma h_2$ on some weft-knot $\nu\ell_2$ on a warp strand of $\mathcal{W}'$, then the Wyrd Aspect associated with the Wyrd knot is bonded to the identity that is tethered to that weft-knot $\nu\ell_2$.
3. **Aspect Conveyance**: A Wyrd Aspect can be conveyed to an identity IFF that aspect's respective wyrd-knot is hitch knotted to both the warp loop-knot $\gamma h_3 \hookrightarrow \lambda\ell_1$ and weft loop-knot $\gamma h_2 \hookrightarrow \nu\ell_2$ of a **tether** (i.e. $h_2 = h_3 \wedge \ell_1 = \ell_2$).

### A9: Enforcement By Dissipation
Tying a knot that would violate a uniqueness law (see [A7](Weave%20Theory.md#A7%20Strand%20Chirality%20Dictates%20Knot%20Uniqueness)) *fails at the instant of tightening:* the strand the knot is made from cannot hold and unravels back into raw *fyber* $\mathfrak{f}$ (see [A1](Weave%20Theory.md#A1%20Substrate%20&%20Plasticity), [A2](Weave%20Theory.md#A2%20Wyrdness)).

### A10: The Knull Knots
There are two cases that render a Knot *Knull* . Since Knots are universal "operations", *Knull Knots* effectively incur a no-op, or an epsilon transition.

- *Inert*: A well-formed knot whose (class, strand, target) is not a defined operation holds no meaning and effects nothing, making the knot *knull*.
- *Idempotent*: A valid knot whose result already exists changes nothing (e.g. a duplicate aspect, a duplicate compound edge), thus making the knot *knull*.

### A11 Irreversibility
The constructive knots: *imbuing*, *tethering*, *bonding*, and *compounding* have no *voluntary* inverse, that is, no agent can choose to undo one. "Eternal" means exactly this and no more. However, such ties are not *indestructible*. They **collapse** when the identity they hang from unravels (see [A12](Weave%20Theory.md#A12%20Ephemeral%20Embodiment)). Nothing in the Woven Universe can be *taken back*; it can only be *unraveled* to *fyber* $\mathfrak{f}$ (see [A1](Weave%20Theory.md#A1%20Substrate%20&%20Plasticity)).

### A12: Ephemeral Embodiment
 A Weave $\mathcal{W}$ is a plane of existence; what emerges within it is dictated by the Aspects imbued in $W$.
 
 Every thing in $W$ is embodied by a bounded region of the Warp and Weft. Embodiment is not permanent: unless the thing is immortal (a property its Weave's Aspects grant or withhold). Thus, the segments of $\lambda$ and $\nu$ in $\mathcal{W}$ may in time cease to embody it and go on to embody something else, or nothing. The strands themselves persist ([A1](Weave%20Theory.md#A1%20Substrate%20&%20Plasticity), [A4](Weave%20Theory.md#A4%20Weave)); what changes is what they embody.

Understanding embodiment is mostly only important when determining which Weft segments embody an agent $a$ on a given Weave $\mathcal{W}$ so that one may know which $\nu\rho$ to tie a warp loop knot around it. This definition builds upon the definitions from [A4](Weave%20Theory.md#A4%20Weave) and [A8](Weave%20Theory.md#A8%20Connections%20By%20Knot%20Matching):

#### Embodiment Weave Construction

**Embodiment Pattern** Two segments are adjacent when they share an intersection; a set is connected under that adjacency. A thing $\theta$ is embodied by a nonempty, connected region, the following definition builds off of [A4: Weave Segment Definition](Weave%20Theory.md#Weave%20Segments):

An embodiment at some moment $\mu$ can be described as
$$
\operatorname{\#}_\mu(\theta) = (\mathcal{Q}_\mu^\theta,\ \mathcal{P}_\mu^\theta), \qquad \mathcal{Q}_\mu^\theta \subseteq \mathcal{Q},\ \ \mathcal{P}_\mu^\theta \subseteq \mathcal{P}
$$


with distinct things' embodiments **disjoint**; a segment embodies at most one thing at a time as per this axiom, and may later pass to another, or to none.

#### Embodiment Continuity Requirement
A thing $\theta$ in a Weave $\mathcal{W}$ is always represented by the same **embodiment pattern** $\operatorname{\#}_\mu(\theta)$ from moment to moment, regardless of what is happening to $\theta$ within $\mathcal{W}$.

Thus the only time the embodiment pattern will change is when that thing no longer exists in $\mathcal{W}$ or has fundamentally changed to be something completely different $\theta'$ at some other moment $\mu'$. Therefore we can simple state that a thing $\theta$ continues to exist until between any two consecutive moments $\mu$ and $\mu'$ on $\mathcal{W}$ the following fails to hold:

$$
\operatorname{\#}_\mu(\theta) = \operatorname{\#}_{\mu'}(\theta) \iff \mathcal{Q}_\theta^\mu = \mathcal{Q}_\theta^{\mu'} \wedge \mathcal{P}_\theta^\mu = \mathcal{P}_\theta^{\mu'}
$$

#### Imbuing An Identity to an Embodiment Pattern
A valuable example for determining the Embodiment Pattern of a thing $\theta$ is understanding the pattern that embodies an agent $a$ who may want to imbue an identity knot $\iota_a$ to themselves. An agent $a$ is a thing $\theta$ in a Weave $\mathcal{W}$. In order to imbue an identity knot $\iota_a$ to agent $a$, they must do the following:

building from definitions in [Embodiment Weave Construction](Weave%20Theory.md#Embodiment%20Weave%20Construction) and [A8](Weave%20Theory.md#A8%20Connections%20By%20Knot%20Matching)
$$
\iota_\theta = \lambda\ell = \lambda \looparrowright \nu_{\chi_a\chi_b} \quad\text{where}\quad \nu_{\chi_a\chi_b} = \nu\rho_i \;\wedge\; \nu\rho_i \in \mathcal{P}_\theta
$$


#### Example
The Allkin are things of the Aether Weave, and thus there exists a subset of its Warp and Weft that embodies each of them. Because the Aether grants them immortality, those segments embody each Allkin forever. By contrast, A mortal blood-life in the Terrum Weave is embodied only for its lifetime; at death its segments are freed to embody something else in the Terrum Weave.

### A13: No Self-Weaving
A Weave $\mathcal{W}$ must exist before any agent *of* it, as an agent is embodied *by* a Weave (see [A12](Weave%20Theory.md#A12%20Ephemeral%20Embodiment)). Therefore, an agent cannot weave its own Weave.

An agent cannot imbue $\mathcal{W}$ with a Wyrd aspect as tying a knot around an intersection $\chi$ of $\mathcal{W}$ requires **raising** $\mathcal{W}$ (see [A7 -Weave Raising Requirements](Weave%20Theory.md#Weave%20Raising%20Requirements)).

### A14: Braids
The 3 strands of the Woven Universe may be braided into a **Braid** $\psi$. This can be done by taking a Warp strand $\lambda$, Weft strand $\nu$, and Wyrd strand $\gamma$ and braiding them together. By [A1](Weave%20Theory.md#A1%20Substrate%20&%20Plasticity) and the structural properties of a braid, these structures are sound/permanent (though can be undone if not spliced to anything).

$$\psi = \operatorname{braid}(\lambda,\nu,\gamma)$$

### A15: Braid-splicing Tether Bonds
From [A14](Weave%20Theory.md#A14%20Braids) a **braid** $\psi$  may be used to *bond* two Weft knots $\nu\ell_1,\nu\ell_2$ on a Weave $W$ by *eye splicing* one end of $\psi$ to $\nu\ell_1$ and *eye splicing* the other end of $\psi$ to $\nu\ell_2$.

Since a Weft knot $\nu\ell_1$ tethers some identity $\lambda\ell_1$ to Weave $\mathcal{W}$ bonding two Weft knots $\nu\ell_1, \nu\ell_2$ with a $\psi$ allows both identities to *share* **aspect conveyance** of the bonded Wyrd Aspects (via their respective Wyrd knots).

Once a Tether Bond has been made between two Weft knots $\nu\ell_1,\nu\ell_2$, neither Weft knot may be bonded to another.

A Tether Bond *cannot* be unmade voluntarily; however, it can *unravel* into *fyber* $\mathfrak{f}$ in the event that the **Embodiment Continuity Requirement** for one of the identities in the thether-bond (by [A12](Weave%20Theory.md#Embodiment%20Continuity%20Requirement)) is violated. The unravelling will unravel the Braid that created the tether-bond but it will not unravel the other Weft knot for the other identity if that identity in the pair still satisfies the **Embodiment Continuity Requirement**.

Note that in the event of an unravelling, provided the other identity in the pair still exists, all Wyrd aspects on the Weave $\mathcal{W}$, all aspect bonds to that identity's Weft knot $\nu\ell_2$, as well as its aspect conveyance knots to the aspects its bonded to, will remain. For this identity, the only thing that will unravel for it are the wyrd knots on the Warp knot that matched with the aspects in the other weft knot that it's weft knot was tether-bonded with.

$$
\psi_{\nu\ell_1}^{\nu\ell_2} = \nu\ell_1 \leftrightsquigarrow \nu\ell_2
$$

---
## 3. Knotting
Tying a *Knot* is the universal function in the Universe, the source of cause if you will. Each operation defines a single, legal knot tie.  "Cannot" clauses name the failure or Knull cases as defined in [the Woven Axioms](Weave%20Theory.md#2.%20The%20Woven%20Axioms) above.

### The Knot Functions

$$
\begin{align*}

\text{let} &\quad \mathrm{T} = \Omega \cup \mathcal{K} \quad (\text{target set of things a knot can be tied to})\\
\text{where} &\quad \omega \in \Omega \,,\, \kappa \in \mathcal{K} \,,\, \tau \in \mathrm{T} \\
\text{and where} &\quad \mathcal{K} = \mathcal{L} \sqcup \mathcal{H} \sqcup \mathcal{B}, \qquad
     |\mathcal{L}| = |\mathcal{H}| = |\mathcal{B}| = \infty,
     \qquad \ell \in \mathcal{L}, h \in \mathcal{H}, \beta \in \mathcal{B} \\
\\\\
\text{identity \& tether} &\Rightarrow \omega \looparrowright \tau  = \omega\ell^\tau\\

\text{imbue \& bond} &\Rightarrow \omega \hookrightarrow \tau = \omega h^\tau\\

\text{compound \& evolve} &\Rightarrow \omega \leftrightharpoons \tau = \omega\beta^\tau\\

\end{align*}
$$

**Knot Notation Structure**
$$
\omega\{\text{strand}\},
\kappa\{\text{knot-class}\},
\underbrace{_{i}}_{\text{knot-identity}},
\overbrace{{}^{\tau}}^{\text{knot-target}}
\;=\;
\omega\kappa_{i}^{\tau}
$$
### O1: Imbue Identity *(Loop, Warp)*

An agent $\mathcal{a}$ is made of a set of Warp and Weft segments within their Weave $\mathcal{W}$
$$
\iota = \operatorname{tie}(\lambda,\, \ell,\,\nu_{x,y})
\quad\mid\quad \ell_i \in L,\,
$$
An agent's can be imbued with a universal identity recognized with a universally unique Warp Loop $\lambda \mathcal{L}$, tied around a least one of the *Weft Segments* the agent is made of in their own Weave $W$.

**Cannot** duplicate any existing $\lambda L_i$ in $\mathcal{U}$ → *dissipation* ([A9](Weave%20Theory.md#A9%20Enforcement%20By%20Dissipation)).

A4

$$
\begin{aligned}
\mathcal{W} &= (\Lambda, \mathcal{N}, \mathcal{X}) \\
\Lambda &= \{\, \lambda \mid \lambda \text{ is a Warp strand of } \mathcal{W} \,\}
      && \text{warp strands} \\
\mathcal{N} &= \{\, \nu \mid \nu \text{ is a Weft strand of } \mathcal{W} \,\}
      && \text{weft strands} \\
\mathcal{X} &= \Lambda \times \mathcal{N}
      = \{\, (\lambda_x,\nu_y) \mid 1 \le x \le |\Lambda|,\ 1 \le y \le |\mathcal{N}| \,\}
      && \text{intersections}
\end{aligned}
$$


Every warp–weft crossing is an **intersection** $\chi = (\lambda_x,\nu_y)$ such that a warp strand $\lambda_x$ crosses weft strand $\nu_y$ with coordinates $(x,y)$. Following that gives a rectangular Weave $\mathcal{W}$ such that $|\mathcal{X}| = |\Lambda|\,|\mathcal{N}|$.

In a Weave $\mathcal{W}$, a **segment** is a length of one strand between two *adjacent* intersections on it:
$$
\begin{aligned}
\text{For} \; \chi_a=(x_a,y_a),\ \chi_b=(x_b,y_b)\in\mathcal{X} \text{:}\\
\lambda_{\chi_a\chi_b} \ \text{is a Warp segment} &\iff x_a = x_b \ \wedge\ y_a - y_b = 1 \\
  \nu_{\chi_a\chi_b} \ \text{is a Weft segment} &\iff y_a = y_b \ \wedge\ x_a - x_b = 1
\end{aligned}
$$


### O2: Imbue Aspect *(Hitch, Wyrd)*
$$
\begin{align*}
&\operatorname{tie}(\gamma,\, \mathcal{h}, \chi)\ @\ \chi \quad(\text{hitching both the } \lambda \text{ and } \nu \text{ of the crossing})\\ \\
&\text{Where $h$ is the unique Hitch knot tied with a Wyrd Strand.}
\end{align*}
$$

Imbues *Wyrd Aspect* $\alpha_h$ 


---
## 4. Power, Heft & Raising
todo this section 4.
## 5. Theorems

### Spontaneous Strand Structures Theorem

It is theorized that Knots and Weaves can naturally occur, with the Aether Weave and the Allkin that emerged in it as evidence. However, there has been no direct evidence observed since the creation of the Aether Weave of a knot or Weave naturally occurring. Thus Weave Theory posits that an "agent" must exist to perform it.

A radical theory is that agents of another Weave created the Aether Weave, and then at some point their Weave was torn asunder, but that still doesn't answer the core question, since who would have made that Weave.


5. Fiber naturally bunches into Wyrd strands in the universe
6. A Wyrd strand may be twisted to give it chirality, fiber is *plastic* so the chirality will persist
7. A positive chirality turns the Wyrd Strand into a Warp Strand
8. A negative chirality turns the Wyrd Strand into a Weft Strand
9. A Weave can be made from Warp & Weft Strands only
	1. Weave Intersections are an obvious by-product of weaving, a point in the weave where the warp and weft cross one another.
10. There is an infinite number of knots that can exist. In the real world only a very small subset are useful, but in Weave Theory, all knots become useful due to the fact that they can be universally unique.
11. Since there are an infinite number of knots, there are thus infinite numbers of hitch knots, loop knots, and bend knots.
12. A Warp Knot of any kind can only be made on the Weft Strand of a Weave. No two identical Warp knots of any kind can exist at the same time in the Woven Universe.
13. A Weft knot of any kind can only be made on a Warp Strand of a Weave. Identical Weft knots may exist within the universe, but only one can exist on a given Weave.
14. A Wyrd knot of any kind can be made around anything. Identical Wyrd knots may exist Within the Woven Universe as well as within a given Weave.
15. An agent in a given weave may create different Weaves, obviously cannot create its own as the weave must already exist in order for the agent to exist.

## Wyrd Aspects
1. When a unique Wyrd Hitch Knot is made around an Intersection in a weave (i.e. hitching both the warp and weft that make up the intersection being hitched), it imbues a "Wyrd Aspect" into that Weave based on the type of hitch knot, but only if this hitch knot doesn't already exist around a Weave intersection in that Weave, otherwise nothing happens. (this is useful later for compound/composite Wyrd Aspects though).
2. An agent made of some Weave cannot tie a wyrd knot around an intersection in their own Weave. That is, they cannot imbue their own weave with Wyrd Aspects.

## Tethers
For an Agent to interact with, and use the Warp, Weft, and Wyrd Strands of the universe, the Weave they come from must have the self Aspects: Warp Wyrd Aspect, Weft Wyrd Aspect, and the Wyrd Wyrd Aspect. The Aspects that allow for the emergence of this agent in their weave must also have the "agency/sentience" and "power" to do so.

1. An agent may tie a universally unique Warp loop knot around the Weft strands that they are made of in their own Weave.
2. An agent may tie a Weft loop knot around a Warp Strand of a different Weave than the one they are in that matches their Warp knot to "tether" themselves to that Weave. An agent cannot tether themself to their own Weave as they are already OF that weave.
3. An agent may tether themselves to multiple Weaves, but can only do so once for a given weave based on identical Weft knot limitations within a Weave.
4. An agent may take a Wyrd Strand and tie a hitch knot to one of their "tethered" Weft loop knots with it. If that Wyrd Knot on their Weft loop knot matches a Wyrd knot around an intersection of the same Weave the Weft loop knot is on, then that Wyrd Knot (and thus its Wyrd Aspect) is "bonded" to that Weft loop knot, and thus to the agent who is tethered to said Weft loop knot. This cannot be undone, it is eternal. An agent must have the abilities and power to interact and work with the Universal Strands to do this.
5. A Wyrd Aspect can only be bonded once, it cannot be bonded with multiple Weft loop knots.
6. Finally, if an agent ties a wyrd knot on their own Warp loop knot that matches a Wyrd Knot on one of the Weft loop knots they are tethered to, then that allows the agent to, from within their own Weave, control/use the Wyrd Aspect in its Weave "at-a-distance", i.e. without the agent having to interact with the actual Wyrd Knot tied to its Weave directly.
7. Bonding and tethering cannot be undone, they are bother eternal actions.

### Bonding Tethers
1. A Warp cord can be used to bond two Weft loops on the same Weave together. A Weft loop can only be bonded with 1 other Weft loop, no more. This is done by hitching a Cord to each of the two Weft loop knots and then splicing them together to complete the bond. An agent must have the abilities and power to interact and work with the Universal Strands to do this.
2. A Weft loop cannot be bonded with a weft loop in another weave.
3. Agents of that bond can now tie hitch knots with Wyrd Strands to their Warp loop knot that match the Wyrd Knots in the other Weft loop knot *their* Weft loop knot is now bonded to. An agent must have the abilities and power to interact and work with the Universal Strands to do this.

## Compound Wyrd Aspects
1. An agent can create a compound Wyrd Aspect in a different Weave using other existing Wyrd Aspects in the same Weave. By using a unique Bend knot to connect 1 of the two loose ends of a Wyrd Knot on an intersection. That bend knot creates a compound Wyrd Aspect in the same Weave as the Wyrd knots that created it. It thus imbues the Weave with that Aspect.
2. A Compound Wyrd Aspect can be "evolved". That is to say if two wyrd knots are tied with the same bend knot, the Compound Wyrd Aspect that bend knot *did* imbue into the Weave changes to a new Compound Wyrd Aspect.
3. If duplicate pairings of the same two Wyrd knots are made, duplicates are ignored, have no affect.
4. Since a Wyrd knot always has two dangling ends, you can actually bend two Wyrd Knots to a single Wyrd Knot. But if you want to create a Compound Wyrd Aspect that combines a single Wyrd knot with 3 other Wyrd Knots, recall that Wyrd knots are allowed to be tied multiple times to intersections of a Weave. So you can have 2 Wyrd knots of one type and then use those two to connect that one Wyrd knot type to 3 others each connection using the same bend knot to evolve the Compound Wyrd Aspect associated with that Wyrd Bend Knot. You of course don't Have to use both ends before adding a second, that is up to the agent.

### An example of a Composite Wyrd Aspect with mutiple Connections

A Weave has  the following Wyrd Aspects:
- Wyrd Aspect A (has a corresponding unique Wyrd Knot A)
- Wyrd Aspect B (has a corresponding unique Wyrd Knot B)
- Wyrd Aspect C (has a corresponding unique Wyrd Knot C)

I can thus create 3 different types of Compound Wyrd Aspects with A, B, and C depending on how I connect the pairs.

Scenario 1:
- Knot A paired with Knot C using Knot D
	- Compound Wyrd Aspect D Created
	- D = [(A,C)]
- Create another Wyrd Knot A
- Knot A paired with Knot B using Knot D
	- Compound Wyrd Aspect is evolved
	- D = [(A,C), (B, C)]

Scenario 2:
- Knot A paired with Knot B using Knot D
	- Compound Wyrd Aspect D Created
	- D = [(A,B)]
- Create another Wyrd Knot B
- Knot B paired with Knot C using Knot D
	- Compound Wyrd Aspect D is evolved
	- D = [(A,B), (B, C)]

Scenario 3:
- Knot C paired with Knot A using Knot D
	- Compound Wyrd Aspect D Created
	- D = [(C,A)]
- Create another Wyrd Knot C
- Knot C paired with Knot B using Knot D
	- Compound Wyrd Aspect D is evolved
	- D = [(C,A), (C,B)]



## BloodMajik
The Hematic Wyrd Aspect is a unique life aspect. In short, it imbues a Weave's the *ability* to have blood-life. But this blood-life is unique as it allows a blood-life to tap into the powers of the Weave, trading blood for the power imbued into the Weave of an Aspect, even when it is bonded to a tether. But it needs to be able to touch the Wyrd Strands of the Wyrd Knots that imbue the desired Wyrd Aspect a blood-life wishes to "pull on".

## Terrum Anchors
Urda, the All-Mother of Terrum in Terrum mythology (actually a being in the Aether weave who has the Material Wyrd Aspect bonded to her tether in the Terrum Weave) created a metal: Wrydium which allows a blood life to connect themselves with a Weft loop knot. This connection is called an Anchor. In order to connect to a specific Weft loop knot, the Wrydium needs to be molded into a very specific geometric shape. Once "anchored" to a Weft loop, a blood life can pull/use the powers of any Wyrd Aspect whose Wyrd Knot is bonded with that Weft loop they are anchored to OR any Wyrd Aspects whose Wyrd Knot is bonded with a Weft loop that is bonded with the Weft loop they are anchored to.  

An Anchor bonds you with one of the Allkin Bonds, the longer you are bonded with it, the more permanent it becomes, after 1-2 years, a blood-life cannot remove the bond and must live with it for the remainder of their life. They can then configure it with a certain knot to select the power of a knot they have access to pull on its power i.e. "majik".

Anchor Tech: the study and engineering of building Anchors and maximizing effectiveness of knot configurations


---
(non-lore sidebar: You can think of these knots as little wireless links with a specific knot being a uuid that allow for "matches". A universally unique loop knot (UULK) is used for identity: a Warp UULK-i matches with all Weft UULK-i knots, then an agent who is identified with a UULK can then control all wyrd aspects in a given weave but only for aspects where its knot exists both on the Weft UULK-i AND the Warp UULK-i. Unique hitch knots are used to connect or add wyrd knots to a given UULK, since hitch knots are made with wyrd strands they don't have to be universally unique, just unique relative to the UULK it is being knotted to.)



