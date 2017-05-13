RNA-Puzzle 12
-----------------------------------------------------------------------------

The natives vs the target sequence provided. Mind the gaps and missing atom `A/21/O6`.

```
> 12_4qln_solution_rpr A:2-16 18-34 39-123
GAUCGCUGAACCCGAAGGGGCGGGGGACCCAGGGGGCGAAUCUCUUCCGAAAGGAAGAGUAGGGUUACUCCUUCGACCCGAGCCCGUCAGCUAACCUCGCAAGCGUCCGAAGGAGAA

> 12_Adamiak_1_rpr A:1-125
GGAUCGCUGAACCCGAAAGGGGCGGGGGACCCAGAAAUGGGGCGAAUCUCUUCCGAAAGGAAGAGUAGGGUUACUCCUUCGACCCGAGCCCGUCAGCUAACCUCGCAAGCGUCCGAAGGAGAAUC

```

```
-GAUCGCUGAACCCGAA-GGGGCGGGGGACCCAGGGGGCG----AAUCUCUUCCGAAAGGAAGAGUAGGGUUACUCCUUCGACCCGAGCCCGUCAGCUAACCUCGCAAGCGUCCGAAGGAGAA-- # 4qln_solution A:2-16 18-34 39-123
GGAUCGCUGAACCCGAAAGGGGCGGGGGACCCAGAAAUGGGGCGAAUCUCUUCCGAAAGGAAGAGUAGGGUUACUCCUUCGACCCGAGCCCGUCAGCUAACCUCGCAAGCGUCCGAAGGAGAAUC # A 1-125
```

Manually:

- The Das lab added AAAA as a lignad. It was removed for these rpr files.
- Atoms of some residues had 'Alternate location indicator'. It was kept only `A`, e.g:

		ATOM    474  N2 A  G A  20      -1.838 -51.308 -33.038  0.61 80.31           N ## this was kept
		ATOM    475  N2 B  G A  20       5.260 -49.743 -36.405  0.39 84.44           N

seq.txt:

	for i in `ls *.pdb`; do rna_pdb_tools.py --get_seq $i; echo ''; done > seq.txt

rmsds.csv

	rna_calc_rmsd.py -t 4qln_solution_rpr.pdb --target_selection A:2-16+34+39-123 --model_selection A:2-16+34+39-123 rpr/*.pdb
	
rpr-ing:

	for i in `ls *.pdb`; do rna_pdb_tools.py --get_rnapuzzle_ready $i > ${i/.pdb/_rpr.pdb}; done
	for i in `ls *Chen*`; do rna_pdb_tools.py --edit 'X:1-125>A:1-125' $i > ${i}_temp; mv ${i}_temp ${i}; done
	for i in `ls *Bujnicki*`; do rna_pdb_tools.py --edit 'R:1-125>A:1-125' $i > ${i}_temp; mv ${i}_temp ${i}; done

Reference:

Crystal structure kindly provided by Dinshaw Patel
Ren A, Patel DJ. 2014. c-di-AMP binds the ydaO riboswitch in two pseudo-symmetry-related pockets. Nat Chem Biol. 10(9):780-6.
