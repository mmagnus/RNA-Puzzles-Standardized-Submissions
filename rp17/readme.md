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

RMSD
-------------------------------------------------------------------------------

```
rna_calc_rmsd.py -t 17_5k7c_solution_rpr.pdb --target-selection A:1-47+52-62 --model-selection A:1-47+52-62 *.pdb -pr -sr
# method: all-atom-built-in
# of models: 108
# of atoms used: 1238
                               fn  rmsd_all
0        17_5k7c_solution_rpr.pdb      0.00
89         17_SimRNAAS2_1_rpr.pdb      5.16
30               17_Das_4_rpr.pdb      7.15
95         17_SimRNAAS2_7_rpr.pdb      7.66
27               17_Das_1_rpr.pdb      8.64
34               17_Das_8_rpr.pdb      8.70
35               17_Das_9_rpr.pdb      8.78
18              17_Chen_5_rpr.pdb      9.44
10          17_Bujnicki_7_rpr.pdb     10.85
33               17_Das_7_rpr.pdb     10.95
24      17_DasExtraInfo_1_rpr.pdb     11.02
28               17_Das_2_rpr.pdb     11.27
32               17_Das_6_rpr.pdb     11.52
15              17_Chen_2_rpr.pdb     11.62
2            17_Adamiak_2_rpr.pdb     11.79
72    17_RNAComposerAS2_3_rpr.pdb     11.92
71    17_RNAComposerAS2_2_rpr.pdb     12.01
25      17_DasExtraInfo_2_rpr.pdb     12.07
94         17_SimRNAAS2_6_rpr.pdb     12.20
11          17_Bujnicki_8_rpr.pdb     12.22
70    17_RNAComposerAS2_1_rpr.pdb     12.31
1            17_Adamiak_1_rpr.pdb     12.33
3            17_Adamiak_3_rpr.pdb     12.38
74    17_RNAComposerAS2_5_rpr.pdb     12.56
96         17_SimRNAAS2_8_rpr.pdb     12.76
75    17_RNAComposerAS2_6_rpr.pdb     12.79
76    17_RNAComposerAS2_7_rpr.pdb     12.83
43              17_Ding_7_rpr.pdb     12.86
26      17_DasExtraInfo_3_rpr.pdb     13.22
46             17_Ding_10_rpr.pdb     13.39
59            17_Major_10_rpr.pdb     13.40
77    17_RNAComposerAS2_8_rpr.pdb     13.51
73    17_RNAComposerAS2_4_rpr.pdb     13.52
104             17_Xiao_7_rpr.pdb     13.84
8           17_Bujnicki_5_rpr.pdb     13.95
12          17_Bujnicki_9_rpr.pdb     13.97
4           17_Bujnicki_1_rpr.pdb     13.97
106             17_Xiao_9_rpr.pdb     14.10
97         17_SimRNAAS2_9_rpr.pdb     14.28
9           17_Bujnicki_6_rpr.pdb     14.35
13         17_Bujnicki_10_rpr.pdb     14.40
5           17_Bujnicki_2_rpr.pdb     14.40
39              17_Ding_3_rpr.pdb     14.53
102             17_Xiao_5_rpr.pdb     14.54
6           17_Bujnicki_3_rpr.pdb     14.64
19              17_Chen_6_rpr.pdb     14.75
44              17_Ding_8_rpr.pdb     14.81
29               17_Das_3_rpr.pdb     14.90
55             17_Major_6_rpr.pdb     14.94
98              17_Xiao_1_rpr.pdb     15.01
49         17_Dohkolyan_3_rpr.pdb     15.02
37              17_Ding_1_rpr.pdb     15.02
92         17_SimRNAAS2_4_rpr.pdb     15.07
17              17_Chen_4_rpr.pdb     15.14
85         17_SimRNAAS1_6_rpr.pdb     15.17
31               17_Das_5_rpr.pdb     15.38
100             17_Xiao_3_rpr.pdb     15.50
107            17_Xiao_10_rpr.pdb     15.52
22              17_Chen_9_rpr.pdb     15.59
91         17_SimRNAAS2_3_rpr.pdb     15.59
79   17_RNAComposerAS2_10_rpr.pdb     15.59
80         17_SimRNAAS1_1_rpr.pdb     15.62
40              17_Ding_4_rpr.pdb     15.74
105             17_Xiao_8_rpr.pdb     15.93
41              17_Ding_5_rpr.pdb     16.01
7           17_Bujnicki_4_rpr.pdb     16.08
38              17_Ding_2_rpr.pdb     16.09
90         17_SimRNAAS2_2_rpr.pdb     16.10
78    17_RNAComposerAS2_9_rpr.pdb     16.10
14              17_Chen_1_rpr.pdb     16.11
48         17_Dohkolyan_2_rpr.pdb     16.27
56             17_Major_7_rpr.pdb     16.47
20              17_Chen_7_rpr.pdb     16.50
99              17_Xiao_2_rpr.pdb     16.55
58             17_Major_9_rpr.pdb     16.59
87         17_SimRNAAS1_8_rpr.pdb     16.59
81         17_SimRNAAS1_2_rpr.pdb     16.60
21              17_Chen_8_rpr.pdb     16.61
57             17_Major_8_rpr.pdb     16.69
45              17_Ding_9_rpr.pdb     16.74
83         17_SimRNAAS1_4_rpr.pdb     16.82
50             17_Major_1_rpr.pdb     16.85
42              17_Ding_6_rpr.pdb     16.94
82         17_SimRNAAS1_3_rpr.pdb     16.97
84         17_SimRNAAS1_5_rpr.pdb     17.05
52             17_Major_3_rpr.pdb     17.05
103             17_Xiao_6_rpr.pdb     17.26
16              17_Chen_3_rpr.pdb     17.35
101             17_Xiao_4_rpr.pdb     17.42
36              17_Das_10_rpr.pdb     17.43
67    17_RNAComposerAS1_8_rpr.pdb     17.60
62    17_RNAComposerAS1_3_rpr.pdb     17.95
51             17_Major_2_rpr.pdb     18.05
69   17_RNAComposerAS1_10_rpr.pdb     18.45
54             17_Major_5_rpr.pdb     18.46
93         17_SimRNAAS2_5_rpr.pdb     18.58
53             17_Major_4_rpr.pdb     18.67
60    17_RNAComposerAS1_1_rpr.pdb     18.78
65    17_RNAComposerAS1_6_rpr.pdb     18.91
23             17_Chen_10_rpr.pdb     18.99
86         17_SimRNAAS1_7_rpr.pdb     19.07
68    17_RNAComposerAS1_9_rpr.pdb     19.67
64    17_RNAComposerAS1_5_rpr.pdb     20.03
63    17_RNAComposerAS1_4_rpr.pdb     20.06
88         17_SimRNAAS1_9_rpr.pdb     20.54
66    17_RNAComposerAS1_7_rpr.pdb     20.65
61    17_RNAComposerAS1_2_rpr.pdb     21.58
47         17_Dohkolyan_1_rpr.pdb     21.78
csv was created!  rmsds.csv
```

