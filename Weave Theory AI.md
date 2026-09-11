# Weave Theory (AI draft)

> This is an AI-generated redraft of `Weave Theory.md`, incorporating the author's
> notes and decisions. It is kept separate so it can be compared against the
> human original and is **not** canon until the author folds it back in.
>
> Goal of this draft: state the system as a small set of **axioms** (irreducible
> truths of the Woven Universe), then derive **what can and cannot be done** from
> them, using notation to carry weight the prose was carrying before.

---

## 1. Notation

| Math           | ASCII   | Object                                                                              |
| -------------- | ------- | ----------------------------------------------------------------------------------- |
| $\mathfrak{f}$ | `f`     | **Fyber** — the sole substrate                                                      |
| $\gamma$       | `y`     | **Wyrd strand** (achiral)                                                           |
| $\lambda$      | `n`     | **Warp strand** ($+$ chirality)                                                     |
| $\nu$          | `u`     | **Weft strand** ($-$ chirality)                                                     |
| $W$            | `W`     | **Weave**                                                                           |
| $\chi$         | `x`     | **Intersection** — one warp–weft crossing in a weave                                |
| $\psi$         | `c`     | **Cord**                                                                            |
| $\mathcal{K}$  | `K`     | infinite alphabet of distinct **knot identities**                                   |
| $\mathcal{L},\,\mathcal{H},\,\mathcal{B}$    | `L,H,B` | knot **classes**: **L**oop, **H**itch, **B**end                                     |
| $a$            | `a`     | **agent**                                                                           |
| $\alpha$       | —       | a **Wyrd Aspect**                                                                   |
| $\varphi$      | `phi`   | the **Wyrd Function** — the (undivined) map from a compound's network to its Aspect |
| $\mathcal{U}$  | `U`     | the whole **Woven Universe**                                                        |
| $\bowtie$      | `><`    | **Match** — the sole connection relation (same id, opposite chirality)              |

**Strand-classes** (by chirality of the tying strand): $\sigma \in \{\lambda, \nu, \gamma\}$.

**Twisting.** Fyber bunches into $\gamma$; twisting fixes chirality:

$$\operatorname{twist}_{+}(\gamma) = \lambda \qquad \operatorname{twist}_{-}(\gamma) = \nu$$

**Tie signature.** Every action in the system is a single tie:

$$\operatorname{tie}(\sigma,\, k)\ @\ \tau \quad\mid\quad \sigma\in\{\lambda,\nu,\gamma\},\ \ k\in\mathcal{K},\ \ \tau=\text{target}$$

Read: *"tie knot $k$, of strand-class $\sigma$, onto target $\tau$."* The knot's class is **intrinsic** — $\mathcal{K}$ is partitioned into $\mathcal{L}$, $\mathcal{H}$, $\mathcal{B}$ (**A5**), so $k$ already *is* a loop, hitch, or bend and no separate class argument is needed. Each operation instead **pins the class with a membership bar**, naming its knot from the appropriate set: $\mid\ \ell\in\mathcal{L}$ ties a loop, $\mid\ h\in\mathcal{H}$ a hitch, $\mid\ b\in\mathcal{B}$ a bend.
A tied knot is written $\sigma k$ (e.g. $\lambda\ell_i$ = a warp loop, identity $i$; $\gamma h$ = a wyrd hitch).

**Matching** ($\bowtie$) — the only mechanism of connection:

$$\lambda \ell_i \bowtie \nu \ell_i \quad\text{iff the same loop } \ell_i,\ \text{opposite chirality.}$$

---

## 2. Axioms

The irreducible truths. Everything in §3–§6 is derived from these.

