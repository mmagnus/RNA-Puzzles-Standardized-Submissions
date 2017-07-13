RNA-Puzzle 14 (free)
-----------------------------------------------------------------------------

Solution sequence vs target sequence - mind the gap in the solution.

```
> 14_5ddo_free_solution_rpr A:1-21 25-61
CGUUGGCCCAGGAAACUGGGUAGUAAGGUCCAUUGCACUCCGGGCCUGAAGCAACGCU

> 14_BujnickiPostExp_1_rpr A:1-61
CGUUGGCCCAGGAAACUGGGUGGAAGUAAGGCCCAUUGCACUCCGGGCCUGAAGCAACGCU
```

rpr:

	for i in `ls *.pdb`; do rna_pdb_tools.py --get_rnapuzzle_ready $i > ${i/.pdb/_rpr.pdb}; done

rmsd:

	rna_calc_rmsd.py -t 14_5ddo_free_solution_rpr.pdb --target_selection A:1-21+25-61 --model_selection A:1-21+25-61 rpr/*.pdb
