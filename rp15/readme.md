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
