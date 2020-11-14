RNA-Puzzle 15
-----------------------------------------------------------------------------

Solution sequence vs target sequence:

```
> 15_RW3DAS1_9_rpr A:1-48
GGGUACUUAAGCCCACUGAUGAGUCGCUGGGAUGCGACGAAACGCCCA
> 15_RW3DAS1_9_rpr B:1-20
GGGCGUCUGGGCAGUACCCA

> 15_solution_0_rpr A:1-48
GGGUACUUAAGCCCACUGAUGAGUCGCUGGGAUGCGACGAAACGCCCA
> 15_solution_0_rpr B:1-20
GGGCGUCUGGGCAGUACCCA
```

Edit chains:

	for i in `ls *3dRNA*`; do rna_pdb_tools.py --edit 'B:49-68>B:1-20' $i > ${i}_temp; mv ${i}_temp ${i}; done
	for i in `ls *Chen*`; do rna_pdb_tools.py --edit 'B:52-71>B:1-20' $i > ${i}_temp; mv ${i}_temp ${i}; done
	for i in `ls *RW3DAS*`; do rna_pdb_tools.py --edit 'A:49-68>B:1-20' $i > ${i}_temp; mv ${i}_temp ${i}; done

RMSD
-------------------------------------------------------------------------------

```
rna_calc_rmsd.py -t 15_solution_0_rpr.pdb --model-selection A:1-48+B:1-20 --target-selection A:1-48+B:1-20 --model-ignore-selection A/7/O2\'  *.pdb -pr -sr
# method: all-atom-built-in
# of models: 75
                             fn  rmsd_all
74        15_solution_0_rpr.pdb      0.00
17         15_Adamiak_8_rpr.pdb      6.68
19        15_Adamiak_10_rpr.pdb      6.82
54       15_SimRNAAS1_1_rpr.pdb      7.30
18         15_Adamiak_9_rpr.pdb      7.98
30  15_RNAComposerAS1_1_rpr.pdb      8.28
11         15_Adamiak_2_rpr.pdb      8.28
31  15_RNAComposerAS1_2_rpr.pdb      8.53
12         15_Adamiak_3_rpr.pdb      8.53
16         15_Adamiak_7_rpr.pdb      8.61
25            15_Chen_6_rpr.pdb      8.67
33  15_RNAComposerAS2_2_rpr.pdb      8.73
14         15_Adamiak_5_rpr.pdb      8.73
13         15_Adamiak_4_rpr.pdb      8.83
32  15_RNAComposerAS2_1_rpr.pdb      8.83
22            15_Chen_3_rpr.pdb      8.93
15         15_Adamiak_6_rpr.pdb      9.02
10         15_Adamiak_1_rpr.pdb      9.18
29           15_Chen_10_rpr.pdb      9.43
70       15_SimRNAAS2_7_rpr.pdb      9.46
20            15_Chen_1_rpr.pdb      9.58
23            15_Chen_4_rpr.pdb     10.17
47         15_RW3DAS2_4_rpr.pdb     10.27
48         15_RW3DAS2_5_rpr.pdb     11.00
26            15_Chen_7_rpr.pdb     11.19
67       15_SimRNAAS2_4_rpr.pdb     11.48
27            15_Chen_8_rpr.pdb     12.14
44         15_RW3DAS2_1_rpr.pdb     12.16
38         15_RW3DAS1_5_rpr.pdb     12.56
51         15_RW3DAS2_8_rpr.pdb     13.41
28            15_Chen_9_rpr.pdb     13.48
50         15_RW3DAS2_7_rpr.pdb     13.76
72       15_SimRNAAS2_9_rpr.pdb     13.92
53        15_RW3DAS2_10_rpr.pdb     14.49
37         15_RW3DAS1_4_rpr.pdb     14.58
42         15_RW3DAS1_9_rpr.pdb     14.61
52         15_RW3DAS2_9_rpr.pdb     14.67
40         15_RW3DAS1_7_rpr.pdb     14.88
64       15_SimRNAAS2_1_rpr.pdb     15.09
39         15_RW3DAS1_6_rpr.pdb     15.29
36         15_RW3DAS1_3_rpr.pdb     15.31
35         15_RW3DAS1_2_rpr.pdb     15.45
21            15_Chen_2_rpr.pdb     15.74
24            15_Chen_5_rpr.pdb     16.08
46         15_RW3DAS2_3_rpr.pdb     16.31
45         15_RW3DAS2_2_rpr.pdb     16.43
56       15_SimRNAAS1_3_rpr.pdb     17.07
34         15_RW3DAS1_1_rpr.pdb     17.07
43        15_RW3DAS1_10_rpr.pdb     17.60
49         15_RW3DAS2_6_rpr.pdb     17.97
60       15_SimRNAAS1_7_rpr.pdb     18.27
65       15_SimRNAAS2_2_rpr.pdb     18.73
62       15_SimRNAAS1_9_rpr.pdb     19.14
63      15_SimRNAAS1_10_rpr.pdb     19.42
73      15_SimRNAAS2_10_rpr.pdb     19.44
66       15_SimRNAAS2_3_rpr.pdb     19.83
41         15_RW3DAS1_8_rpr.pdb     19.83
61       15_SimRNAAS1_8_rpr.pdb     19.91
68       15_SimRNAAS2_5_rpr.pdb     20.08
69       15_SimRNAAS2_6_rpr.pdb     20.46
55       15_SimRNAAS1_2_rpr.pdb     20.72
58       15_SimRNAAS1_5_rpr.pdb     20.91
71       15_SimRNAAS2_8_rpr.pdb     21.98
59       15_SimRNAAS1_6_rpr.pdb     22.19
57       15_SimRNAAS1_4_rpr.pdb     24.19
1         15_3dRNAAS2_2_rpr.pdb     24.53
3         15_3dRNAAS2_4_rpr.pdb     24.54
4         15_3dRNAAS2_5_rpr.pdb     24.56
6         15_3dRNAAS2_7_rpr.pdb     24.56
2         15_3dRNAAS2_3_rpr.pdb     24.57
8         15_3dRNAAS2_9_rpr.pdb     24.57
5         15_3dRNAAS2_6_rpr.pdb     24.60
9        15_3dRNAAS2_10_rpr.pdb     24.61
0         15_3dRNAAS2_1_rpr.pdb     24.64
7         15_3dRNAAS2_8_rpr.pdb     24.75
csv was created!  rmsds.csv
```


