v1.1.2 170727 
----------------------------------------------------------------

Fix annotation of rp06, calc rmsd once again.

v1.1.1 170727
----------------------------------------------------------------

Fix alignment of target and solution seq of rp12.

v1.1 170713 
----------------------------------------------------------------

Fix #3 Add missing models of rp14_bound of Bujnicki group (submitted with modified sequence (see the Bujnicki folder))

Fix #1 and #2

In readmes, `native` -> `solution`.

Following fixes where applied:
	
    sed -i -e '/HEADER ver None/d' *.pdb ;
    sed -i -e 's/HEADER /REMARK 250 /g' *pdb ;
    sed -i -e 's/REMARK 000/REMARK 250/g' *pdb ;

Now the header syntax should look like:

    [mm] rp17$ git:(master) ✗ head *.pdb
    ==> 17_5k7c_solution_rpr.pdb <==
    REMARK 250 Generated with rna-pdb-tools
    REMARK 250 ver ea5e310-dirty
    REMARK 250 https://github.com/mmagnus/rna-pdb-tools
    REMARK 250 Tue May 16 11:43:45 2017
    REMARK 250 Fixed atoms/residues:
    REMARK 250 -  add O2'  in chain: A <Residue G het=  resseq=57 icode= > residue # 53
    ATOM      1  P     C A   1     -29.720 -19.750   3.190  1.00183.16           P
    ATOM      2  OP1   C A   1     -28.490 -20.280   2.531  1.00180.35           O
    ATOM      3  OP2   C A   1     -29.638 -18.728   4.275  1.00185.39           O
    ATOM      4  O5'   C A   1     -30.685 -20.928   3.695  1.00186.30           O

Sometimes rna-pdb-tools generated error in the version line:

	REMARK 250 ver fatal: Not a git repository (or any parent up to mount point /Volumes/mqaprna)
	Stopping at filesystem boundary (GIT_DISCOVERY_ACROSS_FILESYSTEM not set).

or 
	HEADER ver None 
