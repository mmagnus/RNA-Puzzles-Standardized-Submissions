RNA-Puzzle 18
-----------------------------------------------------------------------------

Solution sequence vs target sequence:

```
> 18_0_solution_5TPY_rpr A:1-71
GGGUCAGGCCGGCGAAAGUCGCCACAGUUUGGGGAAAGCUGUGCAGCCUGUAACCCCCCCACGAAAGUGGG

> 18_3dRNA_1_rpr A:1-71
GGGUCAGGCCGGCGAAAGUCGCCACAGUUUGGGGAAAGCUGUGCAGCCUGUAACCCCCCCACGAAAGUGGG
```

Problem with this file. Move to problms.

```
> 18_Nikolay_1_rpr A:1-40
GCAGGGCAAGGCCCAGUCCCGUGCAAGCCGGGACCGCCCC
> 18_Nikolay_1_rpr B:1-22
GGGGCGCGGCGCUCAUUCCUGC
```

Edits:

	for i in `ls *.pdb`; do rna_pdb_tools.py --get_rnapuzzle_ready $i > ${i/.pdb/_rpr.pdb}; done

Manual fix of `18_YagoubAli_1_rpr.pdb`.

Rmsd:

```
rna_calc_rmsd.py -t 18_0_solution_5TPY_rpr.pdb *.pdb
rmsd_calc_rmsd_to_target
--------------------------------------------------------------------------------
 method:
# of models: 53
18_0_solution_5TPY_rpr.pdb 7.91551679689e-15 1527
18_3dRNA_1_rpr.pdb 18.8213795921 1527
18_3dRNA_2_rpr.pdb 19.2070432535 1527
18_3dRNA_3_rpr.pdb 20.2868833898 1527
18_3dRNA_4_rpr.pdb 12.4490483491 1527
18_3dRNA_5_rpr.pdb 24.0911643547 1527
18_Chen_1_rpr.pdb 3.73973678164 1527
18_Chen_2_rpr.pdb 6.63581315583 1527
18_Chen_3_rpr.pdb 9.16534248085 1527
18_Chen_4_rpr.pdb 9.2730675006 1527
18_Chen_5_rpr.pdb 15.8483702839 1527
18_Dokholyan_1_rpr.pdb 8.44028913454 1527
18_Dokholyan_2_rpr.pdb 11.9535363029 1527
18_Dokholyan_3_rpr.pdb 7.90299493677 1527
18_Feng_1_rpr.pdb 20.280072492 1527
18_Feng_2_rpr.pdb 21.1300042248 1527
18_Feng_3_rpr.pdb 16.4499351342 1527
18_Feng_4_rpr.pdb 24.9244273108 1527
18_Feng_5_rpr.pdb 16.1484119123 1527
18_LeeASmodel_1_rpr.pdb 23.1716313885 1527
18_LeeASmodel_2_rpr.pdb 23.4978795436 1527
18_LeeASmodel_3_rpr.pdb 21.4250962129 1527
18_LeeASmodel_4_rpr.pdb 18.9184024542 1527
18_LeeASmodel_5_rpr.pdb 18.4541750956 1527
18_Lee_1_rpr.pdb 22.7929180415 1527
18_Lee_2_rpr.pdb 21.1589247669 1527
18_Lee_3_rpr.pdb 21.4210631233 1527
18_Lee_4_rpr.pdb 22.1575949544 1527
18_Lee_5_rpr.pdb 24.5493057266 1527
18_RNAComposer_1_rpr.pdb 20.7370369759 1527
18_RNAComposer_2_rpr.pdb 21.1431016393 1527
18_RNAComposer_3_rpr.pdb 20.6187055793 1527
18_RNAComposer_4_rpr.pdb 20.7737846893 1527
18_RNAComposer_5_rpr.pdb 15.210634288 1527
18_RW3D_1_rpr.pdb 16.3461695393 1527
18_RW3D_2_rpr.pdb 9.81956268696 1527
18_RW3D_3_rpr.pdb 12.490181049 1527
18_RW3D_4_rpr.pdb 11.5093148449 1527
18_RW3D_5_rpr.pdb 13.3624075748 1527
18_RW3D_6_rpr.pdb 10.3421142623 1527
18_RW3D_7_rpr.pdb 14.9572953509 1527
18_RW3D_8_rpr.pdb 15.7073229859 1527
18_RW3D_9_rpr.pdb 17.2076015535 1527
18_RW3D_10_rpr.pdb 13.3830149599 1527
18_Rhiju_1_rpr.pdb 5.49617190776 1527
18_Rhiju_2_rpr.pdb 3.87747762683 1527
18_Rhiju_3_rpr.pdb 5.63291859804 1527
18_Rhiju_4_rpr.pdb 5.69820182917 1527
18_Rhiju_5_rpr.pdb 10.9037306441 1527
18_YagoubAli_1_rpr.pdb 18.6711314368 1527
18_simRNA_1_rpr.pdb 23.1414073391 1527
18_simRNA_2_rpr.pdb 10.2767963136 1527
18_simRNA_3_rpr.pdb 24.6325094194 1527
# of atoms used: 1527
csv was created!  rmsds.csv
```
