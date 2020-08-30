---
layout: post
title: Why do we add salt to pasta water?
author: Gavin
slug: salted-water
---

I was talking to some friends about cooking and the topic of adding salt to the water you cook pasta in came up. 
Someone asked what purpose of the salt is in the cooking process. 
At first, the answer the foodie on the group came up with was "it makes the pasta cook better", but this wasn't satisfying, so we started brainstorming to come up with some ideas. 
In the end, there were two theories that had the most support:

1.  It prevents the pasta from sticking.
2.  It raises the temperature of the water, cooking the pasta faster.

I don't know enough to pass judgement on the first theory. 
I know that the second is technically true through boiling point elevation, but how much does it really increase the boiling point of the water? 
Let's do the math.
<!--more-->

We can determine the change in boiling point, using the expression:

\$\$ \Delta T_b = K_b b_{solute} i \$\$

* \$ K_b \$ is the ebullioscopic constant, which relates the molality of a solution to boiling point elevation. 
  It is specific for each each solvent and it calculated as \$ \frac{R T_b^2}{1000 L_v} \$, using the ideal gas constant (\$ R \$), boiling temperature of the pure solvent (\$ T_b \$), and latent heat of vapourization (\$ L_v \$). 
  For water this is \$ 0.512 \frac{^\circ C kg}{mol} \$
* \$ b_{solute} \$ is the [molality](https://en.wikipedia.org/wiki/Molality) of the solution.
* \$ i \$ is the van't Hoff factor, a measure of how many particles the solute dissociates into. 
  For sodium chloride (table salt) this is 2.

At this point we need to determine the concentration of the salt water, and with some simple multiplication we will know the boiling point elevation. 
Let us make some assumptions to start with. 
I'll assume we are making a single serving of pasta, so are using only a litre of water, and we have added a teaspoon of salt to the water.

How much is one teaspoon of salt?

\$\$ 1 tsp \* \\frac{5 mL}{1 tsp} \* \\frac{2.16 g NaCl}{1 mL} = 10.8 g NaCl \$\$

So, we are adding 10.8 grams of salt to our water (assuming perfect packing efficiency of the salt crystals in your teaspoon). 
This gives our solution a concentration of

\$\$ \frac{10.8 g \* \frac{1 mol}{58.443 g} NaCl}{1 L \* \frac{1kg}{1L} water} = 0.185 \frac{mol}{kg} \$\$,

which gives us a boiling point elevation of

\$\$ 0.512 \frac{^\circ C kg}{mol} \* 0.185 \frac{mol}{kg} \* 2 = 0.189 ^\circ C \$\$.

Adding 1 teaspoon of salt to 1 litre of water will increase the boiling point of the water by roughly two tenths of a degree Celsius, hardly enough to have any effect on the cooking time. 
The various other impurities in tap water would likely already be changing the boiling point by that much.

What if we did want to reduce the cooking time of our pasta? 
I would guess that we would need to raise the boiling point of the water by at least 10 degrees to see any significant reduction in cooking time.

\$\$ \frac{10 ^\circ C}{0.512 \frac{^\circ C kg}{mol} \* 2} = 9.76 \frac{mol}{kg} \$\$

\$\$ 9.76 mol NaCl \* \frac{58.443 g}{1 mol} = 571 g NaCl \$\$

In order to have any significant effect on the cooking time, we would need to add more than half a kilogram of salt to the water.
