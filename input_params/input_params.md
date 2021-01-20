# Input files

The required input files in the package are

|Input files|Command|Default input name|
| ------ | ------ | ------ |
|[Coordinate file](#Coordinate-file) (.g96 or .gro)|-c|conf.g96|
|[Topology](#Topology) (.top)|-p|topol.top|
|[QM atoms file](#QM-atoms-file)(.ndx)|-n|qmatoms.ndx|
|QM parameters (.dat)|-qm|qm.dat|
|MM parameters (.dat)|-mm|mm.dat|
|QM/MM parameters (.dat)|-qmmm|qmmm.dat|
|Active atoms (.ndx)|-act|act.ndx|
|Path file (.dat)|-path|path.dat|
|Logfile (.log)|-g|logfile|

[Back to HOME](../index)

## Coordinate file

This file should be taken almost as it comes from your Gromacs simulation. It needs “reboxing” in case your box is not cubic. Make sure your molecule is not suffering from periodic boundary artifacts. All these caveats however should be taken care of anyway due to the typical ways of QM/MM practice (such as preparing your system centered on a region of interest, surrounded by a drop of frozen solvent, removing all other parts of the system).

[Back to TOP](input_params)

## Topology

You might need to change the .top file according to your QM/MM preparatory steps (such as reducing the number of solvent molecules and ions in the molecule list at the end of your topology). Apart from that, it is best to copy some of the .itp files and prepare simplified copies. For example, a tip3p.itp in a force field may contain several “if” clauses what to use and when. **gmx2qmmm cannot decide which of the different parameter sets to use!** Therefore, **delete all “if” clauses in your (copied) .itp files and present only the desired parameters!**

Typical pdb2gmx results do not suffer from these problems, so this usually only affects files that are provided with the desired force field.

In some cases, you might also need to provide the mass of an atom, since the force field-provided files are not explicitly writing the mass into the atom definition. This typically affects the water and ions. 

**At the current stage, the user is well advised to copy and fix the water and ions topologies to make sure that gmx2qmmm choses the correct parameters. The files provided with the examples should guide the user towards the required formats.**

[Back to TOP](input_params)

## QM atoms file

The QM atoms file is simply a list of numbers in any order or number of lines. The user may use the free
formatting to, e.g., visually separate different residues.

## QM parameters

[Back to TOP](input_params)

## MM parameters

[Back to TOP](input_params)

## QM/MM parameters

[Back to TOP](input_params)

## Active atoms

[Back to TOP](input_params)

## Path
The path file includes the path of the specific QM and MM software and the executed command for the certain software. The following options, one per line, may be given in this file; in any order.

[Back to TOP](input_params)

## Logfile

This logfile contains all relevant actions of gmx2qmmm with a time stamp for each action. It will also contain the error messages if something went wrong that is not related to the python code.

[Back to TOP](input_params)

[Back to HOME](../index)
