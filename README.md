# Denoise Tool
## Description
Speech denoising is the process of removing unwanted noise from speech signals while preserving the integrity of the speech itself. 
The problem of speech denoising arises when speech signals are corrupted by various types of noise, such as background noise, microphone noise, or electrical interference.

This project aim to denoise signal given input is the noisy signal expected output will give us the denoised signal and evaluate it. The module include 2 methods: Spectral subtraction and FRCRN.

## Prerequisites
To use the FRCNR module, you need to deploy Python environment and install the following modules:

> modelscope
> 
> matplotlib==3.7.3
> 
> numba==0.58.0
> 
> numpy==1.25.2
> 
> python=3.8.8
> 
> pesq==0.0.4
> 
> pypesq==1.2.4
> 
> pystoi==0.3.3
> 
> scipy==1.11.4
> 
> soundfile
> 
> torch==2.1.0+cu118
> 
> torchaudio==2.1.0+cu118
> 
> torchmetrics
> 
> jupyterlab

## Usage explaination
To use the module, open the file FRCRN_denoise\Denoise_module.ipynb. Open the file in Jupiter Environment is the most ideal method, but using other IDE such as Visual Studio Code is fine. Make sure to do the above prerequisites step before continue.
### 1. Import modules
Run the first code block to import modules into the tool. If the code block prints the version of the imported linrary, the package importation is completed.

(image)

The block of code below this is the helper functions. Run the code block to make the tool function properly. From this step, you can choose one of two method to denoise the audio: Spectral Subtraction method or FRCRN method.
### 2. Spectral Subtract method
#### 2.1. Define the path
The path of each audio file is defined in each element of the 'bahna_dataset' array. If the audio is located in another folder, the path can be changed by changing the string parameter of the 'Path()' function. Make sure the string representing the path point to the folder containing the audio only. The audio should be formatted as '.wav' file. Once this step is completed succesfully, the cell will print out the path to the file which its name is the first in alphabetical order of the folder.
#### 2.2. Denoise the audio
Run the [12] cell (the following cell of the path defining step) to create a dataframe to record statistics. Then run the following [13] cell to start the denoise stage. The module then calculate the noise level, perform a noise reduction by simply subtract the frequency components of noises from the noisy audio to get a cleaned/enhanced speech. Then the audio is saved into the destinated folder.


## Commentaries
The spectral subtraction came up with two major shortcomings
- We have to choose a noise from the audio signal to remove it.
- The noise should be present in the entire audio. 
## Citations
## Contacts
