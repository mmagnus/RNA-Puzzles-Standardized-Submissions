RNA-Puzzle 04
-----------------------------------------------------------------------------

Solution sequence vs target sequenece:

```
> 4_0_solution_3V7E_rpr C:1-126
GGCUUAUCAAGAGAGGUGGAGGGACUGGCCCGAUGAAACCCGGCAACCACUAGUCUAGCGUCAGCUUCGGCUGACGCUAGGCUAGUGGUGCCAAUUCCUGCAGCGGAAACGUUGAAAGAUGAGCCA

> 4_adamiak_1_rpr A:1-126
GGCUUAUCAAGAGAGGUGGAGGGACUGGCCCGAUGAAACCCGGCAACCACUAGUCUAGCGUCAGCUUCGGCUGACGCUAGGCUAGUGGUGCCAAUUCCUGCAGCGGAAACGUUGAAAGAUGAGCCA
```

The solution:

- SAM and heteroatoms are removed

Edits:
	
	for i in `ls *das*`; do rna_pdb_tools.py --edit 'B:1-126>A:1-126' $i > ${i}_temp; mv ${i}_temp ${i}; done
	for i in `ls *major*`; do rna_pdb_tools.py --edit 'B:1-126>A:1-126' $i > ${i}_temp; mv ${i}_temp ${i}; done
	for i in `ls *flores*`; do rna_pdb_tools.py --edit 'R:1-125>A:1-125' $i > ${i}_temp; mv ${i}_temp ${i}; done

Problem, shorten by one residue at the end. The 4_flores_1_rpr.pdb is moved to `problem`.

```
> 4_flores_1_rpr R:1-125
GGCUUAUCAAGAGAGGUGGAGGGACUGGCCCGAUGAAACCCGGCAACCACUAGUCUAGCGUCAGCUUCGGCUGACGCUAGGCUAGUGGUGCCAAUUCCUGCAGCGGAAACGUUGAAAGAUGAGCC
```

Rmsd:

```
rna_calc_rmsd.py -t 4_0_solution_3V7E_rpr.pdb *.pdb
rmsd_calc_rmsd_to_target
--------------------------------------------------------------------------------
 method:
# of models: 31
4_0_solution_3V7E_rpr.pdb 9.11688807516e-15 2704
4_adamiak_1_rpr.pdb 4.71842825441 2704
4_adamiak_2_rpr.pdb 4.4908548348 2704
4_adamiak_3_rpr.pdb 4.34462048886 2704
4_adamiak_4_rpr.pdb 6.63599823712 2704
4_adamiak_5_rpr.pdb 4.67585242803 2704
4_bujnicki_1_rpr.pdb 4.20178771468 2704
4_bujnicki_2_rpr.pdb 4.20280913519 2704
4_bujnicki_3_rpr.pdb 4.20827935533 2704
4_bujnicki_4_rpr.pdb 4.20282385597 2704
4_bujnicki_5_rpr.pdb 4.2014420225 2704
4_chen_1_rpr.pdb 3.3580269932 2704
4_chen_2_rpr.pdb 3.35208512141 2704
4_chen_3_rpr.pdb 3.37360883454 2704
4_chen_4_rpr.pdb 3.37164129151 2704
4_chen_5_rpr.pdb 3.3723207656 2704
4_chen_6_rpr.pdb 3.37562832004 2704
4_chen_7_rpr.pdb 3.3689109109 2704
4_chen_8_rpr.pdb 3.36412382731 2704
4_chen_9_rpr.pdb 3.35569334869 2704
4_chen_10_rpr.pdb 3.35699671339 2704
4_das_1_rpr.pdb 4.51083489564 2704
4_das_2_rpr.pdb 4.51122310508 2704
4_das_3_rpr.pdb 4.51111514072 2704
4_das_4_rpr.pdb 4.51115390587 2704
4_das_5_rpr.pdb 4.51122310508 2704
4_dokholyan_1_rpr.pdb 5.37162966166 2704
4_dokholyan_2_rpr.pdb 5.37162966166 2704
4_major_1_rpr.pdb 4.51415839881 2704
4_mikolajczak_1_rpr.pdb 12.7839985801 2704
4_santalucia_1_rpr.pdb 4.12387383462 2704
# of atoms used: 2704
csv was created!  rmsds.csv
```
