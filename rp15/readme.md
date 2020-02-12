RNA-Puzzle 15
-----------------------------------------------------------------------------

Solution sequence vs target sequence:

```
> 15_RW2DAS1_9_rpr A:1-48
GGGUACUUAAGCCCACUGAUGAGUCGCUGGGAUGCGACGAAACGCCCA
> 15_RW2DAS1_9_rpr B:1-20
GGGCGUCUGGGCAGUACCCA

> 15_solution_0_rpr A:1-48
GGGUACUUAAGCCCACUGAUGAGUCGCUGGGAUGCGACGAAACGCCCA
> 15_solution_0_rpr B:1-20
GGGCGUCUGGGCAGUACCCA
```

Edit chains:

	for i in `ls *3dRNA*`; do rna_pdb_tools.py --edit 'B:49-68>B:1-20' $i > ${i}_temp; mv ${i}_temp ${i}; done
	for i in `ls *Chen*`; do rna_pdb_tools.py --edit 'B:52-71>B:1-20' $i > ${i}_temp; mv ${i}_temp ${i}; done
	for i in `ls *RW2DAS*`; do rna_pdb_tools.py --edit 'A:49-68>B:1-20' $i > ${i}_temp; mv ${i}_temp ${i}; done

RMSD
-------------------------------------------------------------------------------

```
rna_calc_rmsd.py -t 15_solution_0_rpr.pdb --model-selection A:1-48+B:1-20 --model-ignore-selection A/7/O2\' *.pdb
method: all-atom-built-in

csv rmsds.csv
column: line too long
fn                           rmsd_all
15_Adamiak_8_rpr.pdb         6.68
15_Adamiak_10_rpr.pdb        6.82
15_SimRNAAS1_1_rpr.pdb       7.3
15_Adamiak_9_rpr.pdb         7.98
15_Adamiak_2_rpr.pdb         8.28
15_RNAComposerAS1_1_rpr.pdb  8.28
15_Adamiak_3_rpr.pdb         8.53
15_RNAComposerAS1_2_rpr.pdb  8.53
15_Adamiak_7_rpr.pdb         8.61
15_Chen_6_rpr.pdb            8.67
15_Adamiak_5_rpr.pdb         8.73
15_RNAComposerAS2_2_rpr.pdb  8.73
15_Adamiak_4_rpr.pdb         8.83
15_RNAComposerAS2_1_rpr.pdb  8.83
15_Chen_3_rpr.pdb            8.93
15_Adamiak_6_rpr.pdb         9.02
15_Adamiak_1_rpr.pdb         9.18
15_Chen_10_rpr.pdb           9.43
15_SimRNAAS2_7_rpr.pdb       9.46
15_Chen_1_rpr.pdb            9.58
15_Chen_4_rpr.pdb            10.17
15_RW2DAS2_4_rpr.pdb         10.27
15_RW2DAS2_5_rpr.pdb         11
15_Chen_7_rpr.pdb            11.19
15_SimRNAAS2_4_rpr.pdb       11.48
15_Chen_8_rpr.pdb            12.14
15_RW2DAS2_1_rpr.pdb         12.16
15_RW2DAS1_5_rpr.pdb         12.56
15_RW2DAS2_8_rpr.pdb         13.41
15_Chen_9_rpr.pdb            13.48
15_RW2DAS2_7_rpr.pdb         13.76
15_SimRNAAS2_9_rpr.pdb       13.92
15_RW2DAS2_10_rpr.pdb        14.49
15_RW2DAS1_4_rpr.pdb         14.58
15_RW2DAS1_9_rpr.pdb         14.61
15_RW2DAS2_9_rpr.pdb         14.67
15_RW2DAS1_7_rpr.pdb         14.88
15_SimRNAAS2_1_rpr.pdb       15.09
15_RW2DAS1_6_rpr.pdb         15.29
15_RW2DAS1_3_rpr.pdb         15.31
15_RW2DAS1_2_rpr.pdb         15.45
15_Chen_2_rpr.pdb            15.74
15_Chen_5_rpr.pdb            16.08
15_RW2DAS2_3_rpr.pdb         16.31
15_RW2DAS2_2_rpr.pdb         16.43
15_RW2DAS1_1_rpr.pdb         17.07
15_SimRNAAS1_3_rpr.pdb       17.07
15_RW2DAS1_10_rpr.pdb        17.6
15_RW2DAS2_6_rpr.pdb         17.97
15_SimRNAAS1_7_rpr.pdb       18.27
15_SimRNAAS2_2_rpr.pdb       18.73
15_SimRNAAS1_9_rpr.pdb       19.14
15_SimRNAAS1_10_rpr.pdb      19.42
15_SimRNAAS2_10_rpr.pdb      19.44
15_RW2DAS1_8_rpr.pdb         19.83
15_SimRNAAS2_3_rpr.pdb       19.83
15_SimRNAAS1_8_rpr.pdb       19.91
15_SimRNAAS2_5_rpr.pdb       20.08
15_SimRNAAS2_6_rpr.pdb       20.46
15_SimRNAAS1_2_rpr.pdb       20.72
15_SimRNAAS1_5_rpr.pdb       20.91
15_SimRNAAS2_8_rpr.pdb       21.98
15_SimRNAAS1_6_rpr.pdb       22.19
15_SimRNAAS1_4_rpr.pdb       24.19
15_3dRNAAS2_2_rpr.pdb        24.53
15_3dRNAAS2_4_rpr.pdb        24.54
15_3dRNAAS2_5_rpr.pdb        24.56
15_3dRNAAS2_7_rpr.pdb        24.56
15_3dRNAAS2_3_rpr.pdb        24.57
15_3dRNAAS2_9_rpr.pdb        24.57
15_3dRNAAS2_6_rpr.pdb        24.6
15_3dRNAAS2_10_rpr.pdb       24.61
15_3dRNAAS2_1_rpr.pdb        24.64
```


