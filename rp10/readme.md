RNA-Puzzle 10
-----------------------------------------------------------------------------

Solution sequence vs target sequence:

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
GGGUGCGAUGAGAAGAAGAGUAUUAAGGAUUUACUAUGAUUAGCGACUCUAGGAUAGUGAAAGCUAGAGGAUAGUAACCUUAAGAAGGCACUUCGAGCACCC # solution
xxx                                                                                                xxx # trimmed the new solution
(((                                                                                                )))
```

t-rna

```
 ----GAGUAGUUCAGUGGUAGAACACCACCUUGCCAAGGUGGGGGUCGCGGGUUCGAAUCCCGUCUCGGGCGAAAGCCC # B # solution
     (((..((((....{..)))).(((((..[[[..))))).....(((((..}....))))))))((((....))))
 GCGGAAGUAGUUCAGUGGUAGAACACCACCUUGCCAAGGUGGGGGUCGCGGGUUCGAAUCCCGUCUUCCGCUCCA---- # model
 ....(((..((((.......)))).(((...........)))......((((.......)))).)))........
     (((..((((.......)))).(((...........)))......((((.......)))).)))........
 ----x                                                             xxxxxxxxxxxxx # xtrimmed the new solution
      6                                                           66
```

Manual: Bujnicki swap chains.

In some cases it important to keep structure exactly the same as the solution. In trimmed_models models, you can find structure that have only parts that are in common between the models and the solution.

	rna_pdb_tools.py --delete B:1-5 --inplace *.pdb
	rna_pdb_tools.py --delete B:67-75 --inplace *.pdb	
	rna_pdb_tools.py --get_seq *.pdb > seqs.txt

Calculate Interaction Network Fidelity (INF) etc using ClaRNA.
	
	$ trimmed_models$ rna_calc_inf.py -t 10_0_solution_4LCK_rpr.pdb *.pdb
	mv inf.csv ../

Calculate Rmsd:

```
rna_calc_rmsd.py -t 10_solution_0_rpr.pdb --target-selection 'A:1-96+B:6-66' --model-selection 'A:1-96+B:6-66' *.pdb -pr -sr # 201114
# method: all-atom-built-in
# of models: 27
# of atoms used: 3372
                         fn  rmsd_all
26    10_solution_0_rpr.pdb      0.00
13         10_Das_3_rpr.pdb      6.84
14         10_Das_4_rpr.pdb      7.08
11         10_Das_1_rpr.pdb      7.61
3     10_Bujnicki_4_rpr.pdb      9.33
0     10_Bujnicki_1_rpr.pdb     10.17
7     10_Bujnicki_8_rpr.pdb     10.19
6     10_Bujnicki_7_rpr.pdb     10.24
4     10_Bujnicki_5_rpr.pdb     10.27
8     10_Bujnicki_9_rpr.pdb     10.35
5     10_Bujnicki_6_rpr.pdb     10.35
2     10_Bujnicki_3_rpr.pdb     10.37
1     10_Bujnicki_2_rpr.pdb     10.38
9    10_Bujnicki_10_rpr.pdb     10.39
15         10_Das_5_rpr.pdb     10.45
12         10_Das_2_rpr.pdb     10.50
10        10_Chen_1_rpr.pdb     11.33
18   10_Dokholyan_3_rpr.pdb     12.50
16   10_Dokholyan_1_rpr.pdb     13.15
25  10_Dokholyan_10_rpr.pdb     13.19
19   10_Dokholyan_4_rpr.pdb     13.35
17   10_Dokholyan_2_rpr.pdb     14.01
23   10_Dokholyan_8_rpr.pdb     15.57
22   10_Dokholyan_7_rpr.pdb     16.25
24   10_Dokholyan_9_rpr.pdb     16.66
20   10_Dokholyan_5_rpr.pdb     16.73
21   10_Dokholyan_6_rpr.pdb     17.42
csv was created!  rmsds.csv
```
