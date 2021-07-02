# ColorIt
- This project is based on the methods proposed in the paper [Colorful Image Colorization](https://github.com/richzhang/colorization) and we aim to improve the performance via training the [ECV16 Model](https://github.com/richzhang/colorization/blob/master/colorizers/eccv16.py) (A normal residual convnet model proposed in the pape) proposed by the authors using Generative Adversial Networks. 
- ECV16 Model is used as the [Generator](https://github.com/aayush9753/ColorIt/blob/main/ECV_Generator.py).
- We are using pre-traine VGG19 model as  [Feature extractor](https://github.com/aayush9753/ColorIt/blob/main/Feature_extractor.py).
This is a noval approach to compare to images and use that comparison as a loss to train a model.
We will use a pre-trained VGG19 model. Two images are passed in it and the activations of the 18th layers are taken for both the images and then this activations are used to calculate the loss which can be calculated using RMSE, MSE etc between the two activations.
- [Discriminator](https://github.com/aayush9753/ColorIt/blob/main/Discriminator.py) is made up of simple architecture which takes an image as input and converts it into a single no. after passing through several convolutional blocks.
- Data can be downloaded from [Kaggle/aayush9753](https://www.kaggle.com/aayush9753/image-colorization-dataset). The data is made by us only. We took 6000 colorful 400X400 images and converted them into greyscale.
- Training of the model either from scratch or further training of our models can be done through [ECV_Gan_Training.ipynb](https://github.com/aayush9753/ColorIt/blob/main/ECV_Gan_Training.ipynb). We trained it on Kaggle Platform using GPU as accelerator. You can see our original training code and cell outputs here -  [gan-ecv-Kaggle.ipynb](https://github.com/aayush9753/ColorIt/blob/main/gan-ecv-Kaggle.ipynb) or at [Kaggle](https://www.kaggle.com/aayush9753/gan-for-image-colorization).
- To test or to generate colorful images, Go through the [Test.ipymb](https://github.com/aayush9753/ColorIt/blob/main/Test.ipynb). It provides methods to generate multiple colotful images at a time via providing the path.
- The Pre-trained model can be downloaded from [Google Drive](https://drive.google.com/drive/folders/153PYVwK_6knKPpDJMhi3onojJdCVUlk2?usp=sharing).

## Sample Outputs
Black and White Image             |  Colorized Image
:-------------------------:|:-------------------------:
![](https://github.com/aayush9753/ColorIt/blob/main/sample/11.jpg)  |  ![](https://github.com/aayush9753/ColorIt/blob/main/Outputs/multiple_Outputs/11.jpg)
![](https://github.com/aayush9753/ColorIt/blob/main/sample/7.jpg)  |  ![](https://github.com/aayush9753/ColorIt/blob/main/Outputs/multiple_Outputs/7.jpg)
![](https://github.com/aayush9753/ColorIt/blob/main/sample/10.jpg)  |  ![](https://github.com/aayush9753/ColorIt/blob/main/Outputs/multiple_Outputs/10.jpg)
![](https://github.com/aayush9753/ColorIt/blob/main/sample/9.jpg)  |  ![](https://github.com/aayush9753/ColorIt/blob/main/Outputs/multiple_Outputs/9.jpg)
