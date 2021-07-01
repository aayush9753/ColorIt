# ColorIt
This project is based on the methods proposed in the paper Colorful Image Colorization !(https://arxiv.org/abs/1603.08511) and we aim to improve the performance via training the ECV model (A normal residual convnet model proposed in the pape) proposed by the authors using Generative Adversial Networks. 
We are using pre-traine VGG19 model as Feature extractor.
This is a noval approach to compare to images and use that comparison as a loss to train a model.
We will use a pre-trained VGG19 model. Two images are passed in it and the activations of the 18th layers are taken for both the images and then this activations are used to calculate the loss which can be calculated using RMSE, MSE etc between the two activations.

## Sample Outputs
Black and White Image             |  Colorized Image
:-------------------------:|:-------------------------:
![](https://github.com/aayush9753/ColorIt/blob/main/sample/11.jpg)  |  ![](https://github.com/aayush9753/ColorIt/blob/main/Outputs/multiple_Outputs/11.jpg)
![](https://github.com/aayush9753/ColorIt/blob/main/sample/7.jpg)  |  ![](https://github.com/aayush9753/ColorIt/blob/main/Outputs/multiple_Outputs/7.jpg)
![](https://github.com/aayush9753/ColorIt/blob/main/sample/10.jpg)  |  ![](https://github.com/aayush9753/ColorIt/blob/main/Outputs/multiple_Outputs/10.jpg)
![](https://github.com/aayush9753/ColorIt/blob/main/sample/9.jpg)  |  ![](https://github.com/aayush9753/ColorIt/blob/main/Outputs/multiple_Outputs/9.jpg)
