RNA-Puzzle 11
-----------------------------------------------------------------------------

NMR structure of the 5'-terminal hairpin of the 7SK snRNA

Solution sequence vs target sequence:

```
> targetA:1-57
GGGAUCUGUCACCCCAUUGAUCGCCUUCGGGCUGAUCUGGCUGGCUAGGCGGGUCCC
> solution_5iemA:1-57
GGGAUCUGUCACCCCAUUGAUCGCCUUCGGGCUGAUCUGGCUGGCUAGGCGGGUCCC
```

In the PDB there are similar structures for this target.
![](docs/mfa.png)
The target sequence is the same in PDB ID: 5iem, chain A, and this structure is used as the reference for this Puzzle.

RMSD

    rna_calc_rmsd.py -t solution_5iem_rpr.pdb *.pdb

    (base) [mm] rp11$ git:(master) ✗ csv rmsds.csv
    fn                      rmsd_all
    11_Adamiak_1_rpr.pdb    8.63
    11_Adamiak_2_rpr.pdb    10.38
    11_Adamiak_3_rpr.pdb    9.63
    11_Adamiak_4_rpr.pdb    8.66
    11_Adamiak_5_rpr.pdb    9.08
    11_Adamiak_6_rpr.pdb    6.37
    11_Adamiak_7_rpr.pdb    7.31
    11_Adamiak_8_rpr.pdb    10.48
    11_Adamiak_9_rpr.pdb    8.43
    11_Adamiak_10_rpr.pdb   9.93
    11_Bujnicki_1_rpr.pdb   6.17
    11_Bujnicki_2_rpr.pdb   18.44
    11_Bujnicki_3_rpr.pdb   6.73
    11_Bujnicki_4_rpr.pdb   6.51
    11_Bujnicki_5_rpr.pdb   9.4
    11_Bujnicki_6_rpr.pdb   12.38
    11_Bujnicki_7_rpr.pdb   7.36
    11_Bujnicki_8_rpr.pdb   11.54
    11_Bujnicki_9_rpr.pdb   5.25
    11_Bujnicki_10_rpr.pdb  7.72
    11_Chen_1_rpr.pdb       5.48
    11_Chen_2_rpr.pdb       7.09
    11_Chen_3_rpr.pdb       4.8
    11_Chen_4_rpr.pdb       6.4
    11_Chen_5_rpr.pdb       8.44
    11_Chen_6_rpr.pdb       6.58
    11_Chen_7_rpr.pdb       6.63
    11_Chen_8_rpr.pdb       7.73
    11_Chen_9_rpr.pdb       7.29
    11_Chen_10_rpr.pdb      8.0
    11_Das_1_rpr.pdb        5.49
    11_Das_2_rpr.pdb        8.34
    11_Das_3_rpr.pdb        7.49
    11_Das_4_rpr.pdb        6.39
    11_Das_5_rpr.pdb        7.34
    11_Das_6_rpr.pdb        6.32
    11_Das_7_rpr.pdb        7.6
    11_Das_8_rpr.pdb        9.44
    11_Das_9_rpr.pdb        18.66
    11_Das_10_rpr.pdb       9.43
    11_Ding_1_rpr.pdb       5.4
    11_Ding_2_rpr.pdb       10.78
    11_Ding_3_rpr.pdb       10.14
    11_Ding_4_rpr.pdb       6.41
    11_Ding_5_rpr.pdb       6.52
    11_Ding_6_rpr.pdb       6.7
    11_Ding_7_rpr.pdb       5.54
    11_Ding_8_rpr.pdb       6.21
    11_Ding_9_rpr.pdb       8.14
    11_Ding_10_rpr.pdb      10.87
    11_Xiao_1_rpr.pdb       8.94
    11_Xiao_2_rpr.pdb       12.73
    11_Xiao_3_rpr.pdb       10.92
    solution_5iem_rpr.pdb   0.0

