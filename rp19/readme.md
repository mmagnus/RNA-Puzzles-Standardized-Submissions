RNA-Puzzle 19
-----------------------------------------------------------------------------

```
> 19_5t5a_solution_0_rpr A:1-40
GCAGGGCAAGGCCCAGUCCCGUGCAAGCCGGGACCGCCCC
> 19_5t5a_solution_0_rpr B:1-22
GGGGCGCGGCGCUCAUUCCUGC

> 19_3dRNA_5_rpr A:1-40
GCAGGGCAAGGCCCAGUCCCGUGCAAGCCGGGACCGCCCC
> 19_3dRNA_5_rpr B:1-22
GGGGCGCGGCGCUCAUUCCUGC
```

Added missing O2' (this is deoxyribonucleoside) to the native. Split the native into chain A and B, like the models.

```
HEADER Generated with rna-pdb-tools
HEADER ver ea5e310-dirty 
HEADER https://github.com/mmagnus/rna-pdb-tools 
HEADER Mon May 15 20:18:25 2017
REMARK 000 Fixed atoms/residues:
REMARK 000 -  add O2'  in chain: B <Residue C het=  resseq=14 icode= > residue # 14
ATOM      1  P     G A   1      15.776  12.040  56.861  1.00 11.89           P
```

Edits:

	for i in `ls *.pdb`; do rna_pdb_tools.py --get_rnapuzzle_ready $i > ${i/.pdb/_rpr.pdb}; done
	for i in `ls *RW3D*`; do rna_pdb_tools.py --edit 'A:41-62>B:1-22' $i > ${i}_temp; mv ${i}_temp ${i}; done
	for i in `ls *.pdb`; do rna_pdb_tools.py --get_seq $i; echo ''; done > seqs.txt

Rmsd:

    rna_calc_rmsd.py -t 19_5t5a_solution_0_rpr.pdb *.pdb
    rmsd_calc_rmsd_to_target
    --------------------------------------------------------------------------------
     method:
    # of models: 55
    19_3dRNA_1_rpr.pdb 15.0576357383 1325
    19_3dRNA_2_rpr.pdb 13.248453618 1325
