RNA-Puzzle 08
-----------------------------------------------------------------------------

```
> 8_0_solution_4L81_rpr A:1-96
GGAUCACGAGGGGGAGACCCCGGCAACCUGGGACGGACACCCAAGGUGCUCACACCGGAGACGGUGGAUCCGGCCCGAGAGGGCAACGAAGUCCGU

> 8_Adamiak_1_rpr A:1-96
GGAUCACGAGGGGGAGACCCCGGCAACCUGGGACGGACACCCAAGGUGCUCACACCGGAGACGGUGGAUCCGGCCCGAGAGGGCAACGAAGUCCGU
```

Edits:

	for i in `ls *.pdb`; do rna_pdb_tools.py --get_rnapuzzle_ready $i > ${i/.pdb/_rpr.pdb}; done

Rmsd:
	
```
rna_calc_rmsd.py -t 8_0_solution_4L81_rpr.pdb *pdb
rmsd_calc_rmsd_to_target
--------------------------------------------------------------------------------
method: all-atom-built-in
# of models: 43
8_0_solution_4L81_rpr.pdb 0.0 2074
8_Adamiak_1_rpr.pdb 13.9 2074
8_Adamiak_2_rpr.pdb 14.46 2074
8_Bujnicki_1_rpr.pdb 12.27 2074
8_Bujnicki_2_rpr.pdb 11.84 2074
8_Bujnicki_3_rpr.pdb 11.31 2074
8_Bujnicki_4_rpr.pdb 12.17 2074
8_Bujnicki_5_rpr.pdb 11.03 2074
8_Bujnicki_6_rpr.pdb 11.78 2074
8_Bujnicki_7_rpr.pdb 6.71 2074
8_Bujnicki_8_rpr.pdb 11.48 2074
8_Bujnicki_9_rpr.pdb 6.81 2074
8_Bujnicki_10_rpr.pdb 10.8 2074
8_Chen_1_rpr.pdb 13.08 2074
8_Chen_2_rpr.pdb 12.79 2074
8_Chen_3_rpr.pdb 11.29 2074
8_Chen_4_rpr.pdb 12.88 2074
8_Chen_5_rpr.pdb 11.67 2074
8_Chen_6_rpr.pdb 11.77 2074
8_Chen_7_rpr.pdb 12.8 2074
8_Chen_8_rpr.pdb 15.81 2074
8_Chen_9_rpr.pdb 11.3 2074
8_Chen_10_rpr.pdb 12.15 2074
8_Das_1_rpr.pdb 6.38 2074
8_Das_2_rpr.pdb 10.65 2074
8_Das_3_rpr.pdb 4.8 2074
8_Das_4_rpr.pdb 10.78 2074
8_Das_5_rpr.pdb 10.8 2074
8_Das_6_rpr.pdb 10.77 2074
8_Ding_1_rpr.pdb 12.09 2074
8_Ding_2_rpr.pdb 13.5 2074
8_Ding_3_rpr.pdb 11.33 2074
8_Ding_4_rpr.pdb 15.17 2074
8_Ding_5_rpr.pdb 12.39 2074
8_Ding_6_rpr.pdb 13.53 2074
8_Ding_7_rpr.pdb 12.48 2074
8_Ding_8_rpr.pdb 14.99 2074
8_Ding_9_rpr.pdb 16.22 2074
8_Ding_10_rpr.pdb 11.33 2074
8_Dokholyan_1_rpr.pdb 23.69 2074
8_Dokholyan_2_rpr.pdb 18.62 2074
8_Dokholyan_3_rpr.pdb 24.75 2074
8_Dokholyan_4_rpr.pdb 31.29 2074
# of atoms used: 2074
csv was created!  rmsds.csv
```
