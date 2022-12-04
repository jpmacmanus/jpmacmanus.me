---
layout: post
title: "A Brief History of Three-Dimensional Manifolds"
author: Joseph
tags: maths metric-geometry topology 
---

We give a broad-brush account of some milestones in the theory of 3-dimensional manifolds, particularly the Poincaré Conjecture and its
proof. We also discuss Thurston’s Geometrisation Programme.

This post is adapted from a short project I completed last year. Do get in touch with any corrections. 


## 1. The Beginning - from Poincaré to Dehn

The theory of three-dimensional manifolds has been a topic of great interest for well over a century, and we begin our account with the work of Henri Poincaré. 

In [25], Poincaré introduces the notion of the *fundamental group* of a space. He believed that such a tool could lead to a more sophisticated classification of topological spaces than had existed before. In a later work [26], Poincaré raises the following question, which inspired generations of mathematicians. 

> *Est-il possible qu le groupe fondamental de $$V$$ se réduise à la substitution identique, et que pourtant $$V$$ ne soit pas simplement  connexe?*

With modern terminology, this translates to the question "Is it possible for the fundamental group of [the 3-manifold] $$V$$ to be trivial, but that $$V$$ is not homeomorphic to the 3-sphere?" This question came to be known as the *Poincaré conjecture*. As a small aside, it is worth pointing out that the above literally translates to "Is it possible that the fundamental group of $$V$$ consists of only the identity, and that yet $$V$$ is not simply connected?" This is obviously false under modern definitions. Indeed the definition of *simply connected* has changed over time, and this is an interesting example of how terminology can evolve.

The work of Poincaré was of incredible importance, due to the new ideas it put forward. However, Chandler and Magnus [5] remark that much of Poincaré's work is difficult to read and sometimes imprecise, as much of the work fails to "separate intuition from proof".
Many of these ideas were reformulated in a rigorous fashion by Tietze, in his landmark work [36]. This article is based on the work of Poincaré, and re-introduces the concept of a manifold (defined as a cell complex), as well as the fundamental group of such a space.
Tietze goes on to prove many foundational results which set the stage for algebraic topology, such as the fact that homeomorphic manifolds have isomorphic fundamental groups. Considering 3-manifolds in particular, Tietze summarises his findings with the following quote:

>[...] *the fundamental group of an orientable closed three-dimensional manifold contributes more to its characterisation than all the presently known topological invariants taken together.*

The above only consolidates the importance of the Poincaré conjecture. 

Indeed, Poincaré's work inspired that of many more mathematicians, including that of Max Dehn. In [7], Dehn builds upon the work of Tietze and Poincaré to make further progress in studying and classifying 3-manifolds based on their fundamental groups. This work then inspired much of Dehn's contributions to group theory, leading to a later paper [8] formulating his three famous fundamental problems: the *word*, *conjugacy*, and *isomorphism* problems. 

There is much more that could be said about this period, but it is beyond the scope of this report. We thus point the interested reader to [5] for a detailed account of this period and the subsequent emergence of combinatorial (later, geometric) group theory. 


## 2. The Mid-20th Century - from Kneser to Johannson

We now jump ahead in time, and consider a selection of important results from the middle of the twentieth century. 
We begin with a classical decomposition theorem, for the statement of which we will need the following definition. 


**Definition 2.1.** We say that a 3-manifold $$M$$ is *prime* if $$M$$ cannot be expressed as a connected sum $$M \cong M_1 \# M_2$$, where neither $$M_i$$ is $$S^3$$. 

<!--break-->

We can then state the following result.

**Theorem 2.2.** (Kneser-Milnor)
*Let $$M$$ be a closed orientable three-dimensional manifold. Then there is a unique finite collection of prime 3-manifolds $$M_1, \ldots , M_k$$ such that*

$$
M \cong M_1 \# \cdots \# M_k. 
$$