- **A1 — Substrate & plasticity.** All that exists is fyber $\mathfrak{f}$. Fyber is *plastic*: any deformation imparted to it persists.
- **A2 — Wyrd.** Fyber spontaneously bunches into achiral Wyrd strands $\gamma$.
- **A3 — Chirality.** A Wyrd strand may be twisted into a Warp strand $\lambda$ ($+$) or a Weft strand $\nu$ ($-$). By **A1**, the chirality is permanent.
- **A4 — Weave.** A Weave is woven from Warp and Weft strands **only**, and is the triple $W = (\Lambda,\ \mathcal{N},\ \mathcal{X})$ of its warp strands, weft strands, and intersections:

  $$
  \begin{aligned}
  \Lambda &= \{\, \lambda \mid \lambda \text{ is a Warp strand of } W \,\}, \qquad
  \mathcal{N} = \{\, \nu \mid \nu \text{ is a Weft strand of } W \,\}, \\
  \mathcal{X} &= \Lambda \times \mathcal{N} = \{\, \chi = (\lambda_x,\nu_y) \mid 1 \le x \le |\Lambda|,\ 1 \le y \le |\mathcal{N}| \,\}
  \end{aligned}
  $$

  Every warp–weft crossing is an **intersection** $\chi = (\lambda_x,\nu_y)$ with coordinates $(x,y)$ — a full rectangular weave, so $|\mathcal{X}| = |\Lambda|\,|\mathcal{N}|$. A **segment** is a length of one strand between two *adjacent* intersections on it, named for the strand it is *part of* (never for the knot that lands on it). For $\chi_a=(x_a,y_a),\ \chi_b=(x_b,y_b)\in\mathcal{X}$:

  $$
  \begin{aligned}
  \lambda_{\chi_a\chi_b} \ \text{is a Warp segment} &\iff x_a = x_b \ \wedge\ |y_a - y_b| = 1 \\
  \nu_{\chi_a\chi_b} \ \text{is a Weft segment} &\iff y_a = y_b \ \wedge\ |x_a - x_b| = 1
  \end{aligned}
  $$

  A Warp segment can host a **Weft** knot; a Weft segment a **Warp** knot (**A7**).
- **A5 — Knot alphabet.** There is an infinite alphabet $\mathcal{K}$ of distinct knot identities, partitioned by topology into three infinite classes — **Loops** $\mathcal{L}$, **Hitches** $\mathcal{H}$, and **Bends** $\mathcal{B}$:

  $$
  \mathcal{K} = \mathcal{L} \sqcup \mathcal{H} \sqcup \mathcal{B}, \qquad |\mathcal{L}| = |\mathcal{H}| = |\mathcal{B}| = \infty
  $$

  The $\sqcup$ is a **disjoint union** — the three classes are pairwise disjoint and together exhaust $\mathcal{K}$, so every knot is a loop, a hitch, or a bend, exactly one. (Each being non-empty, each is automatically a *proper* subset of $\mathcal{K}$.)
- **A6 — Function follows class.** Knot *class* fixes what a knot can do:

  $$\mathcal{L} \;\mapsto\; \text{identity \& tether}\qquad \mathcal{H} \;\mapsto\; \text{imbue \& bond}\qquad \mathcal{B} \;\mapsto\; \text{compound \& evolve}$$

  A tie whose class does not match the attempted operation is **inert** (see **A10**).
- **A7 — Chirality fixes placement and uniqueness:**

| tied of        | rides only on     | identity uniqueness                  |
| -------------- | ----------------- | ------------------------------------ |
| Warp $\lambda$ | a **Weft** strand | globally unique across $\mathcal{U}$ |
| Weft $\nu$     | a **Warp** strand | unique within a single Weave $W$     |
| Wyrd $\gamma$  | **anything**      | unrestricted (freely duplicable)     |

- **A8 — Connection is matching.** Structures connect *only* through matching $\bowtie$ — never by proximity, will, or resemblance. Two tied knots match iff they carry the **same identity** in $\mathcal{K}$, in the role their strand allows:

  $$
  \lambda\ell_1 \bowtie \nu\ell_2 \iff \ell_1 = \ell_2 \qquad\qquad \gamma h_1 \bowtie \gamma h_2 \iff h_1 = h_2
  $$

  A **warp loop matches the weft loops of its identity** (one warp, one weft, same $\ell$ — an identity to its tethers); a **wyrd hitch matches the wyrd hitch of the same id** wherever it sits (achiral — the two ends of a bond or a control).
- **A9 — Enforcement by dissipation.** A tie that would violate a uniqueness law (**A7**) *fails at the instant of tightening*: the knot cannot hold and unravels back into raw fyber $\mathfrak{f}$. The agent must begin again.
- **A10 — The two silent failures.**
  - *Inert:* a well-formed tie whose (class, strand, target) is not a defined operation holds no meaning and effects nothing.
  - *Idempotent:* a valid operation whose result already exists changes nothing (a duplicate aspect, a duplicate compound edge).
