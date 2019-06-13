# SrTiO relaxation 

the system in `srtio3_rlx.in` is distored. Run a molecular simulation with 
relax to relax it. Try first keeping the Ti atom fixed as is already done in 
the input, after it is is finished try letting the Ti atom to relax. 

command:
```
mpirun -np 4 pw.x < srtio3_rlx.in
```
  