We call such a decomposition a *prime decomposition*.
The existence of such a decomposition is due to Kneser in [15]. However, the exact formulation of this result, as well as uniqueness, was given later by Milnor in [16]. One can view this result as a topological analogue to Grushko's Theorem, which gives a similar unique decomposition of a finitely-generated group into a finite free product. 

The next problem we discuss relates to the notion of *triangulisability*. Recall that we say a manifold $$M$$ is triangulisable if it is homeomorphic to the geometric realization of some simplicial complex. The question of whether any manifold $$M$$ is triangulisable is one which was in the heads of many of the people we have seen already. In [26], Poincaré asked whether every smooth manifold was triangulisable. This was answered by Cairn [4], and later independently by Whitehead [37]. 

**Theorem 2.3.** (Cairn-Whitehead)
*Every smooth manifold admits a triangulation.*

Years after Poincaré asked about the existence of triangulations of smooth manifolds, in 1923 Kneser asked the same question of topological manifolds. It is a theorem of Radó [28] that every topological surface admits a triangulation. Amazingly, this result generalises to 3-manifolds too, a result which is due to Moise [17]. As a small aside, Moise was the PhD supervisor of Munkres, author of the classic introductory topology text [18].

**Theorem 2.4.** (Moise)
*Every topological 3-manifold admits a unique smooth structure, and thus a triangulation.*

The wonderful consequence of this is that the classification of smooth 3-manifolds and topological 3-manifolds coincide completely. Thus, if one wishes to prove a fact about topological 3-manifolds (such as the Poincaré conjecture), one could make some progress on this by classifying smooth 3-manifolds. Indeed this is exactly what happened, as we will see later on. From this point onward, we will not bother to make the distinction between smooth and topological 3-manifolds.

We conclude this section by discussing another important decomposition result. First, we need the following definitions, the first of which is a notion very similar to that of a prime manifold, but more specific to 3-manifolds. 

**Definition 2.5.** (Irreducible 3-manifold)
We say that a 3-manifold $$M$$ is *irreducible* if every smooth embedding of $$S^2$$ in $$M$$ bounds a ball.

To see how this notion is related to that of being prime, note that it can be shown that a 3-manifold is prime if and only if it is irreducible, or is a fiber of $$S^2$$ over $$S^1$$. 

We are going to introduce a decomposition of a manifold $$M$$ into a collection of pieces of two types. We must however first describe what these pieces will look like. The first kind is an *atoroidal* manifold.

**Definition 2.6.** (Atoroidal)
Let $$M$$ be a 3-manifold. We say that an embedded torus $$T^2 \subseteq M$$ is *essential* if it is incompressible and not isotopic to a component of $$\partial M$$. If $$M$$ does not contain an essential torus, we say that $$M$$ is *atoroidal*.

In plain English, a 3-manifold $$M$$ is atoroidal if every embedded torus is freely homotopic to either a point, or a component of $$\partial M$$. That is, it doesn't contain any "interesting" tori. 
The second kind of manifold we will need to introduce is more complicated, and we will only do so briefly. We have the following definition, due to Seifert. 

**Definition 2.7** (Seifert-fibered spaces)
Define the *standard fibered torus* corresponding to a pair of coprime integers $$(a,b)$$ with $$a > 1$$ as the surface bundle of the automorphism of a disk given by rotation by an angle of $$2\pi b/a$$.

We say that a closed 3-manifold $$M$$ is *Seifert fibered* if it can be decomposed into a disjoint union of circles, called *fibers*, where each fiber has a tubular neighbourhood forming a standard fibered torus. 

There is a lot of to understand in this definition, and we will try to give some intuition here.
We have our manifold $$M$$, decomposed as a disjoint union of circles.
Then, by a *tubular neighbourhood* of a fiber, we essentially mean a closed ball around our fiber, forming a solid torus. We might call this fiber the "middle" fiber of the torus.
When we say that this torus is *standard fibered*, we mean that this torus is itself a disjoint union of circles, each circle running around the hole of torus, alongside the middle fiber. 
Moreover, we require is that through some uniform, rational "twisting" of the torus, we can unwind our fibers so that every fiber runs perfectly parallel to the middle fiber. 

