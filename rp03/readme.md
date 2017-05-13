RNA-Puzzle 03 
-----------------------------------------------------------------------------

```
> 3_solution_0_rpr A:1-84
CUCUGGAGAGAACCGUUUAAUCGGUCGCCGAAGGAGCAAGCUCUGCGGAAACGCAGAGUGAAACUCUCAGGCAAAAGGACAGAG

> 3_bujnicki_1_rpr A:1-84
CUCUGGAGAGAACCGUUUAAUCGGUCGCCGAAGGAGCAAGCUCUGCGCAUAUGCAGAGUGAAACUCUCAGGCAAAAGGACAGAG
```

rpr:

	for i in `ls *.pdb`; do rna_pdb_tools.py --get_rnapuzzle_ready $i > ${i/.pdb/_rpr.pdb}; done
