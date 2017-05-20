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
xxx                                                                                                xxx # trimmed the new native
(((                                                                                                )))
```

t-rna

```
 ----GAGUAGUUCAGUGGUAGAACACCACCUUGCCAAGGUGGGGGUCGCGGGUUCGAAUCCCGUCUCGGGCGAAAGCCC # B # native
     (((..((((....{..)))).(((((..[[[..))))).....(((((..}....))))))))((((....))))
 GCGGAAGUAGUUCAGUGGUAGAACACCACCUUGCCAAGGUGGGGGUCGCGGGUUCGAAUCCCGUCUUCCGCUCCA---- # model
 ....(((..((((.......)))).(((...........)))......((((.......)))).)))........
     (((..((((.......)))).(((...........)))......((((.......)))).)))........
 ----x                                                             xxxxxxxxxxxxx # xtrimmed the new native
      6                                                           66
```

Manual: Bujnicki swap chains.

In some cases it important to keep structure exactly the same as the native. In trimmed_models models, you can find structure that have only parts that are in common between the models and the native.

	rna_pdb_tools.py --delete B:1-5 --inplace *.pdb
	rna_pdb_tools.py --delete B:67-75 --inplace *.pdb	
	rna_pdb_tools.py --get_seq *.pdb > seqs.txt

Calculate Interaction Network Fidelity (INF) etc using ClaRNA.
	
	$ trimmed_models$ rna_calc_inf.py -t 10_0_solution_4LCK_rpr.pdb *.pdb
	mv inf.csv ../

Calculate Rmsd:

```
rna_calc_rmsd.py -t 10_0_solution_4LCK_rpr.pdb --target_selection 'A:1-96+B:6-66' --model_selection 'A:1-96+B:6-66' *.pdb
rmsd_calc_rmsd_to_target
--------------------------------------------------------------------------------
method: all-atom-built-in
# of models: 27
10_0_solution_4LCK_rpr.pdb 0.0 3372
10_BUJNICKI_1_rpr.pdb 10.17 3372
10_BUJNICKI_2_rpr.pdb 10.38 3372
10_BUJNICKI_3_rpr.pdb 10.37 3372
10_BUJNICKI_4_rpr.pdb 9.33 3372
10_BUJNICKI_5_rpr.pdb 10.27 3372
10_BUJNICKI_6_rpr.pdb 10.35 3372
10_BUJNICKI_7_rpr.pdb 10.24 3372
10_BUJNICKI_8_rpr.pdb 10.19 3372
10_BUJNICKI_9_rpr.pdb 10.35 3372
10_BUJNICKI_10_rpr.pdb 10.39 3372
10_CHEN_1_rpr.pdb 11.33 3372
10_DAS_1_rpr.pdb 7.61 3372
10_DAS_2_rpr.pdb 10.5 3372
10_DAS_3_rpr.pdb 6.84 3372
10_DAS_4_rpr.pdb 7.08 3372
10_DAS_5_rpr.pdb 10.45 3372
10_DING_1_rpr.pdb 13.15 3372
10_DING_2_rpr.pdb 14.01 3372
10_DING_3_rpr.pdb 12.5 3372
10_DING_4_rpr.pdb 13.35 3372
10_DING_5_rpr.pdb 16.73 3372
10_DING_6_rpr.pdb 17.42 3372
10_DING_7_rpr.pdb 16.25 3372
10_DING_8_rpr.pdb 15.57 3372
10_DING_9_rpr.pdb 16.66 3372
10_DING_10_rpr.pdb 13.19 3372
# of atoms used: 3372
csv was created!  rmsds.csv
```
