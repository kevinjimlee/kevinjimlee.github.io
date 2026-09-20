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
<ol>
    <li>For a permanent to have Champion exist on the battlefiled, another object (permanent) must be exiled.</li>
    <ul>
        <li>This means there is an inherent "two-for-one" nature that occurs with every Champion card.</li>
    </ul>
    <li>Champion is a triggered ability that exiles a permanent upon resolution and returns that permanent when the Champion leaves.</li>
    <ul>
        <li>Enter the Battlefield (ETB), Leave the Battlefield (LTB), and when objects enter exile from the battlefield effects can be compounded through Champion permanents.</li>
        <li>This can be an intentional tool to build into the set throughout as a theme (See MaRo's articles about A+B designs). </li>
    </ul>
</ol>
If we look an examine 1. above further, what does the "two-for-one" nature of Champion implicate (and restrict) on our set design?

For starters, unless we want our Champion mechanic to not live through at common,  we HAVE to restrict the power of instant speed (creature) interaction.
Why?

Consider [Unsummon](https://scryfall.com/card/m20/78/unsummon) and any of the common Champion creatures, say [Common Blue Champion](https://github.com/kevinjimlee/mse/blob/main/SMH/CU02%20%E2%80%94%20Common%20Blue%20Champion.png).

![Common Blue Champion](https://raw.githubusercontent.com/kevinjimlee/mse/main/SMH/CU02%20%E2%80%94%20Common%20Blue%20Champion.png)

Suppose you have one creature on the battlefield and you cast Common Blue Champion. Your opponent has two opportunities in interacting with your Champion: either before the Champion hits the battlefield (and its ETB triggers) or after the Champion triggers are on the stack. In either case if your opponent Unsummons the creature you currently have on board your Champion must be sacrificed due to 702.72a as you have nothing to exile underneath Common Blue Champion.

So what is our workaround here? Unsummon as interaction gives back the creature to the opponent (except tokens), but in this case it acts as a one mana murder that severely affects your tempo.

This means ALL interaction (at least at common) must be built with Champion in mind, otherwise Champion will lead to feel-bad moments where the player casting it will be two-for-one'd, and Champions will act no better than a glorified Aura (more on this later).

The initial playtests for SMH had two main philosophies for interaction:
<ol>
    <li>To prvent two-for-ones interaction has to be at sorcery speed.</li>
    <li>If a piece of interaction must be at instant speed, the caster has to invest a signficiant amount of mana (4+ mana)</li>
</ol>

In the end the first restriction turned out to be too swingy. The common Champion cycle is strong; their stats were designed such that any one common Champion can trade with another Champion and they act as mana efficient french vanilla creatures usually slightly ahead of the curve. With a sorcery speed restriction the philopshy was to allow the Champion caster to always get value out of their creature. Compare to how Bestow or Mutate are worded to ensure the caster always gains something, we *cannot* do that here with how Champion is keyworded. 

This unfortunately created a play pattern where one player establishes a threatening board and the defending player must claw back to regain some form of stability, but they have to invest that mana *on their own turn*. Magic is a game of interaction, of trading resources efficiently and effectively, and of playing your pieces in such a way to gain advantages with those resources. Even if the sorceries were efficient or powerful removal pieces, when you are constantly on the backfoot using your own mana on your turn to deal with your opponents' threats (Champions) you are NOT advancing your own boardstate and consuming your own cards and mana to do so.

The second restriction worked well in principle, it significantly reduced any moment of feeling bad when casting a Champion and losing it for a two-for-one, as the large 4+ mana (typically 5 mana for the commons except for one blue instant) would telegraph the interaction and it communicated the risk the player was casting into.

We ended up adjusting the first restriction (and made a bunch of spells wordier) by allowing these spells to be cast with flash but only during the combat phase. This allowed interaction and mana to be spent on your opponents turn (which turns out to be a fundamental piece to how Magic works as a game), and guarantees the Champion caster always gained value from their creature. These changes occured to the cheap interaction pieces.

![Flames of the Beyond](https://raw.githubusercontent.com/kevinjimlee/mse/main/SMH/CR13%20%E2%80%94%20Flames%20of%20the%20Beyond.png)

Another knob we adjusted was to incentivize the higher mana value interaction to be *desirable*. Common removal should be strong enough to deal with the threats that appear at rare and across the board at common. This design trend has been propogating across premier MTG sets as removal is key to limited: Bombs need ways to be dealt with. By twisting the timing incentive, we adjust the pieces to question *when* should you play pieces? 
![Soul Reaving](https://raw.githubusercontent.com/kevinjimlee/mse/main/SMH/CB12%20%E2%80%94%20Soul%20Reaving.png)

With the looping interaction that Champion leads with its exile clause, we leaned to use LTB effects as the central focus for the set. Many sets and designers use ETBs as you want to accrue the value immediately when you play any card, but for the design of SMH we wanted to really play in that *when* question. *When* are you getting that value of your card?

At the face of it the value of an LTB effect versus ETB effect is only a matter of how soon that effect resolves.


## Champions are Glorified Auras
So what else can we do with Champion?

## The Cycle of Five 4-Colour Legends