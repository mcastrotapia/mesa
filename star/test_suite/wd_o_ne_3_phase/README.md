This test case demonstrates the implementation of three-component phase separation in an ONeNa white dwarf (see [Castro-Tapia & Cumming 2025](https://iopscience.iop.org/article/10.3847/1538-4357/adf745)).

##Part 1## (`inlist_create_wd`) (optional) creates an $8.3 M_{\odot}$, $Z = 0.02$ metallicity pre-main-sequence star and evolves it to the end of the AGB phase. The result is a $1.1 M_{\odot}$ ONeNa white dwarf. Since this is a "sped-up" method for producing an O/Ne white dwarf, it is recommended to accrete some helium and/or hydrogen onto the surface of the resulting white dwarf to obtain a more accurate cooling model. Alternatively, any white dwarf model can be used as the input model.

##Part 2## (`inlist_wd_o_ne_3_phase`) loads `wd1_10_mi8_3_ONeNa.mod`, a $1.1 M_{\odot}$ ONeNa white dwarf with a helium atmosphere, and evolves it until the core temperature drops below $2 \times 10^6 K$.

Throughout the white dwarf cooling phase, phase separation occurs as a result of crystallization. With `phase_separation_option = '3c'`, the three most abundant elements in the core that transition to the solid phase undergo fractionation, as predicted by ternary phase diagrams.

Example of the cooling before crystallization:
Plot1

Example with a portion of the core crystallized:
Plot2
