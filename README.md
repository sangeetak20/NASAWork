To pull this repo, you will need to have had `git lfs` installed since that is how I was able to upload some of these files (GitHub is weird about file storage). You should be able to do this by typing into your terminal `brew install gitlfs` if you have a brew environment. If not, go here: https://docs.github.com/en/repositories/working-with-files/managing-large-files/installing-git-large-file-storage

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

# How to run these notebooks:
## Make sure to change the paths in all code, both for reading directories and for saving images/csv files 
1. Create nion.txt files using `calc_nion_v2_9_19.ipynb` (do not need to re-run this for each run, only need it once, unless you are changing the code itself
2. Run `run_bubbles_v4_9_19.ipynb` and make sure to change the paths for the directories, also changing the `real_no` since that represents different realizations/wide cones generated
3. Run `CorrectionFactorAllCode.ipynb` to get the LAEs, ionization maps with LAEs, radius, post-IGM transmission, and LF images

# Some Notes . . . 

`CorrectionFactorAllCode.ipynb` creates the following csv files: 
1. radius.csv: LAEs w/ redshift, radius (0-360 angle), lya-lum before transmission, lya-lum after transmission (0-360 angle)
2. pre_transmission_lf.csv / transmission_lf.csv: LF w/ errors and lum bins for both pre and post IGM transmission
3. NeutralFraction.csv: one column is the averaged neutral fraction across a redshift bin corresponding to how the redshifts were binned for the LF calculation. Example: the first cell in NeutralFraction.csv underneath the "Neutral fraction" column is 0.581. This neutral fraction corresponds to a redshift range of 5.5-5.775. The second cell would then correspond to the next redshift range and so on and so forth. The other columns in this file are the number of LAEs pre and post IGM and are binned according to their luminosity function binning. 