Seifert-fibered manifolds are incredibly important in three-dimensional topology, with many common examples of 3-manifolds falling into this class. Seifert himself completely classified these manifolds in [31], up to fiber-preserving homeomorphism. It was later shown in [20] that this very same classification is purely topological, and classifies these spaces completely up to homeomorphism. One can find a complete introduction to Seifert-fibered spaces, including a proof of their classification, in [3].

With these two definitions in mind, we then have the following decomposition of an irreducible manifold, known sometimes as a *torus decomposition*. This result is due to Jaco, Shalen, and Johannson, and thus we also refer to such a decomposition as a *JSJ decomposition* of a manifold. The first two of these worked together [12], while the latter discovered this result independently [13]. 

**Theorem 2.8.** (Jaco-Shalen, Johannson)
*Let $$M$$ be an irreducible three-dimensional manifold. Then there exists a minimal set of disjoint embedded tori in $$M$$, unique up to isotopy, such that each of the components of $$M$$ obtained by cutting along these tori is either atoroidal or Seifert fibered.*

Combining this with Theorem 2.2 above, one deduces a very powerful decomposition. One can find a complete proof of this result, as well as a proof of the Prime decomposition, an introduction to Seifert manifolds, and more, in these notes [11] by Hatcher. 


This topological idea has been carried over to group theory, giving rise to the idea of a *JSJ decomposition of a group*. The idea is we split a group into a graph of groups, where every vertex is either "surface-like" or indecomposable. This decomposition also has the property that it "contains" every splitting of our group, in some sense. Further discussion of this topic is definitely beyond the scope of this report, and so we direct the interested reader to [9] for a complete introduction. 


## 3. Geometrisation - Thurston's Conjecture

In this section, we will build upon the decomposition theorems of the previous section by discussing what is known as the *Geometrisation conjecture*, which can be seen as another, more powerful decomposition, leading to a complete classification of 3-manifolds.
We begin by introducing the relevant geometric notions.


The main geometric notion which we will need is that of a *model geometry*. Informally, a manifold $$M$$ can be said to have a geometric structure modelled on some simply connected manifold $$X$$, if $$M$$ can be viewed as a "nice" quotient of $$X$$. We formalise this with the following. 

**Definition 3.1.** (Model geometry)
A *model geometry* is a pair $$(X,G)$$, where $$X$$ is a simply connected smooth manifold, and $$G$$ is a Lie group acting smoothly and transitively on $$X$$ with compact stabilisers.

We say that a model geometry $$(X,G)$$ is *maximal* if $$G$$ is maximal among those Lie groups acting smoothly and transitively on $$X$$. 

**Definition 3.2.** (Geometric structure)
Let $$M$$ be a smooth manifold. Then a *geometric structure* on $$M$$ is maximal model geometry $$(X, G)$$, together with a diffeomorphism $$M \to X / \Gamma$$, where $$\Gamma$$ is a discrete subgroup of $$G$$ acting freely on $$X$$. 

We may omit mention of $$G$$ for simplicity, and say that $$M$$ *admits a geometric structure modelled on $$X$$*. 
We call a geometric structure $$X$$ a *Thurston geometry* if there is at least one closed three-dimensional manifold $$M$$ which admits a geometry modelled on $$X$$. Thurston showed that there are precisely eight such geometries. Thurston's proof of this classification can be found in [35], together with explanations of these geometries. 

