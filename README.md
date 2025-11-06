Explanation of Repo: 

# Notebooks

`AnalysisNotLF.ipynb` contains code that is being used to create figures in overleaf

`CorrectionFactorAllCode.ipynb` contains code for calculating SFR, creating ionization maps with LAEs, calculating radius and post-IGM transmission, and calculating LF 

`LuminosityFunctionCalculation9_19.ipynb` contains code for calculating LF (which is copy and pasted into `CorrectionFactorAllCode.ipynb`) and creating the Correction_Table.csv (which accounts for ionization from 12 M_sun > halos > 10 M_sun) 

`RunRadiusCalculations_9_19.ipynb` contains code for calculating the radius + transmission for different methods (A, B, B+C)

`bubble_viz_v2_9_19.ipynb` contains code copy + pasted into `CorrectionFactorAllCode.ipynb` that visuzlies the ionization maps (Austen's code) 

`calc_nion_v2_9_19.ipynb` from Austen, calculates ionizing photons for each galaxy 

`run_bubbles_v4_9_19.ipynb` from Austen, code to run the ionization maps, takes approx ~20 hours per realization 

# Folders
`AustenBubbles/AustenBubbles` contains notebooks gien from Austen at around March 

`OldNotebooks` contains jupyter notebooks that I have used to calculate LF, radius, transmission in the past and are dated, but may contain useful code, also is useful to know where all code comes from 

`Results` is a folder that contains all results from different runs 

`Results/AllMethods` contains results from where I used methods A, B, and B+C, but do not account for the correction factor from halos 

`Results/CorrectionFactorMaps` contains results (including .h5 & .pkl files from ionization map run) only using B+C method and include correction factor 
