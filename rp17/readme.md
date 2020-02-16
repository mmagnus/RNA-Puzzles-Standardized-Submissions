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

    rna_calc_rmsd.py -t 17_5k7c_solution_rpr.pdb --target-selection A:1-47+52-62 --model-selection A:1-47+52-62 *.pdb -pr -sr
    # method: all-atom-built-in
    # of models: 90
    # of atoms used: 1238
                                  fn  rmsd_all
    0       17_5k7c_solution_rpr.pdb      0.00
    30              17_Das_4_rpr.pdb      7.15
    27              17_Das_1_rpr.pdb      8.64
    34              17_Das_8_rpr.pdb      8.70
    35              17_Das_9_rpr.pdb      8.78
    18             17_Chen_5_rpr.pdb      9.44
    10         17_Bujnicki_7_rpr.pdb     10.85
    33              17_Das_7_rpr.pdb     10.95
    24     17_DasExtraInfo_1_rpr.pdb     11.02
    28              17_Das_2_rpr.pdb     11.27
    32              17_Das_6_rpr.pdb     11.52
    15             17_Chen_2_rpr.pdb     11.62
    2           17_Adamiak_2_rpr.pdb     11.79
    72   17_RNAComposerAS2_3_rpr.pdb     11.92
    71   17_RNAComposerAS2_2_rpr.pdb     12.01
    25     17_DasExtraInfo_2_rpr.pdb     12.07
    11         17_Bujnicki_8_rpr.pdb     12.22
    70   17_RNAComposerAS2_1_rpr.pdb     12.31
    1           17_Adamiak_1_rpr.pdb     12.33
    3           17_Adamiak_3_rpr.pdb     12.38
    74   17_RNAComposerAS2_5_rpr.pdb     12.56
    75   17_RNAComposerAS2_6_rpr.pdb     12.79
    76   17_RNAComposerAS2_7_rpr.pdb     12.83
    43             17_Ding_7_rpr.pdb     12.86
    26     17_DasExtraInfo_3_rpr.pdb     13.22
    46            17_Ding_10_rpr.pdb     13.39
    59           17_Major_10_rpr.pdb     13.40
    77   17_RNAComposerAS2_8_rpr.pdb     13.51
    73   17_RNAComposerAS2_4_rpr.pdb     13.52
    86             17_Xiao_7_rpr.pdb     13.84
    8          17_Bujnicki_5_rpr.pdb     13.95
    12         17_Bujnicki_9_rpr.pdb     13.97
    4          17_Bujnicki_1_rpr.pdb     13.97
    88             17_Xiao_9_rpr.pdb     14.10
    9          17_Bujnicki_6_rpr.pdb     14.35
    5          17_Bujnicki_2_rpr.pdb     14.40
    13        17_Bujnicki_10_rpr.pdb     14.40
    39             17_Ding_3_rpr.pdb     14.53
    84             17_Xiao_5_rpr.pdb     14.54
    6          17_Bujnicki_3_rpr.pdb     14.64
    19             17_Chen_6_rpr.pdb     14.75
    44             17_Ding_8_rpr.pdb     14.81
    29              17_Das_3_rpr.pdb     14.90
    55            17_Major_6_rpr.pdb     14.94
    80             17_Xiao_1_rpr.pdb     15.01
    37             17_Ding_1_rpr.pdb     15.02
    49        17_Dohkolyan_3_rpr.pdb     15.02
    17             17_Chen_4_rpr.pdb     15.14
    31              17_Das_5_rpr.pdb     15.38
    82             17_Xiao_3_rpr.pdb     15.50
    89            17_Xiao_10_rpr.pdb     15.52
    22             17_Chen_9_rpr.pdb     15.59
    79  17_RNAComposerAS2_10_rpr.pdb     15.59
    40             17_Ding_4_rpr.pdb     15.74
    87             17_Xiao_8_rpr.pdb     15.93
    41             17_Ding_5_rpr.pdb     16.01
    7          17_Bujnicki_4_rpr.pdb     16.08
    38             17_Ding_2_rpr.pdb     16.09
    78   17_RNAComposerAS2_9_rpr.pdb     16.10
    14             17_Chen_1_rpr.pdb     16.11
    48        17_Dohkolyan_2_rpr.pdb     16.27
    56            17_Major_7_rpr.pdb     16.47
    20             17_Chen_7_rpr.pdb     16.50
    81             17_Xiao_2_rpr.pdb     16.55
    58            17_Major_9_rpr.pdb     16.59
    21             17_Chen_8_rpr.pdb     16.61
    57            17_Major_8_rpr.pdb     16.69
    45             17_Ding_9_rpr.pdb     16.74
    50            17_Major_1_rpr.pdb     16.85
    42             17_Ding_6_rpr.pdb     16.94
    52            17_Major_3_rpr.pdb     17.05
    85             17_Xiao_6_rpr.pdb     17.26
    16             17_Chen_3_rpr.pdb     17.35
    83             17_Xiao_4_rpr.pdb     17.42
    36             17_Das_10_rpr.pdb     17.43
    67   17_RNAComposerAS1_8_rpr.pdb     17.60
    62   17_RNAComposerAS1_3_rpr.pdb     17.95
    51            17_Major_2_rpr.pdb     18.05
    69  17_RNAComposerAS1_10_rpr.pdb     18.45
    54            17_Major_5_rpr.pdb     18.46
    53            17_Major_4_rpr.pdb     18.67
    60   17_RNAComposerAS1_1_rpr.pdb     18.78
    65   17_RNAComposerAS1_6_rpr.pdb     18.91
    23            17_Chen_10_rpr.pdb     18.99
    68   17_RNAComposerAS1_9_rpr.pdb     19.67
    64   17_RNAComposerAS1_5_rpr.pdb     20.03
    63   17_RNAComposerAS1_4_rpr.pdb     20.06
    66   17_RNAComposerAS1_7_rpr.pdb     20.65
    61   17_RNAComposerAS1_2_rpr.pdb     21.58
    47        17_Dohkolyan_1_rpr.pdb     21.78
    csv was created!  rmsds.csv

INFs
-------------------------------------------------------------------------------

    for i in *pdb; do rna_pdb_toolsx.py --delete A:48-51 $i > clarna/$i ; done
