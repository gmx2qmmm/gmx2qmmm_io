## Welcome to gmx2qmmm

**gmx2qmmm** is a python interface for Quantum mechanics/Molecular mechanics (QM/MM) calculation.
 

## Overview

**gmx2qmmm** is a python package to bridge [Gaussian] and [Gromacs]. The test runs were performed using [Gaussian16] and [Gromacs 5.0.2], but the code should be able to read earlier Gaussian and other Gromacs versions. The only limits are the formats of the human-readable input and output files of each program, as such, conversion scripts can be written to make the interface work with any version, if the current code does not support it.
Conceptually, **gmx2qmmm** creates a QM/MM potential and performs either single point calculations (i.e., the current energy of your system) or geometry optimizations. (Other ultilities are ongoing)

## System requirements
 - [python 2.7] 
 - [Gaussian16] (and earlier version)
 - [Gromacs 5.0.2] (and earlier version)

## **gmx2qmmm** job

|Job type|Calculation|
| --- | --- |
|Single point calcuation (SP)|Calculate single point energy and forces (.xyz) |
|Geometry optimizations (OPT)|Optimize the system energy via optimizer ([Steepest descent], [Conjugate gradient] or [BFGS])|

[Steepest descent]:<https://en.wikipedia.org/wiki/Gradient_descent>
[Conjugate gradient]:<https://en.wikipedia.org/wiki/Conjugate_gradient_method>
[BFGS]:<https://en.wikipedia.org/wiki/Broyden%E2%80%93Fletcher%E2%80%93Goldfarb%E2%80%93Shanno_algorithm>

## **gmx2qmmm** parameters
- [QM parameters](qm_param)

## References

> A user‐friendly, Python‐based quantum mechanics/Gromacs interface: gmx2qmmm
> Jan P. Götze, Yuan‐Wei Pi, Simon Petry, Fabian Langkabel,  Jan Felix Witte, Oliver Lemke
> [https://doi.org/10.1002/qua.26486]

## Support and development
For bug reports/suggestions/complaints please raise an issue on [GitHub].

Or contact us directly: [gmx2qmmm@gmail.com]
 
[python 2.7]:<https://www.python.org/download/releases/2.7>
[Gaussian16]:<https://gaussian.com/gaussian16/>
[Gromacs 5.0.2]:<http://www.gromacs.org>
[Gaussian]:<https://gaussian.com/gaussian16/>
[Gromacs]:<http://www.gromacs.org>
[GitHub]:<https://github.com/gmx2qmmm/gmx2qmmm_portable/issues>
[gmx2qmmm@gmail.com]:<mailto:gmx2qmmm@gmail.com>
[gmx2qmmm reference]:<https://drive.google.com/file/d/1B6YNfCFRB4jqweVABamPQWlgziFlNIDK/view?usp=sharing>
[https://doi.org/10.1002/qua.26486]:<https://doi.org/10.1002/qua.26486>
 
<!--You can use the [editor on GitHub](https://github.com/gmx2qmmm/gmx2qmmm_io/edit/gh-pages/index.md) to maintain and preview the content for your website in Markdown files.-->

<!--Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.-->

<!--For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).-->

<!--### Jekyll Themes-->

<!--Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/gmx2qmmm/gmx2qmmm_io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.-->

<!--### Support or Contact-->

<!--Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.-->