- **A11 — No self-authorship.** A Weave must exist before any agent *of* it (an agent is embodied *by* a Weave, **A13**), so an agent cannot weave its own Weave — nor imbue or re-knot it. The bar is *mechanical, not decreed*: mutating a Weave means **raising** it (§4), and raising needs purchase on its strands from **outside** — but an agent embodied *within* a Weave has no vantage outside the one Weave it is made of. You cannot lift the floor you stand on. **Distortion** is the exception that proves the rule: an agent that can wield the strands may squeeze, stretch, or fold its own Weave — deforming the *embedding* (useful for travel), never re-tying the *structure* — because that acts on the whole from within and adds no knot.
- **A12 — Irreversibility.** The constructive ties — imbuing, tethering, bonding, compounding — have no *voluntary* inverse: no agent can choose to undo one. "Eternal" means exactly this and no more — such ties are not *indestructible*. They **collapse** when the identity they hang from unravels (**A13**). Nothing in the Woven Universe can be *taken back*; it can only be *unmade*.
- **A13 — Ephemeral Embodiment.** Every *thing* in a Weave $W$ is **embodied** by a bounded region of its Warp and Weft — the **segments** (**A4**) that, for now, *are* that thing. Embodiment is not permanent: unless the thing is **immortal** (a property its Weave's Aspects grant or withhold), its segments may cease to embody it and go on to embody something else, or nothing. The strands persist (**A1**, **A4**); only *what they embody* changes. And an identity loop (O1) tied around a freed embodiment has nothing left to hold — it unravels into fyber (**A9**), and its name $\ell_i$ returns to the alphabet, free to be tied anew. And it does not fall alone: by the **unravel-cascade**, everything hanging from that identity collapses with it — the weft tethers matched to it (**A8**), every wyrd hitch tied on those loops (the bonds of O4, the controls of O5), and the imbuing hitches those bonds reached — **dis-imbuing** their Aspects (O2) — and, through the bends tied onto those hitches, the compound aspects built on them (**O7**). This cascade is the *only* force that removes an Aspect from a Weave: a being bonded to an Aspect is its **keystone**, and unmaking the being unmakes the Aspect.
  > *Example.* The Allkin are things of the Aether Weave — a subset of its Warp & Weft embodies each of them. Because the Aether grants them immortality, those segments embody each Allkin forever. A mortal blood-life is embodied only for its lifetime; at death its segments — and any identity tied around them — dissolve back to fyber, to be woven anew.

  *Formally* (from **A4**). All warp and all weft segments of $\mathcal{W}$:

  $$
  \mathcal{Q} = \{\, \lambda_{\chi_a\chi_b} : \chi_a,\chi_b\in\mathcal{X},\ x_a=x_b,\ |y_a-y_b|=1 \,\}, \qquad
  \mathcal{P} = \{\, \nu_{\chi_a\chi_b} : \chi_a,\chi_b\in\mathcal{X},\ y_a=y_b,\ |x_a-x_b|=1 \,\}
  $$

  with $|\mathcal{Q}| = |\Lambda|\,(|\mathcal{N}|-1)$ and $|\mathcal{P}| = (|\Lambda|-1)\,|\mathcal{N}|$. Calling two segments *adjacent* when they share an intersection, at a moment $\mu$ a **thing** $\theta$ is embodied by a nonempty, **connected** region $\operatorname{emb}_\mu(\theta) = (\mathcal{Q}^\theta_\mu, \mathcal{P}^\theta_\mu)$, with $\mathcal{Q}^\theta_\mu \subseteq \mathcal{Q}$, $\mathcal{P}^\theta_\mu \subseteq \mathcal{P}$, and distinct things' embodiments **disjoint** (a segment embodies one thing at a time). The pattern is **constant while $\theta$ exists**: $\operatorname{emb}_\mu(\theta) = \operatorname{emb}_{\mu'}(\theta)$ across consecutive moments $\mu,\mu'$; the first moment that fails, $\theta$ has either ceased (its segments freed) or become a *different* thing $\theta'$. So a thing does **not** drift through the Weave by re-embodying — motion and growth ride on distortion (**A11**), not on trading segments. An **agent** $a$ is a thing that also bears an **identity** (**A8**): its warp loop $\lambda\ell$ loops a nonempty subset $\mathcal{P}^a_\iota \subseteq \mathcal{P}^a_\mu$ of its own weft segments — the segments through which its $\bowtie$-matches (tethers) reach other weaves.

