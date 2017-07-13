RNA-Puzzle 17
-----------------------------------------------------------------------------

Solution sequence vs target sequence:

```
CGUGGUUAGGGCCACGUUAAAUAGUUGCUUAAGCCCUAAGCGUUGAU----AUCAGGUGCAA # solution
CGUGGUUAGGGCCACGUUAAAUAGUUGCUUAAGCCCUAAGCGUUGAUAAAUAUCAGGUGCAA # target seq
```

```
> 17_5k7c_solution_rpr A:1-47 52-62
CGUGGUUAGGGCCACGUUAAAUAGUUGCUUAAGCCCUAAGCGUUGAUAUCAGGUGCAA

> 17_Adamiak_1_rpr A:1-62
CGUGGUUAGGGCCACGUUAAAUAGUUGCUUAAGCCCUAAGCGUUGAUAAAUAUCAGGUGCAA
```

Added missing O2' (this is deoxyribonucleoside) to the solution.

```
head 17_5k7c_solution_rpr.pdb
HEADER Generated with rna-pdb-tools
HEADER ver ea5e310-dirty
HEADER https://github.com/mmagnus/rna-pdb-tools
HEADER Tue May 16 11:43:45 2017
REMARK 000 Fixed atoms/residues:
REMARK 000 -  add O2'  in chain: A <Residue G het=  resseq=57 icode= > residue # 53
ATOM      1  P     C A   1     -29.720 -19.750   3.190  1.00183.16           P
```

Edits:

	for i in `ls *.pdb`; do rna_pdb_tools.py --get_rnapuzzle_ready $i > ${i/.pdb/_rpr.pdb}; done

Rmsd:

	rna_calc_rmsd.py -t 17_5k7c_solution_rpr.pdb --target_selection A:1-47+52-62 --model_selection A:1-47+52-62 *.pdb