**Theorem 3.3.** (Thurston)
*There are precisely eight Thurston geometries, listed below.*
1. *Spherical geometry modelled on $$S^3$$,*
2. *Euclidean geometry modelled on $$\mathbb E^3$$,*
3. *Hyperbolic geometry modelled on $$\mathbb H^3$$,*
4. *Geometry modelled on $$S^2 \times \mathbb{R}$$,*
5. *Geometry modelled on $$\mathbb H^2 \times \mathbb{R}$$,*
6. *Geometry modelled on the universal cover of $$\mathrm{SL} _2(\mathbb{R})$$,*
7. *Geometry modelled on the Lie group $$\mathrm{Nil}$$,*
8. *Geometry modelled on the Lie group $$\mathrm{Sol}$$.* 

The first three of these geometries are the *constant curvature geometries*, and the latter five are often referred to as the *fibered geometries*. 
We direct the reader to [30] for a complete survey of these geometries, including definitions of the Lie groups $$\mathrm{Nil}$$ and $$\mathrm{Sol}$$. 

We have the following geometrisation theorem for compact surfaces. This was first conjectured by Klein and Poincaré at the end of the 19th century, with one of the first proofs appearing in 1908, due to Poincaré [27]. This classical result is usually known as the *Uniformisation Theorem*. 

**Theorem 3.4.** (Uniformisation)\label{thm:uniform}
*Every closed surface $$M$$ admits a geometric structure modelled on either $$S^2$$, $$\mathbb E^2$$, or $$\mathbb H^2$$.*

Thurston believed that this could be somehow generalised to three dimensions. The first step made towards this idea was a result known as the *Hyperbolisation Theorem for Haken Manifolds*. This result gives necessary and sufficient conditions for a manifold known as a Haken manifold to admit a hyperbolic geometry. Haken manifolds can be defined as follows. This definition is taken from [21].

**Definition 3.5.** (Haken manifolds)
We say that an irreducible 3-manifold $$M$$ is a *Haken* manifold if $$M$$ contains a properly embedded incompressible surface, i.e. an embedded surface $$S \subseteq M$$ such that
1. The fundamental group $$\pi_1(S)$$ embeds into $$\pi_1(M)$$, and the relative fundamental group $$\pi_1(S, \partial S)$$ embeds into $$\pi_1(M, \partial M)$$,
2. $$S$$ is not isotopic to a component of $$\partial M$$. 

We then state the Hyperbolisation Theorem as follows.

**Theorem 3.6.** (Hyperbolisation)
Let $$M$$ be a Haken manifold. Then $$M$$ is hyperbolic if and only if $$M$$ is atoroidal.

Thurston never published a complete proof of his Hyperbolisation Theorem, and gives his reasons for this in [34]. However, a complete argument can be found in [21]. 

In 1982, Thurston was awarded the Fields Medal for his proof of the Hyperbolisation Theorem.
At around the same time as the announcement of this result, Thurston also announced his *Geometrisation Conjecture*, stated below.  

**Conjecture 3.7.** (Geometrisation)
Every prime three-dimensional manifold can be cut along tori, so that the interiors of the resulting components have a geometric structure with finite volume. 

Thurston gives more details of this conjecture in [33], along with justification for his conviction as to why it should be true. 
Note that this decomposition may not be the same as that given by the JSJ decomposition discussed above. Indeed, a JSJ decomposition may admit pieces with no finite volume geometric structure. 
The *Elliptisation Conjecture* is another big part of this programme. This (sub)conjecture states the following.

**Conjecture 3.8.** (Elliptisation)
If a closed 3-manifold $$M$$ has finite fundamental group, then $$M$$ admits a geometric structure modelled on $$S^3$$.

We can obtain a proof to the Poincaré conjecture as an almost immediate corollary to the above. 
Indeed suppose $$M$$ is a closed, simply connected manifold. By elliptisation, we have that $$M$$ admits spherical geometry. It is then a standard fact from metric geometry that the universal cover of $$M$$ is the sphere $$S^3$$. Since $$M$$ is simply connected, it is homeomorphic to every cover, and we are done. Indeed it was Perelman's work on the Elliptisation Conjecture which proved the Poincaré Conjecture, and we will discuss this in the next section.  



## 4. Ricci Flow and the Perelman's Proof