> **Failure taxonomy (from A9–A10).** Every disallowed act resolves one of three ways:
> **dissipation** (violates a uniqueness law → unravels to fyber), **inert** (wrong tool → nothing), or
> **idempotent** (already done → nothing). There are no other outcomes, and no exceptions.

---

## 3. Operations — what can be done

Each operation is one legal tie. "Cannot" clauses name the failure mode from the taxonomy above.

### O1 · Identity  *(Loop, Warp)*
$$\operatorname{tie}(\lambda,\, \ell_i)\ @\ \text{own weft-strands} \quad\mid\quad \ell_i \in \mathcal{L}$$
An agent's identity is a globally unique Warp loop $\lambda\ell_i$ tied around the weft strands it is made of, in its own weave.
- **Cannot** duplicate any existing $\lambda\ell_i$ in $\mathcal{U}$ → *dissipation* (**A9**). This is the hard law: forge a taken identity and it unravels in your hands.

### O2 · Imbue Aspect  *(Hitch, Wyrd)*
$$\operatorname{tie}(\gamma,\, h)\ @\ \chi \quad\mid\quad h \in \mathcal{H} \qquad(\text{hitching both the } \lambda \text{ and } \nu \text{ of the crossing})$$
Imbues Wyrd Aspect $\alpha_h$ into weave $W$.
- **Idempotent** if a wyrd hitch $h$ already sits on any intersection of $W$ (**A10**).
- **Cannot** imbue your own weave (**A11**).

### O3 · Tether  *(Loop, Weft)*
$$\operatorname{tie}(\nu,\, \ell_i)\ @\ \text{warp-strand of a foreign } W' \quad\mid\quad \ell_i \in \mathcal{L},\ \ \nu \ell_i \bowtie \lambda \ell_i$$
Ties a Weft loop *matching your own identity* onto a warp strand of another weave, tethering you to $W'$.
- **Can** tether to many weaves — but at most once per weave.
- **Cannot** tether to your own weave (you are already *of* it) → *inert*. (To reach an own-weave Aspect, use an **anchor** instead — §6.)
- **Cannot** hold two $\nu\ell_i$ in the same weave → *dissipation* (**A7**).

### O4 · Bond Aspect → Tether  *(Hitch, Wyrd)*
$$\operatorname{tie}(\gamma,\, h)\ @\ \text{your tethered weft-loop on } W' \quad\mid\quad h \in \mathcal{H}$$
If some intersection of $W'$ is imbued by the matching wyrd hitch $h$, then $\alpha_h$ **bonds** to that weft-loop, and thereby to you. Eternal (**A12**).
- **Cannot** bond one aspect to more than one weft-loop → *idempotent / inert*.

### O5 · Remote control ("at-a-distance")  *(Hitch, Wyrd, on your own identity)*
$$\operatorname{tie}(\gamma,\, h)\ @\ \text{your own warp-loop } \lambda \ell_i \quad\mid\quad h \in \mathcal{H}$$
If $h$ matches a wyrd hitch on one of your tethered weft-loops, you may wield $\alpha_h$ *from home* — without touching $W'$'s wyrd knot directly. (You now hold $h$ at **both** endpoints: your warp identity and the remote weft tether.)

### O6 · Bond Tether ↔ Tether  *(Cord splice, same weave)*
Splice two of your weft-loops **on the same weave** with a warp cord $\psi$: hitch $\psi$ to each weft-loop, then splice.
- Each weft-loop bonds with **at most one** partner.
- **Cannot** bond weft-loops across different weaves → *inert*.
- **Effect:** agents of the bond may then apply **O5**-style hitches on their warp-loop that match aspects on the *partner's* weft-loop — i.e. **one-hop transitive access** to a neighbour's bonded aspects.

