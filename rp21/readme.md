RNA-Puzzle 21
-----------------------------------------------------------------------------

Solution sequence vs target sequence:

    > 21_solution_2 A:1-41
    CCGGACGAGGUGCGCCGUACCCGGUCACGACAAGACGGCGC
    > 21_3dRNA_1_rpr A:1-41
    CCGGACGAGGUGCGCCGUACCCGGUCACGACAAGACGGCGC

Processing:

    rna_pdb_toolsx.py --rpr --inplace --dont_rename_chains *

INFs
-------------------------------------------------------------------------------

```
[mm] rp21$ git:(master) ✗ column -s, -t < inf.csv
column: line too long
target                       fn                              inf_all  inf_stack  inf_WC  inf_nWC  sns_WC  ppv_WC  sns_nWC  ppv_nWC
21_solution_2_rpr.pdb.outCR  21_solution_2_rpr.pdb.outCR     1        0          1       1        1       1       1        1
21_solution_2_rpr.pdb.outCR  21_Adamiak_3_rpr.pdb.outCR      0.764    0          0.909   0.5      0.909   0.909   0.25     1
21_solution_2_rpr.pdb.outCR  21_Adamiak_4_rpr.pdb.outCR      0.764    0          0.909   0.5      0.909   0.909   0.25     1
21_solution_2_rpr.pdb.outCR  21_Adamiak_1_rpr.pdb.outCR      0.728    0          0.909   0.354    0.909   0.909   0.125    1
21_solution_2_rpr.pdb.outCR  21_RNAComposer_3_rpr.pdb.outCR  0.725    0          0.953   0        0.909   1       0        0
21_solution_2_rpr.pdb.outCR  21_RNAComposer_4_rpr.pdb.outCR  0.725    0          0.953   0        0.909   1       0        0
21_solution_2_rpr.pdb.outCR  21_Adamiak_2_rpr.pdb.outCR      0.7      0          0.87    0.354    0.909   0.833   0.125    1
21_solution_2_rpr.pdb.outCR  21_Adamiak_5_rpr.pdb.outCR      0.692    0          0.909   0        0.909   0.909   0        0
21_solution_2_rpr.pdb.outCR  21_3dRNA_4_rpr.pdb.outCR        0.459    0          0.64    0        0.545   0.75    0        0
21_solution_2_rpr.pdb.outCR  21_3dRNA_1_rpr.pdb.outCR        0.41     0          0.603   0        0.364   1       0        0
21_solution_2_rpr.pdb.outCR  21_3dRNA_2_rpr.pdb.outCR        0.41     0          0.603   0        0.364   1       0        0
21_solution_2_rpr.pdb.outCR  21_3dRNA_3_rpr.pdb.outCR        0.41     0          0.603   0        0.364   1       0        0
21_solution_2_rpr.pdb.outCR  21_RW3D_6_rpr.pdb.outCR         0.401    0          0.545   0.158    0.545   0.545   0.125    0.2
21_solution_2_rpr.pdb.outCR  21_RNAComposer_2_rpr.pdb.outCR  0.397    0          0.572   0        0.545   0.6     0        0
21_solution_2_rpr.pdb.outCR  21_RW3D_9_rpr.pdb.outCR         0.389    0          0.545   0.144    0.545   0.545   0.125    0.167
21_solution_2_rpr.pdb.outCR  21_3dRNA_5_rpr.pdb.outCR        0.382    0          0.545   0        0.545   0.545   0        0
21_solution_2_rpr.pdb.outCR  21_RNAComposer_5_rpr.pdb.outCR  0.382    0          0.545   0        0.545   0.545   0        0
21_solution_2_rpr.pdb.outCR  21_RW3D_3_rpr.pdb.outCR         0.379    0          0.545   0.134    0.545   0.545   0.125    0.143
21_solution_2_rpr.pdb.outCR  21_simRNA_1_rpr.pdb.outCR       0.344    0          0.467   0        0.545   0.4     0        0
21_solution_2_rpr.pdb.outCR  21_RW3D_5_rpr.pdb.outCR         0.334    0          0.522   0        0.545   0.5     0        0
21_solution_2_rpr.pdb.outCR  21_RW3D_8_rpr.pdb.outCR         0.334    0          0.522   0        0.545   0.5     0        0
21_solution_2_rpr.pdb.outCR  21_simRNA_4_rpr.pdb.outCR       0.334    0          0.467   0        0.545   0.4     0        0
21_solution_2_rpr.pdb.outCR  21_RW3D_10_rpr.pdb.outCR        0.324    0          0.522   0        0.545   0.5     0        0
21_solution_2_rpr.pdb.outCR  21_RW3D_1_rpr.pdb.outCR         0.324    0          0.522   0        0.545   0.5     0        0
21_solution_2_rpr.pdb.outCR  21_RW3D_2_rpr.pdb.outCR         0.316    0          0.522   0        0.545   0.5     0        0
21_solution_2_rpr.pdb.outCR  21_RW3D_4_rpr.pdb.outCR         0.316    0          0.522   0        0.545   0.5     0        0
21_solution_2_rpr.pdb.outCR  21_RW3D_7_rpr.pdb.outCR         0.316    0          0.522   0        0.545   0.5     0        0
21_solution_2_rpr.pdb.outCR  21_simRNA_2_rpr.pdb.outCR       0.308    0          0.452   0        0.545   0.375   0        0
21_solution_2_rpr.pdb.outCR  21_RNAComposer_1_rpr.pdb.outCR  0.296    0          0.426   0.134    0.364   0.5     0.125    0.143
21_solution_2_rpr.pdb.outCR  21_simRNA_3_rpr.pdb.outCR       0.278    0          0.403   0        0.455   0.357   0        0
```

