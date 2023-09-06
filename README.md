# Semantic-Segmentation-for-Self-Driving-Cars

The goal of this Repo is to use Deepl learning to Make Semantic Segmentation for Self Driving Cars from Dataset with Semantic Segmentation Labels generated via via CARLA simulator. There are 5 Categories in the Dataset, which includes 13 classes from 0 to 12.
this dataset contains images of HandWritten belonging to 10 different Classes.

## About Dataset:

### Context:
This dataset provides data images and labeled semantic segmentations captured via CARLA self-driving car simulator. The data was generated as part of the Lyft Udacity Challenge . This dataset can be used to train ML algorithms to identify semantic segmentation of cars, roads etc in an image.

The data has 5 sets of 1000 images and corresponding labels.

### Content:
The data set contains sets of RGB and the corresponding semantic segments.
See link below for details
http://carla.readthedocs.io/en/latest/cameras_and_sensors/#camera-semantic-segmentation

### Acknowledgements:
CARLA Self Driving Cars Simulator
Some of the data come from
https://github.com/ongchinkiat/LyftPerceptionChallenge/releases/download/v0.1/carla-capture-20180513A.zip


## Installation Instructions:
- just download the dataset from this **[Dataset](https://www.kaggle.com/datasets/kumaresanmanickavelu/lyft-udacity-challenge)** then just download repo and here you are ready to run the code or you can use the model.h5 instead of all these steps.

## Usage Guide:
- I Split the data into 3 parts: training, test and validation and load the masks with images as you can see how it looks like.
  <div align="center">
    <img src="https://github.com/Bassem-2000/Semantic-Segmentation-for-Self-Driving-Cars/blob/main/Images/img-mask.png?raw=true" alt="img-mask">
  </div>


- I Used Data Augmentation and applied to both masks and images using imageaug library as you can see.

<div align="center">
    <img src="https://github.com/Bassem-2000/Semantic-Segmentation-for-Self-Driving-Cars/blob/main/Images/aug.png?raw=true" alt="augment">
</div>

 
- After that, I made a Class to handle all of the steps to load the data as bathes in the training using data augmentation once and without data augmentation one here is the class. 
  
 <!--![Class](https://github.com/Bassem-2000/Semantic-Segmentation-for-Self-Driving-Cars/blob/main/Images/calass.png?raw=true)-->

## Model Architecture:
- I used Unet Architecture to train the semantic segmentation model with 13 classes in the final output and make the shape of the images and masks (512, 512) 
  
 <div align="center">
  <img src="https://github.com/Bassem-2000/Semantic-Segmentation-for-Self-Driving-Cars/blob/main/Images/u-net-architecture.png?raw=true" alt="Architecture">
 </div>


## Evaluation:
- I used Different approaches to test the performance of the architecture and the model like accuracy, loss, IOU and Dice. here are the two approches that i could see the model doing well and the evaluation on two models the agmentation model and the model without augmentation:
  <div align="center">
    <img src="https://github.com/Bassem-2000/Semantic-Segmentation-for-Self-Driving-Cars/blob/main/Images/eval.png?raw=true" alt="eval1">
  </div>
  
  <div align="center">
    <img src="https://github.com/Bassem-2000/Semantic-Segmentation-for-Self-Driving-Cars/blob/main/Images/eval2.png?raw=true" alt="eval2">
  </div>



## Example:
- I test the model with a random images and visualize it here you can see the image with the prediction masks both the augmented model and the ordinary model as title and the real image:

 ![Example](https://github.com/Bassem-2000/Semantic-Segmentation-for-Self-Driving-Cars/blob/main/Images/example.png?raw=true)


## Contact:

[<img alt="alt_text" width="30px" src="https://cdn2.iconfinder.com/data/icons/social-media-2285/512/1_Whatsapp2_colored_svg-512.png" />](https://wa.me/+201006491306)
&nbsp;&nbsp;
[<img alt="alt_text" width="30px" src="https://cdn2.iconfinder.com/data/icons/social-media-2285/512/1_Linkedin_unofficial_colored_svg-512.png" />](https://www.linkedin.com/in/bassem-ahmed-ahmed/)
&nbsp;&nbsp;
[<img alt="alt_text" width="30px" src="https://cdn4.iconfinder.com/data/icons/social-media-logos-6/512/112-gmail_email_mail-256.png" />](mailto:bassemahmed.am@gmail.com)
&nbsp;&nbsp;
[<img alt="alt_text" width="30px" src="https://cdn2.iconfinder.com/data/icons/social-media-2285/512/1_Facebook2_colored_svg-512.png" />](https://www.facebook.com/bassem.ahmed.7712/)

Can you please provide me with feedback on how I can improve myself and any ideas to improve the model, I am eager to receive any advice that can help me develop my skills.

&nbsp;&nbsp;
**Wish you a nice day :)**
