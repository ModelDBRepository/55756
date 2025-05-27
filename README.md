Note: the following is a local copy of a page from the Rudy lab web site:
[http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/HRD%20Introduction.html](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/HRD%20Introduction.html).

---

# The Hund-Rudy Dynamic (HRd) Model of the Canine Ventricular Myocyte

| ![HRD schematic](index_files/HRD%2520schematic.gif) | The Hund-Rudy dynamic (HRd) model is based on data from the canine epicardial ventricular myocyte. Rate-dependent phenomena associated with ion channel kinetics, action potential properties and Ca<sup>2+</sup> handling are simulated by the model. Distinguishing features of the HRd include (1) regulation of Ca<sup>2+</sup>-handling by Ca<sup>2+</sup>/calmodulin dependent protein kinase (CaMKII), (2) incorporation of the late Na<sup>+</sup> current (I<sub>NaL</sub>) and Ca<sup>2+</sup> dependent transient outward current (I<sub>to2</sub>, in addition to I<sub>to1</sub>), (3) dynamic intracellular Cl<sup>-</sup> handling and (4) a novel formulation of calcium release from the junctional sarcoplasmic reticulum (JSR). Interaction between dihydropyridine receptors (I<sub>CaL</sub>) and ryanodine receptors (RyR) occurs in a restricted Ca<sup>2+</sup> subspace. The calcium release formulation incorporates activation of RyR by I<sub>CaL</sub>, Ca<sup>2+</sup>-dependent inactivation of RyR, and modulation of RyR open-probability by both JSR and subspace Ca<sup>2+</sup>. |
|---|---|

**Originally published in:**

