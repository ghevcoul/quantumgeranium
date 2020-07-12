Title: Potential Energy Surfaces for Shearing Materials
Date: 2014-10-06 15:12
Author: gavin
Slug: potential-energy-surfaces-for-shearing-materials
Status: published

A set of Python scripts for generating a potential energy surface (PES)
for the shearing of a material using the PWSCF program within [Quantum
ESPRESSO](http://www.quantum-espresso.org/). It does this by defining
two slabs in the simulation cell and calculates the energy of a grid of
points representing one slab moving relative to the other. The outputs
from PWSCF are read and converted into a format
[gnuplot](http://www.gnuplot.info/) can read to make a graphic
representing the PES. These are licensed under a 2-Clause (Simplified)
BSD License.

[pes\_builder.py](https://github.com/ghevcoul/MaterialsPES/blob/master/pes_builder.py)
- This script takes an input file containing a set of atomic coordinates
and lattice vectors, definition of the potential energy surface region
and resolution, and some information required by Quantum ESPRESSO. It
calculates the movement of the atoms and lattice vectors for each point
on the PES and writes a PWSCF input file for each point. Also, writes an
XYZ file for easy visualization of each point on the PES. An example of
the input file, calculating the shear of an alumina cell, can be seen
[here](https://github.com/ghevcoul/MaterialsPES/blob/master/example_input_alumina).

[results\_grabber\_pes.py](https://github.com/ghevcoul/MaterialsPES/blob/master/results_grabber_pes.py)
- This script reads the Quantum ESPRESSO output files generated from
running the PWSCF calculations set up by the previous script. Calculates
the energies of each point relative to the lowest energy point and
generates a formatted table of energies and an input file for gnuplot to
make a graphic of the PES.

\[caption id="attachment\_110" align="aligncenter"
width="300"\][![Potential energy surface of an alumina unit cell cleaved
in the centre of the
cell.](http://www.quantumgeranium.com/wp-content/uploads/2014/04/aluminaPES-300x224.png){.size-medium
.wp-image-110 width="300"
height="224"}](http://www.quantumgeranium.com/wp-content/uploads/2014/04/aluminaPES.png)
Potential energy surface of an alumina unit cell cleaved in the centre
of the cell.\[/caption\]

Both scripts are compatible with Python 2.6/2.7 - they *should*[ work
with Python 3.x after running the 2to3 utility, but this has not been
thoroughly tested.]{style="line-height: 1.5;"}
