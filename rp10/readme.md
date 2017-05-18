RNA-Puzzle 10
-----------------------------------------------------------------------------

```
> 10_0_solution_4LCK_rpr A:1-96
UGCGAUGAGAAGAAGAGUAUUAAGGAUUUACUAUGAUUAGCGACUCUAGGAUAGUGAAAGCUAGAGGAUAGUAACCUUAAGAAGGCACUUCGAGCA
> 10_0_solution_4LCK_rpr B:5-67
GAGUAGUUCAGUGGUAGAACACCACCUUGCCAAGGUGGGGGUCGCGGGUUCGAAUCCCGUCUC

> 10_BUJNICKI_10_rpr A:1-96
UGCGAUGAGAAGAAGAGUAUUAAGGAUUUACUAUGAUUAGCGACUCUAGGAUAGUGAAAGCUAGAGGAUAGUAACCUUAAGAAGGCACUUCGAGCA
> 10_BUJNICKI_10_rpr B:1-75
GCGGAAGUAGUUCAGUGGUAGAACACCACCUUGCCAAGGUGGGGGUCGCGGGUUCGAAUCCCGUCUUCCGCUCCA
```

t-box
```
---UGCGAUGAGAAGAAGAGUAUUAAGGAUUUACUAUGAUUAGCGACUCUAGGAUAGUGAAAGCUAGAGGAUAGUAACCUUAAGAAGGCACUUCGAGCA # target
GGGUGCGAUGAGAAGAAGAGUAUUAAGGAUUUACUAUGAUUAGCGACUCUAGGAUAGUGAAAGCUAGAGGAUAGUAACCUUAAGAAGGCACUUCGAGCACCC # native
xxx                                                                                                xxx # trimmed new native
(((                                                                                                )))
```

t-rna

```
 ----GAGUAGUUCAGUGGUAGAACACCACCUUGCCAAGGUGGGGGUCGCGGGUUCGAAUCCCGUCUCGGGCGAAAGCCC # B # native
     (((..((((....{..)))).(((((..[[[..))))).....(((((..}....))))))))((((....))))
 GCGGAAGUAGUUCAGUGGUAGAACACCACCUUGCCAAGGUGGGGGUCGCGGGUUCGAAUCCCGUCUUCCGCUCCA---- # model
 ....(((..((((.......)))).(((...........)))......((((.......)))).)))........
     (((..((((.......)))).(((...........)))......((((.......)))).)))........
 ----x                                                             xxxxxxxxxxxxx # xtrimmed
      6                                                           66
```

Manual: Bujnicki swap chains.

Rmsd:

```
rna_calc_rmsd.py -t 10_0_solution_4LCK_rpr.pdb --target_selection 'A:1-96+B:6-67' --model_selection 'A:1-96+B:6-67' *.pdb
rmsd_calc_rmsd_to_target
--------------------------------------------------------------------------------
method: all-atom-built-in
# of models: 27
10_0_solution_4LCK_rpr.pdb 0.0 3392
10_BUJNICKI_1_rpr.pdb 10.15 3392
10_BUJNICKI_2_rpr.pdb 10.36 3392
10_BUJNICKI_3_rpr.pdb 10.34 3392
10_BUJNICKI_4_rpr.pdb 9.31 3392
10_BUJNICKI_5_rpr.pdb 10.24 3392
10_BUJNICKI_6_rpr.pdb 10.33 3392
10_BUJNICKI_7_rpr.pdb 10.21 3392
10_BUJNICKI_8_rpr.pdb 10.16 3392
10_BUJNICKI_9_rpr.pdb 10.32 3392
10_BUJNICKI_10_rpr.pdb 10.36 3392
10_CHEN_1_rpr.pdb 11.3 3392
10_DAS_1_rpr.pdb 7.61 3392
10_DAS_2_rpr.pdb 10.5 3392
10_DAS_3_rpr.pdb 6.85 3392
10_DAS_4_rpr.pdb 7.1 3392
10_DAS_5_rpr.pdb 10.46 3392
10_DING_1_rpr.pdb 13.14 3392
10_DING_2_rpr.pdb 14.02 3392
10_DING_3_rpr.pdb 12.48 3392
10_DING_4_rpr.pdb 13.33 3392
10_DING_5_rpr.pdb 16.7 3392
10_DING_6_rpr.pdb 17.4 3392
10_DING_7_rpr.pdb 16.22 3392
10_DING_8_rpr.pdb 15.53 3392
10_DING_9_rpr.pdb 16.65 3392
10_DING_10_rpr.pdb 13.18 3392
# of atoms used: 3392
csv was created!  rmsds.csv
```