INFS
-------------------------------------------------------------------------------

```
rna_calc_inf.py -t 15_solution_0_rpr.pdb *.pdb --stacking -f # py2-106-g77f5b66
csv inf.csv
target                       fn                                 inf_all  inf_stack  inf_WC  inf_nWC  sns_WC  ppv_WC  sns_nWC  ppv_nWC
15_solution_0_rpr.pdb.outCR  15_solution_0_rpr.pdb.outCR        1        1          1       1        1       1       1        1
15_solution_0_rpr.pdb.outCR  15_Chen_3_rpr.pdb.outCR            0.836    0.853      0.827   0.671    0.941   0.727   0.75     0.6
15_solution_0_rpr.pdb.outCR  15_Adamiak_3_rpr.pdb.outCR         0.832    0.834      0.86    0.75     1       0.739   0.75     0.75
15_solution_0_rpr.pdb.outCR  15_RNAComposerAS1_2_rpr.pdb.outCR  0.832    0.834      0.86    0.75     1       0.739   0.75     0.75
15_solution_0_rpr.pdb.outCR  15_Adamiak_2_rpr.pdb.outCR         0.816    0.811      0.86    0.75     1       0.739   0.75     0.75
15_solution_0_rpr.pdb.outCR  15_RNAComposerAS1_1_rpr.pdb.outCR  0.816    0.811      0.86    0.75     1       0.739   0.75     0.75
15_solution_0_rpr.pdb.outCR  15_Adamiak_8_rpr.pdb.outCR         0.814    0.83       0.842   0.5      1       0.708   0.25     1
15_solution_0_rpr.pdb.outCR  15_RW2DAS2_10_rpr.pdb.outCR        0.805    0.831      0.809   0.447    0.941   0.696   0.5      0.4
15_solution_0_rpr.pdb.outCR  15_Chen_4_rpr.pdb.outCR            0.804    0.807      0.847   0.577    0.941   0.762   0.5      0.667
15_solution_0_rpr.pdb.outCR  15_Adamiak_10_rpr.pdb.outCR        0.795    0.812      0.842   0.354    1       0.708   0.25     0.5
15_solution_0_rpr.pdb.outCR  15_Chen_1_rpr.pdb.outCR            0.789    0.802      0.794   0.577    0.882   0.714   0.5      0.667
15_solution_0_rpr.pdb.outCR  15_Chen_5_rpr.pdb.outCR            0.787    0.8        0.794   0.577    0.882   0.714   0.5      0.667
15_solution_0_rpr.pdb.outCR  15_Adamiak_7_rpr.pdb.outCR         0.785    0.781      0.86    0.5      1       0.739   0.25     1
15_solution_0_rpr.pdb.outCR  15_RW2DAS2_9_rpr.pdb.outCR         0.783    0.785      0.809   0.671    0.941   0.696   0.75     0.6
15_solution_0_rpr.pdb.outCR  15_RW2DAS2_1_rpr.pdb.outCR         0.782    0.785      0.809   0.671    0.941   0.696   0.75     0.6
15_solution_0_rpr.pdb.outCR  15_Chen_2_rpr.pdb.outCR            0.779    0.777      0.827   0.671    0.941   0.727   0.75     0.6
15_solution_0_rpr.pdb.outCR  15_RW2DAS1_1_rpr.pdb.outCR         0.778    0.794      0.827   0.408    0.941   0.727   0.5      0.333
15_solution_0_rpr.pdb.outCR  15_Adamiak_4_rpr.pdb.outCR         0.777    0.762      0.86    0.707    1       0.739   0.5      1
15_solution_0_rpr.pdb.outCR  15_Adamiak_5_rpr.pdb.outCR         0.777    0.77       0.842   0.707    1       0.708   0.5      1
15_solution_0_rpr.pdb.outCR  15_RNAComposerAS2_1_rpr.pdb.outCR  0.777    0.762      0.86    0.707    1       0.739   0.5      1
15_solution_0_rpr.pdb.outCR  15_RNAComposerAS2_2_rpr.pdb.outCR  0.777    0.77       0.842   0.707    1       0.708   0.5      1
15_solution_0_rpr.pdb.outCR  15_SimRNAAS2_8_rpr.pdb.outCR       0.775    0.791      0.809   0.447    0.941   0.696   0.5      0.4
15_solution_0_rpr.pdb.outCR  15_RW2DAS1_6_rpr.pdb.outCR         0.768    0.779      0.827   0.289    0.941   0.727   0.25     0.333
15_solution_0_rpr.pdb.outCR  15_RW2DAS1_7_rpr.pdb.outCR         0.766    0.77       0.827   0.447    0.941   0.727   0.5      0.4
15_solution_0_rpr.pdb.outCR  15_Adamiak_6_rpr.pdb.outCR         0.765    0.762      0.86    0.354    1       0.739   0.25     0.5
15_solution_0_rpr.pdb.outCR  15_RW2DAS1_5_rpr.pdb.outCR         0.763    0.773      0.809   0.447    0.941   0.696   0.5      0.4
15_solution_0_rpr.pdb.outCR  15_RW2DAS2_6_rpr.pdb.outCR         0.763    0.779      0.809   0.408    0.941   0.696   0.5      0.333
15_solution_0_rpr.pdb.outCR  15_RW2DAS2_2_rpr.pdb.outCR         0.76     0.77       0.792   0.5      0.941   0.667   0.5      0.5
15_solution_0_rpr.pdb.outCR  15_SimRNAAS2_2_rpr.pdb.outCR       0.757    0.777      0.792   0.25     0.941   0.667   0.25     0.25
15_solution_0_rpr.pdb.outCR  15_RW2DAS1_9_rpr.pdb.outCR         0.756    0.77       0.827   0.378    0.941   0.727   0.5      0.286
15_solution_0_rpr.pdb.outCR  15_RW2DAS2_7_rpr.pdb.outCR         0.756    0.764      0.809   0.447    0.941   0.696   0.5      0.4
15_solution_0_rpr.pdb.outCR  15_RW2DAS1_2_rpr.pdb.outCR         0.752    0.751      0.827   0.354    0.941   0.727   0.25     0.5
15_solution_0_rpr.pdb.outCR  15_Chen_6_rpr.pdb.outCR            0.751    0.753      0.827   0.354    0.941   0.727   0.25     0.5
15_solution_0_rpr.pdb.outCR  15_Adamiak_9_rpr.pdb.outCR         0.749    0.723      0.86    0.707    1       0.739   0.5      1
15_solution_0_rpr.pdb.outCR  15_SimRNAAS2_6_rpr.pdb.outCR       0.749    0.77       0.809   0.224    0.941   0.696   0.25     0.2
15_solution_0_rpr.pdb.outCR  15_SimRNAAS2_3_rpr.pdb.outCR       0.749    0.748      0.809   0.5      0.941   0.696   0.5      0.5
15_solution_0_rpr.pdb.outCR  15_RW2DAS2_5_rpr.pdb.outCR         0.745    0.748      0.809   0.447    0.941   0.696   0.5      0.4
15_solution_0_rpr.pdb.outCR  15_RW2DAS1_3_rpr.pdb.outCR         0.743    0.741      0.809   0.5      0.941   0.696   0.5      0.5
15_solution_0_rpr.pdb.outCR  15_RW2DAS2_8_rpr.pdb.outCR         0.742    0.739      0.809   0.5      0.941   0.696   0.5      0.5
15_solution_0_rpr.pdb.outCR  15_SimRNAAS2_4_rpr.pdb.outCR       0.742    0.751      0.809   0.408    0.941   0.696   0.5      0.333
15_solution_0_rpr.pdb.outCR  15_SimRNAAS2_9_rpr.pdb.outCR       0.741    0.743      0.847   0.378    0.941   0.762   0.5      0.286
15_solution_0_rpr.pdb.outCR  15_RW2DAS1_10_rpr.pdb.outCR        0.74     0.746      0.827   0.378    0.941   0.727   0.5      0.286
15_solution_0_rpr.pdb.outCR  15_Chen_7_rpr.pdb.outCR            0.739    0.753      0.827   0        0.941   0.727   0        0
15_solution_0_rpr.pdb.outCR  15_SimRNAAS1_10_rpr.pdb.outCR      0.739    0.779      0.693   0.447    0.824   0.583   0.5      0.4
15_solution_0_rpr.pdb.outCR  15_RW2DAS1_4_rpr.pdb.outCR         0.738    0.745      0.827   0.378    0.941   0.727   0.5      0.286
15_solution_0_rpr.pdb.outCR  15_Chen_8_rpr.pdb.outCR            0.734    0.741      0.779   0.354    0.824   0.737   0.25     0.5
15_solution_0_rpr.pdb.outCR  15_RW2DAS2_4_rpr.pdb.outCR         0.734    0.763      0.809   0.189    0.941   0.696   0.25     0.143
15_solution_0_rpr.pdb.outCR  15_SimRNAAS2_7_rpr.pdb.outCR       0.733    0.731      0.809   0.447    0.941   0.696   0.5      0.4
15_solution_0_rpr.pdb.outCR  15_SimRNAAS1_1_rpr.pdb.outCR       0.73     0.737      0.809   0.25     0.941   0.696   0.25     0.25
15_solution_0_rpr.pdb.outCR  15_SimRNAAS2_1_rpr.pdb.outCR       0.73     0.735      0.827   0.378    0.941   0.727   0.5      0.286
15_solution_0_rpr.pdb.outCR  15_SimRNAAS2_5_rpr.pdb.outCR       0.73     0.735      0.809   0.408    0.941   0.696   0.5      0.333
15_solution_0_rpr.pdb.outCR  15_RW2DAS2_3_rpr.pdb.outCR         0.728    0.739      0.809   0.354    0.941   0.696   0.5      0.25
15_solution_0_rpr.pdb.outCR  15_Adamiak_1_rpr.pdb.outCR         0.726    0.721      0.794   0.577    0.882   0.714   0.5      0.667
15_solution_0_rpr.pdb.outCR  15_RW2DAS1_8_rpr.pdb.outCR         0.725    0.73       0.809   0.378    0.941   0.696   0.5      0.286
15_solution_0_rpr.pdb.outCR  15_SimRNAAS1_9_rpr.pdb.outCR       0.724    0.735      0.741   0.5      0.824   0.667   0.5      0.5
15_solution_0_rpr.pdb.outCR  15_SimRNAAS2_10_rpr.pdb.outCR      0.719    0.722      0.809   0.25     0.941   0.696   0.25     0.25
15_solution_0_rpr.pdb.outCR  15_Chen_10_rpr.pdb.outCR           0.714    0.728      0.741   0.354    0.824   0.667   0.25     0.5
15_solution_0_rpr.pdb.outCR  15_SimRNAAS1_8_rpr.pdb.outCR       0.712    0.723      0.724   0.5      0.824   0.636   0.5      0.5
15_solution_0_rpr.pdb.outCR  15_3dRNAAS2_7_rpr.pdb.outCR        0.709    0.7        0.759   0.707    0.824   0.7     0.5      1
15_solution_0_rpr.pdb.outCR  15_3dRNAAS2_6_rpr.pdb.outCR        0.701    0.689      0.759   0.707    0.824   0.7     0.5      1
15_solution_0_rpr.pdb.outCR  15_Chen_9_rpr.pdb.outCR            0.701    0.701      0.765   0.354    0.765   0.765   0.25     0.5
15_solution_0_rpr.pdb.outCR  15_3dRNAAS2_2_rpr.pdb.outCR        0.695    0.681      0.759   0.707    0.824   0.7     0.5      1
15_solution_0_rpr.pdb.outCR  15_3dRNAAS2_4_rpr.pdb.outCR        0.695    0.681      0.759   0.707    0.824   0.7     0.5      1
15_solution_0_rpr.pdb.outCR  15_3dRNAAS2_5_rpr.pdb.outCR        0.695    0.681      0.759   0.707    0.824   0.7     0.5      1
15_solution_0_rpr.pdb.outCR  15_3dRNAAS2_10_rpr.pdb.outCR       0.693    0.679      0.759   0.707    0.824   0.7     0.5      1
15_solution_0_rpr.pdb.outCR  15_3dRNAAS2_1_rpr.pdb.outCR        0.693    0.679      0.759   0.707    0.824   0.7     0.5      1
15_solution_0_rpr.pdb.outCR  15_3dRNAAS2_8_rpr.pdb.outCR        0.693    0.679      0.759   0.707    0.824   0.7     0.5      1
15_solution_0_rpr.pdb.outCR  15_3dRNAAS2_3_rpr.pdb.outCR        0.693    0.679      0.759   0.707    0.824   0.7     0.5      1
15_solution_0_rpr.pdb.outCR  15_3dRNAAS2_9_rpr.pdb.outCR        0.688    0.671      0.759   0.707    0.824   0.7     0.5      1
15_solution_0_rpr.pdb.outCR  15_SimRNAAS1_7_rpr.pdb.outCR       0.682    0.714      0.672   0.25     0.765   0.591   0.25     0.25
15_solution_0_rpr.pdb.outCR  15_SimRNAAS1_5_rpr.pdb.outCR       0.663    0.718      0.556   0.289    0.647   0.478   0.25     0.333
15_solution_0_rpr.pdb.outCR  15_SimRNAAS1_2_rpr.pdb.outCR       0.645    0.697      0.556   0.25     0.647   0.478   0.25     0.25
15_solution_0_rpr.pdb.outCR  15_SimRNAAS1_4_rpr.pdb.outCR       0.588    0.741      0.223   0.158    0.235   0.211   0.25     0.1
15_solution_0_rpr.pdb.outCR  15_SimRNAAS1_6_rpr.pdb.outCR       0.525    0.657      0.114   0.204    0.118   0.111   0.25     0.167
```
