RNA-Puzzle 14 (bound)
-----------------------------------------------------------------------------

Solution sequence vs target sequence:

```
> 14_5ddp_bound_solution_rpr A:1-61
CGUUGACCCAGGAAACUGGGCGGAAGUAAGGUCCAUUGCACUCCGGGCCUGAAGCAACGCG

> 14_AdamiakPostExp_1_rpr A:1-61
CGUUGACCCAGGAAACUGGGCGGAAGUAAGGCCCAUUGCACUCCGGGCCUGAAGCAACGCG
```

Manual:

- remove a protein from `14_BujnickiPostExp_1_rpr.pdb`

The Bujnicki group submitted modified sequence (see the Bujnicki folder):

```
CGUUGACCCAGGAAACUGGGCGGAAGUAAGGUCCAUUGCACUCCGGGCCUGAAGCAACGCG # solution/target
||||..|||||||||||||||||||||||||.|||||||||||||||||||||||||||||
CGUUAGCCCAGGAAACUGGGCGGAAGUAAGGCCCAUUGCACUCCGGGCCUGAAGCAACGCG # BujnickiLab_RNApuzzle14_n0[1-4]bound_rpr
```

rpr:


	for i in `ls *.pdb`; do rna_pdb_tools.py --get_rnapuzzle_ready $i > ${i/.pdb/_rpr.pdb}; done

rmsd:

    rna_calc_rmsd.py -t rp14_5ddp_bound_solution_rpr.pdb rpr/*.pdb

