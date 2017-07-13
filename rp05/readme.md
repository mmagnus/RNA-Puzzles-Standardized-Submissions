RNA-Puzzle 05
-----------------------------------------------------------------------------

Solution sequence vs target sequence:

```
> 5_0_solution_4p8z_rpr A:1-188
GGUUGGGUUGGGAAGUAUCAUGGCUAAUCACCAUGAUGCAAUCGGGUUGAACACUUAAUUGGGUUAAAACGGUGGGGGACGAUCCCGUAACAUCCGUCCUAACGGCGACAGACUGCACGGCCCUGCCUCUUAGGUGUGUCCAAUGAACAGUCGUUCCGAAAGGAAGCAUCCGGUAUCCCAAGACAAUC
|||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||.||||||||||||||||||||||||||||||||||||||||||||||||
GGUUGGGUUGGGAAGUAUCAUGGCUAAUCACCAUGAUGCAAUCGGGUUGAACACUUAAUUGGGUUAAAACGGUGGGGGACGAUCCCGUAACAUCCGUCCUAACGGCGACAGACUGCACGGCCCUGCCUCUUAGGUGUGUUCAAUGAACAGUCGUUCCGAAAGGAAGCAUCCGGUAUCCCAAGACAAUC
> target sequence (.e.g 5_adamiak_1_rpr A:1-188)

! mind mismatch at position 140
```

Edits:

	for i in `ls *.pdb`; do rna_pdb_tools.py --get_rnapuzzle_ready $i > ${i/.pdb/_rpr.pdb}; done
    Cheng U -> A , Xioa L -> A
    [mm] rpr rna_pdb_tools.py --get_seq 5_chen_1_rpr.pdb
    > 5_chen_1_rpr.pdb U:1-188
    [mm] rpr rna_pdb_tools.py --edit 'U:1-188>A:1-188' 5_chen_1_rpr.pdb > 5_chen_1_rpr1.pdb
    [mm] rpr rna_pdb_tools.py --edit 'U:1-188>A:1-188' 5_chen_2_rpr.pdb > 5_chen_2_rpr1.pdb
    [mm] rpr rna_pdb_tools.py --edit 'U:1-188>A:1-188' 5_chen_3_rpr.pdb > 5_chen_3_rpr1.pdb
    [mm] rpr rna_pdb_tools.py --edit 'U:1-188>A:1-188' 5_chen_4_rpr.pdb > 5_chen_4_rpr1.pdb
    [mm] rpr rna_pdb_tools.py --edit 'U:1-188>A:1-188' 5_chen_5_rpr.pdb > 5_chen_5_rpr1.pdb
    [mm] rpr rna_pdb_tools.py --edit 'U:1-188>A:1-188' 5_chen_6_rpr.pdb > 5_chen_6_rpr1.pdb
    [mm] rpr rna_pdb_tools.py --edit 'U:1-188>A:1-188' 5_chen_7_rpr.pdb > 5_chen_7_rpr1.pdb
    [mm] rpr rna_pdb_tools.py --edit 'L:1-188>A:1-188' 5_xiao_1_rpr.pdb > 5_xiao_1_rpr.pdb1
    [mm] rpr rna_pdb_tools.py --edit 'L:1-188>A:1-188' 5_xiao_2_rpr.pdb > 5_xiao_2_rpr.pdb1

Rmsd (there is a mismatch at position 140, so N of cytidine is superimposed on O of uridine):

```
rna_calc_rmsd.py -t 5_0_solution_4p8z_rpr.pdb *.pdb
rmsd_calc_rmsd_to_target
--------------------------------------------------------------------------------
method: all-atom-built-in
# of models: 26
5_0_solution_4p8z_rpr.pdb 0.0 4014
5_adamiak_1_rpr.pdb 16.38 4014
5_bujnicki_1_rpr.pdb 24.64 4014
5_bujnicki_2_rpr.pdb 20.27 4014
5_bujnicki_3_rpr.pdb 22.01 4014
5_bujnicki_4_rpr.pdb 22.41 4014
5_bujnicki_5_rpr.pdb 23.74 4014
5_chen_1_rpr.pdb 26.54 4014
5_chen_2_rpr.pdb 25.61 4014
5_chen_3_rpr.pdb 29.23 4014
5_chen_4_rpr.pdb 31.47 4014
5_chen_5_rpr.pdb 31.0 4014
5_chen_6_rpr.pdb 31.5 4014
5_chen_7_rpr.pdb 26.13 4014
5_das_1_rpr.pdb 9.75 4014
5_das_2_rpr.pdb 9.03 4014
5_ding_1_rpr.pdb 26.97 4014
5_ding_2_rpr.pdb 19.36 4014
5_ding_3_rpr.pdb 23.25 4014
5_ding_4_rpr.pdb 19.36 4014
5_ding_5_rpr.pdb 22.6 4014
5_dokholyan_1_rpr.pdb 21.22 4014
5_dokholyan_2_rpr.pdb 21.85 4014
5_dokholyan_3_rpr.pdb 24.72 4014
5_xiao_1_rpr.pdb 36.18 4014
5_xiao_2_rpr.pdb 32.55 4014
# of atoms used: 4014
csv was created!  rmsds.csv
```
