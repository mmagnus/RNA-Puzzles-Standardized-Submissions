RNA-Puzzle 03 
-----------------------------------------------------------------------------

Solution sequence vs target sequence:

```
> 3_solution_0_rpr A:1-84
CUCUGGAGAGAACCGUUUAAUCGGUCGCCGAAGGAGCAAGCUCUGCGGAAACGCAGAGUGAAACUCUCAGGCAAAAGGACAGAG
|||||||||||||||||||||||||||||||||||||||||||||||.|.|.||||||||||||||||||||||||||||||||
CUCUGGAGAGAACCGUUUAAUCGGUCGCCGAAGGAGCAAGCUCUGCGCAUAUGCAGAGUGAAACUCUCAGGCAAAAGGACAGAG
> target sequence (3_bujnicki_1_rpr A:1-84)

! mind mismatches at position 48,50, and 52
```

rpr:

	for i in `ls *.pdb`; do rna_pdb_toolsx.py --get-rnapuzzle-ready $i > ${i/.pdb/_rpr.pdb}; done

Calc RMSD:

    rna_calc_rmsd.py -t 3_solution_0_rpr.pdb --target-selection A:1-47+49+51+53-84 --model-selection A:1-47+49+51+53-84 *.pdb
    rmsd_calc_rmsd_to_target
    --------------------------------------------------------------------------------
    method: all-atom-built-in
    # of models: 13
    3_bujnicki_1_rpr.pdb 12.16 1747
    3_bujnicki_2_rpr.pdb 14.25 1747
    3_chen_1_rpr.pdb 7.6 1747
    3_das_1_rpr.pdb 15.68 1747
    3_das_2_rpr.pdb 12.15 1747
    3_das_3_rpr.pdb 16.92 1747
    3_das_4_rpr.pdb 18.21 1747
    3_das_5_rpr.pdb 12.07 1747
    3_dokholyan_1_rpr.pdb 16.85 1747
    3_dokholyan_2_rpr.pdb 11.4 1747
    3_major_1_rpr.pdb 24.26 1747
    3_major_2_rpr.pdb 13.8 1747
    3_solution_0_rpr.pdb 0.0 1747
    # of atoms used: 1747
    csv was created!  rmsds.csv

