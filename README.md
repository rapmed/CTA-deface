# CTA-DEFACE

## CTA-DEFACE: De-Identification Network for CT Angiography 


This repository provides an easy to use Python tool for automated de-identification of CT angiography images. 

If you are using CTA-DEFACE, please cite the following publication: 


- Mustafa Ahmed Mahmutoglu, Aditya Rastogi, Gianluca Brugnara, Michael Baumgartner, Martha Foltyn-Dumitru, Marianne Schell, Martin Bendszus, Philipp Vollmuth. Deep-Learning-based Defacing Tool for CT Angiography. 



Compared to other previously published brain CT defacing tools, CTA-DEFACE has some significant advantages:
- The CTA-DEFACE model was able to reliably segment soft face tissue in CTA data achieving DSC of 0.94±0.02 on an external test set. 

- After applying face detection and verification networks, our model showed substantially lower face detection probability (p < 0.001) and similarity to the original CTA image (p < 0.001). 



# Installation Instructions 
There are two options to use the CTA-DEFACE tool. 

## 1) Creating a new python environment

Since our model is heavily dependend on nnUNet, please visit their repository for installation instructions and also cite their paper:

```shell
Isensee, F., Jaeger, P. F., Kohl, S. A., Petersen, J., & Maier-Hein, K. H. (2021). nnU-Net: a self-configuring 
method for deep learning-based biomedical image segmentation. Nature methods, 18(2), 203-211.

https://github.com/MIC-DKFZ/nnUNet
```
After installation, download the weights of our model provided in the .....................


# How to use it 


Here is a minimalistic example of how you can use CTA-DEFACE. 

```bash
nnUNet_predict CTA-DEFACE -i <INPUT_FOLDER> -o <OUTPUT_FOLDER> -c 3d_lowres
```

The above command will look for all nifti files (*.nii.gz) in the INPUT_FOLDER and save the renamed NIfTI files in THE OUTPUT_FOLDER with the predicted face masks. 


## 2) Docker file

Download the docker file ( --- coming soon ---).

```bash
docker pull ..........................
```

Create a parent folder (for example a folder named as `mount_folder` ) which includes the folders `input`, `output` and `code`. Copy the `run.sh` file into the `code` folder.
Run the following command to mount the parent folder and run the HD-SEQ-ID. 

```bash
docker run -it --name ................. --gpus all --mount type=bind,source="<mount_folder>",target=/mnt/ .................. /bin/bash -c "/mnt/code/run.sh"
```

If you're using the docker version, you don't need to install the weights manually, they are already in the docker image.


 
 
