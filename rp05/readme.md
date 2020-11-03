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
$ rna_calc_rmsd.py -t 5_solution_0_rpr.pdb *.pdb -sr -pr # @3.5.4+59
# method: all-atom-built-in
# of models: 26
# of atoms used: 4014
                       fn  rmsd_all
23   5_solution_0_rpr.pdb      0.00
14        5_das_2_rpr.pdb      9.03
13        5_das_1_rpr.pdb      9.75
0     5_adamiak_1_rpr.pdb     16.38
18  5_dokholyan_4_rpr.pdb     19.36
16  5_dokholyan_2_rpr.pdb     19.36
2    5_bujnicki_2_rpr.pdb     20.27
20  5_dokholyan_6_rpr.pdb     21.22
21  5_dokholyan_7_rpr.pdb     21.85
3    5_bujnicki_3_rpr.pdb     22.01
4    5_bujnicki_4_rpr.pdb     22.41
19  5_dokholyan_5_rpr.pdb     22.60
17  5_dokholyan_3_rpr.pdb     23.25
5    5_bujnicki_5_rpr.pdb     23.74
1    5_bujnicki_1_rpr.pdb     24.64
22  5_dokholyan_8_rpr.pdb     24.72
7        5_chen_2_rpr.pdb     25.61
12       5_chen_7_rpr.pdb     26.13
6        5_chen_1_rpr.pdb     26.54
15  5_dokholyan_1_rpr.pdb     26.97
8        5_chen_3_rpr.pdb     29.23
10       5_chen_5_rpr.pdb     31.00
9        5_chen_4_rpr.pdb     31.47
11       5_chen_6_rpr.pdb     31.50
25       5_xiao_2_rpr.pdb     32.55
24       5_xiao_1_rpr.pdb     36.18
csv was created!  rmsds.csv
```
