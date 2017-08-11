### OPLS-aa parameters for perfluoroalkanes


 * Source: Watkins and Jorgensen, J. Phys. Chem. A, 105, 2001 pp 4118-4125 http://dx.doi.org/10.1021/jp004071w

 * Forcefield file initially created 04 August 2017 by C.R. Iacovella

#### Source Notes:
While all parameters are listed in Watkins and Jorgensen, bond and angle parameters have various original sources, as detailed in the manuscript.  
These are summarized below:
* CT-F Bonds come from reference http://dx.doi.org/10.1002/jcc.540130806
* F-CT-F angles are from reference http://dx.doi.org/10.1021/ja00124a002
* CT-CT-F angles are the same as CT-CT-OH and CT-CT-OS from reference: http://dx.doi.org/10.1021/ja00124a002
* Bonds and angles for the CT-CT and CT-CT-CT  are the same as for alkanes from reference, http://dx.doi.org/10.1021/ja9621760

#### Additional Notes:
* These are the "general" parameters for perfluoroalkanes; specific dihedrals exist for 4 and 5-mers
* The backbone dihedral specifically references opls_962 (i.e. C-CF2-C) rather than only using the "CT" class;
if only the "CT" class were used, this would create a conflict with alkane systems if the parameters were merged.
* To be consistent with conversions performed by OpenMM:
- The original parameters are defined as kcal/mol, this file uses kJ/mol; a conversion factor of 4.184 was used. 
- PI is defined as 3.141592653589 for conversion to radians.
* Atom type names, e.g., opls_961, correspond to those defined in the OPLS forcefield itp file distributed with GROMACS.
* Conversion from OPLS-style dihedrals to RB follow the formulas detailed in the GROMACS manual. Specifically,
OPLS form:
```bash
0.5*(F1*(1+cos(phi))+ F2*(1-cos(2phi))+ F3*(1+cos(3phi))+F4*(1-cos(4phi)))
```
RB mapping:
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


