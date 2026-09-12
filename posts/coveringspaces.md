# Covering Spaces and the Universal Covering Space
Kevin Lee
University of Toronto

## &sect;0. Abstract
In this report we collect the definitions related towards covering maps to give rise to the notion of a universal covering space. In Section 1 we recall some definitions and theorems related to covering maps and lifts, in Section 2 we set up and define what the universal covering space is, and in Section 3 and 4 we construct/expose two classic and interesting examples in the study of universal covering spaces. We consulted references [2], [3], [4] for the theorems stated in this report, and will cite these for the proofs later on. We will assume some familiarity and knowledge with point set topology, group theory, some homotopy theory, and what the fundamental group of a topological space is.
	
## &sect;1. Covering Maps and Lifts
We begin by defining what a covering map and respectively what a covering space is for a topological space X.

Definition: Let E and X be topological spaces, and let q: E→X be a continuous map. 
	An open subset U⊆X is said to be evenly covered by q if q-1(U) is a disjoint union of open subsets called sheets in E, each of which are mapped homeomorphically onto U (q is a local homeomorphism from E to X)
	A covering map is a continuous surjective map q:E→X such that every point in X has an evenly covered neighbourhood. We say E is a covering space of X and X as the base space.
	A covering map by definition will be a local homeomorphism, an open map, and a quotient map. If the covering map is injective, it is also a homeomorphism.

For simplicity E is typically required to be connected and locally path connected as this provides a richer environment to study, and for this fact we will assume this as well, as this induces our space X to also be locally path connected and connected as well.

Intuitively the local homeomorphism condition alongside the evenly covered condition requires that our space E to have “miniature copies” of X within the space that correspond to where the pre-images lie. The pre-images of an open set U in X is often described as a “stack of pancakes” that are all the same size and shape of U, and the map q cleanly collapses all these copies down onto U.
Proposition: For every covering map q:E→X, and a point x∈U⊆X, the cardinality of the fibers q-1(x)  is the same for all fibers, and the number of sheets will be the connected components of q-1(U)
Proof: We will define an equivalence relation on X, by x\~x’ if and only if q-1(x) and     q-1(x’) have the same cardinality. For x∈X, let U be an evenly covered neighbourhood of x. Each sheet q-1(U) must contain exactly one point for each fiber of q-1(x), and so for any x’∈U, there is a one-to-one correspondence between the pre-images q-1(x), the sheets of q-1(U), and the pre-images q-1(x’).
This shows x’\~x, and so U must be contained in the equivalence class of [x].
It follows that connected sets have only one equivalence class, and as it is [x], the sheets must be the connected components.
□

In the study of the fundamental group, the equivalence classes of loops were the objects being worked with. It is a natural tool to look at how covering maps treat these loops and paths in general in our range space X then, and in studying covering spaces we see what information we can uncover within X from a setting in E. To study X in this way we need to introduce the notion of a lift that will allow us to translate paths in X in a workable manner.

Definition: If q:E→X is a covering map and Φ:Y→X  is any continuous map, we say a lift of Φ is a continuous map Ψ:Y→E such that q◦Ψ=Φ. Visually this can be represented by this commutative diagram:

IMAGE GOES HERE


The following theorems are the technical tools when working with lifts and paths with respect to covering spaces, which we will state down below. The proofs of these theorems can be found in [2] Chapter 1.3 or [3] Chapter 11.

The main gist of the following theorems is that if we have a sufficiently nice space Y, then when we lift paths from X “upstairs” to E, that we can guarantee certain nice properties being preserved through and within our lifts. In particular we preserve a sense of uniqueness for our lifts when “carrying up” to our space E, and also preserving the homotopies and homotopic properties when “carried up to” our space E.

Theorem: Unique Lifting Property
Let q:E→X be a covering map, and suppose Y is a connected space. 
Let g:Y→X be continuous.
If ĝ1,ĝ2:Y→E are lifts of g, then ĝ1 = ĝ2 (the two lifts are identically equal).

Theorem: Homotopy Lifting Property
Let q:E→X be a covering map, and let Y be a locally connected space.
Suppose g1,g2:Y→X are continuous maps, H:YxI→X is a homotopy from g1 to g2, and ĝ1:Y→E being a lift of g1.
Then there exists a unique homotopy Ĥ:YxI→E of ĝ1 that lifts H.

If we reduce the requirements of the homotopy lifting property strictly to paths, we gain the corollary known as the path lifting property.

Corollary: The Path Lifting Property
Let q:E→X be a covering map. 
Let h:I→X be any path, and let e∈E be any point in the fiber q-1(h(0)).
Then there exists a unique lift ĥ:I→E of h such that ĥ(0)=e.

