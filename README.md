# IPBR_Cell_Counting_Project
# Cell Counting Project

## Description
This program counts the number of cells in untreated and staurosporine-treated 
microscopy images using image preprocessing and connected-component labeling.

## Introduction
Cell counting is important during cancer treatment testing. The process is quite
simple when it comes to one iteration, but with large batches of microscopy 
images and multiple variables, it gets a little more tricky. I took these
images from the IDR Open Microsopy website and used two images referenced in the 
paper, "High-Content Phenotypic Profiling of Drug Response Signatures across 
Distinct Cancer Cells" by Caie et al (https://doi.org/10.1158/1535-7163.MCT-09-1148).
The images used in this program are of MCF-7 breast cancer cells treated for 24hrs. 
The "Treated" image shows cells treated by the drug staurosporine at its highest
dosage, 1 micromolar. The "Untreated" image shows cancer cells without treatment, 
acting as a control comparison for the image analysis. Before image preprocessing, 
the image settings were changed in order to isolate the DNA/nuclei stain. This
was done by going to the OMERO.iviewer provided in the IDR Open Microscopy website, 
turning the DAPI settings towards the left and the Tubulin and Actin settings
towards the right. This makes the image preprocessing easier. 

# Image Information
Website: https://idr.openmicroscopy.org/
Public data file: idr0035-caie-drugresponse/screenA
Subfile: Week3_25441, Field 1
Treated: Well C3
Untreated: Well C2

## Requirements
- Python 3
- numpy
- matplotlib
- scikit-image

## Running the program
1. Download the notebook and the microscopy images.
2. Place the images in the same folder as the notebook.
3. Open the notebook in Jupyter Notebook or Google Colab.
4. Run all cells from top to bottom.

The program will:
- preprocess both images,
- identify individual cells,
- count the number of cells in each image,
- calculate the estimated reduction in cell count,
- display the results.