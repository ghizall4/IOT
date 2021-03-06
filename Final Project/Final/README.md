
# Intelligent Recyclable Identification System (sort of)

The Intelligent Recyclable Identification System is a supervised learning system designed to classify objects into categories based on their material and sort those objects into recyclable or non recyclable. The system will utilize a Raspberry Pi running MATLAB, a USB camera, and a laptop with MATLAB in order to train, test, and implement the Intelligent Recyclable Identification System. The project will complete the dataset and train the convolutional neural network on the laptop, and then will utilize the Raspberry Pi and USB camera in deployment of the system. Based on the results of the convolutional neural network, the system will sort similar materials into appropriate groups.
***
***
## Table of Contents
1. [Prerequisite Installations](#prereqs)
2. [System Requirements](#systeqs)
3. [Installation & Integration](#install)
4. [Execution & How to Use](#exeUses)
***
***
### Prerequisite Installations
The required installations needed to run this project include:
   1. Laptop with Matlab2017b or greater installed.
   1. Raspberry Pi with Matlab installed
***
***
### System Requirements
#### Component Requirements
To properly run the system, the following components are needed:
   1. A laptop with Matlab 
   1. A Raspberry Pi with Matlab
   1. A USB webcam
   1. A router

#### Functional Requirements
The system will:
   1. Train itself with a dataset
   1. Take an image and compare that against the dataset 
   1. Sort the material into one of the pre-listed categories
   1. Be able to determine the the recyclable category with reasonable accuracy
***
***
### Installation & Integration
The required installations needed to run this project include:
   1. Laptop with Matlab2017b or greater installed.
      1. Matlab Wavelet Toolbox
      1. Matlab Neural Network Toolbox
      1. Matlab Support Package for Raspberry Pi
      1. USB Webcam Support with Matlab
   1. Raspberry Pi with Matlab installed
   
To run this project, the following steps must be taken:
   1. Boot the Raspberry Pi
   1. Boot the laptop
   1. Ensure that the Raspberry Pi and laptop are connected to the same router.
   1. Validate the required installations.

***
***
### Execution and How to Use
The following steps must be followed to successfully run the program.
   1. Download DataSet
      1. [Flickr Material Database](https://people.csail.mit.edu/celiu/CVPR2010/FMD/)
   1. BuildDataSet.m
      1. Add FilePath of the downloaded dataset to the builddataset.m directory.
      1. Run the BuildDataSet.m
      1. Wait for export of dataset .csv file to the directory.
   1. ConvolutionalNN.m
      1. Make sure dataset .csv file is in the directory of this file.
      1. Run the TrainNN.m
      1. Creates A trained and tested Neural Network based on the csv.
      1. Saves a .mat file to your computer
   1. Deploy.m
      1. Calls the raspberry pi for an image.
      1. Loads the .mat file into the workspace.
      1. Takes the image and performs the wavelet transform.
      1. Builds the feature vector.
      1. Gets classified by the neural network.
      1. Outputs result to the matlab console.
      
***
***
### Additional Information
For Additional Information, please view the system documentation located in this repository.
***
***
### Credits
* Moises Cruz
* Devon Graves
* Kyle Jonas
* Robert Parise
