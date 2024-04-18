This project main goal is to classificate melanoma images (as benign or malignant).

Melanoma is a type of skin cancer that can spread to other areas of the body. The main cause of melanoma is ultraviolet light, which comes from the sun and is used in sunbeds.
The American Cancer Society’s estimates for melanoma in the United States for 2024 are: About 100 640 new melanomas will be diagnosed (59% men and 41% women), About 8 290 people are expected to die of melanoma (about 5 430 men and 2 860 women)

I chose this dataset: https://www.kaggle.com/datasets/bhaveshmittal/melanoma-cancer-dataset/data?select=train
This dataset has a train folder with 6289 benigh images, 5590 malignant images; and a test folder with 1000 benigh images, 1000 malignant images. 

I started by loading the images and since there was an inbalance in the number of training images, I decided to randomly delete 699 benign images.
Then, I checked the class distribution was balanced, that the images were correctly loaded, the mean pixel value (153.70) and the standard deviation of pixel values (43.92), that the image size was the same for all images, and the color distribution.

After this, I splited the training dataset into training and validation sets. Training set: (8943, 224, 224, 3) (8943,)
Validation set: (2236, 224, 224, 3) (2236,)
I encoded the labels, 0 being benign and 1 being malignant, and I flatten the images to 1D and 787 pixels.

Then I started to define my model. For my first model I used the images flatten to 1D, and got a accuracy of 0.8445.
After, I decided to use the pre-trained VGG16 model to help me improve my model. In this approach I used the image size (224, 224), removed the top layers of the pre-trained mode and added new layers on top of that base model. I got an accuracy of 0.9275.

The main take aways are that this kind of models that a lot of time to run, and to improve, but this was an awesome experience tht allowed me to learn a lot and explore a subject I realy like.