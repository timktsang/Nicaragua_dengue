# Nicaragua_dengue

Here we provide code and data related to our paper titled “Effects of Infection History on Dengue Virus Infection and Pathogenicity” published in Nature Communications. This paper is about modeling infection and disease dynamics of the four dengue serotypes in a prospective pediatric cohort in Nicaragua. Using R coupled with C++, we simulated dengue epidemics and conducted Bayesian inference on serotype-specific annual probabilities of infection, probabilities of subsequent disease given infection, and effects of prior infections, age and socioeconomic indicators. Our method and code are suitable when you have both longitudinal cohort data and reliable surveillance data, but the underlying infection outcomes are only partially observed.

The raw data cannot be made publicly available due to IRBs requirements. Interested parties can send inquiries to the UC Berkeley Center for the Protection of Human Subjects at ophs@berkeley.edu.

Soucre_data.zip is a zipped folder containing summary data for generating Figures 1-4 and Supplementary Figures 1-3  in the manuscript.

R_code_for_figure.zip is a zipped folder containing R code files that read in the summary data to generate the figures.

Code_for_simulation_and_analysis.zip is a zipped folder containing R and C++ programs for simulating dengue infection and disease epidemics in the cohort and for conducting Bayesian inference. The three subfolders correspond to sampling 1, 2 and 4 serotypes simultaneously, with the purpose to show that sampling all 4 serotypes together yields the best estimation. Taking 4-serotype sampling as an example, the R code “dengue_main_4serotype.R” is the major file, which will read in the data and call the C++ code file “dengue_4serotype.cpp”. The surveillance data is provided in “reported_n.txt”. As the raw data cannot be made publicly available, we provide a mock version of the data in a format needed by the C++ program. This data file is called “dengue_c_data.csv”. In simulation, this file provides the population structure for the hypothetical cohort. In data analysis, this file provides all the necessary infection and disease outcomes and covariates. This file has the following columns (columns like age and gender are self-obvious and thus not explained):

yinf_1 – yinf_4: infection years for serotypes 1-4. ‘-1’ indicates no infection, ‘999’ indicates unknown.

y0_1 – y0_4: indicate whether prior infection with serotypes 1-4 is possible or not; y0_5 indicates whether dengue-naïve at baseline is possible or not.

y1_1 – y1_4:  indicate whether infection with serotype 1-4 during year 1 is possible or not. y1_5 indicates whether no infection at all during year 1 is possible or not.

y2_1 – y2_5, y3_1 – y3_5, y4_1 – y4_5, y5_1 – y5_5, y6_1 – y6_5: similar as above, but for years 1-6 (corresponding to 2004-2009 for the Nicaragua cohort data).

elisa_0 – elisa_6: ELISA titer at baseline and at the end of years 1-6.

date_symptom_0: not used

date_symptom_1 - date_symptom_6: whether symptoms occurred during years 1-6

For simulation, extra covariates such as socioeconomic variables (home ownership, number of electronic fans) are not considered. For data analysis, these extra covariates should be merged with this data file
We also provided shell scripts for running the programs only as examples, as the actual shell commands needed may vary from system to system.
 
For questions regarding programs or summary data, please contact Tim Tsang at  timtsang@connect.hku.hk or Yang Yang at yangyang@ufl.edu
