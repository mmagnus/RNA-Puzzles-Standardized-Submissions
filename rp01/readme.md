
   for i in `ls *.pdb`; do rna_pdb_tools.py --get_seq $i; echo ''; done > seq.txt

Split one chain into two:

- 1_santalucia_1_rpr
- 1_major_1_rpr.pdb
- 1_das_5_rpr.pdb
- 1_das_4_rpr.pdb
- 1_das_3_rpr.pdb
- 1_das_2_rpr.pdb
- 1_das_1_rpr.pdb
- 1_chen_1_rpr.pdb
