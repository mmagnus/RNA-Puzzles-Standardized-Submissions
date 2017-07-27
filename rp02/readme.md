RNA-Puzzle 02
-----------------------------------------------------------------------------

Crazy manually fixing with PyMOL.

There is a gap in the solution, chain G:

    > 2_0_solution G:1-10 13-15
    CCGGAGGAACCUG


Solution sequence vs target sequence:

```
> 2_0_solution A:1-15
CCGGAGGAACUACUG
> 2_0_solution B:1-10
CCGGCAGCCU
> 2_0_solution C:1-15
CCGGAGGAACUACUG
> 2_0_solution D:1-10
CCGGCAGCCU
> 2_0_solution E:1-15
CCGGAGGAACUACUG
> 2_0_solution F:1-10
CCGGCAGCCU
> 2_0_solution G:1-10 13-15
CCGGAGGAACCUG
> 2_0_solution H:1-10
CCGGCAGCCU

> 2_bujnicki_1_rpr A:1-15
CCGGAGGAACUACUG
> 2_bujnicki_1_rpr B:1-10
CCGGCAGCCU
> 2_bujnicki_1_rpr C:1-15
CCGGAGGAACUACUG
> 2_bujnicki_1_rpr D:1-10
CCGGCAGCCU
> 2_bujnicki_1_rpr E:1-15
CCGGAGGAACUACUG
> 2_bujnicki_1_rpr F:1-10
CCGGCAGCCU
> 2_bujnicki_1_rpr G:1-15
CCGGAGGAACUACUG
> 2_bujnicki_1_rpr H:1-10
CCGGCAGCCU
```

I gave up in fixing `problem/2_major_1_rpr.pdb`.

Edits:

	for i in `ls *pdb*`; do rna_pdb_tools.py --rpr $i --inplace;done

```
rna_calc_rmsd.py -t 2_0_solution.pdb --target_selection A:1-15+B:1-10+C:1-15+D:1-10+E:1-15+F:1-10+G:1-10+13-15+H:1-10 --model_selection A:1-15+B:1-10+C:1-15+D:1-10+E:1-15+F:1-10+G:1-10+13-15+H:1-10 *.pdb
rmsd_calc_rmsd_to_target
--------------------------------------------------------------------------------
method: all-atom-built-in
# of models: 13
2_0_solution.pdb 0.0 2094
2_bujnicki_1_rpr.pdb 2.66 2094
2_bujnicki_2_rpr.pdb 2.3 2094
2_bujnicki_3_rpr.pdb 2.33 2094
2_chen_1_rpr.pdb 2.82 2094
2_das_1_rpr.pdb 2.5 2094
2_das_2_rpr.pdb 3.04 2094
2_das_3_rpr.pdb 3.03 2094
2_das_4_rpr.pdb 2.83 2094
2_das_5_rpr.pdb 3.46 2094
2_dokholyan_1_rpr.pdb 2.55 2094
2_santalucia_1_rpr.pdb 3.66 2094
2_wildauer_1_rpr.pdb 3.46 2094
# of atoms used: 2094
csv was created!  rmsds.csv
```

```
rna_calc_inf.py -t 2_0_solution.pdb *.pdb
100% (13 of 13) |#####################################################################################################################################################| Elapsed Time: 0:02:11 ETA:  0:00:00csv was created!  inf.csv
target                  fn                            inf_all  inf_stack  inf_WC  inf_nWC  sns_WC  ppv_WC  sns_nWC  ppv_nWC
2_0_solution.pdb.outCR  2_0_solution.pdb.outCR        1.000    0.000      1.000   1.000    1.000   1.000   1.000    1.000
2_0_solution.pdb.outCR  2_das_4_rpr.pdb.outCR         0.923    0.000      0.973   0.333    1.000   0.946   0.333    0.333
2_0_solution.pdb.outCR  2_das_1_rpr.pdb.outCR         0.923    0.000      0.960   0.408    1.000   0.921   0.333    0.500
2_0_solution.pdb.outCR  2_das_3_rpr.pdb.outCR         0.912    0.000      0.973   0.289    1.000   0.946   0.333    0.250
2_0_solution.pdb.outCR  2_bujnicki_1_rpr.pdb.outCR    0.912    0.000      0.960   0.333    1.000   0.921   0.333    0.333
2_0_solution.pdb.outCR  2_das_2_rpr.pdb.outCR         0.935    0.000      0.973   0.408    1.000   0.946   0.333    0.500
2_0_solution.pdb.outCR  2_bujnicki_3_rpr.pdb.outCR    0.868    0.000      0.901   0.408    0.914   0.889   0.333    0.500
2_0_solution.pdb.outCR  2_bujnicki_2_rpr.pdb.outCR    0.895    0.000      0.917   0.577    0.943   0.892   0.333    1.000
2_0_solution.pdb.outCR  2_chen_1_rpr.pdb.outCR        0.905    0.000      0.943   0.000    0.943   0.943   0.000    0.000
2_0_solution.pdb.outCR  2_santalucia_1_rpr.pdb.outCR  0.898    0.000      0.935   0.000    1.000   0.875   0.000    0.000
2_0_solution.pdb.outCR  2_wildauer_1_rpr.pdb.outCR    0.890    0.000      0.928   0.000    0.914   0.941   0.000    0.000
2_0_solution.pdb.outCR  2_dokholyan_1_rpr.pdb.outCR   0.909    0.000      0.932   0.577    0.971   0.895   0.333    1.000
2_0_solution.pdb.outCR  2_das_5_rpr.pdb.outCR         0.921    0.000      0.973   0.000    1.000   0.946   0.000    0.000
```
