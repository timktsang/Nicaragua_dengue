# Nicaragua_dengue

In a project of modeling dengue transmission in a prospective pediatric cohort in Nicaragua, we developed a software program in R coupled with C++ for simulating dengue epidemics and for making Bayesian inference on serotype-specific infection risks and associated effects of historical infections as well as other risk factors, while accounting for incompletely observed infection history and disease outcomes. To reduce the computational burden of sampling unobserved infection history, the program offers the option of sampling either two serotypes or all four serotypes simultaneously. This program can be generalized to cohort data of other infectious pathogens for which reliable surveillance data exist.

The raw data cannot be publised due to IRBs requirement. Therefore, a data template is provided.

Soucre_data.zip is the zip file for the source file for all table/figure in the manuscript.

R_code_for_figures.zip is the file for the R code that used to generate figures/tables.

Code_for_simulation_and_analysis.zip is the zip file for the code for simulation and analysis using 1/2/4 serotype sampling when updating infection histroy.