INF

    rna_calc_inf.py -t solution_5iem_rpr.pdb *.pdb
    $ csv inf.csv
    target                       fn                            inf_all  inf_stack  inf_WC  inf_nWC  sns_WC  ppv_WC  sns_nWC  ppv_nWC
    solution_5iem_rpr.pdb.outCR  11_Adamiak_5_rpr.pdb.outCR    0.794    0.710      1.000   0.866    1.000   1.000   0.750    1.000
    solution_5iem_rpr.pdb.outCR  11_Adamiak_10_rpr.pdb.outCR   0.738    0.724      0.800   0.707    0.778   0.824   1.000    0.500
    solution_5iem_rpr.pdb.outCR  11_Bujnicki_10_rpr.pdb.outCR  0.755    0.808      0.693   0.530    0.611   0.786   0.750    0.375
    solution_5iem_rpr.pdb.outCR  11_Adamiak_6_rpr.pdb.outCR    0.485    0.000      0.943   0.667    0.889   1.000   1.000    0.444
    solution_5iem_rpr.pdb.outCR  11_Adamiak_1_rpr.pdb.outCR    0.434    0.000      0.766   0.750    0.722   0.812   0.750    0.750
    solution_5iem_rpr.pdb.outCR  11_Bujnicki_1_rpr.pdb.outCR   0.520    0.000      0.949   0.750    1.000   0.900   0.750    0.750
    solution_5iem_rpr.pdb.outCR  11_Adamiak_7_rpr.pdb.outCR    0.545    0.000      0.973   0.894    1.000   0.947   1.000    0.800
    solution_5iem_rpr.pdb.outCR  11_Adamiak_2_rpr.pdb.outCR    0.465    0.000      0.800   0.894    0.778   0.824   1.000    0.800
    solution_5iem_rpr.pdb.outCR  11_Bujnicki_2_rpr.pdb.outCR   0.362    0.000      0.738   0.000    0.778   0.700   0.000    0.000
    solution_5iem_rpr.pdb.outCR  11_Adamiak_8_rpr.pdb.outCR    0.446    0.000      0.825   0.707    0.778   0.875   1.000    0.500
    solution_5iem_rpr.pdb.outCR  11_Adamiak_3_rpr.pdb.outCR    0.437    0.000      0.800   0.707    0.778   0.824   1.000    0.500
    solution_5iem_rpr.pdb.outCR  11_Bujnicki_3_rpr.pdb.outCR   0.499    0.000      0.949   0.612    1.000   0.900   0.750    0.500
    solution_5iem_rpr.pdb.outCR  11_Adamiak_9_rpr.pdb.outCR    0.446    0.000      0.800   0.756    0.778   0.824   1.000    0.571
    solution_5iem_rpr.pdb.outCR  11_Adamiak_4_rpr.pdb.outCR    0.488    0.147      0.852   0.750    0.778   0.933   0.750    0.750
    solution_5iem_rpr.pdb.outCR  11_Bujnicki_4_rpr.pdb.outCR   0.506    0.000      0.919   0.750    0.944   0.895   0.750    0.750
    solution_5iem_rpr.pdb.outCR  11_Bujnicki_5_rpr.pdb.outCR   0.768    0.768      0.778   0.750    0.778   0.778   0.750    0.750
    solution_5iem_rpr.pdb.outCR  11_Chen_10_rpr.pdb.outCR      0.847    0.813      0.949   0.750    1.000   0.900   0.750    0.750
    solution_5iem_rpr.pdb.outCR  11_Chen_5_rpr.pdb.outCR       0.818    0.787      0.915   0.750    0.889   0.941   0.750    0.750
    solution_5iem_rpr.pdb.outCR  11_Chen_1_rpr.pdb.outCR       0.543    0.000      1.000   0.750    1.000   1.000   0.750    0.750
    solution_5iem_rpr.pdb.outCR  11_Bujnicki_6_rpr.pdb.outCR   0.455    0.147      0.800   0.671    0.778   0.824   0.750    0.600
    solution_5iem_rpr.pdb.outCR  11_Chen_6_rpr.pdb.outCR       0.523    0.000      0.973   0.756    1.000   0.947   1.000    0.571
    solution_5iem_rpr.pdb.outCR  11_Chen_2_rpr.pdb.outCR       0.517    0.000      0.944   0.750    0.944   0.944   0.750    0.750
    solution_5iem_rpr.pdb.outCR  11_Bujnicki_7_rpr.pdb.outCR   0.430    0.000      0.778   0.671    0.778   0.778   0.750    0.600
    solution_5iem_rpr.pdb.outCR  11_Chen_7_rpr.pdb.outCR       0.509    0.000      0.949   0.671    1.000   0.900   0.750    0.600
    solution_5iem_rpr.pdb.outCR  11_Chen_3_rpr.pdb.outCR       0.515    0.000      0.943   0.750    0.889   1.000   0.750    0.750
    solution_5iem_rpr.pdb.outCR  11_Bujnicki_8_rpr.pdb.outCR   0.430    0.000      0.766   0.756    0.722   0.812   1.000    0.571
    solution_5iem_rpr.pdb.outCR  11_Chen_8_rpr.pdb.outCR       0.520    0.000      0.949   0.750    1.000   0.900   0.750    0.750
    solution_5iem_rpr.pdb.outCR  11_Chen_4_rpr.pdb.outCR       0.506    0.000      0.919   0.750    0.944   0.895   0.750    0.750
    solution_5iem_rpr.pdb.outCR  11_Bujnicki_9_rpr.pdb.outCR   0.545    0.000      0.949   1.000    1.000   0.900   1.000    1.000
    solution_5iem_rpr.pdb.outCR  11_Chen_9_rpr.pdb.outCR       0.509    0.000      0.949   0.671    1.000   0.900   0.750    0.600
    solution_5iem_rpr.pdb.outCR  11_Das_10_rpr.pdb.outCR       0.545    0.000      0.973   0.894    1.000   0.947   1.000    0.800
    solution_5iem_rpr.pdb.outCR  11_Das_5_rpr.pdb.outCR        0.428    0.000      0.825   0.632    0.778   0.875   1.000    0.400
    solution_5iem_rpr.pdb.outCR  11_Ding_10_rpr.pdb.outCR      0.424    0.000      0.782   0.671    0.611   1.000   0.750    0.600
    solution_5iem_rpr.pdb.outCR  11_Das_1_rpr.pdb.outCR        0.523    0.000      1.000   0.707    1.000   1.000   1.000    0.500
    solution_5iem_rpr.pdb.outCR  11_Das_6_rpr.pdb.outCR        0.481    0.000      0.944   0.632    0.944   0.944   1.000    0.400
    solution_5iem_rpr.pdb.outCR  11_Ding_1_rpr.pdb.outCR       0.486    0.000      0.852   0.866    0.778   0.933   0.750    1.000
    solution_5iem_rpr.pdb.outCR  11_Das_2_rpr.pdb.outCR        0.523    0.000      1.000   0.707    1.000   1.000   1.000    0.500
    solution_5iem_rpr.pdb.outCR  11_Das_7_rpr.pdb.outCR        0.467    0.000      0.915   0.632    0.889   0.941   1.000    0.400
    solution_5iem_rpr.pdb.outCR  11_Ding_2_rpr.pdb.outCR       0.500    0.000      0.882   0.866    0.778   1.000   0.750    1.000
    solution_5iem_rpr.pdb.outCR  11_Das_3_rpr.pdb.outCR        0.534    0.000      0.973   0.816    1.000   0.947   1.000    0.667
    solution_5iem_rpr.pdb.outCR  11_Das_8_rpr.pdb.outCR        0.545    0.000      0.973   0.894    1.000   0.947   1.000    0.800
    solution_5iem_rpr.pdb.outCR  11_Ding_3_rpr.pdb.outCR       0.514    0.000      0.913   0.866    0.833   1.000   0.750    1.000
    solution_5iem_rpr.pdb.outCR  11_Das_4_rpr.pdb.outCR        0.523    0.000      0.973   0.756    1.000   0.947   1.000    0.571
    solution_5iem_rpr.pdb.outCR  11_Das_9_rpr.pdb.outCR        0.480    0.000      0.943   0.567    0.889   1.000   0.750    0.429
    solution_5iem_rpr.pdb.outCR  11_Ding_4_rpr.pdb.outCR       0.485    0.000      0.850   0.866    0.722   1.000   0.750    1.000
    solution_5iem_rpr.pdb.outCR  11_Ding_5_rpr.pdb.outCR       0.454    0.147      0.745   0.866    0.556   1.000   0.750    1.000
    solution_5iem_rpr.pdb.outCR  11_Xiao_1_rpr.pdb.outCR       0.446    0.000      0.825   0.707    0.778   0.875   1.000    0.500
    solution_5iem_rpr.pdb.outCR  11_Ding_6_rpr.pdb.outCR       0.471    0.000      0.819   0.866    0.722   0.929   0.750    1.000
    solution_5iem_rpr.pdb.outCR  11_Xiao_2_rpr.pdb.outCR       0.503    0.000      0.884   0.894    0.833   0.938   1.000    0.800
    solution_5iem_rpr.pdb.outCR  11_Ding_7_rpr.pdb.outCR       0.485    0.000      0.850   0.866    0.722   1.000   0.750    1.000
    solution_5iem_rpr.pdb.outCR  11_Xiao_3_rpr.pdb.outCR       0.470    0.000      0.915   0.567    0.889   0.941   0.750    0.429
    solution_5iem_rpr.pdb.outCR  solution_5iem_rpr.pdb.outCR   1.000    1.000      1.000   1.000    1.000   1.000   1.000    1.000
    solution_5iem_rpr.pdb.outCR  11_Ding_8_rpr.pdb.outCR       0.529    0.147      0.913   0.866    0.833   1.000   0.750    1.000
    solution_5iem_rpr.pdb.outCR  11_Ding_9_rpr.pdb.outCR       0.470    0.000      0.816   0.866    0.667   1.000   0.750    1.000
