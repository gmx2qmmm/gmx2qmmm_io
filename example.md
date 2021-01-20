# Quick Start : glycine serine (GLYSER)

Glycine serine (GLYSER) includes 21 atoms. In this case, we select the first 7 atoms in the QM region and other atoms are in MM region. The figure is showed below.

![alt text](https://github.com/gmx2qmmm/gmx2qmmm_portable/blob/master/example/glyser.png?raw=true)

### If you want to build everything from the beginning and customize the input file name, follow the process below.

1. Prepare **Coordinate file (.g96 or .gro)** and **Topology (.top)** files of GLYSER.
2. Since we select the first 7 atoms in the QM region, set **QM atom file (.ndx)**
    ```
    1 2 3 4 5 6 7
    ```
3. The total chages of QM region is 1, so set the parameter _charge=1_ in **QM parameters (.dat)**. Others are maintained as default.
    ```
    charge=1
    ```
4. We use default setting in **MM parameters (.dat)**, **QM/MM parameters (.dat)**, so keep the file empty.
5. Setup your software path in **path.dat**
6. Select active atoms in the calculation, in this case we select all. So set **Active atoms (.ndx)
**,
    ```
    1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21
    ```
7. Run 
```python [path of gmx2qmmm.py ][-h] [-c COORD] [-p TOP] [-n QMATOMS] [-qm QMFILE] [-mm MMFILE] [-qmmm QMMMFILE] [-act ACT] [-path PATHFILE] [-g LOGFILE]```




[Back to HOME](index)
