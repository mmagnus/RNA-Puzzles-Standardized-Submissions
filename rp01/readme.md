RNA-Puzzle 01
-----------------------------------------------------------------------------

Solution sequence vs target sequence:

      > 1_solution_0_rpr A:1-23
      CCGCCGCGCCAUGCCUGUGGCGG
      > 1_solution_0_rpr B:1-23
      CCGCCGCGCCAUGCCUGUGGCGG

`seq.txt`:

      for i in `ls *.pdb`; do rna_pdb_tools.py --get_seq $i; echo ''; done > seq.txt

Split one chain into two:

- 1_santalucia_1_rpr
- 1_major_1_rpr.pdb
- 1_das_5_rpr.pdb
- 1_das_4_rpr.pdb
- 1_das_3_rpr.pdb
- 1_das_2_rpr.pdb
- 1_das_1_rpr.pdb
- 1_chen_1_rpr.pdb

```
rna_calc_rmsd.py -t 1_solution_0_rpr.pdb *.pdb
method: all-atom-built-in
# of models: 16
1_bujnicki_1_rpr.pdb 5.71 978
1_bujnicki_2_rpr.pdb 6.16 978
1_bujnicki_3_rpr.pdb 5.3 978
1_bujnicki_4_rpr.pdb 4.95 978
1_bujnicki_5_rpr.pdb 5.1 978
1_chen_1_rpr.pdb 4.35 978
1_chen_1_rpr_v2.pdb 4.35 978
1_das_1_rpr.pdb 3.97 978
1_das_2_rpr.pdb 4.48 978
1_das_3_rpr.pdb 3.43 978
1_das_4_rpr.pdb 3.92 978
1_das_5_rpr.pdb 4.57 978
1_dokholyan_1_rpr.pdb 7.25 978
1_major_1_rpr.pdb 4.34 978
1_santalucia_1_rpr.pdb 5.76 978
1_solution_0_rpr.pdb 0.0 978
# of atoms used: 978
csv was created!  rmsds.csv
```

```
rna_calc_inf.py -t 1_solution_0_rpr.pdb *.pdb
 93% (14 of 15) |############################################################################################################################################          | Elapsed Time: 0:01:45 ETA: 0:00:07csv was created!  inf.csv

target                      fn                            inf_all  inf_stack  inf_WC  inf_nWC  sns_WC  ppv_WC  sns_nWC  ppv_nWC
1_solution_0_rpr.pdb.outCR  1_das_2_rpr.pdb.outCR         0.837    0.000      0.941   0.447    0.941   0.941   0.500    0.400
1_solution_0_rpr.pdb.outCR  1_das_1_rpr.pdb.outCR         0.910    0.000      0.972   0.671    1.000   0.944   0.750    0.600
1_solution_0_rpr.pdb.outCR  1_bujnicki_4_rpr.pdb.outCR    0.709    0.000      0.840   0.250    0.706   1.000   0.250    0.250
1_solution_0_rpr.pdb.outCR  1_bujnicki_3_rpr.pdb.outCR    0.874    0.000      0.910   0.707    0.882   0.938   0.500    1.000
1_solution_0_rpr.pdb.outCR  1_bujnicki_5_rpr.pdb.outCR    0.701    0.000      0.840   0.378    0.706   1.000   0.500    0.286
1_solution_0_rpr.pdb.outCR  1_chen_1_rpr.pdb.outCR        0.873    0.000      0.970   0.000    0.941   1.000   0.000    0.000
1_solution_0_rpr.pdb.outCR  1_bujnicki_1_rpr.pdb.outCR    0.930    0.000      0.972   0.750    1.000   0.944   0.750    0.750
1_solution_0_rpr.pdb.outCR  1_bujnicki_2_rpr.pdb.outCR    0.830    0.000      0.941   0.289    0.941   0.941   0.250    0.333
1_solution_0_rpr.pdb.outCR  1_solution_0_rpr.pdb.outCR    1.000    0.000      1.000   1.000    1.000   1.000   1.000    1.000
1_solution_0_rpr.pdb.outCR  1_dokholyan_1_rpr.pdb.outCR   0.905    0.000      0.970   0.671    0.941   1.000   0.750    0.600
1_solution_0_rpr.pdb.outCR  1_das_4_rpr.pdb.outCR         0.930    0.000      0.970   0.816    0.941   1.000   1.000    0.667
1_solution_0_rpr.pdb.outCR  1_santalucia_1_rpr.pdb.outCR  0.927    0.000      1.000   0.577    1.000   1.000   0.500    0.667
1_solution_0_rpr.pdb.outCR  1_das_5_rpr.pdb.outCR         0.905    0.000      0.941   0.750    0.941   0.941   0.750    0.750
1_solution_0_rpr.pdb.outCR  1_das_3_rpr.pdb.outCR         0.977    0.000      1.000   0.894    1.000   1.000   1.000    0.800
1_solution_0_rpr.pdb.outCR  1_major_1_rpr.pdb.outCR       0.901    0.000      0.970   0.577    0.941   1.000   0.500    0.667
```
