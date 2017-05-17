RNA-Puzzle 06
-----------------------------------------------------------------------------

```
> 6_0_solution_4GXY_rpr A:1-17 24-110 115-168
CGGCAGGUGCUCCCGACGUCGGGAGUUAAAAGGGAAGCCGGUGCAAGUCCGGCACGGUCCCGCCACUGUGACGGGGAGUCGCCCCUCGGGAUGUGCCACUGGCCGGCCGGGAAGGCGGAGGGGCGGCGAGGAUCCGGAGUCAGGAAACCUGCCUGCCG

> 6_Blanchet_1_rpr A:1-168
CGGCAGGUGCUCCCGACCCUGCGGUCGGGAGUUAAAAGGGAAGCCGGUGCAAGUCCGGCACGGUCCCGCCACUGUGACGGGGAGUCGCCCCUCGGGAUGUGCCACUGGCCCGAAGGCCGGGAAGGCGGAGGGGCGGCGAGGAUCCGGAGUCAGGAAACCUGCCUGCCG
```

The natives was trimmed by 2bp helix GG+UC, too keep the numbering of the models as it is. After the renumbering the native, 111C was removed since it was incomplete.

```
GGCGGCAGGUGCUCCCGAC------GUCGGGAGUUAAAAGGGAAGCCGGUGCAAGUCCGGCACGGUCCCGCCACUGUGACGGGGAGUCGCCCCUCGGGAUGUGCCACUGGCCCG---GCCGGGAAGGCGGAGGGGCGGCGAGGAUCCGGAGUCAGGAAACCUGCCUGCCGUC  # native
--CGGCAGGUGCUCCCGACCCUGCGGUCGGGAGUUAAAAGGGAAGCCGGUGCAAGUCCGGCACGGUCCCGCCACUGUGACGGGGAGUCGCCCCUCGGGAUGUGCCACUGGCCCGAAGGCCGGGAAGGCGGAGGGGCGGCGAGGAUCCGGAGUCAGGAAACCUGCCUGCCG-- # predicted
--CGGCAGGUGCUCCCGAC------GUCGGGAGUUAAAAGGGAAGCCGGUGCAAGUCCGGCACGGUCCCGCCACUGUGACGGGGAGUCGCCCCUCGGGAUGUGCCACUGGCCCG---GCCGGGAAGGCGGAGGGGCGGCGAGGAUCCGGAGUCAGGAAACCUGCCUGCCG-- # !!! new native !!!
``` 

The new native numbering:

```
                                                                                                                /111C removed, not complete residues
 CGGCAGGUGCUCCCGAC------GUCGGGAGUUAAAAGGGAAGCCGGUGCAAGUCCGGCACGGUCCCGCCACUGUGACGGGGAGUCGCCCCUCGGGAUGUGCCACUGGCCC----GGCCGGGAAGGCGGAGGGGCGGCGAGGAUCCGGAGUCAGGAAACCUGCCUGCCG # !!! new native !!!
 1               14     24                                                                                    110   115                                                168
 # A:1-14+24-110+115-168
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
rna_calc_rmsd.py -t 6_0_solution_4GXY_rpr.pdb --target_selection=A:1-14+24-110+115-168 --model_selection=A:1-14+24-110+115-168 *.pdb
rmsd_calc_rmsd_to_target
--------------------------------------------------------------------------------
method: all-atom-built-in
# of models: 37
6_0_solution_4GXY_rpr2.pdb 0.0 3344
6_0_solution_4GXY_rpr2_rpr.pdb 0.0 3344
6_0_solution_4GXY_rpr.pdb 0.0 3344
6_Blanchet_1_rpr.pdb 21.62 3344
6_Blanchet_2_rpr.pdb 20.86 3344
6_Blanchet_3_rpr.pdb 20.62 3344
6_Blanchet_4_rpr.pdb 21.61 3344
6_Blanchet_5_rpr.pdb 23.52 3344
6_Blanchet_6_rpr.pdb 22.16 3344
6_Blanchet_7_rpr.pdb 21.23 3344
6_Bujnicki_1_rpr.pdb 36.4 3344
6_Bujnicki_2_rpr.pdb 30.43 3344
6_Bujnicki_3_rpr.pdb 31.76 3344
6_Bujnicki_4_rpr.pdb 31.65 3344
6_Chen_1_rpr.pdb 24.42 3344
6_Chen_2_rpr.pdb 22.35 3344
6_Chen_3_rpr.pdb 23.83 3344
6_Chen_4_rpr.pdb 22.26 3344
6_Chen_5_rpr.pdb 23.65 3344
6_Chen_6_rpr.pdb 35.79 3344
6_Chen_7_rpr.pdb 31.15 3344
6_DAS_1_rpr.pdb 13.98 3344
6_DAS_2_rpr.pdb 13.46 3344
6_DAS_3_rpr.pdb 15.51 3344
6_DAS_4_rpr.pdb 11.33 3344
6_DAS_5_rpr.pdb 15.35 3344
6_DAS_6_rpr.pdb 12.08 3344
6_DAS_7_rpr.pdb 17.52 3344
6_DAS_8_rpr.pdb 17.5 3344
6_DAS_9_rpr.pdb 14.89 3344
6_DAS_10_rpr.pdb 27.8 3344
6_Dokholian_1_rpr.pdb 25.17 3344
6_Dokholian_2_rpr.pdb 25.69 3344
6_Dokholian_3_rpr.pdb 25.15 3344
6_Dokholian_4_rpr.pdb 23.6 3344
6_Dokholian_5_rpr.pdb 22.75 3344
6_Dokholian_6_rpr.pdb 36.83 3344
# of atoms used: 3344
csv was created!  rmsds.csv
```
