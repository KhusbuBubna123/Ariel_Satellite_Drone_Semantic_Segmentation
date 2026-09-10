# Arial Image Semantic Segmentation using UNet Architecture.
In this project, arial satellite images were divided into 6 semantic regions as follows:
#Building: #3C1098 (Royal Purple)
#Land (unpaved area): #8429F6 (Vibrant Purple)
#Road: #6EC1E4. #Sky Blue
#Vegetation: #FEDD3A #warm shade of yellow
#Water: #E2A929 #Orange
#Unlabeled: #9B9B9B #Gray.

The UNet architecture consisting of Encoder and Decoder was used for semantic segmentation of ariel satellite images. The 
network was trained for 15 epochs. Also SAM(Segmenent Anything Model) architecture could also have been used. But in this
project, UNet architecture was used for semantic segmentation.
# Dataset Description
About Dataset (Source:Kaggle)
Dataset Resource: https://www.tugraz.at/index.php?id=22387

Citation If you use this dataset in your research, please cite the following URL:

http://dronedataset.icg.tugraz.at

License The Drone Dataset is made freely available to academic and non-academic entities for non-commercial purposes such as
academic research, teaching, scientific publications, or personal experimentation. Permission is granted to use the data given
that you agree:

That the dataset comes "AS IS", without express or implied warranty. Although every effort has been made to ensure accuracy, 
we (Graz University of Technology) do not accept any responsibility for errors or omissions. That you include a reference to the
Semantic Drone Dataset in any work that makes use of the dataset. For research papers or other media link to the Semantic Drone 
Dataset webpage. That you do not distribute this dataset or modified versions. It is permissible to distribute derivative works in 
as far as they are abstract representations of this dataset (such as models trained on it or additional annotations that do not directly 
include any of our data) and do not allow to recover the dataset or something similar in character. That you may not use the dataset or any 
derivative work for commercial purposes as, for example, licensing or selling the data, or using the data with a purpose to procure a 
commercial gain. That all rights not expressly granted to you are reserved by us (Graz University of Technology).

Dataset Overview The Semantic Drone Dataset focuses on semantic understanding of urban scenes for increasing the safety of autonomous drone 
flight and landing procedures. The imagery depicts more than 20 houses from nadir (bird's eye) view acquired at an altitude of 5 to 30 meters
above ground. A high resolution camera was used to acquire images at a size of 6000x4000px (24Mpx). The training set contains 400 publicly 
available images and the test set is made up of 200 private images.

PERSON DETECTION For the task of person detection the dataset contains bounding box annotations of the training and test set.

SEMANTIC SEGMENTATION We prepared pixel-accurate annotation for the same training and test set. The complexity of the dataset is 
limited to 20 
classes as listed in the following table.

Table 1: Semantic classes of the Drone Dataset

tree, gras, other vegetation, dirt, gravel, rocks, water, paved area, pool, person, dog, car, bicycle, roof, wall, fence, 
fence-pole, window, door, obstacle

# Results
After training the UNet model for 15 epochs, the training and validation loss obtained were as follows:
<img width="584" height="455" alt="Training ValidationLoss" src="https://github.com/user-attachments/assets/cac80c32-895b-4b6c-953e-f659be517e83" />
The Training and Validation Intersection Over Union was as follows:
<img width="576" height="455" alt="Training ValidationIOU" src="https://github.com/user-attachments/assets/aeb4edae-3a44-4077-8c6a-d55b34fe3b2b" />
But if the model