We give a brief introduction to Ricci flow, and describe how Hamilton and Perelman used it to complete the proof of the Poincaré conjecture. 

In short, Ricci flow is a method of continuously deforming a Riemannian metric, in a way that mimics the heat equation. In order to make this more precise, we need to briefly introduce *Ricci curvature*, which is in some sense a directional version of the usual notion of scalar curvature. We will introduce it in the context of Riemannian surfaces,
for the sake of exposition, as in higher dimensions things get quite a bit more complicated. This is a bit cheeky, as in two dimensions we actually have that Ricci curvature and scalar curvature differ by a constant factor of 2. Nevertheless, we will press on. This brief description is due to Tao [32].

Recall that a Riemannian metric $$g$$ on a surface $$M$$ allows us to discuss not just distance, but the ideas of *angle* and *area* too. Let $$\angle(x,r \theta, v)$$ denote the angular sector based at $$x$$, with angle $$\theta$$ and radius $$r$$, centered on the tangent vector $$v$$. Let $$|\angle(x,r, \theta, v)|$$ denote the area of this segment. Recall that such a segment in Euclidean space will have area $$\frac 1 2 \theta r^2$$, but such a segment in $$M$$ may have a slightly different area. 
Ricci curvature measures precisely this difference, and is thus defined as 

$$
\mathrm{Ric}_g(x)(v,v) := \lim_{r \to 0} \lim_{\theta \to 0} \frac{\tfrac{1}{2} \theta r^2 - |\angle(x,r ,\theta, v)|}{\theta r^2 / 24} .
$$

As mentioned above, things get much more complicated in higher dimensions. In general, given a choice of Riemannian metric $$g$$, this idea of Ricci curvature leads to a tensor $$\mathrm{Ric}_g$$, but we will not discuss the details of this here. 


Ricci flow was introduced by Richard S. Hamilton in 1982 [10]. Informally, we wish to "contract" areas of our metric space which feature positive curvature, and "expand" areas with negative curvature. Slightly more formally, if we let $$\{g(t)\}$$ be a smooth one-parameter family of Riemannian metrics on our manifold, then the process of Ricci flow can be roughly defined by the differential equation

$$
\frac{d}{dt}g(t) = -2\mathrm{Ric}_{g(t)}.
$$

There is of course some hand-waving in the above definition, and the interested reader can find the  precise formalism of this definition, as well as the formalism surrounding Ricci curvature, in [6].


Hamilton noticed that Ricci flow is a powerful tool for simplifying the structure of manifolds. For example, when Ricci flow is run on a Riemannian surface, this metric will be deformed into one of constant curvature, giving another proof of the celebrated Uniformisation Theorem (cf. 3.4). Hamilton also showed that a similar thing happens when Ricci flow is applied to positively curved 3-manifolds, leading to the following result. 

**Theorem 4.1.** (Hamilton)
*Let $$M$$ be a compact three-dimensional manifold which admits a Riemannian metric of strictly positive curvature. Then $$M$$ admits a Riemannian metric of constant positive curvature.* 

Note that this proves the Elliptisation Conjecture (and thus the Poincaré Conjecture) for positively-curved 3-manifolds. 
Hamilton also believed that this method could be used to settle the wider Geometrisation Conjecture in general, but in trying to run Ricci flow on arbitrary 3-manifolds, we are met with problems. 
The main difficulty that Ricci flow presents is the appearance of "singularities". We'd like it if we were able to run this procedure forever, until our manifold becomes something very recognisable. However, this sadly is not the case. A *singularity* is a point where our manifold $$M$$ stops looking locally like $$\mathbb{R}^3$$. A simple example of this phenomenon is if we run Ricci flow on a standard unit 3-sphere, the sphere will eventually contract to a point. Another example is a cylinder, eventually collapsing to its axis.
Hamilton failed to fully understand these singularities, but the mystery of these singularities was later clarified by Perelman. 


