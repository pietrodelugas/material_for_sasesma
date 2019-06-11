# Convergence test of ecuthro

This exercise demonstrates that for PAW and USPP it is necessary
to check that the value of ecutrho is large enough. 

1. run `srtio3_ecutrho.0.in` with `pw.x` save the result in `out_ecutrho_160` 
   the name is not important obviously just note the ecutrho used in the run. 

2. run in succession `srtio3_ecutrho.in` updatng the value to always groowing 
   values (e.g 240, 320, 400, 480, 600). 

3. See how the value of the energy changes from run to run. 
   Comment on its behavior. 
   - Is it variational ?
   - Does the variation from run to run decrease enough ?

4. Note that in srtio3_ecutrho we reuse density and wavefunctions obtained in
   previous calculation. The scf error at the first step is a good measure of 
   how close are ground state densities at different ecutrho.
