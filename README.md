# CTA-DEFACE

## Deep learning-based defacing tool for CT angiography: CTA-DEFACE


This repository provides an easy to use tool based on `nnUNet` for automated de-identification of CT angiography images. 

If you are using CTA-DEFACE, please cite the following publication:


```shell
Mahmutoglu MA, Rastogi A, Schell M, Foltyn-Dumitru M, Baumgartner M, Maier-Hein KH, Deike-Hofmann K, Radbruch A, Bendszus M, Brugnara G, Vollmuth P. 
Deep learning-based defacing tool for CT angiography: CTA-DEFACE. 
Eur Radiol Exp. 2024 Oct 9;8(1):111. 

doi: 10.1186/s41747-024-00510-9.
```

![alt text](https://github.com/CCI-Bonn/CTA-DEFACE/blob/main/CTA-DEFACE_example.png?raw=true)

The example image above was rendered in 3D Slicer software using "CT-Muscle" display preset. 


Key points:
*	The developed ANN model (CTA-DEFACE) automatically generates facemasks for CT angiography images and subtracts them py replacing the mask with the 10th percentile in the CT image (representing void space/air). 
*	By means of graphics processing unit optimization, our model ensures rapid processing of medical images.
*	Our model underwent external validation, underscoring its reliability for real-world application.


# Installation Instructions 



Since our model is heavily dependend on nnUNet, please visit their repository for installation instructions and also cite their paper:

```shell
Isensee, F., Jaeger, P. F., Kohl, S. A., Petersen, J., & Maier-Hein, K. H. (2021). nnU-Net: a self-configuring 
method for deep learning-based biomedical image segmentation. Nature methods, 18(2), 203-211.

```



# How to use it 


Please install nnunetv2 following the instructions here:

```shell
https://github.com/MIC-DKFZ/nnUNet
```

Clone this repository and add your images to the input folder. 
Create `input`, `output` and `model` folders in the same folder as the `run_CTA-DEFACE.py`.

```bash
mkdir input
mkdir output
mkdir model
```

Download the trained model from the following link and put the `Dataset001_DEFACE` folder inside the `model` folder.

```bash
https://drive.google.com/drive/folders/1k4o35Dkl7PWd2yvHqWA2ia-BNKrWBrqg?usp=sharing
```

Make sure the CT or CTA input image names end with `_0000.nii.gz`, which is important to be recognized by the model. 

```bash
python run_CTA-DEFACE.py -i input -o output
```

The above command will look for all nifti files (*.nii.gz) in the `input` folder and save the <ins>defaced NIfTI files</ins> and the <ins>face mask</ins> in the `output` folder. 


 
 
