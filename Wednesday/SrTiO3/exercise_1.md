# STO dos exercise

In this exercise you will compute the DOS of SrTiO_3. 

* First step do a self consistent computation. Input is ready to be run:
the command is 
```
mpirun -np 4 pw.x -i srtio3_scf.in > srtio3_scf_out
```

* Second step compute the eigenvalues and wavefunctions in a denser grid. This computation will be non self consistent. The program will read the charge density saved in the previous run. It will initialize the hamiltonian and compute the eigenvalues in the new mesh of k-points without recalculating the charge. 
```
mpirun -np 4 pw.x -i srtio3_nscf.in > srtio3_nscf_out 
```

* Now the eigenvalues are saved in the srtio.save file. The program dos.x will read them and compute the density of states. The command is:
```
dos.x < input_dos > outdos 
```

Plot the file with: 
```
xmgrace -nxy srtio.dos
```

* Look at the plot the one plot is the density of states the other one is the ingrated density of states. Knowing that in the cell there are 40 valence electron what is the highest occupied eigenvalue ? 
 
 	