For notation we will denote this unique lift of the path by ĥe:I→E as it satisfies ĥe(0)=e 

The next theorem establishes fully that if two paths are homotopic, we can consider their lifts to be homotopic as well when “upstairs” in the space E, and it provides some grounding for understanding how the fundamental groups of X and E will relate later on.

Theorem: Let q:E→X be a covering map. 
Suppose g and h are two paths in X with the same starting and end point, and that ĝe and ĥe are their respective lifts that both have the same intial point e∈E.
Then:  i) ĝe\~ĥe if and only if g~h (The lifts are homotopic i.f.f. the paths are homotopic)
	ii) If g~h, then ĝ(1) = ĥ(1) (The lifts have the same endpoint)
Proof:
If ĝe\~ĥe then note that g~h as the composition with q will preserve the path homotopy.
If g~h, we can let H:IxI→X be a path homotopy between them, and the previous homotopy lifting property implies H will lift to a homotopy Ĥ:IxI→E between ĝe and a lift for h starting at e. This lift will have to equal ĥe due to the unique lifting property.
Since g~h implies that ĝe\~ĥe, and also path homotopy, they must also have the same end point.
□

We are now ready to state and prove our first theorem that relates the fundamental groups of E and X when there is a covering map between them.

Theorem: The Injectivity Theorem
Let q:E→X be a covering map. 
For any point e∈E, the induced homomorphism q*: Π1(E,e)→Π1(X,q(e)) is injective.
Proof: Suppose [f] ∈ Π1(E,e) is in the kernel of q*. So this means q*([f]) = [cx], the equivalence class of the constant loop where x = q(e). As q◦f ~ cx, by the previous theome, any lifts of these two that start at the same point must be path-homotopic in E.
f is a lift of q◦f that starts at e, and the constant loop ce is a lift of cx that starts at the same point. Thus f ~ ce, and so [f] is the identity.
□
By the injectivity theorem, the covering space’s fundamental group must be isomorphic to some subgroup of the fundamental group of the base space. We say that this subgroup is induced by the covering, as we will see later on; the choice of base point in E will affect the nature of the subgroup.

## &sect;2. The Universal Covering Space
The nature of the Universal Covering Space by its name is a covering space that covers all other covering spaces, however its existence is not guaranteed for any topological space X. The universal covering space has a sense of “universality” due to its nature of being equivalent to any other space that covers every other covering space, but to do so we have to introduce a notion of when two covering spaces are “equivalent”.

Definition: Let q:E→X and q’:E’→X be covering maps. These maps are said to be equivalent if there exists a homeomorphism h:E→E’ such that q=q’◦h. h is said to be an equivalence of covering spaces or a covering isomorphism, and we say these two coverings are isomorphic if there is a covering isomorphism between them.

With this definition in hand, we need criteria for when a covering isomorphism can exist, and to do so we must generalize the path lifting property, to the General Lifting Lemma.


Theorem: The General Lifting Lemma
Let q:E→X be a covering map, and let q(e0)=x0. Let g:Y→X be a continuous map from a connected and locally path-connected space Y, such that g(y0)=x0.
The map g can be lifted to a unique map ĝ:Y→E such that ĝ(y0)=e0 
if and only if the g*(Π1(Y, y0)) ⊂ q*(Π1(E, e0)) 
In other words image subgroup is contained in the subgroup induced by the covering map.

The proof is lengthy and can be found in [3] Chapter 11 and [4] Section 79.

Definition: A topological space X is simply connected if X is path-connected and the fundamental group is trivial. A topological space is said to be locally simply connected if it admits a basis of simply connected open subsets.

We have two corollaries that immediately follow from the general lifting lemma, with regards to simply connected spaces. As we will see later on, a Universal Covering Space must be simply connected space, and so the following corollaries will apply immediately in these scenarios.

Corollary: Lifting from Simply Connected Spaces
If q:E→X is a covering map, and Y is a simply connected and locally path-connected space, then every continuous map g:Y→X has a lift to E.
Given any point y0∈Y, the lift can be chosen to take y0 to any point in q-1(y0)

Corollary: Lifting to Simply Connected Spaces
Suppose q:E→X is a covering map, and E is simply connected.
For any connected and locally path-connected space Y, a continuous map g:Y→X has a lift to E if and only if ĝ is the trivial homomorphism for some base point y¬0∈Y.
If so, then the lift can be chosen to take y0¬ to any point in q-1(y0).

From here we can introduce a theorem for when two covering spaces are equivalent. The proof of this criterion can be found in [3] Chapter 11 and [4] Section 79, and it relies on the general lifting lemma being applied repeatedly.