### O7 · Compound Aspect  *(Bend, Wyrd)*
$$\operatorname{tie}(\gamma,\, b)\ \text{joining a loose end of one wyrd hitch to a loose end of another (both on intersections of } W) \quad\mid\quad b \in \mathcal{B}$$
Every splice made with the same bend $b$ records a **connection between two wyrd knots**. Taken together these connections form a network, and the compound aspect is a function of that whole network — not of any single splice. In graph terms:

- $V_b$ — the **vertices**: the wyrd knots that bend $b$ has spliced (the aspects being combined).
- $E_b$ — the **edges**: the splices themselves, each an unordered pair $\{x,y\}$ of the two knots it joins.
- $G_b = (V_b,\, E_b)$ — the **network** bend $b$ has built so far (its vertices and edges together).
- $\varphi$ — the **Wyrd Function**: the map from that network to the Aspect it produces. It is real and consistent — the *same* network always yields the *same* Aspect — but no-one has yet divined how the Wyrd Strands decide what to make. There is *some* sense to it, yet it remains more art than science, even for the powerful Allkin who can wield the Strands of the Universe.

$$\alpha_b = \varphi(G_b),\qquad G_b = (V_b,\, E_b),\qquad E_b \subseteq \{\, \{x,y\} : x,y \in V_b \,\}$$