"Rate dependence and regulation of action potential and calcium transient
in a canine cardiac ventricular cell model."
Hund TJ, Rudy Y.
[**Circulation. 2004 Nov 16;110(20):4008-74.**](http://circ.ahajournals.org/cgi/content/full/110/20/3168)

**ERRATUM**:

In the online supplement for the HRD code, there is a typo in the formulation of the Na<sup>+</sup> current rate constant. The equation should read:

If _V_ mV,

![Equation 1](index_files/image004.gif)

![Equation 2](index_files/image006.gif)

---

## SIMULATION NOTES:

- [Note on achieving steady state during ultra-long term continuous pacing.](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/ultra-long%20pacing.htm)
- [Note on modifications to HRD code for simulation of propagation.](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/HRD%20propagation%20simulation.htm)

|   |   |
|---|---|
|   | **To directly access the C++ code, (Last updated on September 29, 2005) [click here](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/HRD%20Code.html).** |
|   | **To download the Matlab code, (Last updated on October 5, 2005.  Backward Compatibility with Matlab 6.5) [click here](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/HRd2004.zip).** |
|   | **For sample output, and directions on how to use the code [click here](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/using%20the%20HRD.htm).** |
|   | **To view a concise description of the model formulations, [click here](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/formulation.html).** |
|   | **Question about the model?** [Email Tom Hund.](mailto:thund@pathology.wustl.edu) **Question about the code?** [Email Keith Decker](mailto:kfd1@cec.wustl.edu) |

---

# Linked Index to the C++ Code and Descriptions of Formulations

| A. Currents                  | Variable | Formulation                                                                 | Code Definition                                                                                     | Code Implementation                                                                                   |
|-----------------------------|----------|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| 1. fast Na+ current          | ina      | [link](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/formulation.html#formIna)            | [definition](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/HRD%20Code.html#classHRDina)    | [implementation](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/HRD%20Code.html#implementHRDina)        |
| 2. late Na+ current          | inal     | [link](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/formulation.html#formInal)           | [definition](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/HRD%20Code.html#classHRDinal)   | [implementation](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/HRD%20Code.html#implementHRDinal)      |
| 3. L-type Ca2+ current       | ical     | [link](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/formulation.html#formIcal)            | [definition](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/HRD%20Code.html#classHRDical)    | [implementation](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/HRD%20Code.html#implementHRDical)        |
| 4. rapid delayed rectifier K+ current | ikr      | [link](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/formulation.html#formIkr)             | [definition](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/HRD%20Code.html#classHRDikr)    | [implementation](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/HRD%20Code.html#implementHRDikr)        |
| 5. slow delayed rectifier K+ current | iks      | [link](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/formulation.html#formIks)             | [definition](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/HRD%20Code.html#classHRDiks)    | [implementation](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/HRD%20Code.html#implementHRDiks)        |
| 6. 4AP-sensitive transient outward K+ current | ito1     | [link](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/formulation.html#formIto1)            | [definition](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/HRD%20Code.html#classHRDito1)   | [implementation](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/HRD%20Code.html#implementHRDito1)      |
| 7. Ca2+ dependent transient outward Cl- current | ito2     | [link](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/formulation.html#formIto2)            | [definition](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/HRD%20Code.html#classHRDito2)   | [implementation](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/HRD%20Code.html#implementHRDito2)      |
| 8. time-independent K+ current | ik1      | [link](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/formulation.html#formIk1)             | [definition](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/HRD%20Code.html#classHRDik1)    | [implementation](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/HRD%20Code.html#implementHRDik1)        |
| 9. background Ca2+ current    | icab     | [link](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/formulation.html#formIcab)            | [definition](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/HRD%20Code.html#classHRDicab)   | [implementation](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/HRD%20Code.html#implementHRDicab)      |
| 10. plateau K+ current         | ikp      | [link](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/formulation.html#formIkp)             | [definition](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/HRD%20Code.html#classHRDikp)    | [implementation](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/HRD%20Code.html#implementHRDikp)        |
| 11. Cl- background current    | iclb     | [link](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/formulation.html#formIclb)            | [definition](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/HRD%20Code.html#classHRDiclb)   | [implementation](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/HRD%20Code.html#implementHRDiclb)      |

| B. Pumps and Exchangers       | Variable | Formulation | Code Definition | Code Implementation |
|------------------------------|----------|-------------|-----------------|---------------------|
| 1. Na+-Ca2+ exchanger          | inaca    | [link](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/formulation.html#formInaca)         | [definition](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/HRD%20Code.html#classHRDinaca) | [implementation](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/HRD%20Code.html#implementHRDinaca)   |
| 2. Na+-K+ pump                | inak     | [link](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/formulation.html#formInak)            | [definition](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/HRD%20Code.html#classHRDinak)   | [implementation](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/HRD%20Code.html#implementHRDinak)     |
| 3. Sarcolemmal Ca2+ pump           | ipca     | [link](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/formulation.html#formIpca)            | [definition](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/HRD%20Code.html#classHRDipca)   | [implementation](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/HRD%20Code.html#implementHRDipca)      |

| C. Transporters               | Variable | Formulation | Code Definition | Code Implementation |
|------------------------------|----------|-------------|-----------------|---------------------|
| 1. Na+-Cl- cotransporter      | ctnacl   | [link](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/formulation.html#formNacl)          | [definition](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/HRD%20Code.html#classHRDnacl) | [implementation](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/HRD%20Code.html#implementHRDnacl)     |
| 2. K+-Cl- cotransporter       | ctkcl    | [link](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/formulation.html#formKcl)           | [definition](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/HRD%20Code.html#classHRDkcl)  | [implementation](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/HRD%20Code.html#implementHRDkcl)      |

| D. Ionic Fluxes              | Variable | Formulation                                                                 | Code Definition                                                                                     | Code Implementation                                                                                   |
|-----------------------------|----------|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| 1. Ca2+ leak from JSR to myoplasm  | qleak    | [link](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/formulation.html#formQleak)          | [definition](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/HRD%20Code.html#classHRDqleak) | [implementation](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/HRD%20Code.html#implementHRDqleak)   |
| 2. Ca2+ release from JSR to subspace | qrelease | [link](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/formulation.html#formQrel)           | [definition](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/HRD%20Code.html#classHRDqrel) | [implementation](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/HRD%20Code.html#implementHRDqrel)    |
| 3. Ca2+ transfer from NSR to JSR | qtr      | [link](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/formulation.html#formQtr)            | [definition](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/HRD%20Code.html#classHRDqtr)  | [implementation](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/HRD%20Code.html#implementHRDqtr)     |
| 4. Ca2+ uptake from myoplasm to NSR | qup      | [link](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/formulation.html#formQup)             | [definition](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/HRD%20Code.html#classHRDqup)    | [implementation](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/HRD%20Code.html#implementHRDqup)        |

| E. Dynamic Concentrations    | Variable | Formulation                                                                 | Code Implementation                                                                                   |
|-----------------------------|----------|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| 1. myoplasmic Na+            | nai      | [link](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/formulation.html#formNai)            | [implementation](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/HRD%20Code.html#implementHRDconc) |
| 2. myoplasmic K+             | ki       | [link](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/formulation.html#formKi)             | [implementation](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/HRD%20Code.html#implementHRDconc)   |
| 3. myoplasmic Cl-            | cli      | [link](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/formulation.html#formClli)            | [implementation](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/HRD%20Code.html#implementHRDconc)   |
| 4. myoplasmic Ca2+           | cai      | [link](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/formulation.html#formCai)             | [implementation](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/HRD%20Code.html#implementHRDconc)   |
| 5. JSR Ca2+                  | cajsr    | [link](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/formulation.html#formCajsr)           | [implementation](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/HRD%20Code.html#implementHRDconc)   |
| 6. NSR Ca2+                  | cansr    | [link](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/formulation.html#formCansr)           | [implementation](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/HRD%20Code.html#implementHRDconc)   |
| 7. restricted space Ca2+     | car      | [link](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/formulation.html#formCar)             | [implementation](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/HRD%20Code.html#implementHRDconc)   |
| 8. CaMKinase                | camk     | [link](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/formulation.html#formCamk)            | [implementation](http://rudylab.wustl.edu/research/cell/methodology/cellmodels/HRd/HRD%20on%20the%20web/HRD%20Code.html#implementHRDconc)   |

---

2025-05-27 – Standardized to Markdown.