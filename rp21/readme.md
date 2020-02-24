RNA-Puzzle 21
-----------------------------------------------------------------------------

Solution sequence vs target sequence:

    > 21_solution_2 A:1-41
    CCGGACGAGGUGCGCCGUACCCGGUCACGACAAGACGGCGC
    > 21_3dRNA_1_rpr A:1-41
    CCGGACGAGGUGCGCCGUACCCGGUCACGACAAGACGGCGC

Processing:

    rna_pdb_toolsx.py --rpr --inplace --dont_rename_chains *

RMSD
-------------------------------------------------------------------------------

    rna_calc_rmsd.py -t 21_solution_2_rpr.pdb *.pdb -pr -sr
    # method: all-atom-built-in
    # of models: 60
    # of atoms used: 881
                              fn  rmsd_all
    59     21_solution_2_rpr.pdb      0.00
    21   21_ChenLowLig_2_rpr.pdb      3.83
    16  21_ChenHighLig_2_rpr.pdb      3.83
    20   21_ChenLowLig_1_rpr.pdb      4.14
    15  21_ChenHighLig_1_rpr.pdb      4.14
    25     21_DasLORES_1_rpr.pdb      4.34
    26     21_DasLORES_2_rpr.pdb      4.55
    8       21_Adamiak_4_rpr.pdb      4.74
    7       21_Adamiak_3_rpr.pdb      4.75
    5       21_Adamiak_1_rpr.pdb      4.80
    6       21_Adamiak_2_rpr.pdb      4.81
    23   21_ChenLowLig_4_rpr.pdb      4.82
    18  21_ChenHighLig_4_rpr.pdb      4.82
    22   21_ChenLowLig_3_rpr.pdb      5.10
    17  21_ChenHighLig_3_rpr.pdb      5.10
    32          21_Das_3_rpr.pdb      5.19
    31          21_Das_2_rpr.pdb      5.62
    9       21_Adamiak_5_rpr.pdb      5.69
    30          21_Das_1_rpr.pdb      5.76
    33          21_Das_4_rpr.pdb      5.77
    34          21_Das_5_rpr.pdb      6.37
    13     21_Bujnicki_4_rpr.pdb      6.54
    28     21_DasLORES_4_rpr.pdb      6.59
    10     21_Bujnicki_1_rpr.pdb      6.87
    19  21_ChenHighLig_5_rpr.pdb      7.24
    24   21_ChenLowLig_5_rpr.pdb      7.24
    11     21_Bujnicki_2_rpr.pdb      9.02
    29     21_DasLORES_5_rpr.pdb      9.17
    57       21_simRNA_4_rpr.pdb     10.85
    55       21_simRNA_2_rpr.pdb     11.72
    54       21_simRNA_1_rpr.pdb     12.05
    0         21_3dRNA_1_rpr.pdb     12.09
    12     21_Bujnicki_3_rpr.pdb     12.14
    37  21_RNAComposer_3_rpr.pdb     12.23
    2         21_3dRNA_3_rpr.pdb     12.28
    1         21_3dRNA_2_rpr.pdb     12.41
    38  21_RNAComposer_4_rpr.pdb     13.02
    56       21_simRNA_3_rpr.pdb     13.29
    58       21_simRNA_5_rpr.pdb     13.29
    53  21_Sanbonmatsu_4_rpr.pdb     14.17
    52  21_Sanbonmatsu_3_rpr.pdb     14.17
    27     21_DasLORES_3_rpr.pdb     14.54
    51  21_Sanbonmatsu_2_rpr.pdb     14.60
    50  21_Sanbonmatsu_1_rpr.pdb     14.60
    35  21_RNAComposer_1_rpr.pdb     14.63
    41         21_RW3D_2_rpr.pdb     16.05
    49        21_RW3D_10_rpr.pdb     16.23
    45         21_RW3D_6_rpr.pdb     16.98
    39  21_RNAComposer_5_rpr.pdb     17.04
    4         21_3dRNA_5_rpr.pdb     17.49
    47         21_RW3D_8_rpr.pdb     17.66
    42         21_RW3D_3_rpr.pdb     17.81
    40         21_RW3D_1_rpr.pdb     17.92
    48         21_RW3D_9_rpr.pdb     18.03
    46         21_RW3D_7_rpr.pdb     18.05
    3         21_3dRNA_4_rpr.pdb     18.09
    44         21_RW3D_5_rpr.pdb     18.11
    43         21_RW3D_4_rpr.pdb     18.21
    36  21_RNAComposer_2_rpr.pdb     18.21
    14     21_Bujnicki_5_rpr.pdb     21.49
    csv was created!  rmsds.csv

