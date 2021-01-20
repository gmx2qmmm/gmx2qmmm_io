# Input files

The required input files in the package are

|Input files|Command|Default input name|
| ------ | ------ | ------ |
|[Coordinate file](#Coordinate-file) (.g96 or .gro)|-c|conf.g96|
|Topology (.top)|-p|topol.top|
|QM atoms file(.ndx)|-n|qmatoms.ndx|
|QM parameters (.dat)|-qm|qm.dat|
|MM parameters (.dat)|-mm|mm.dat|
|QM/MM parameters (.dat)|-qmmm|qmmm.dat|
|Active atoms (.ndx)|-act|act.ndx|
|Path file (.dat)|-path|path.dat|
|Logfile (.log)|-g|logfile|


## Coordinate file

This file should be taken almost as it comes from your Gromacs simulation. It needs “reboxing” in case
your box is not cubic. Make sure your molecule is not suffering from periodic boundary artifacts. All
these caveats however should be taken care of anyway due to the typical ways of QM/MM practice (such
as preparing your system centered on a region of interest, surrounded by a drop of frozen solvent,
removing all other parts of the system).
