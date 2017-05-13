RNA-Puzzle 14 (bound)
-----------------------------------------------------------------------------

```
> 14_5ddp_bound_solution_rpr A:1-61
CGUUGACCCAGGAAACUGGGCGGAAGUAAGGUCCAUUGCACUCCGGGCCUGAAGCAACGCG

> 14_AdamiakPostExp_1_rpr A:1-61
CGUUGACCCAGGAAACUGGGCGGAAGUAAGGCCCAUUGCACUCCGGGCCUGAAGCAACGCG
```

Manual:

- remove a protein from `14_BujnickiPostExp_1_rpr.pdb`

rpr:

	for i in `ls *.pdb`; do rna_pdb_tools.py --get_rnapuzzle_ready $i > ${i/.pdb/_rpr.pdb}; done

rmsd:

    rna_calc_rmsd.py -t rp14_5ddp_bound_solution_rpr.pdb rpr/*.pdb
