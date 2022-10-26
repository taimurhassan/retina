# Angular Contrastive Distillation Driven Self-Supervised Scanner Independent Screening and Grading of Retinopathy
<p align="justify">
This repository contains the source code (based on <b>TensorFlow 2.1.0, Python 3.7.9</b>) for the manuscript titled <b>"Angular Contrastive Distillation Driven Self-Supervised Scanner Independent Screening and Grading of Retinopathy"</b>, Submitted in <b>Information Fusion</b>
</p>

![BD](/images/block_diagram2.jpg) 
<p align="center"> Block Diagram of the Proposed Framework</p>

## Installation and Configuration
<p align="justify">
   
1) Platform: Anaconda and MATLAB R2021a (with deep learning, image processing and computer vision toolbox).
2) Install required packages from the provided ‘environment.yml’ file or alternatively you can install following packages yourself:
   - Python 3.7.9 or above
   - TensorFlow 2.1.0 or above 
   - Keras 2.0.0 or above
   - OpenCV 4.2 or above
   - imgaug 0.2.9 or above
   - tqdm   
3) Download the desired dataset:
   - Zhang [URL]()
   - Duke-1 [URL]()
   - Duke-2 [URL]()
   - Duke-3 [URL]()
   - Rabbani [URL]()
   - BIOMISA [URL]()
   - AFIO [URL]()
   
4) Create the two folders named as 'trainingDataset' and 'testingDataset'.
5) Put training images of the desired dataset in '…\trainingDataset\trainImages_K' folder where 'K' represents the iteration or model instance.
6) Put training annotation in '…\trainingDataset\trainGT_K' folder.
7) Put validation images in '…\trainingDataset\valImages_K' folder.
8) Put validation annotations in '…\trainingDataset\valGT_K' folder.
9) Put test images in '…\testingDataset\test_images' folder and their annotations in '…\testingDataset\test_annotations' folder.
    - Note: the images and annotations should have same name and extension (preferably png).
10) Apart from this, the 'segmentation_resultsK' folder in 'testingDataset' will contains the segmented results.
11) Provide training configurations in ‘config.py’ file.

</p>

## Steps
<p align="justify">
   
1) Use 'trainer.py' to incrementally train the segmentation network. The following script will also save the model instances in the h5 file.
2) Use 'tester.py' file to extract segmentation results for each model (the model results will be saved in 'segmentation_resultsK' folder.
3) We have also provided some converter scripts to port TF keras models into MATLAB etc.

</p>

## Contact
Please feel free to contact us in case of any query at: taimur.hassan@ku.ac.ae