Theorem: Covering Isomorphism Criterion
Let q:E→X and q’:E’→X be covering maps, and let q(e0)=q’(e’0)=x0.
There is a unique equivalence h:E→E’ such that h(e0)=e’0 if and only if the following groups H0 = q*(Π1(E,e)) and H’0 = q’*(Π1(E’, e’0)) are equal.
As we have noted before, the induced homomorphisms of the covering maps will produce an image subgroup within the fundamental group of the base space, and as the theorem shows above, these equivalences have to map the base points towards each other. 

It can entirely be the case however, that there is no equivalence that carries e0 to e’0 in the image subgroup, but instead carrying e0 to some other e’1 in the fiber q’¬-1(x0) corresponding to a different subgroup with a different base point entirely. Algebraically, this can be seen structurally as subgroups that are “similar” enough to each other but don’t agree necessarily as sets. 

As we already know that the covering maps induce a subgroup within the fundamental group of the base space, the next two theorems will show how the correspondence between subgroups of the fundamental groups relates to the equivalences between covering spaces. The proofs of both theorems can be found in [4] Section 79, and an alternative proof of the second theorem can be found in [3] Chapter 11.

Theorem: Let q:E→X be a covering map, and let e0,e1 be points in q-1(x0).
Let Hi¬ = q*(Π1(E, ei)).
Then: 	1) If g is any path in E from e0 to e1, and a is the loop q◦g in X, then the equation as subgroups [g]*H1*[g]-1 = H0 holds. (H0 and H1 are conjugate)
2) Given e0 and a subgroup H of Π1(X, x0) conjugate to H0, there exists a point e1 of q-1(b0) such that H1 = H. 

Theorem: Let q:E→X and q’:E’→X be covering maps, and let q(e0)=q’(e’0)=x0. 
The covering maps q and q’ are equivalent if and only if the following subgroups 
H0 = q*(Π1(E,e)) and H’0 = q’*(Π1(E’, e’0)) of Π1(X, x0) are conjugate.

This relationship is sometimes called the Galois correspondence as it relates a group theoretical structure involving the conjugacy classes of subgroups to a corresponding covering map involving E and X.

Defintion: Let q:E→X be a covering map. If E is simply connected, we say E is the universal covering space of X.

As the universal covering space is simply connected, its fundamental group is trivial and so the induced homomorphism maps into the trivial subgroup in the base space’s fundamental group. The following theorem presents elegantly relationship between covering maps, and it will highlight why the universal covering space is called as such.
Theorem: Let p, q, r, be continuous maps such that p = r◦q, for the topological spaces as follows:

IMAGE GOES HERE


Then:	1) If p and r are covering maps, then so is q
	2) If p and q are covering maps, then so is r.
3) If X is simply connected, and p, r are both covering maps, then there is a covering map q such that r◦q = p

The last statement shows us why it is called a universal covering space, as it will cover every other covering space with appropriate choice of functions. From the previous equivalency theorems, we can see that the universal covering space is unique up to isomorphism. 

We will conclude this section by stating some sufficient conditions for when a topological space will admit a universal covering space.

Theorem: The Existence of the Universal Covering Space
Every connected and locally simply connected topological space has a universal covering space.
Proof (Sketch):
To produce a simply connected space E it would help to understand that all paths from our base space X must lift to paths in a space E that are null-homotopic. We can construct our space E as a set of path classes of paths in X starting at x0 and define a “covering map” q:E→X by q([g])=g(1).

Step 1: Topologize the space E. We can define a topology on E by constructing a basis. For each [g] ∈E, and each simply connected open subset U⊆X containing g(1), we construct the basis elements to be the collection of 
[g•U] = {[g•a]| for a being a path in U starting at g(1)}
and we can show that this collection satisfies being a basis.
Step 2: Show E is path-connected. We can construct a path in the space X from x0 to g(t), and using the path lifting lemmas above, we will produce a path from the lifted point of x0 which is a constant path class to any arbitrary path class in E. When doing this, we must show that the lift is also continuous.
Step 3: Show that q is a covering map. This involves proving for any simply connected U⊆X that U is evenly covered and that q acts as a local homeomorphism from [g•U] onto U. This will require the hypotheses imposed on the space X.
Step 4: Showing E is simply connected. From the unique lifting properties and the lifts constructed in step 2, we can apply the homotopy theory stated above to show that any loop must be null-homotopic.
□
The full details of the proof can be found in [3] Chapter 11.

In actuality we do not need to imagine our space E as a space of path classes, and in practice it is easier to imagine it as just a simply connected space with a covering map to X.

The necessary and sufficient conditions for when a space admits a universal cover can actually be weakened from what was required in the previous theorem.

Definition: A subset U⊆X of a topological space is said to be relatively simply connected if the inclusion U→X induces the trivial homomorphism on fundamental groups. X is said to be semilocally simply connected if X admits a basis that of relatively simply connected neighbourhoods.