In the first of three prepints posted on the arXiv [22], Perelman published several celebrated results,  including one known as the *Canonical Neighbourhood Theorem*. This theorem provided a quantitative understanding of the singularities caused by Ricci flow, and essentially says that the only possible singularities that may occur are the two we mentioned above: spheres collapsing to a point, or cylinders collapsing to their axes. 

This then paved the way for the work of the second preprint [24], where Perelman applies his Canonical Neighbourhood Theorem, and introduces a modified version of Ricci flow, called Ricci flow *with surgery*. In this variant, when singularities develop we "excise" them, and replace the holes left in our manifold with a small disc, so our space once again looks locally Euclidean. Note that after this surgery, the topology of our manifold may have changed. In particular, a once connected manifold may become disconnected after this procedure.

In the third and final preprint [23], Perelman takes a manifold satisfying the hypothesis of the Poincaré conjecture, and runs his modified Ricci flow with surgery. He shows that after a finite number of "cuts", one reaches a disjoint union of spheres. He then pastes these spheres together again with three-dimensional cylinders, restoring the original topology. In doing so, we see that the original manifold was in fact a sphere, and thus the Poincaré conjecture is proven. 

In these preprints, much progress is made on proving the full Geometrisation conjecture, although this is not quite fully settled in this work due to a gap. The main missing piece is ensuring that Ricci flow with surgery will always terminate after a finite number of cuts. Perelman's proof of this fact relied on a result, Theorem 7.4, which in this preprint is stated without proof. Eventually many proofs of this missing Theorem appeared in the literature. The full details of Perelman's argument, plus a proof of Theorem 7.4, can be found in [14]. 


In August 2006, Perelman was awarded the Fields medal, but turned it down.
Upon turning down the Fields Medal, Perelman is quoted [1] to have said:

> *I'm not interested in money or fame, I don't want to be on display like an animal in a zoo. I'm not a hero of mathematics. I'm not even that successful; that is why I don't want to have everybody looking at me.*

Despite this refusal, in March 2010 the decision was made to award Perelman with the Millennium Prize, worth $1,000,000 USD. Perelman declined this prize also, and did not appear at a conference in July 2010, held in Paris in his honour. The main reason Perelman cites for his refusal is that the prize could not be shared with Hamilton, who he believed had contributed at least as much as himself. Perelman is quoted [29] as saying:

> *To put it short, the main reason is my disagreement with the organized mathematical community, I don't like their decisions, I consider them unjust.*