INFS
-------------------------------------------------------------------------------

```
rna_calc_inf.py -t 15_solution_0_rpr.pdb *.pdb -pr -sr -f
100% (75 of 75) |###########################################################################################################################################################| Elapsed Time: 0:08:30 ETA:  00:00:00csv was created!  inf.csv
                   target                           fn  inf_all  inf_stack  inf_WC  inf_nWC  sns_WC  ppv_WC  sns_nWC  ppv_nWC
72  15_solution_0_rpr.pdb        15_solution_0_rpr.pdb     1.00       1.00    1.00     1.00    1.00    1.00     1.00     1.00
27  15_solution_0_rpr.pdb            15_Chen_3_rpr.pdb     0.84       0.85    0.83     0.67    0.94    0.73     0.75     0.60
31  15_solution_0_rpr.pdb  15_RNAComposerAS1_2_rpr.pdb     0.83       0.83    0.86     0.75    1.00    0.74     0.75     0.75
19  15_solution_0_rpr.pdb         15_Adamiak_3_rpr.pdb     0.83       0.83    0.86     0.75    1.00    0.74     0.75     0.75
28  15_solution_0_rpr.pdb  15_RNAComposerAS1_1_rpr.pdb     0.82       0.81    0.86     0.75    1.00    0.74     0.75     0.75
16  15_solution_0_rpr.pdb         15_Adamiak_2_rpr.pdb     0.82       0.81    0.86     0.75    1.00    0.74     0.75     0.75
14  15_solution_0_rpr.pdb         15_Adamiak_8_rpr.pdb     0.81       0.83    0.84     0.50    1.00    0.71     0.25     1.00
10  15_solution_0_rpr.pdb        15_Adamiak_10_rpr.pdb     0.80       0.81    0.84     0.35    1.00    0.71     0.25     0.50
48  15_solution_0_rpr.pdb        15_RW3DAS2_10_rpr.pdb     0.80       0.83    0.81     0.45    0.94    0.70     0.50     0.40
30  15_solution_0_rpr.pdb            15_Chen_4_rpr.pdb     0.80       0.81    0.85     0.58    0.94    0.76     0.50     0.67
21  15_solution_0_rpr.pdb            15_Chen_1_rpr.pdb     0.79       0.80    0.79     0.58    0.88    0.71     0.50     0.67
33  15_solution_0_rpr.pdb            15_Chen_5_rpr.pdb     0.79       0.80    0.79     0.58    0.88    0.71     0.50     0.67
38  15_solution_0_rpr.pdb  15_RNAComposerAS2_2_rpr.pdb     0.78       0.77    0.84     0.71    1.00    0.71     0.50     1.00
51  15_solution_0_rpr.pdb         15_RW3DAS2_1_rpr.pdb     0.78       0.78    0.81     0.67    0.94    0.70     0.75     0.60
2   15_solution_0_rpr.pdb         15_Adamiak_4_rpr.pdb     0.78       0.76    0.86     0.71    1.00    0.74     0.50     1.00
34  15_solution_0_rpr.pdb  15_RNAComposerAS2_1_rpr.pdb     0.78       0.76    0.86     0.71    1.00    0.74     0.50     1.00
23  15_solution_0_rpr.pdb         15_RW3DAS1_1_rpr.pdb     0.78       0.79    0.83     0.41    0.94    0.73     0.50     0.33
5   15_solution_0_rpr.pdb         15_Adamiak_5_rpr.pdb     0.78       0.77    0.84     0.71    1.00    0.71     0.50     1.00
24  15_solution_0_rpr.pdb            15_Chen_2_rpr.pdb     0.78       0.78    0.83     0.67    0.94    0.73     0.75     0.60
68  15_solution_0_rpr.pdb       15_SimRNAAS2_8_rpr.pdb     0.78       0.79    0.81     0.45    0.94    0.70     0.50     0.40
11  15_solution_0_rpr.pdb         15_Adamiak_7_rpr.pdb     0.78       0.78    0.86     0.50    1.00    0.74     0.25     1.00
55  15_solution_0_rpr.pdb         15_RW3DAS2_9_rpr.pdb     0.78       0.78    0.81     0.67    0.94    0.70     0.75     0.60
40  15_solution_0_rpr.pdb         15_RW3DAS1_7_rpr.pdb     0.77       0.77    0.83     0.45    0.94    0.73     0.50     0.40
37  15_solution_0_rpr.pdb         15_RW3DAS1_6_rpr.pdb     0.77       0.78    0.83     0.29    0.94    0.73     0.25     0.33
45  15_solution_0_rpr.pdb         15_RW3DAS1_9_rpr.pdb     0.76       0.77    0.83     0.38    0.94    0.73     0.50     0.29
54  15_solution_0_rpr.pdb         15_RW3DAS2_2_rpr.pdb     0.76       0.77    0.79     0.50    0.94    0.67     0.50     0.50
46  15_solution_0_rpr.pdb         15_RW3DAS2_6_rpr.pdb     0.76       0.78    0.81     0.41    0.94    0.70     0.50     0.33
35  15_solution_0_rpr.pdb         15_RW3DAS1_5_rpr.pdb     0.76       0.77    0.81     0.45    0.94    0.70     0.50     0.40
49  15_solution_0_rpr.pdb         15_RW3DAS2_7_rpr.pdb     0.76       0.76    0.81     0.45    0.94    0.70     0.50     0.40
69  15_solution_0_rpr.pdb       15_SimRNAAS2_2_rpr.pdb     0.76       0.78    0.79     0.25    0.94    0.67     0.25     0.25
8   15_solution_0_rpr.pdb         15_Adamiak_6_rpr.pdb     0.76       0.76    0.86     0.35    1.00    0.74     0.25     0.50
71  15_solution_0_rpr.pdb       15_SimRNAAS2_3_rpr.pdb     0.75       0.75    0.81     0.50    0.94    0.70     0.50     0.50
64  15_solution_0_rpr.pdb       15_SimRNAAS2_6_rpr.pdb     0.75       0.77    0.81     0.22    0.94    0.70     0.25     0.20
17  15_solution_0_rpr.pdb         15_Adamiak_9_rpr.pdb     0.75       0.72    0.86     0.71    1.00    0.74     0.50     1.00
36  15_solution_0_rpr.pdb            15_Chen_6_rpr.pdb     0.75       0.75    0.83     0.35    0.94    0.73     0.25     0.50
26  15_solution_0_rpr.pdb         15_RW3DAS1_2_rpr.pdb     0.75       0.75    0.83     0.35    0.94    0.73     0.25     0.50
29  15_solution_0_rpr.pdb         15_RW3DAS1_3_rpr.pdb     0.74       0.74    0.81     0.50    0.94    0.70     0.50     0.50
73  15_solution_0_rpr.pdb       15_SimRNAAS2_4_rpr.pdb     0.74       0.75    0.81     0.41    0.94    0.70     0.50     0.33
52  15_solution_0_rpr.pdb         15_RW3DAS2_8_rpr.pdb     0.74       0.74    0.81     0.50    0.94    0.70     0.50     0.50
70  15_solution_0_rpr.pdb       15_SimRNAAS2_9_rpr.pdb     0.74       0.74    0.85     0.38    0.94    0.76     0.50     0.29
43  15_solution_0_rpr.pdb         15_RW3DAS2_5_rpr.pdb     0.74       0.75    0.81     0.45    0.94    0.70     0.50     0.40
39  15_solution_0_rpr.pdb            15_Chen_7_rpr.pdb     0.74       0.75    0.83     0.00    0.94    0.73     0.00     0.00
41  15_solution_0_rpr.pdb        15_RW3DAS1_10_rpr.pdb     0.74       0.75    0.83     0.38    0.94    0.73     0.50     0.29
32  15_solution_0_rpr.pdb         15_RW3DAS1_4_rpr.pdb     0.74       0.74    0.83     0.38    0.94    0.73     0.50     0.29
58  15_solution_0_rpr.pdb      15_SimRNAAS1_10_rpr.pdb     0.74       0.78    0.69     0.45    0.82    0.58     0.50     0.40
67  15_solution_0_rpr.pdb       15_SimRNAAS2_1_rpr.pdb     0.73       0.74    0.83     0.38    0.94    0.73     0.50     0.29
66  15_solution_0_rpr.pdb       15_SimRNAAS2_7_rpr.pdb     0.73       0.73    0.81     0.45    0.94    0.70     0.50     0.40
57  15_solution_0_rpr.pdb         15_RW3DAS2_3_rpr.pdb     0.73       0.74    0.81     0.35    0.94    0.70     0.50     0.25
61  15_solution_0_rpr.pdb       15_SimRNAAS1_1_rpr.pdb     0.73       0.74    0.81     0.25    0.94    0.70     0.25     0.25
60  15_solution_0_rpr.pdb         15_RW3DAS2_4_rpr.pdb     0.73       0.76    0.81     0.19    0.94    0.70     0.25     0.14
74  15_solution_0_rpr.pdb       15_SimRNAAS2_5_rpr.pdb     0.73       0.74    0.81     0.41    0.94    0.70     0.50     0.33
13  15_solution_0_rpr.pdb         15_Adamiak_1_rpr.pdb     0.73       0.72    0.79     0.58    0.88    0.71     0.50     0.67
22  15_solution_0_rpr.pdb            15_Chen_8_rpr.pdb     0.73       0.74    0.78     0.35    0.82    0.74     0.25     0.50
42  15_solution_0_rpr.pdb         15_RW3DAS1_8_rpr.pdb     0.72       0.73    0.81     0.38    0.94    0.70     0.50     0.29
65  15_solution_0_rpr.pdb      15_SimRNAAS2_10_rpr.pdb     0.72       0.72    0.81     0.25    0.94    0.70     0.25     0.25
63  15_solution_0_rpr.pdb       15_SimRNAAS1_9_rpr.pdb     0.72       0.74    0.74     0.50    0.82    0.67     0.50     0.50
1   15_solution_0_rpr.pdb        15_3dRNAAS2_7_rpr.pdb     0.71       0.70    0.76     0.71    0.82    0.70     0.50     1.00
20  15_solution_0_rpr.pdb           15_Chen_10_rpr.pdb     0.71       0.73    0.74     0.35    0.82    0.67     0.25     0.50
62  15_solution_0_rpr.pdb       15_SimRNAAS1_8_rpr.pdb     0.71       0.72    0.72     0.50    0.82    0.64     0.50     0.50
25  15_solution_0_rpr.pdb            15_Chen_9_rpr.pdb     0.70       0.70    0.76     0.35    0.76    0.76     0.25     0.50
12  15_solution_0_rpr.pdb        15_3dRNAAS2_4_rpr.pdb     0.70       0.68    0.76     0.71    0.82    0.70     0.50     1.00
18  15_solution_0_rpr.pdb        15_3dRNAAS2_6_rpr.pdb     0.70       0.69    0.76     0.71    0.82    0.70     0.50     1.00
15  15_solution_0_rpr.pdb        15_3dRNAAS2_5_rpr.pdb     0.70       0.68    0.76     0.71    0.82    0.70     0.50     1.00
7   15_solution_0_rpr.pdb        15_3dRNAAS2_2_rpr.pdb     0.70       0.68    0.76     0.71    0.82    0.70     0.50     1.00
6   15_solution_0_rpr.pdb        15_3dRNAAS2_9_rpr.pdb     0.69       0.67    0.76     0.71    0.82    0.70     0.50     1.00
4   15_solution_0_rpr.pdb        15_3dRNAAS2_8_rpr.pdb     0.69       0.68    0.76     0.71    0.82    0.70     0.50     1.00
9   15_solution_0_rpr.pdb        15_3dRNAAS2_3_rpr.pdb     0.69       0.68    0.76     0.71    0.82    0.70     0.50     1.00
3   15_solution_0_rpr.pdb        15_3dRNAAS2_1_rpr.pdb     0.69       0.68    0.76     0.71    0.82    0.70     0.50     1.00
0   15_solution_0_rpr.pdb       15_3dRNAAS2_10_rpr.pdb     0.69       0.68    0.76     0.71    0.82    0.70     0.50     1.00
59  15_solution_0_rpr.pdb       15_SimRNAAS1_7_rpr.pdb     0.68       0.71    0.67     0.25    0.76    0.59     0.25     0.25
53  15_solution_0_rpr.pdb       15_SimRNAAS1_5_rpr.pdb     0.66       0.72    0.56     0.29    0.65    0.48     0.25     0.33
44  15_solution_0_rpr.pdb       15_SimRNAAS1_2_rpr.pdb     0.64       0.70    0.56     0.25    0.65    0.48     0.25     0.25
50  15_solution_0_rpr.pdb       15_SimRNAAS1_4_rpr.pdb     0.59       0.74    0.22     0.16    0.24    0.21     0.25     0.10
56  15_solution_0_rpr.pdb       15_SimRNAAS1_6_rpr.pdb     0.52       0.66    0.11     0.20    0.12    0.11     0.25     0.17
47  15_solution_0_rpr.pdb       15_SimRNAAS1_3_rpr.pdb     0.50       0.65    0.05     0.22    0.06    0.05     0.25     0.20
```