INFs
-------------------------------------------------------------------------------

    for i in *pdb; do rna_pdb_toolsx.py --delete A:48-51 $i > clarna/$i ; done

    rna_calc_inf.py -t 17_solution_0_rpr.pdb clarna/*.pdb --sort-results
    100% (108 of 108) |##########################################################################################################################################################################################################| Elapsed Time: 0:00:25 ETA:  00:00:00
    csv was created!  inf.csv
    (py37) [mx] rp17$ git:(master) ✗ csv inf.csv
    target                 fn                            inf_all  inf_stack  inf_WC  inf_nWC  sns_WC  ppv_WC  sns_nWC  ppv_nWC
    17_solution_0_rpr.pdb  17_solution_0_rpr.pdb         1.0      1.0        1.0     1.0      1.0     1.0     1.0      1.0
    17_solution_0_rpr.pdb  17_Das_1_rpr.pdb              0.81     0.83       0.92    0.41     0.94    0.9     0.33     0.5
    17_solution_0_rpr.pdb  17_Chen_2_rpr.pdb             0.77     0.79       0.84    0.38     0.89    0.8     0.22     0.67
    17_solution_0_rpr.pdb  17_DasExtraInfo_1_rpr.pdb     0.76     0.78       0.84    0.41     0.89    0.8     0.33     0.5
    17_solution_0_rpr.pdb  17_Das_8_rpr.pdb              0.76     0.77       0.9     0.3      0.94    0.85    0.22     0.4
    17_solution_0_rpr.pdb  17_Das_4_rpr.pdb              0.76     0.78       0.86    0.33     0.89    0.84    0.22     0.5
    17_solution_0_rpr.pdb  17_DasExtraInfo_2_rpr.pdb     0.76     0.77       0.86    0.38     0.89    0.84    0.22     0.67
    17_solution_0_rpr.pdb  17_SimRNAAS2_1_rpr.pdb        0.75     0.78       0.93    0.13     1.0     0.86    0.11     0.14
    17_solution_0_rpr.pdb  17_Das_9_rpr.pdb              0.75     0.78       0.86    0.15     0.89    0.84    0.11     0.2
    17_solution_0_rpr.pdb  17_Das_7_rpr.pdb              0.75     0.78       0.83    0.33     0.83    0.83    0.22     0.5
    17_solution_0_rpr.pdb  17_Das_6_rpr.pdb              0.75     0.77       0.84    0.38     0.89    0.8     0.22     0.67
    17_solution_0_rpr.pdb  17_Bujnicki_6_rpr.pdb         0.75     0.76       0.84    0.47     0.89    0.8     0.22     1.0
    17_solution_0_rpr.pdb  17_Bujnicki_8_rpr.pdb         0.75     0.78       0.89    0.17     0.89    0.89    0.11     0.25
    17_solution_0_rpr.pdb  17_Bujnicki_7_rpr.pdb         0.74     0.75       0.89    0.19     0.89    0.89    0.11     0.33
    17_solution_0_rpr.pdb  17_Das_5_rpr.pdb              0.74     0.77       0.84    0.17     0.89    0.8     0.11     0.25
    17_solution_0_rpr.pdb  17_DasExtraInfo_3_rpr.pdb     0.74     0.77       0.84    0.24     0.89    0.8     0.11     0.5
    17_solution_0_rpr.pdb  17_SimRNAAS2_7_rpr.pdb        0.73     0.76       0.84    0.33     0.89    0.8     0.33     0.33
    17_solution_0_rpr.pdb  17_Das_2_rpr.pdb              0.73     0.76       0.86    0.15     0.89    0.84    0.11     0.2
    17_solution_0_rpr.pdb  17_Chen_6_rpr.pdb             0.72     0.74       0.73    0.58     0.67    0.8     0.33     1.0
    17_solution_0_rpr.pdb  17_Das_3_rpr.pdb              0.72     0.74       0.83    0.38     0.83    0.83    0.33     0.43
    17_solution_0_rpr.pdb  17_SimRNAAS2_8_rpr.pdb        0.72     0.74       0.82    0.38     0.89    0.76    0.33     0.43
    17_solution_0_rpr.pdb  17_Chen_9_rpr.pdb             0.71     0.72       0.86    0.19     0.83    0.88    0.11     0.33
    17_solution_0_rpr.pdb  17_SimRNAAS2_2_rpr.pdb        0.71     0.73       0.77    0.38     0.89    0.67    0.22     0.67
    17_solution_0_rpr.pdb  17_Bujnicki_4_rpr.pdb         0.71     0.72       0.86    0.17     0.89    0.84    0.11     0.25
    17_solution_0_rpr.pdb  17_SimRNAAS2_9_rpr.pdb        0.7      0.71       0.82    0.19     0.89    0.76    0.11     0.33
    17_solution_0_rpr.pdb  17_Chen_7_rpr.pdb             0.7      0.71       0.83    0.24     0.83    0.83    0.11     0.5
    17_solution_0_rpr.pdb  17_SimRNAAS2_4_rpr.pdb        0.7      0.74       0.74    0.33     0.78    0.7     0.22     0.5
    17_solution_0_rpr.pdb  17_SimRNAAS2_6_rpr.pdb        0.7      0.74       0.78    0.24     0.78    0.78    0.22     0.25
    17_solution_0_rpr.pdb  17_Bujnicki_3_rpr.pdb         0.7      0.73       0.81    0.17     0.83    0.79    0.11     0.25
    17_solution_0_rpr.pdb  17_Chen_1_rpr.pdb             0.7      0.72       0.8     0.19     0.78    0.82    0.11     0.33
    17_solution_0_rpr.pdb  17_Chen_4_rpr.pdb             0.7      0.72       0.76    0.5      0.67    0.86    0.33     0.75
    17_solution_0_rpr.pdb  17_SimRNAAS1_2_rpr.pdb        0.7      0.77       0.8     0.2      0.78    0.82    0.22     0.18
    17_solution_0_rpr.pdb  17_SimRNAAS1_3_rpr.pdb        0.69     0.75       0.74    0.22     0.72    0.76    0.22     0.22
    17_solution_0_rpr.pdb  17_SimRNAAS1_6_rpr.pdb        0.69     0.75       0.77    0.21     0.72    0.81    0.22     0.2
    17_solution_0_rpr.pdb  17_Bujnicki_2_rpr.pdb         0.69     0.69       0.84    0.17     0.89    0.8     0.11     0.25
    17_solution_0_rpr.pdb  17_Bujnicki_1_rpr.pdb         0.69     0.72       0.82    0.15     0.89    0.76    0.11     0.2
    17_solution_0_rpr.pdb  17_SimRNAAS2_5_rpr.pdb        0.69     0.72       0.77    0.27     0.72    0.81    0.22     0.33
    17_solution_0_rpr.pdb  17_SimRNAAS2_3_rpr.pdb        0.69     0.7        0.78    0.41     0.78    0.78    0.33     0.5
    17_solution_0_rpr.pdb  17_Bujnicki_9_rpr.pdb         0.69     0.72       0.82    0.15     0.89    0.76    0.11     0.2
    17_solution_0_rpr.pdb  17_Dohkolyan_3_rpr.pdb        0.69     0.71       0.83    0.0      0.83    0.83    0.0      0.0
    17_solution_0_rpr.pdb  17_Bujnicki_10_rpr.pdb        0.69     0.69       0.84    0.17     0.89    0.8     0.11     0.25
    17_solution_0_rpr.pdb  17_Xiao_3_rpr.pdb             0.69     0.75       0.75    0.0      0.61    0.92    0.0      0.0
    17_solution_0_rpr.pdb  17_Bujnicki_5_rpr.pdb         0.69     0.72       0.81    0.15     0.83    0.79    0.11     0.2
    17_solution_0_rpr.pdb  17_Das_10_rpr.pdb             0.69     0.68       0.84    0.33     0.89    0.8     0.22     0.5
    17_solution_0_rpr.pdb  17_Ding_4_rpr.pdb             0.68     0.75       0.63    0.33     0.61    0.65    0.22     0.5
    17_solution_0_rpr.pdb  17_Ding_5_rpr.pdb             0.68     0.74       0.67    0.19     0.67    0.67    0.11     0.33
    17_solution_0_rpr.pdb  17_Chen_5_rpr.pdb             0.68     0.69       0.72    0.5      0.61    0.85    0.33     0.75
    17_solution_0_rpr.pdb  17_SimRNAAS1_8_rpr.pdb        0.68     0.72       0.74    0.25     0.72    0.76    0.22     0.29
    17_solution_0_rpr.pdb  17_Ding_7_rpr.pdb             0.68     0.71       0.77    0.19     0.72    0.81    0.11     0.33
    17_solution_0_rpr.pdb  17_Ding_1_rpr.pdb             0.68     0.77       0.59    0.19     0.56    0.62    0.11     0.33
    17_solution_0_rpr.pdb  17_SimRNAAS1_1_rpr.pdb        0.67     0.71       0.74    0.25     0.72    0.76    0.22     0.29
    17_solution_0_rpr.pdb  17_Chen_8_rpr.pdb             0.67     0.66       0.86    0.0      0.83    0.88    0.0      0.0
    17_solution_0_rpr.pdb  17_Ding_8_rpr.pdb             0.67     0.66       0.8     0.33     0.78    0.82    0.22     0.5
    17_solution_0_rpr.pdb  17_Xiao_2_rpr.pdb             0.67     0.68       0.76    0.33     0.67    0.86    0.22     0.5
    17_solution_0_rpr.pdb  17_SimRNAAS1_5_rpr.pdb        0.66     0.72       0.71    0.2      0.67    0.75    0.22     0.18
    17_solution_0_rpr.pdb  17_RNAComposerAS2_2_rpr.pdb   0.66     0.64       0.86    0.24     0.83    0.88    0.11     0.5
    17_solution_0_rpr.pdb  17_Chen_3_rpr.pdb             0.65     0.68       0.73    0.0      0.67    0.8     0.0      0.0
    17_solution_0_rpr.pdb  17_Ding_3_rpr.pdb             0.64     0.69       0.63    0.19     0.61    0.65    0.11     0.33
    17_solution_0_rpr.pdb  17_Adamiak_3_rpr.pdb          0.64     0.61       0.81    0.38     0.83    0.79    0.22     0.67
    17_solution_0_rpr.pdb  17_Ding_10_rpr.pdb            0.64     0.65       0.77    0.3      0.72    0.81    0.22     0.4
    17_solution_0_rpr.pdb  17_Ding_9_rpr.pdb             0.64     0.65       0.77    0.17     0.72    0.81    0.11     0.25
    17_solution_0_rpr.pdb  17_SimRNAAS1_4_rpr.pdb        0.64     0.71       0.71    0.19     0.67    0.75    0.22     0.17
    17_solution_0_rpr.pdb  17_Xiao_5_rpr.pdb             0.63     0.66       0.71    0.0      0.56    0.91    0.0      0.0
    17_solution_0_rpr.pdb  17_RNAComposerAS2_6_rpr.pdb   0.62     0.61       0.76    0.24     0.78    0.74    0.11     0.5
    17_solution_0_rpr.pdb  17_RNAComposerAS2_7_rpr.pdb   0.62     0.63       0.76    0.19     0.78    0.74    0.11     0.33
    17_solution_0_rpr.pdb  17_Ding_6_rpr.pdb             0.62     0.64       0.73    0.17     0.67    0.8     0.11     0.25
    17_solution_0_rpr.pdb  17_Major_1_rpr.pdb            0.62     0.66       0.65    0.25     0.61    0.69    0.22     0.29
    17_solution_0_rpr.pdb  17_RNAComposerAS2_5_rpr.pdb   0.61     0.58       0.82    0.24     0.78    0.88    0.11     0.5
    17_solution_0_rpr.pdb  17_Adamiak_1_rpr.pdb          0.61     0.57       0.79    0.38     0.83    0.75    0.22     0.67
    17_solution_0_rpr.pdb  17_RNAComposerAS2_4_rpr.pdb   0.61     0.6        0.76    0.24     0.78    0.74    0.11     0.5
    17_solution_0_rpr.pdb  17_Dohkolyan_2_rpr.pdb        0.6      0.62       0.73    0.17     0.67    0.8     0.11     0.25
    17_solution_0_rpr.pdb  17_Adamiak_2_rpr.pdb          0.6      0.59       0.76    0.24     0.78    0.74    0.11     0.5
    17_solution_0_rpr.pdb  17_Xiao_1_rpr.pdb             0.59     0.6        0.75    0.0      0.61    0.92    0.0      0.0
    17_solution_0_rpr.pdb  17_Ding_2_rpr.pdb             0.59     0.62       0.63    0.24     0.61    0.65    0.11     0.5
    17_solution_0_rpr.pdb  17_RNAComposerAS2_8_rpr.pdb   0.59     0.57       0.77    0.24     0.72    0.81    0.11     0.5
    17_solution_0_rpr.pdb  17_RNAComposerAS1_1_rpr.pdb   0.59     0.66       0.5     0.27     0.44    0.57    0.22     0.33
    17_solution_0_rpr.pdb  17_Major_4_rpr.pdb            0.59     0.66       0.61    0.0      0.61    0.61    0.0      0.0
    17_solution_0_rpr.pdb  17_Major_5_rpr.pdb            0.58     0.64       0.57    0.25     0.56    0.59    0.22     0.29
    17_solution_0_rpr.pdb  17_RNAComposerAS2_10_rpr.pdb  0.58     0.58       0.68    0.24     0.56    0.83    0.11     0.5
    17_solution_0_rpr.pdb  17_RNAComposerAS1_10_rpr.pdb  0.58     0.65       0.5     0.27     0.44    0.57    0.22     0.33
    17_solution_0_rpr.pdb  17_Xiao_9_rpr.pdb             0.58     0.61       0.63    0.24     0.44    0.89    0.11     0.5
    17_solution_0_rpr.pdb  17_Major_3_rpr.pdb            0.58     0.64       0.61    0.13     0.61    0.61    0.11     0.14
    17_solution_0_rpr.pdb  17_RNAComposerAS1_6_rpr.pdb   0.58     0.64       0.5     0.33     0.44    0.57    0.22     0.5
    17_solution_0_rpr.pdb  17_RNAComposerAS2_1_rpr.pdb   0.58     0.54       0.79    0.24     0.83    0.75    0.11     0.5
    17_solution_0_rpr.pdb  17_Xiao_8_rpr.pdb             0.57     0.61       0.58    0.0      0.33    1.0     0.0      0.0
    17_solution_0_rpr.pdb  17_Xiao_10_rpr.pdb            0.57     0.61       0.58    0.0      0.39    0.88    0.0      0.0
    17_solution_0_rpr.pdb  17_RNAComposerAS1_3_rpr.pdb   0.56     0.6        0.59    0.24     0.5     0.69    0.22     0.25
    17_solution_0_rpr.pdb  17_Dohkolyan_1_rpr.pdb        0.56     0.64       0.5     0.14     0.44    0.57    0.11     0.17
    17_solution_0_rpr.pdb  17_RNAComposerAS1_9_rpr.pdb   0.56     0.58       0.55    0.45     0.5     0.6     0.33     0.6
    17_solution_0_rpr.pdb  17_Major_2_rpr.pdb            0.56     0.61       0.6     0.15     0.61    0.58    0.11     0.2
    17_solution_0_rpr.pdb  17_RNAComposerAS1_4_rpr.pdb   0.56     0.61       0.5     0.33     0.44    0.57    0.22     0.5
    17_solution_0_rpr.pdb  17_Xiao_4_rpr.pdb             0.55     0.6        0.58    0.17     0.39    0.88    0.11     0.25
    17_solution_0_rpr.pdb  17_RNAComposerAS1_8_rpr.pdb   0.55     0.6        0.5     0.3      0.44    0.57    0.22     0.4
    17_solution_0_rpr.pdb  17_RNAComposerAS2_9_rpr.pdb   0.55     0.54       0.72    0.19     0.61    0.85    0.11     0.33
    17_solution_0_rpr.pdb  17_RNAComposerAS2_3_rpr.pdb   0.55     0.59       0.55    0.3      0.39    0.78    0.22     0.4
    17_solution_0_rpr.pdb  17_RNAComposerAS1_5_rpr.pdb   0.53     0.56       0.59    0.25     0.5     0.69    0.22     0.29
    17_solution_0_rpr.pdb  17_Xiao_6_rpr.pdb             0.53     0.55       0.62    0.0      0.39    1.0     0.0      0.0
    17_solution_0_rpr.pdb  17_Xiao_7_rpr.pdb             0.53     0.55       0.62    0.0      0.39    1.0     0.0      0.0
    17_solution_0_rpr.pdb  17_SimRNAAS1_9_rpr.pdb        0.53     0.64       0.3     0.27     0.28    0.31    0.22     0.33
    17_solution_0_rpr.pdb  17_Major_8_rpr.pdb            0.5      0.56       0.47    0.17     0.33    0.67    0.11     0.25
    17_solution_0_rpr.pdb  17_Major_6_rpr.pdb            0.49     0.58       0.43    0.0      0.33    0.55    0.0      0.0
    17_solution_0_rpr.pdb  17_Major_7_rpr.pdb            0.48     0.55       0.44    0.0      0.28    0.71    0.0      0.0
    17_solution_0_rpr.pdb  17_SimRNAAS1_7_rpr.pdb        0.48     0.62       0.17    0.22     0.17    0.18    0.22     0.22
    17_solution_0_rpr.pdb  17_RNAComposerAS1_2_rpr.pdb   0.48     0.6        0.2     0.21     0.17    0.25    0.22     0.2
    17_solution_0_rpr.pdb  17_RNAComposerAS1_7_rpr.pdb   0.48     0.61       0.2     0.2      0.17    0.23    0.22     0.18
    17_solution_0_rpr.pdb  17_Major_9_rpr.pdb            0.45     0.5        0.42    0.17     0.22    0.8     0.11     0.25
    17_solution_0_rpr.pdb  17_Chen_10_rpr.pdb            0.45     0.56       0.2     0.21     0.17    0.23    0.22     0.2
    17_solution_0_rpr.pdb  17_Major_10_rpr.pdb           0.41     0.48       0.36    0.14     0.22    0.57    0.11     0.17