At this conference, many great names in Topology and Geometry expressed their admiration of Perelman, with speakers including Gromov, Thurston, and more. Their laudations can be read [here](https://www.claymath.org/perelman-laudations).






## References

1. Russian maths genius Perelman urged to take $1m prize. *BBC News*, March 2010.

2. L. Bessières, G. Besson, M. Boileau, S. Maillot, and J. Porti. *Geometrisation of 3-manifolds*, volume 13. European Mathematical Society, 2010.

3. M. G. Brin. Seifert fibered spaces: Notes for a course given in the Spring of 1993. *arXiv preprint arXiv:0711.1346*, 2007.

4. S. S. Cairns. Triangulation of the manifold of class one. *Bulletin of the American Mathematical Society*, 41(8):549–552, 1935.

5. B. Chandler and W. Magnus. The history of combinatorial group theory. *Sources in the History of Mathematics and Physical Sciences*, 9, 1982.

6. B. Chow and D. Knopf. The Ricci flow: an introduction. *Mathematical surveys and monographs*, 110, 2008.

7. M. Dehn. Über die Topologie des dreidimensionalen Raumes. *Mathematische Annalen*, 69(1):137–168, 1910.

8. M. Dehn. Über unendliche diskontinuierliche Gruppen. *Mathematische Annalen*, 71(1):116–144, 1911.

9. V. Guirardel and G. Levitt. JSJ decompositions of groups. *arXiv preprint arXiv:1602.05139*, 2016.

10. R. S. Hamilton. Three-manifolds with positive Ricci curvature. *Journal of Differential geometry*, 17(2):255–306, 1982.

11. A. Hatcher. Notes on basic 3-manifold topology, 2007.

12. W. Jaco and P. B. Shalen. Seifert fibered spaces in 3-manifolds. In *Geometric topology*, pages 91–99. Elsevier, 1979.

13. K. Johannson. *Homotopy equivalences of 3-manifolds with boundaries*, volume 761. Springer, 2006.

14. B. Kleiner, J. Lott, et al. Notes on Perelman’s papers. *Geometry & Topology*, 12(5):2587–2855, 2008.

15. H. Kneser. Geschlossene Flächen in dreidimensionalen Mannigfaltigkeiten. *Jahresbericht der Deutschen Mathematiker-Vereinigung*, 38:248–259, 1929.

16. J. Milnor. A unique decomposition theorem for 3-manifolds. *American Journal of Mathematics*, 84(1):1–7, 1962.

17. E. E. Moise. Affine structures in 3-manifolds: V. the triangulation theorem and Hauptvermutung. *Annals of mathematics*, pages 96–114, 1952.

18. J. R. Munkres. Topology, 2000.

19. W. D. Neumann and G. A. Swarup. Canonical decompositions of 3–manifolds.*Geometry & Topology*, 1(1):21–40, 1997.

20. P. Orlik, E. Vogt, and H. Zieschang. Zur Topologie gefaserter dreidimensionaler Mannigfaltigkeiten. *Topology*, 6(1):49–64, 1967.

21. J.-P. Otal. Thurston’s hyperbolization of Haken manifolds. *Surveys in differential geometry*, 3(1):77–194, 1996.

22. G. Perelman. The entropy formula for the Ricci flow and its geometric applications. *arXiv preprint math/0211159*, 2002.

23. G. Perelman. Finite extinction time for the solutions to the Ricci flow on certain three-manifolds. *arXiv preprint math/0307245*, 2003.

24. G. Perelman. Ricci flow with surgery on three-manifolds. *arXiv preprint math/0303109*, 2003.

25. H. Poincaré. *Analysis situs*. Gauthier-Villars Paris, France, 1895.

26. H. Poincaré. Cinquième complément à l’analysis situs. *Rendiconti del Circolo Matematico di Palermo (1884-1940)*, 18(1):45–110, 1904.

27.  H. Poincaré. Sur l’uniformisation des fonctions analytiques. *Acta mathematica*, 31:1–63, 1908.

28. T. Radó. Über den begriff der riemannschen fläche. *Acta Litt. Sci. Szeged*, 2(101-121):10, 1925.

29. M. Ritter. Russian mathematician rejects $1 million prize. *The Boston Globe*, 1, 2010.

30. P. Scott. The geometries of 3-manifolds. *Bulletin of the London Mathematical Society*, 15(5):401–487, 1983.

31. H. Seifert. Topologie dreidimensionaler gefaserter R ̈aume. *Acta Mathematica*, 60(1):147–238, 1933.

32. T. Tao. Notes on Ricci flow, March 2008. PDF available [here](https://terrytao.files.wordpress.com/2008/03/ricci.pdf).

33. W. P. Thurston. Three dimensional manifolds, Kleinian groups and hyperbolic geometry. *Bulletin (New Series) of the American Mathematical Society*, 6(3):357–381, 1982.

34. W. P. Thurston. On proof and progress in mathematics. *New directions in the philosophy of mathematics*, pages 337–355, 1998.

35. W. P. Thurston et al. *Three-dimensional geometry and topology*, volume 1. Princeton university press, 1997.

36. H. Tietze. Über die topologischen Invarianten mehrdimensionaler Mannigfaltigkeiten. *Monatshefte für Mathematik und Physik*, 19(1):1–118, 1908.

37. J. H. C. Whitehead. On C1-complexes. *Annals of Mathematics*, pages 809–824, 1940.