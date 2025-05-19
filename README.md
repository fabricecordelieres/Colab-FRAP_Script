# **FRAP Analysis**

---
## **Data organization**
This notebook takes as an input a single zip file containing several excel files generating using an ImageJ data extraction toolset (one file per dataset). Each Xls file is expected to contain one columns per analyzed ROI where values corresponds to the following normalization of fluorescence:
* "MM_Roi_XX": Double normalized fluorescence for ROI_XX.
* "Full_Scale_MM_Roi_XX": Full scale, double normalized fluorescence for ROI_XX.
* "Time_sec": Extracted timestamp.

Additionnal columns may appear but won't be taken care of.

---
## **How to run this script**

1.   Have all you data ready: the toolset should have generated a **"_dataToUpload.zip"** file in the output folder: locate it and get ready to select it when asked.
2.   Run each step: press the play button, on the left side of the relevent cells
  1. **Step 1** is non interactive: point at the \[   \] mark. It will change to a play button. Press play and wait for a green tick mark to appear on the left.
  2. **Step 2** is interactive: if applicable, unfold the cell and point at the \[   \] mark. It will change to a play button. Press play: a **"Select file"** button should appear below the cell. Use it to navigate your drive and locate the zip file. The selected file will be uploaded to the swap space of the Google Colab environment, will be unzip.
  3. **Step 3** is non interactive: point at the \[   \] mark. It will change to a play button. Press play and wait for a green tick mark to appear on the left.  During this step, data compilation will occur. The resulting files will be zipped and directly downloaded to your computer.

---
# **What's in the output ?**

Once the script has finished processing the data, all outputs will be automatically zipped (Fitted_data.zip) and downloaded. It contains one folder per input dataset, named after the dataset. Each folder contains the following files:
- **DATASET-NAME_single-exponential_plots.pdf:** for data where fitting against a single exponential was possible, displays one page per ROI, overlaying as a graph the fitted data to the original data.
- **DATASET-NAME_single-exponential_fitted_values.xlsx:** for double normalized and full scale data, displays the modelized the values (when fitting a single exponential was possible).
- **DATASET-NAME_single-exponential_fitting_parameters.xlsx:** for double normalized and full scale data, displays the parameters for the single exponential model, a goodness of fitting value and estimation of both the t_half and mobile fraction (when fitting was possible).
- **DATASET-NAME_double-exponential_plots.pdf:** for data where fitting against a double exponential was possible, displays one page per ROI, overlaying as a graph the fitted data to the original data.
- **DATASET-NAME_double-exponential_fitted_values.xlsx:** for double normalized and full scale data, displays the modelized the values (when fitting a double exponential was possible).
