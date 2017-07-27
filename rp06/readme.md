RNA-Puzzle 06
-----------------------------------------------------------------------------

Solution sequence vs target sequence:

```
> 6_0_solution_4GXY_rpr A:1-17 24-110 115-168
CGGCAGGUGCUCCCGACGUCGGGAGUUAAAAGGGAAGCCGGUGCAAGUCCGGCACGGUCCCGCCACUGUGACGGGGAGUCGCCCCUCGGGAUGUGCCACUGGCCGGCCGGGAAGGCGGAGGGGCGGCGAGGAUCCGGAGUCAGGAAACCUGCCUGCCG

> 6_Blanchet_1_rpr A:1-168
CGGCAGGUGCUCCCGACCCUGCGGUCGGGAGUUAAAAGGGAAGCCGGUGCAAGUCCGGCACGGUCCCGCCACUGUGACGGGGAGUCGCCCCUCGGGAUGUGCCACUGGCCCGAAGGCCGGGAAGGCGGAGGGGCGGCGAGGAUCCGGAGUCAGGAAACCUGCCUGCCG
```

The solution was trimmed by 2bp helix GG+UC, too keep the numbering of the models as it is. After the renumbering the solution, 111C was removed since it was incomplete.

```
GGCGGCAGGUGCUCCCGAC------GUCGGGAGUUAAAAGGGAAGCCGGUGCAAGUCCGGCACGGUCCCGCCACUGUGACGGGGAGUCGCCCCUCGGGAUGUGCCACUGGCCCG---GCCGGGAAGGCGGAGGGGCGGCGAGGAUCCGGAGUCAGGAAACCUGCCUGCCGUC  # solution
--CGGCAGGUGCUCCCGACCCUGCGGUCGGGAGUUAAAAGGGAAGCCGGUGCAAGUCCGGCACGGUCCCGCCACUGUGACGGGGAGUCGCCCCUCGGGAUGUGCCACUGGCCCGAAGGCCGGGAAGGCGGAGGGGCGGCGAGGAUCCGGAGUCAGGAAACCUGCCUGCCG-- # target
--CGGCAGGUGCUCCCGAC------GUCGGGAGUUAAAAGGGAAGCCGGUGCAAGUCCGGCACGGUCCCGCCACUGUGACGGGGAGUCGCCCCUCGGGAUGUGCCACUGGCCCG---GCCGGGAAGGCGGAGGGGCGGCGAGGAUCCGGAGUCAGGAAACCUGCCUGCCG-- # !!! new solution !!!
``` 

The new solution numbering:

```
                                                                                                                /111C removed, not complete residue
 CGGCAGGUGCUCCCGAC------GUCGGGAGUUAAAAGGGAAGCCGGUGCAAGUCCGGCACGGUCCCGCCACUGUGACGGGGAGUCGCCCCUCGGGAUGUGCCACUGGCCC----GGCCGGGAAGGCGGAGGGGCGGCGAGGAUCCGGAGUCAGGAAACCUGCCUGCCG # !!! new solution !!!
 1               17     24                                                                                    110   115                                                  168
 # A:1-17+24-110+115-168
```

Edits:

    [mm] rpr rna_pdb_tools.py --edit 'U:1-168>A:1-168' 6_Chen_1_rpr.pdb > ../6_Chen_1_rpr.pdb
    [mm] rpr rna_pdb_tools.py --edit 'U:1-168>A:1-168' 6_Chen_2_rpr.pdb > ../6_Chen_2_rpr.pdb
    [mm] rpr rna_pdb_tools.py --edit 'U:1-168>A:1-168' 6_Chen_3_rpr.pdb > ../6_Chen_3_rpr.pdb
    [mm] rpr rna_pdb_tools.py --edit 'U:1-168>A:1-168' 6_Chen_4_rpr.pdb > ../6_Chen_4_rpr.pdb
    [mm] rpr rna_pdb_tools.py --edit 'U:1-168>A:1-168' 6_Chen_5_rpr.pdb > ../6_Chen_5_rpr.pdb
    [mm] rpr rna_pdb_tools.py --edit 'U:1-168>A:1-168' 6_Chen_6_rpr.pdb > ../6_Chen_6_rpr.pdb
    [mm] rpr rna_pdb_tools.py --edit 'U:1-168>A:1-168' 6_Chen_7_rpr.pdb > ../6_Chen_7_rpr.pdb
	for i in `ls *.pdb`; do rna_pdb_tools.py --get_rnapuzzle_ready $i > ${i/.pdb/_rpr.pdb}; done

Rmsd:

```
rna_calc_rmsd.py -t 6_0_solution_4GXY_rpr.pdb --model_selection=A:1-17+24-110+115-168 *.pdb
method: all-atom-built-in
# of models: 35
6_0_solution_4GXY_rpr.pdb 0.0 3409
6_Blanchet_1_rpr.pdb 22.31 3409
6_Blanchet_2_rpr.pdb 21.76 3409
6_Blanchet_3_rpr.pdb 21.32 3409
6_Blanchet_4_rpr.pdb 22.22 3409
6_Blanchet_5_rpr.pdb 24.17 3409
6_Blanchet_6_rpr.pdb 23.28 3409
6_Blanchet_7_rpr.pdb 22.26 3409
6_Bujnicki_1_rpr.pdb 36.95 3409
6_Bujnicki_2_rpr.pdb 30.9 3409
6_Bujnicki_3_rpr.pdb 32.1 3409
6_Bujnicki_4_rpr.pdb 32.04 3409
6_Chen_1_rpr.pdb 24.29 3409
6_Chen_2_rpr.pdb 22.16 3409
6_Chen_3_rpr.pdb 23.62 3409
6_Chen_4_rpr.pdb 22.12 3409
6_Chen_5_rpr.pdb 23.53 3409
6_Chen_6_rpr.pdb 35.93 3409
6_Chen_7_rpr.pdb 30.97 3409
6_DAS_1_rpr.pdb 14.11 3409
6_DAS_2_rpr.pdb 13.45 3409
6_DAS_3_rpr.pdb 15.54 3409
6_DAS_4_rpr.pdb 11.6 3409
6_DAS_5_rpr.pdb 15.56 3409
6_DAS_6_rpr.pdb 12.22 3409
6_DAS_7_rpr.pdb 17.78 3409
6_DAS_8_rpr.pdb 17.76 3409
6_DAS_9_rpr.pdb 14.87 3409
6_DAS_10_rpr.pdb 28.96 3409
6_Dokholian_1_rpr.pdb 26.06 3409
6_Dokholian_2_rpr.pdb 26.55 3409
6_Dokholian_3_rpr.pdb 26.18 3409
6_Dokholian_4_rpr.pdb 24.93 3409
6_Dokholian_5_rpr.pdb 22.58 3409
6_Dokholian_6_rpr.pdb 37.37 3409
# of atoms used: 3409
csv was created!  rmsds.csv
```