- **Undirected:** $\{x,y\} = \{y,x\}$ — a splice does not care which end of which hitch came first.
- **Evolve (voluntary):** further splices with the same bend $b$ add edges to $E_b$; $G_b$ grows and so $\alpha_b$ changes.
- **Idempotent:** a repeated splice adds no new edge, $E_b \cup \{p\} = E_b$ (**A10**).
- Each $\gamma$-knot has two ends, and Wyrd knots are duplicable (**A7**), so a hub knot may take arbitrarily many edges by tying extra instances of it.
- **Vertices may themselves be compounds.** A bend end may attach to a base aspect's imbuing hitch *or* to another bend knot — so a pair can join two base aspects, a base and a compound, or two compounds. Compounds therefore stack into an **acyclic** network of networks (a DAG; a cycle can never form, since a bend can only pair aspects that already exist).
- **Devolve (involuntary):** the mirror of Evolve, and never a choice — it happens only when a vertex unravels: a base Aspect unmade by the cascade (**A13**), or a sub-compound that has itself vanished. Because each pair is a bend tied *onto the ends* of the knots it joins, losing a knot unravels every pair touching it; those edges are pruned from $E_b$, and the smaller $G_b$ yields a *different* aspect under the same $\varphi$ — the compound **devolves**. If $E_b$ empties, $\alpha_b$ is **dis-imbued** and vanishes — and since $\alpha_b$ may be a vertex in higher bends, that prunes *their* edges in turn, the cascade climbing the DAG. (How "foundational" a base aspect is to a compound is not a separate property — it is simply how many of the compound's edges touch it: touch every edge and its loss empties the compound; touch one and it merely devolves.)

**Worked example.** From three aspects imbued by wyrd hitches $h_1, h_2, h_3$, three ways of connecting pairs with the same bend $b$ give three *distinct* networks, hence three distinct compound aspects:

| Build | $E_b$ | Network |
|---|---|---|
| 1 | $\{\{h_1,h_2\},\{h_1,h_3\}\}$ | star centered on $h_1$ |
| 2 | $\{\{h_1,h_2\},\{h_2,h_3\}\}$ | star centered on $h_2$ |
| 3 | $\{\{h_1,h_3\},\{h_2,h_3\}\}$ | star centered on $h_3$ |

All three share the same *shape* (a two-edge star) and differ only in *which* hitches are joined — yet they are still three distinct aspects, because the Wyrd Function acts on the specific knots, not the bare shape.

### Reach & Wield  *(derived from O3–O6)*

For an identity $\ell$ tethered to a weave $W$, write $\operatorname{on}(k)$ for the wyrd-hitch ids tied onto a knot $k$, and $\operatorname{Asp}(W)$ for the hitch ids imbued on $W$'s intersections (its Aspects). Then the aspects that identity can touch on $W$ are:

$$
\begin{aligned}
\operatorname{Access}_W(\ell) &= \operatorname{Asp}(W) \cap \Big( \operatorname{on}(\nu\ell) \ \cup\!\!\bigcup_{\nu\ell' \,\leftrightarrow\, \nu\ell}\!\! \operatorname{on}(\nu\ell') \Big) &&\text{reachable through the tether (+ one O6 hop)} \\
\operatorname{Wield}_W(\ell) &= \operatorname{Access}_W(\ell) \cap \operatorname{on}(\lambda\ell) &&\text{of those, controllable at-a-distance (O5)}
\end{aligned}
$$

An aspect is **reachable** once its hitch sits on the agent's tether (**O4**), or on a weft-loop cord-bonded to it (**O6**, one hop). It is **wieldable from home** only when the same hitch *also* sits on the agent's identity loop (**O5**) — the id present at **both** endpoints, $\operatorname{on}(\lambda\ell)\cap\operatorname{on}(\nu\ell)\cap\operatorname{Asp}(W)$. The aspects themselves are $\{\alpha_h : h \in \operatorname{Wield}_W(\ell)\}$.

---

## 4. Power, Heft & Raising

Every operation in §3 acts on a Weave's strands — and a Weave at rest cannot be worked. To tie or alter a knot on a Weave (O2, O3, O4, O6, O7), that Weave must first be **raised** into a workable state and *held* there for the whole duration of the tie. Raising costs; wielding what is already tied does not.

**Power** — $P(a) \ge 0$, an agent's capacity to grip the Warp & Weft. Agents acting in concert pool it:

$$P_{\text{group}} = \sum_{a \in G} P(a)$$

Blood-life have $P \approx 0$ — natively they cannot grip the Strands at all.

**Heft** — $H(\text{op})$, the power an operation demands, sustained for its entire duration. An operation completes only if enough power is held the whole time:

$$\text{completes} \iff P_{\text{available}} \ge H(\text{op}) \ \text{throughout.}$$

Fall below $H$ mid-tie and the Weave **drops** — the operation fails.

**Two regimes.** Heft is dominated by whether the infrastructure already exists:

| Regime | Act | Heft |
|---|---|---|
| **Raising** | lifting a *fresh* Weave into a workable state to imbue (O2), tether (O3), bond (O4/O6), or compound (O7) on it | **large** — scales with the Weave's size and complexity |
| **Wielding** | using an *already-established* channel: at-a-distance control (O5), or pulling a bonded aspect through an anchor | **small** — flows along what already exists; solo |

- **Raising is the prerequisite** for every constructive operation on a Weave. Establishing infrastructure is costly and often cooperative; *using* it afterward is cheap and solo.
- **You cannot raise your own Weave** (**A11**): self-authorship is barred, so no agent can lift the Weave it is *of* into a workable state.
- **Blood-life never raise** ($P \approx 0$): they only ever *wield* channels others established — paying for the grip in blood (see §6, BloodMajik & Anchors).

**What needs raising — from chirality (A3, A7).** Call a **positive target** any Warp strand that *makes up* a Weave, any intersection (it contains such a strand), or anything tied onto them; a **negative target** is a Weft segment. Tying onto a positive target needs a raise; onto a negative one it does not. So only two operations are **raise-free**: **identity (O1)**, a warp loop around a *weft* segment, and **at-a-distance control (O5)**, a hitch onto your own *warp loop*. O5 is the subtle case — a warp loop is $+$chirality yet is a *knot*, not a strand that makes up the Weave, so working it needs no purchase on the Weave. That is exactly how an agent controls its own aspects at a distance without raising the Weave it can never raise (**A11**). Tether (O3), imbue (O2), bond (O4), and compound (O7) all land on positive targets — all require the raise.

> *Out of scope:* what the raised state *is* — the dimensional nature of a lifted Weave — is deliberately left undefined here. This section fixes only its **economics** (who can raise, at what cost, and how it fails), which the rest of the system and the story depend on.

---

## 5. Emergence & Agency

A weave can host an emergent agent only if it already carries the required aspects:

$$\operatorname{Hosts}(W) \iff \{\underbrace{\text{Warp},\ \text{Weft},\ \text{Wyrd}}_{\text{self-aspects}}\} \subseteq W \ \wedge\ \text{Agency/Sentience} \in W \ \wedge\ \text{Power} \in W$$

Only when $\operatorname{Hosts}(W)$ holds may an agent $a \sqsubset W$ emerge and act on the Universal Strands — and it needs the *power* aspect to interact with them at all.

Combined with **A11** (no self-authorship), this forces a chain of causation: **every agent's weave was prepared by prior agents.** No agent is self-made. The first cause is therefore a matter of cosmology, resolved in the core creation story, not in these axioms.

---

## 6. Applied layer (derived, not axiomatic)

These are consequences and inventions built *on top of* §2–§5 — the layer mortals and myth actually touch.

### Access vs. use

Being *connected* (**A8**) is not the same as being able to *use*. Three layers stand between a being and an Aspect's power:

1. **Connected** — knots matched (**A8**).
2. **Access** — the being can *reach* the Aspect: either it is an agent whose identity is tethered and bonded to it (the $\operatorname{Access}_W(\ell)$ set of §3), **or** it has seated an **anchor** on the Aspect's intersection.
3. **Use** — actually *pulling* the Aspect's majik. Access is only a line to the power; using it takes a **pull faculty**.

**Anchors — access for the powerless.** A Weave is a geometric object and every knot sits at a definite point, so an Aspect can be reached bodily, with no identity and no tether. Take an object of sufficient **Wyrd Weight** — enough to bear on the Weave's strands — and mould it into a precise shape that seats onto the intersection $\chi$ whose Aspect $\alpha_h$ you want; that is an **anchor**, and it grants **access** to $\alpha_h$, nothing more. Because it needs no tether, a being may even anchor to its **own** Weave's Aspects — the one Weave it can never tether to (**O3**).

**Use — the pull faculty.** To turn access into power a being must be able to *pull* on the Aspect's wyrd strands. Nothing grants this universally; with infinite Aspects there are infinitely many ways a Weave might. Two that exist:

- **Terrum — blood.** The **Hematic** Aspect gives a Weave *blood-life*; a blood-life pulls an Aspect by spending **blood** — finite, and lethal to overdraw. Its anchors are **Wyrdium**, a metal made by **Urda** (in myth the All-Mother; in fact an Aether agent with the **Material** Aspect bonded into Terrum). A Wyrdium anchor grows irremovable after 1–2 years and is set with a **selecting knot** to choose which reachable power to pull — this pulling is *majik*.
- **Aether — direct.** The Aether carries Aspects that let the Allkin perceive and work the three strands directly, so they need neither anchor nor blood.

> Because Terrum's anchors seat on the intersections the **Allkin** imbued and hold, mortal majik is borrowed access to divine infrastructure — which is why only tiny sects "scratch the surface": they are reverse-engineering a protocol they did not build.

---

## 7. Open laws flagged for the author

Deliberately left out of the axioms, but the system will eventually need them:

1. **Unmaking — mostly resolved.** **A13** and its **unravel-cascade** now define how anything is removed: freeing an embodiment recycles the identity ($\ell_i$ returns to the alphabet) and collapses its whole apparatus — matched tethers, the hitches on them, the bonds those hitches held, the **Aspects** those bonds keystone, and the **compounds** built on them (devolving, or vanishing up the DAG). **A12** is read to match: constructive ties have no *voluntary* inverse but are not indestructible. This is the *only* way to remove an Aspect from a Weave. **Still open — the trigger:** what can unmake a powerful, normally immortal agent in the first place? Mortals carry the Death Aspect; agents do not yet. That is the last piece of the decay law.
2. **Blood cost — resolved.** Blood is finite and lethal to overdraw (§6); a mortal spends it to *pull* an accessed Aspect. The finer curve (proportional? renewable?) is story-tuning, not an open law.

---

## Appendix · Intuition (non-lore)

The system is an access-control / graph model, which is why its edge cases have principled answers:

- **Warp loop** $\lambda\ell_i$ = a globally unique **identity** (a keypair / UUID).
- **Weft loop** $\nu\ell_i$ = the **matching counterpart** placed into a foreign weave (a connection / session), reusable but one-per-weave.
- **Wyrd knot / Aspect** = a reusable **capability** (a permission), freely duplicable.
- **Matching** $\bowtie$ = the handshake; **remote control (O5)** = holding the capability at *both* endpoints.
- **Compound aspects (O7)** = a **labeled graph**; the aspect is a function of the whole edge-set.
