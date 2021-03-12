# Continue the calculation
To continue the calculation at some point, please follow the steps below,

### Optimization

1. Specify the current step of optimization in QM/MM parameters input files.
   - For example: Start from optimized step2
      ```
      current_step=2
      ```
      
2. Make sure the enegy and forces file are in the base directory. In BFGS calculation, the `bfgs_hessian.txt` should also exist. The program will read the last enegies and forces to continue the calculation. 


    ```bash
    base_directory/
    |-- oenergy.txt
    |-- oforces.txt
    |-- (bfgs_hessian.txt)
    ...
    ```

3. Run `python gmx2qmmm.py` to continue. 






### Scan

1. Specify the current step of optimization in QM/MM parameters input files.
   - For example: Linear scan atom1 and atom2 with 3 steps, and continue from scan step2 and optimized step3
      ```
      scan_step=2
      current_step=3
      ```
      
2. Make sure the enegy and forces file are in the base directory. In BFGS calculation, the `bfgs_hessian.txt` should also exist. The program will read the last enegies and forces to continue the calculation. 
   - For example: Linear scan atom1 and atom2 with 3 steps, and continue from scan step2 and optimized step3

       ```bash
       base_directory/
       |-- oenergy_scanR1-2_1.txt (OPT energies in scan step 1)
       |-- oenergy_scanR1-2_2.txt (OPT energies in scan step 2)
       |-- oforces_scanR1-2_1.txt (OPT forces in scan step 1)
       |-- oforces_scanR1-2_2.txt (OPT forces in scan step 2)
       |-- (bfgs_hessian.txt)
       ...
       ```


3. Run `python gmx2qmmm.py` to continue. 



[Back to HOME](index)
