---
layout: page
title: A Field Guide to Exotic Trees
subtitle: Looking Behind the Curtain
slug: field-guide-to-exotic-trees
---

{% include image.html
    img="assets/exotic-trees/european-maple.png"
    title="European Maple"
    caption="European Maple" %}

This is a bit of whimsical [generative art](https://en.wikipedia.org/wiki/Generative_art) project that I've been working on off-and-on for a while.

# The Origins
The idea for this started with what I was calling a [fractal tree generator](https://github.com/ghevcoul/fractal_app) based on the [Lindenmayer system](https://en.wikipedia.org/wiki/L-system#Example_2:_Fractal_(binary)_tree) binary tree concepts.
The initial implementation built a basic, symmetrical fractal tree that looked like this:

{% include image.html
    img="assets/img/L-tree.svg"
    title="Basic L-tree" %}

I'd recently learned the Flask framework for Python and liked the idea of a webpage that would randomly generate a tree when you visited.
Once you left the page, that particular tree would never be seen again.
So, I modified the algorithm to randomize the tree a bit by changing the number of branches, their lengths, and the angles between them.
That gave the trees a bit of variety, but they still looked pretty scraggly and not quite like real trees much of the time.

{% include image.html
    img="assets/img/random-L-tree.svg"
    title="Randomized L-tree" %}

I created a very bare-bones Flask app to display the trees, just a basic HTML page that embedded an SVG image (more on that later), and forgot about it for a while.

# The Resurrection
Some time later, I decided to come back to this project.
The first thing I did was pull out the tree generation code into a [new repo](https://github.com/ghevcoul/field-guide-to-exotic-trees) and modernize the codebase to Python 3.7 (3.4 was the current version when I wrote the Flask app).
I wanted to use some of the newer Python features I'd heard about but hadn't had a chance to use yet, since my work programming had moved away from Python, especially [data classes](https://docs.python.org/3.7/library/dataclasses.html) and type hinting.
I'd recently done a bit of work in Scala and was instantly enamoured with their case classes.
I felt it was a big missing tool in Python and was very excited when I heard data classes were being added to the standard library (yes, I know much of what you can do with data classes could already be done with [named tuples](https://docs.python.org/3.7/library/collections.html#collections.namedtuple), but for some reason I've never liked that solution, it always felt rather clunky and inelegant).

Once I had a cleaner codebase to work with, I set to work improving the tree generation algorithm to produce better looking trees.
The trees became larger and bushier, which definitely made them look more tree-like, but also pushed up the size of the SVG images I was writing.
Some of the largest trees I'd built had more than 400,000 branches and produced an 85 MB SVG file.
While Firefox could (eventually) render it, it took quite some time and was obvious that the SVG format was untenable going forward.
It had seemed like the perfect fit when I started making trees, the trees were simple line graphics and the SVG could be directly embedded into an HTML document so I didn't need to bother figuring out sending a PNG image in the original Flask app.
In the end, thanks to the excellent [Pillow](https://python-pillow.org/), I was able to add support for writing PNG bitmaps in just a couple hours having never used the library before.
Now, instead of writing SVGs tens of MB large, I was writing PNGs tens of KB small. 

The other major addition in this iteration of the project was giving the trees unique names.
There's not much to say on that, I created a basic system that randomly draws modifiers and species from a [list of options](https://github.com/ghevcoul/field-guide-to-exotic-trees/blob/master/FractalTree/names.py) to create a name for this particular tree.
I'm generally happy with the results of that, but I might make the two modifier names more common since they tend to sound simultaneously more real and more silly.

# The Future
While I'm happy with the current state of this code, there are some areas that could be improved or added to when I get inspiration to come back to this.
Years of academic papers means that I can't write up a project without a "future work" section, so in no particular order potential additions to this are:
* The current tree generation algorithm produces decidedly deciduous trees, it'd be nice to support other types like conifers and palms
* Expand the list of options for names so the results are less repetitive
* Turn it into a "real" field guide by writing full entries for each tree, maybe using something like a [Markov chain](https://en.wikipedia.org/wiki/Markov_chain) trained on the Audubon guide to trees if I can get my hands on a digital copy
