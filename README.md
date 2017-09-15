### OPLS-aa parameters for alkylsilanes


 * Source: Lorentz, Webb, Stevens, Chandross, and Grest, Tribology Letters, 19, 2005 pp 93-98 http://dx.doi.org/10.1007/s11249-005-5085-4

 * Forcefield file initially created 14 September 2017 by A.Z. Summers

#### Source Notes:

#### Additional Notes:
* To be consistent with conversions performed by OpenMM (http://openmm.org)
    - The original parameters are defined as kcal/mol, this file uses kJ/mol; a conversion factor of 4.184 was used. 
    - PI is defined as 3.141592653589 for conversion to radians.
* Conversion from OPLS-style dihedrals to RB follow the formulas detailed in the GROMACS manual (http://gromacs.org). 
    * Specifically, the OPLS form is given as:
```bash
0.5*(F1*(1+cos(phi))+ F2*(1-cos(2phi))+ F3*(1+cos(3phi))+F4*(1-cos(4phi)))
```
   * The RB mapping:
```bash
c0 = F2+0.5*(F1+F3)
c1 = 0.5*(-F1+3F3)
c2 = -F2 + 4F4
c3 = -2F3
c4 = -4F4
c5 = 0
```

* Example molecules with correct atomtypes are defined as test cases. Execute the testing script using `py.test -v --tb=line`

### Force field DOI


