# Arial Image Semantic Segmentation using UNet Architecture.


In this project, arial satellite images were divided into 6 semantic regions as follows:
1) Building: #3C1098 (Deep royal blue, dark iris, or vivid indigo)
2) Land (unpaved area): #8429F6 (Vibrant Purple)
3) Road: #6EC1E4. (Sky Blue)
4) Vegetation: #FEDD3A (bright, vibrant Yellow)
5) Water: #E2A929 (Orange)
6) Unlabeled: #9B9B9B (Gray).

An example satellite Image and its corresponding Semnatic Segmenatation Masks: \
<img width="150" height="180" alt="image_part_001" src="https://github.com/user-attachments/assets/a0925987-4563-45ce-9424-700ec51ed178" />
<img width="150" height="180" alt="image_part_001" src="https://github.com/user-attachments/assets/2a753704-22ca-4552-af8f-123fa00dcbe4" /> \

The UNet architecture consisting of Encoder and Decoder was used for semantic segmentation of ariel satellite images. The 
network was trained for 15 epochs. Also SAM(Segmenent Anything Model) architecture could also have been used. But in this
project, UNet architecture was used for semantic segmentation.

# Dataset Description
Humans in the Loop is publishing an open access dataset annotated for a joint project with the Mohammed Bin Rashid Space Center in Dubai, the UAE. 

**Content** \
The dataset (source:Kaggle) consists of aerial imagery of Dubai obtained by MBRSC satellites and annotated with pixel-wise semantic segmentation in 6 classes. The total volume of the dataset is 72 images grouped into 6 larger tiles. The classes are:

1) Building: #3C1098
2) Land (unpaved area): #8429F6
3) Road: #6EC1E4
4) Vegetation: #FEDD3A
5) Water: #E2A929
6) Unlabeled: #9B9B9B \

**Acknowledgements**
The images were segmented by the trainees of the _"Roia Foundation"_ in Syria.

# Results
The predictions of semantic segmenatation obtained on a sample ariel satellite image were as follows:
<img width="993" height="339" alt="Predictions_Test_Image_Satellite" src="https://github.com/user-attachments/assets/787b355a-f369-4063-9835-8f16be8b3948" />
<img width="993" height="339" alt="Prections_Test_Image_Satelitte" src="https://github.com/user-attachments/assets/b90ce241-84e7-418b-a2c9-60d2a2f195c6" />
The predictions on test image obtained were not good as compared to the ground truth semantic segmentation
since the Unet model was trained for a very less no. of epochs(only 15 epochs) due to lack to time and GPU resources.

After training the UNet model for 15 epochs, the training and validation loss obtained were as follows:
<img width="584" height="455" alt="Training ValidationLoss" src="https://github.com/user-attachments/assets/0f3fdcef-3439-4e25-8516-9684b14618a4" />

The Training and Validation Intersection Over Union was as follows:
<img width="576" height="455" alt="Training ValidationIOU" src="https://github.com/user-attachments/assets/8ea7cc97-eb59-4ff5-b717-49ee7d3723e1" />

But suppose instead if the model was trained for more no. of epochs,(i.e. 100 epochs) then, we would have achieved much better predictions results on Test Image and the Training and Validation Accuracy obtained would be much higher. Also the Training and Validation IOU (Intersection Over Union) results obtained would have been much better. 

