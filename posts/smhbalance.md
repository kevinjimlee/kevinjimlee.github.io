# The Problem(s) of Balancing SMH
Here is a collection of ramblings around the act of balancing SMH.

## Initial Rambling
SMH was an interesting set to work on and currently it lives in an essentially finalized state.

The set was first initiated with the idea, "How do we make Champion work as a set mechanic?"

For those that don't know, here is the official rules text on Champion in MTG:
<blockquote>
<ul>
<strong>702.72. Champion</strong>
<li>702.72a Champion represents two triggered abilities. “Champion an [object]” means “When this permanent enters, sacrifice it unless you exile another [object] you control” and “When this permanent leaves the battlefield, return the exiled card to the battlefield under its owner’s control.”</li>
<li>702.72b The two abilities represented by champion are linked. See rule 607, “Linked Abilities.”</li>
<li>702.72c A permanent is “championed” by another permanent if the latter exiles the former as the direct result of a champion ability.</li>
</ul>
</blockquote>

Champion thus poses two inherent balance concerns:
1. For a permanent to have Champion exist on the battlefiled, another object (permanent) must be exiled.
- This means there is an inherent "two-for-one" nature that occurs with every Champion card.
2. Champion is a triggered ability that exiles a permanent upon resolution and returns that permanent when the Champion leaves.
- Enter the Battlefield (ETB), Leave the Battlefield (LTB), and when objects enter exile from the battlefield effects can be compounded through Champion permanents.
- This can be an intentional tool to build into the set throughout as a theme (See MaRo's articles about A+B designs).

If we look an examine 1. above further, what does the "two-for-one" nature of Champion implicate (and restrict) on our set design?

For starters, unless we want our Champion mechanic to not live through at common,  we HAVE to restrict the power of instant speed (creature) interaction.
Why?

Consider [Unsummon](https://scryfall.com/card/m20/78/unsummon) and any of the common Champion creatures, say [Common Blue Champion](https://github.com/kevinjimlee/mse/blob/main/SMH/CU02%20%E2%80%94%20Common%20Blue%20Champion.png).

![Common Blue Champion](https://raw.githubusercontent.com/kevinjimlee/mse/main/SMH/CU02%20%E2%80%94%20Common%20Blue%20Champion.png)

Suppose you have one creature on the battlefield and you cast Common Blue Champion.

## The Cycle of Five 4-Colour Legends