RMSD
-------------------------------------------------------------------------------

    [mm] rp21$ git:(master) ✗ rna_calc_rmsd.py -t 21_solution_2_rpr.pdb *.pdb
    method: all-atom-built-in
    # of models: 31
    21_3dRNA_1_rpr.pdb 12.09 881
    21_3dRNA_2_rpr.pdb 12.41 881
    21_3dRNA_3_rpr.pdb 12.28 881
    21_3dRNA_4_rpr.pdb 18.09 881
    21_3dRNA_5_rpr.pdb 17.49 881
    21_Adamiak_1_rpr.pdb 4.8 881
    21_Adamiak_2_rpr.pdb 4.81 881
    21_Adamiak_3_rpr.pdb 4.75 881
    21_Adamiak_4_rpr.pdb 4.74 881
    21_Adamiak_5_rpr.pdb 5.69 881
    21_RNAComposer_1_rpr.pdb 14.63 881
    21_RNAComposer_2_rpr.pdb 18.21 881
    21_RNAComposer_3_rpr.pdb 12.23 881
    21_RNAComposer_4_rpr.pdb 13.02 881
    21_RNAComposer_5_rpr.pdb 17.04 881
    21_RW3D_1_rpr.pdb 17.92 881
    21_RW3D_2_rpr.pdb 16.05 881
    21_RW3D_3_rpr.pdb 17.81 881
    21_RW3D_4_rpr.pdb 18.21 881
    21_RW3D_5_rpr.pdb 18.11 881
    21_RW3D_6_rpr.pdb 16.98 881
    21_RW3D_7_rpr.pdb 18.05 881
    21_RW3D_8_rpr.pdb 17.66 881
    21_RW3D_9_rpr.pdb 18.03 881
    21_RW3D_10_rpr.pdb 16.23 881
    21_simRNA_1_rpr.pdb 12.05 881
    21_simRNA_2_rpr.pdb 11.72 881
    21_simRNA_3_rpr.pdb 13.29 881
    21_simRNA_4_rpr.pdb 10.85 881
    21_simRNA_5_rpr.pdb 13.29 881
    21_solution_2_rpr.pdb 0.0 881
    # of atoms used: 881
    csv was created!  rmsds.csv

Archive
-------------------------------------------------------------------------------

In the archive folder, there are more solution structures with one mismatch compared to the target sequence.

    CCGGACGAGGUGCGCCGUACCCGGUCAGGACAAGACGGCGC # 21_solution_0_rpr
    CCGGACGAGGUGCGCCGUACCCGGUCACGACAAGACGGCGC # 21_3dRNA_1_rpr
                               x mismatch

    [mm] archive$ git:(master) ✗ rna_pdb_toolsx.py --get_seq *
    # 21_solution_0
    > A:1-41
    CCGGACGAGGUGCGCCGUACCCGGUCAGGACAAGACGGCGC
    > B:1-41
    CCGGACGAGGUGCGCCGUACCCGGUCAGGACAAGACGGCGC
    # 21_solution_1
    > A:1-41
    CCGGACGAGGUGCGCCGUACCCGGUCAGGACAAGACGGCGC
    > B:1-41
    CCGGACGAGGUGCGCCGUACCCGGUCAGGACAAGACGGCGC
    # 21_solution_2
    > A:1-41
    CCGGACGAGGUGCGCCGUACCCGGUCACGACAAGACGGCGC
    
Solutions
-------------------------------------------------------------------------------

![](solutions/rp21-solutions.png)
