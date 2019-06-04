RNA-Puzzle 12
-----------------------------------------------------------------------------

The solution vs the target sequence provided. Mind the gaps and missing atom `A/21/O6`.

```
> 12_4qln_solution_rpr A:2-16 18-34 39-123
GAUCGCUGAACCCGAAGGGGCGGGGGACCCAGGGGGCGAAUCUCUUCCGAAAGGAAGAGUAGGGUUACUCCUUCGACCCGAGCCCGUCAGCUAACCUCGCAAGCGUCCGAAGGAGAA

> 12_Adamiak_1_rpr A:1-125
GGAUCGCUGAACCCGAAAGGGGCGGGGGACCCAGAAAUGGGGCGAAUCUCUUCCGAAAGGAAGAGUAGGGUUACUCCUUCGACCCGAGCCCGUCAGCUAACCUCGCAAGCGUCCGAAGGAGAAUC

```

```
 -GAUCGCUGAACCCGAA-GGGGCGGGGGACCCAG----GGGGCGAAUCUCUUCCGAAAGGAAGAGUAGGGUUACUCCUUCGACCCGAGCCCGUCAGCUAACCUCGCAAGCGUCCGAAGGAGAA-- # 4qln_solution A:2-16 18-34 39-123
 GGAUCGCUGAACCCGAAAGGGGCGGGGGACCCAGAAAUGGGGCGAAUCUCUUCCGAAAGGAAGAGUAGGGUUACUCCUUCGACCCGAGCCCGUCAGCUAACCUCGCAAGCGUCCGAAGGAGAAUC # A 1-125
```

Manually:

- The Das lab added AAAA as a ligand. It was removed for these rpr files.
- Atoms of some residues had 'Alternate location indicator'. It was kept only `A`, e.g:

		ATOM    474  N2 A  G A  20      -1.838 -51.308 -33.038  0.61 80.31           N ## this was kept
		ATOM    475  N2 B  G A  20       5.260 -49.743 -36.405  0.39 84.44           N

seq.txt:

	for i in `ls *.pdb`; do rna_pdb_tools.py --get_seq $i; echo ''; done > seq.txt

rpr-ing:

	for i in `ls *.pdb`; do rna_pdb_tools.py --get_rnapuzzle_ready $i > ${i/.pdb/_rpr.pdb}; done
	for i in `ls *Chen*`; do rna_pdb_tools.py --edit 'X:1-125>A:1-125' $i > ${i}_temp; mv ${i}_temp ${i}; done
	for i in `ls *Bujnicki*`; do rna_pdb_tools.py --edit 'R:1-125>A:1-125' $i > ${i}_temp; mv ${i}_temp ${i}; done

rmsds.csv

    [mm] rp12$ git:(master) ✗ rna_calc_rmsd.py -t 12_4qln_solution_rpr.pdb --target_selection A:2-16+34+39-123 --model_selection A:2-16+34+39-123 *.pdb
    method: all-atom-built-in
    # of models: 52
    12_4qln_solution_rpr.pdb 0.0 2162
    12_Adamiak_1_rpr.pdb 15.65 2162
    12_Adamiak_2_rpr.pdb 14.37 2162
    12_Adamiak_3_rpr.pdb 14.27 2162
    12_Bujnicki_1_rpr.pdb 21.35 2162
    12_Bujnicki_2_rpr.pdb 18.52 2162
    12_Bujnicki_3_rpr.pdb 10.82 2162
    12_Bujnicki_4_rpr.pdb 14.7 2162
    12_Bujnicki_5_rpr.pdb 12.06 2162
    12_Bujnicki_6_rpr.pdb 14.21 2162
    12_Bujnicki_7_rpr.pdb 14.41 2162
    12_Bujnicki_8_rpr.pdb 10.59 2162
    12_Bujnicki_9_rpr.pdb 13.11 2162
    12_Bujnicki_10_rpr.pdb 12.73 2162
    12_Chen_1_rpr.pdb 21.55 2162
    12_Chen_2_rpr.pdb 18.67 2162
    12_Chen_3_rpr.pdb 18.9 2162
    12_Chen_4_rpr.pdb 15.8 2162
    12_Chen_5_rpr.pdb 19.17 2162
    12_Chen_6_rpr.pdb 19.62 2162
    12_Chen_7_rpr.pdb 19.61 2162
    12_Chen_8_rpr.pdb 17.65 2162
    12_Chen_9_rpr.pdb 18.3 2162
    12_Chen_10_rpr.pdb 19.83 2162
    12_Das_1_rpr.pdb 13.42 2162
    12_Das_2_rpr.pdb 12.78 2162
    12_Das_3_rpr.pdb 13.5 2162
    12_Das_4_rpr.pdb 17.27 2162
    12_Das_5_rpr.pdb 13.69 2162
    12_Das_6_rpr.pdb 13.15 2162
    12_Das_7_rpr.pdb 12.28 2162
    12_Das_8_rpr.pdb 12.26 2162
    12_Das_9_rpr.pdb 13.15 2162
    12_Das_10_rpr.pdb 17.11 2162
    12_Ding_1_rpr.pdb 12.53 2162
    12_Ding_2_rpr.pdb 19.69 2162
    12_Ding_3_rpr.pdb 16.35 2162
    12_Ding_4_rpr.pdb 12.88 2162
    12_Ding_5_rpr.pdb 20.58 2162
    12_Ding_6_rpr.pdb 14.87 2162
    12_Ding_7_rpr.pdb 17.1 2162
    12_Ding_8_rpr.pdb 12.54 2162
    12_Ding_9_rpr.pdb 14.09 2162
    12_Ding_10_rpr.pdb 17.3 2162
    12_Ding_11_rpr.pdb 9.49 2162
    12_Ding_12_rpr.pdb 9.82 2162
    12_Kevin_1_rpr.pdb 20.45 2162
    12_Kevin_2_rpr.pdb 20.25 2162
    12_Kevin_3_rpr.pdb 19.96 2162
    12_Xiao_1_rpr.pdb 30.68 2162
    12_Xiao_2_rpr.pdb 30.05 2162
    12_Xiao_3_rpr.pdb 35.92 2162
    # of atoms used: 2162
    csv was created!  rmsds.csv
    	
Reference:

Crystal structure kindly provided by Dinshaw Patel
Ren A, Patel DJ. 2014. c-di-AMP binds the ydaO riboswitch in two pseudo-symmetry-related pockets. Nat Chem Biol. 10(9):780-6.
