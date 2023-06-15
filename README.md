# HSI Topographic Correction
---

This README file can be used to better understand how to use the R Scripts (available on GitHub at github.com/aduro005/HSITopographicCorrectionRScripts) and the data (available on Dryad Data Repository UCR) associated with the HSI Topographic Correction.

Hyperspectral imaging was performed with a high-sensitivity sCMOS VNIR hyperspectral camera (MSV 500, Middleton Spectral Vision, Middleton, WI). Each soil sample was positioned under the hyperspectral camera and imaged at 91 slope, aspect orientations using a custom designed and 3-D printed sample array. The design for this sample array can be found on GitHub at github.com/aduro005/HSITopographicCorrectionSampleWellArray. 

574 soil samples were provided by the NEON Initial Characterization Soils Archive at the University of Michigan Biological Station—Sample Archive Facility in Ehlers (UMBS-SAFE) with accompanying soil properties data obtained from the NEON Data Archive. Soil samples obtained from NEON were described, sampled, and analyzed for particle-size distribution and SOC by the US Department of Agriculture—National Resources Conservation Service following standard methods. 

450 soil samples were collected from Duke Farms in Hillsborough Township, New Jersey. The Duke Farms samples were dried, ground, and sieved through a 2-mm screen, then subsamples of at least 500 mg were weighed into stainless steel crucibles for analysis in a carbon/nitrogen analyzer (Vario MAX Cub, Elementar Americas, Inc., Ronkonkoma, NY). Total C results were assumed to be equivalent to SOC since no inorganic carbon is expected in the soils collected from Duke Farms. 

57 soil samples were collected in 2018 and 2019 from locations in the Santa Ana Mountains, California that were affected by the 2018 Holy Fire. The Holy Fire soil samples were oven dried, ground, and sieved, then weight percent carbon was determined by elemental analysis using a carbon/nitrogen analyzer (Flash EA, Thermo Fisher Scientific, Waltham, MA). Total carbon was assumed to be equal to SOC in the Holy Fire samples since none of these samples effervesced when treated with 10% HCl.


## Description of the data and file structure

Soil spectra (observed, uncorrected) obtained at each slope, aspect configuration along with selected soil properties can be found on the UCR Dryad Data Repository (HSICalLib_b1_b30_p.RData). This file is output from the Step 7 of HSI Data Processing R script (HSICalLib_4_intmean_to_masterintmean_to_p.R) which can be found on GitHub. Starting with this file, you can follow Steps 8-14 of HSI Data Processing to obtain all files necessary for Steps 1-4 of the HSI Data Analysis workflow used for the HSI Topographic Correction. Nonetheless, all files used during the HSI Topographic Correction that are output after HSICalLib_b1_b30_p.RData in the Data Processing and HSI Data Analysis workflows can be found on the UCR Dryad Data Repository. Therefore, you can look at the beginning of any script after Step 7 of HSI Data Processing (i.e., HSICalLib_4_intmean_to_masterintmean_to_p.R) and the necessary files can be found on the UCR Dryad Data Repository.

Abbreviations: 
obsI = observed, uncorrected VNIR reflectance spectra
refI = reference, mean VNIR reflectance spectra across all aspects at slope = 0
dIp = predicted dI 
dIc = dI corrected VNIR reflectance spectra
coscorI = cosine corrected VNIR reflectance spectra
ccorI = C corrected VNIR reflectance spectra


## Sharing/Access information

This is a section for linking to other ways to access the data, and for linking to sources the data is derived from, if any.

Links to other publicly accessible locations of the data:
  * github.com/aduro005/HSITopographicCorrectionSampleWellArray (custom designed and 3-D printed sample array)
  * github.com/aduro005/HSITopographicCorrectionRScripts (R Scripts used to manipulate the data found on the UCR Dryad Data Repository)

Data was derived from the following sources:
  * data.neonscience.org/home (574 soil samples obtained from NEON Initial Characterization Soils Archive at the University of Michigan Biological Station—Sample Archive Facility in Ehlers (UMBS-SAFE) with accompanying soil properties data obtained from the NEON Data Archive)


## Code/Software

This is an optional, freeform section for describing any code in your submission and the software used to run it.

Describe any scripts, code, or notebooks (e.g., R, Python, Mathematica, MatLab) as well as the software versions (including loaded packages) that you used to run those files. If your repository contains more than one file whose relationship to other scripts is not obvious, provide information about the workflow that you used to run those scripts and notebooks.