The above theorem can be adapted as below to show that a space admits a universal covering space if and only if that space is connected, locally path-connected, and semilocally simply connected.

## &sect;3. Covering Spaces of S1∨S1
If we consider the wedge sum of two circles, X=S1∨ S1, we show and compute its fundamental group to find it is isomorphic to the free group on two generators with no relations.




X can be easily visualized as a graph with a vertex in the middle and two edges. We can label each edge with an orientation a and b so that there is an end of each edge corresponding towards or away from the center vertex as above.

As shown in [2] Chapter 1.3, this is a 2-oriented graph that we can identify with X, and we can construct a homeomorphism from the edges of X to our oriented graph that preserves the orientation as well. Topologically we can treat these spaces as “the same”, and working with the oriented graphs, provides a cleaner view of how covering spaces of X relate to it.

In [2] Chapter 1.3, there is a nice visualization provided of other covering spaces of X that are not universal covering spaces, but show a lovely representation of the symmetries possible for covering spaces of X and corresponding subgroups and conjugate subgroups of its fundamental group.

We will outline and restate the construction done in [1] for a simply connected covering space for X, and thus construct its Universal Covering Space for a fixed base point.
This construction will start out branching from the main “plus sign” in R2, and ensure each branch does not overlap with any other, and will produce a simply connected space that can cover X.

We begin by starting with the coordinate axes of R2, and take the open intervals (-1, 1) as segments on each axis. For a fixed number r, such that 0 < r < 1/2, adjoin four open segments of length 2r, at distance r from the ends of the previous segments.
From here, add perpendicular open segments again but of length 2r2 at a distance r2 from the endpoints constructed previously.
Repeat this process indefinitely for each n-th stage adding an open segment of length 2rn-1 at a distance of rn-1 from all previous endpoints.

Taking the union of these segments we produce a graph with infinitely many ends. If we identify each horizontal edge as a when oriented to the right away from the origin, and each vertical edge as b when oriented upward away from the origin, this will produce an oriented graph that we can map its vertices towards X that will preserve this orientation.


IMAGE GOES HERE



This constructed space is simply connected as by its construction it is contractible. This can be visualized by shrinking the space back down to the origin. Any loops corresponding to the edges in X can be traced via the oriented branching paths done in this covering space.

## &sect;4. The Hawaiian Earrings
The Hawaiian Earrings which we will denote by H, is a topological space that can be constructed by taking the union, ⋃_(n∈N)▒C_n , for C_n being a circle of radius 1/n centered at the point (1/n, 0) in R2. The union of these circles equipped with the subspace topology forms the following topological space:



IMAGE GOES HERE



The fundamental group of H is an interesting beast within itself, but H is a classic example of a connected and locally path connected space that does not admit a Universal covering space. 

To prove this fact we need the following lemma that follows from the theorems stated in §2 as can be found in [3].

Lemma: Let q:E→X  be a covering map and let q(e0)=x0.
If E is simply connected, then x0 has a neighbourhood U such that the inclusion map i:U→B induces the trivial homomorphism i*: Π1(U,x0)→Π1(B, x0).

If we consider any open neighbourhood U around the origin x0=(0, 0), we will have to include at least one circle from H, for a sufficiently large enough n value. In fact we will contain an infinite number of circles, but at least one circle suffices
.
For this sufficiently large n, consider a retraction r:H→Cn by mapping each Ci for i≠n to the origin.




By the following diagram of homomorphisms induced by inclusion we can observe that H cannot have a universal covering space as the homomorphism i* cannot be trivial.

As a final interesting counterexample while working with the Hawaiian Earrings, this space is also an example where the composition of covering maps need not be a covering map itself.

As asked in [4] as an exercise, it can be shown that for maps q:X→Y, r:Y→Z, and the map p:X→Z, where p=r◦z, if r-1(z) is finite for each z∈Z, then p is a covering map.

If we consider the following diagram provided by [1], we can observe there is a two-fold covering between the top and middle spaces, but the bottom map will have an infinite number of fibers between the middle space and H. As noted in the discussion, this map will satisfy the unique path lifting property and be a local homeomorphism, but it will fail as a composition to be a covering map.


## &sect;5. Bibliography
[1] Brazas, J. (https://math.stackexchange.com/users/88848/jeremy-brazas), Is composition of covering maps covering map?, URL (version: 2014-10-25): https://math.stackexchange.com/q/990389
[2] Hatcher, A. (2002). Algebraic topology. New York: Cambridge University Press.
[3] Lee, J. M. (2011). Introduction to topological manifolds. New York: Springer.
[4] Munkres, J. R. (2018). Topology. New York, NY: Pearson.
