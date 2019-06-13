---
title: "Convergence test"
output:
  github_document:
    pandoc_args: --webtex
---

# Convergence test (total energy vs ecutwfc )

ecutwc parameters controls the maximum length of the wave vectors of 
your plane wave basis set. In this exercise you have to run scf 
calculation increasing gradually the value of `ecutwfc`. At each calculation 
the plane waves basis set will include more wave vectors and for the 
variational principle the total energy at each calculation should 
decrease down until reache a converged value. 
Chose a cut-off energy such that you may consider the total energy converged 
down to an error of $1^{-6}$. 

1.  edit the `si.primitive.scf.in` file in order to use $6\times 6 \times 6$ 
    Monckorst-Pack mesh and run the first calcuation saving it in a file. 
    The launch command could be something like:
``` 
mpirun -np 4 pw.x < si.primitive.scf.in > out_ecut_20
```

2. edit the `si.primitive.scf.in` file increasing ecutwfc. You start from the 
density and wave functions save by your previous calculations. To do it add to 
the `&electrons` namelist these two flags:
```
startingpot = 'file'
startingwfc = 'file'
```

3. After you have run the calculation for a large enough set of ecutwfc values, collect your results in a file, plot them and chose the value of ecutwfc that 
guarantees you the deisred precision.    
