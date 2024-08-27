# CTA-DEFACE

## Deep learning-based defacing tool for CT angiography: CTA-DEFACE


This repository provides an easy to use Python tool for automated de-identification of CT angiography images. 

If you are using CTA-DEFACE, please cite the following publication (accepted for publication, coming soon): 

```shell
- Mustafa Ahmed Mahmutoglu, Aditya Rastogi, Marianne Schell, Martha Foltyn-Dumitru, Michael Baumgartner, Klaus Hermann Maier-Hein, Katerina Deike-Hofmann, Alexander Radbruch, Martin Bendszus, Gianluca Brugnara, Philipp Vollmuth. 
  "Deep-Learning-based Defacing Tool for CT Angiography: CTA-DEFACE" 

```

Key points:
*	The developed ANN model (CTA-DEFACE) automatically generates facemasks for CT angiography images. 
*	CTA-DEFACE offers superior deidentification capabilities compared to a publicly available model.
*	By means of graphics processing unit optimization, our model ensures rapid processing of medical images.
*	Our model underwent external validation, underscoring its reliability for real-world application.



# Installation Instructions 

## Creating a new python environment

Since our model is heavily dependend on nnUNet, please visit their repository for installation instructions and also cite their paper:

```shell
Isensee, F., Jaeger, P. F., Kohl, S. A., Petersen, J., & Maier-Hein, K. H. (2021). nnU-Net: a self-configuring 
method for deep learning-based biomedical image segmentation. Nature methods, 18(2), 203-211.

https://github.com/MIC-DKFZ/nnUNet
```
After installation, download the weights of our model provided in this link: (coming soon)


# How to use it 


Here is a minimalistic example of how you can use CTA-DEFACE. (the code will be added soon)

```bash
python run_CTA-DEFACE.py -i <INPUT_FOLDER> -o <OUTPUT_FOLDER>
```

The above command will look for all nifti files (*.nii.gz) in the INPUT_FOLDER and save the renamed NIfTI files in THE OUTPUT_FOLDER with the predicted face masks. 


 
 