INFs
-------------------------------------------------------------------------------

```
rna_calc_inf.py -t 21_solution_2_rpr.pdb *.pdb -sr -pr
 98% (54 of 55) |##################################################################################################################   | Elapsed Time: 0:00:02 ETA:   0:00:00csv was created!  inf.csv

(base) [mx] rp21$ git:(master) ✗ csv inf.csv
target                 fn                        inf_all  inf_stack  inf_WC  inf_nWC  sns_WC  ppv_WC  sns_nWC  ppv_nWC
21_solution_2_rpr.pdb  21_solution_2_rpr.pdb     1.0      1.0        1.0     1.0      1.0     1.0     1.0      1.0
21_solution_2_rpr.pdb  21_DasLORES_1_rpr.pdb     0.76     0.8        0.91    0.32     0.91    0.91    0.25     0.4
21_solution_2_rpr.pdb  21_Das_5_rpr.pdb          0.75     0.74       0.91    0.59     0.91    0.91    0.62     0.56
21_solution_2_rpr.pdb  21_DasLORES_2_rpr.pdb     0.73     0.74       0.91    0.35     0.91    0.91    0.25     0.5
21_solution_2_rpr.pdb  21_Bujnicki_4_rpr.pdb     0.72     0.73       0.91    0.25     0.91    0.91    0.12     0.5
21_solution_2_rpr.pdb  21_ChenHighLig_2_rpr.pdb  0.72     0.75       0.91    0.18     0.91    0.91    0.12     0.25
21_solution_2_rpr.pdb  21_ChenLowLig_2_rpr.pdb   0.72     0.75       0.91    0.18     0.91    0.91    0.12     0.25
21_solution_2_rpr.pdb  21_ChenLowLig_1_rpr.pdb   0.69     0.72       0.91    0.0      0.91    0.91    0.0      0.0
21_solution_2_rpr.pdb  21_ChenHighLig_1_rpr.pdb  0.69     0.72       0.91    0.0      0.91    0.91    0.0      0.0
21_solution_2_rpr.pdb  21_ChenHighLig_5_rpr.pdb  0.69     0.7        0.91    0.0      0.91    0.91    0.0      0.0
21_solution_2_rpr.pdb  21_ChenLowLig_5_rpr.pdb   0.69     0.7        0.91    0.0      0.91    0.91    0.0      0.0
21_solution_2_rpr.pdb  21_ChenHighLig_4_rpr.pdb  0.67     0.68       0.86    0.32     0.82    0.9     0.25     0.4
21_solution_2_rpr.pdb  21_ChenLowLig_4_rpr.pdb   0.67     0.68       0.86    0.32     0.82    0.9     0.25     0.4
21_solution_2_rpr.pdb  21_Bujnicki_2_rpr.pdb     0.67     0.69       0.91    0.0      0.91    0.91    0.0      0.0
21_solution_2_rpr.pdb  21_Bujnicki_1_rpr.pdb     0.66     0.7        0.86    0.13     0.82    0.9     0.12     0.14
21_solution_2_rpr.pdb  21_Das_2_rpr.pdb          0.65     0.7        0.91    0.11     0.91    0.91    0.12     0.09
21_solution_2_rpr.pdb  21_Das_4_rpr.pdb          0.64     0.68       0.87    0.13     0.91    0.83    0.12     0.14
21_solution_2_rpr.pdb  21_Adamiak_4_rpr.pdb      0.64     0.57       0.91    0.61     0.91    0.91    0.38     1.0
21_solution_2_rpr.pdb  21_DasLORES_4_rpr.pdb     0.63     0.65       0.87    0.0      0.91    0.83    0.0      0.0
21_solution_2_rpr.pdb  21_ChenHighLig_3_rpr.pdb  0.62     0.64       0.91    0.0      0.91    0.91    0.0      0.0
21_solution_2_rpr.pdb  21_ChenLowLig_3_rpr.pdb   0.62     0.64       0.91    0.0      0.91    0.91    0.0      0.0
21_solution_2_rpr.pdb  21_RNAComposer_4_rpr.pdb  0.62     0.57       0.95    0.0      0.91    1.0     0.0      0.0
21_solution_2_rpr.pdb  21_RNAComposer_3_rpr.pdb  0.61     0.56       0.95    0.0      0.91    1.0     0.0      0.0
21_solution_2_rpr.pdb  21_Das_1_rpr.pdb          0.61     0.65       0.91    0.11     0.91    0.91    0.12     0.1
21_solution_2_rpr.pdb  21_RW3D_9_rpr.pdb         0.6      0.7        0.55    0.14     0.55    0.55    0.12     0.17
21_solution_2_rpr.pdb  21_DasLORES_5_rpr.pdb     0.6      0.6        0.87    0.0      0.91    0.83    0.0      0.0
21_solution_2_rpr.pdb  21_RW3D_6_rpr.pdb         0.59     0.68       0.55    0.16     0.55    0.55    0.12     0.2
21_solution_2_rpr.pdb  21_Adamiak_3_rpr.pdb      0.59     0.48       0.91    0.61     0.91    0.91    0.38     1.0
21_solution_2_rpr.pdb  21_DasLORES_3_rpr.pdb     0.59     0.59       0.84    0.0      0.91    0.77    0.0      0.0
21_solution_2_rpr.pdb  21_3dRNA_4_rpr.pdb        0.58     0.63       0.64    0.0      0.55    0.75    0.0      0.0
21_solution_2_rpr.pdb  21_RW3D_3_rpr.pdb         0.58     0.68       0.55    0.13     0.55    0.55    0.12     0.14
21_solution_2_rpr.pdb  21_Adamiak_5_rpr.pdb      0.58     0.5        0.91    0.35     0.91    0.91    0.12     1.0
21_solution_2_rpr.pdb  21_simRNA_4_rpr.pdb       0.57     0.68       0.47    0.0      0.55    0.4     0.0      0.0
21_solution_2_rpr.pdb  21_Adamiak_1_rpr.pdb      0.57     0.5        0.91    0.35     0.91    0.91    0.12     1.0
21_solution_2_rpr.pdb  21_RW3D_10_rpr.pdb        0.56     0.68       0.52    0.0      0.55    0.5     0.0      0.0
21_solution_2_rpr.pdb  21_3dRNA_5_rpr.pdb        0.56     0.64       0.55    0.0      0.55    0.55    0.0      0.0
21_solution_2_rpr.pdb  21_Das_3_rpr.pdb          0.56     0.53       0.91    0.24     0.91    0.91    0.25     0.22
21_solution_2_rpr.pdb  21_RW3D_8_rpr.pdb         0.55     0.65       0.52    0.0      0.55    0.5     0.0      0.0
21_solution_2_rpr.pdb  21_Adamiak_2_rpr.pdb      0.55     0.45       0.87    0.5      0.91    0.83    0.25     1.0
21_solution_2_rpr.pdb  21_RW3D_4_rpr.pdb         0.55     0.66       0.52    0.0      0.55    0.5     0.0      0.0
21_solution_2_rpr.pdb  21_RW3D_2_rpr.pdb         0.54     0.66       0.52    0.0      0.55    0.5     0.0      0.0
21_solution_2_rpr.pdb  21_simRNA_2_rpr.pdb       0.54     0.66       0.45    0.0      0.55    0.38    0.0      0.0
21_solution_2_rpr.pdb  21_RNAComposer_2_rpr.pdb  0.52     0.57       0.57    0.0      0.55    0.6     0.0      0.0
21_solution_2_rpr.pdb  21_RW3D_1_rpr.pdb         0.52     0.61       0.52    0.0      0.55    0.5     0.0      0.0
21_solution_2_rpr.pdb  21_RW3D_7_rpr.pdb         0.52     0.63       0.52    0.0      0.55    0.5     0.0      0.0
21_solution_2_rpr.pdb  21_simRNA_3_rpr.pdb       0.5      0.61       0.4     0.0      0.46    0.36    0.0      0.0
21_solution_2_rpr.pdb  21_simRNA_1_rpr.pdb       0.5      0.58       0.47    0.0      0.55    0.4     0.0      0.0
21_solution_2_rpr.pdb  21_RW3D_5_rpr.pdb         0.5      0.58       0.52    0.0      0.55    0.5     0.0      0.0
21_solution_2_rpr.pdb  21_simRNA_5_rpr.pdb       0.5      0.61       0.4     0.0      0.46    0.36    0.0      0.0
21_solution_2_rpr.pdb  21_Bujnicki_3_rpr.pdb     0.5      0.57       0.45    0.0      0.55    0.38    0.0      0.0
21_solution_2_rpr.pdb  21_RNAComposer_5_rpr.pdb  0.49     0.55       0.55    0.0      0.55    0.55    0.0      0.0
21_solution_2_rpr.pdb  21_Sanbonmatsu_1_rpr.pdb  0.48     0.5        0.57    0.0      0.55    0.6     0.0      0.0
21_solution_2_rpr.pdb  21_Sanbonmatsu_2_rpr.pdb  0.48     0.5        0.57    0.0      0.55    0.6     0.0      0.0
21_solution_2_rpr.pdb  21_Sanbonmatsu_3_rpr.pdb  0.48     0.52       0.52    0.0      0.55    0.5     0.0      0.0
21_solution_2_rpr.pdb  21_Sanbonmatsu_4_rpr.pdb  0.48     0.52       0.52    0.0      0.55    0.5     0.0      0.0
21_solution_2_rpr.pdb  21_3dRNA_3_rpr.pdb        0.46     0.48       0.6     0.0      0.36    1.0     0.0      0.0
21_solution_2_rpr.pdb  21_RNAComposer_1_rpr.pdb  0.45     0.54       0.43    0.13     0.36    0.5     0.12     0.14
21_solution_2_rpr.pdb  21_3dRNA_2_rpr.pdb        0.43     0.45       0.6     0.0      0.36    1.0     0.0      0.0
21_solution_2_rpr.pdb  21_3dRNA_1_rpr.pdb        0.4      0.41       0.6     0.0      0.36    1.0     0.0      0.0
21_solution_2_rpr.pdb  21_Bujnicki_5_rpr.pdb     0.36     0.51       0.0     0.0      0.0     0.0     0.0      0.0

```


Archive
-------------------------------------------------------------------------------

In the archive folder, there are more solution structures with one mismatch compared to the target sequence.

    CCGGACGAGGUGCGCCGUACCCGGUCAGGACAAGACGGCGC # 21_solution_0_rpr
    CCGGACGAGGUGCGCCGUACCCGGUCACGACAAGACGGCGC # 21_3dRNA_1_rpr
                               x mismatch

    [mm] archive$ git:(master) ✗ rna_pdb_toolsx.py --get_seq *
    # 21_solution_0
    > A:1-41
    CCGGACGAGGUGCGCCGUACCCGGUCAGGACAAGACGGCGC
    > B:1-41
    CCGGACGAGGUGCGCCGUACCCGGUCAGGACAAGACGGCGC
    # 21_solution_1
    > A:1-41
    CCGGACGAGGUGCGCCGUACCCGGUCAGGACAAGACGGCGC
    > B:1-41
    CCGGACGAGGUGCGCCGUACCCGGUCAGGACAAGACGGCGC
    # 21_solution_2
    > A:1-41
    CCGGACGAGGUGCGCCGUACCCGGUCACGACAAGACGGCGC
    
Solutions
-------------------------------------------------------------------------------

![](solutions/rp21-solutions.png)
