# ColorIt
- This project is based on the methods proposed in the paper [Colorful Image Colorization](https://github.com/richzhang/colorization), and we aim to improve the performance via training the [ECCV16 Architecture](https://github.com/richzhang/colorization/blob/master/colorizers/eccv16.py), a standard residual convolutional network proposed by the authors, using Generative Adversarial Networks. 
- ECCV16 Architecture is used as the [Generator](https://github.com/aayush9753/ColorIt/blob/main/ECV_Generator.py).
- We are using a pre-trained VGG19 model as the [Feature extractor](https://github.com/aayush9753/ColorIt/blob/main/Feature_extractor.py),
a novel approach to compare images and use that comparison to compute the loss.
Two images are passed in it, and the activations of the 18th layers are taken for both the images and then these activations are used to calculate the loss using RMSE, MSE etc., between the two activations.
- [Discriminator](https://github.com/aayush9753/ColorIt/blob/main/Discriminator.py) is made up of simple architecture which takes an image as input and converts it into a single no. after passing through several convolutional blocks.
- Data can be downloaded from [Kaggle/aayush9753](https://www.kaggle.com/aayush9753/image-colorization-dataset). We have curated the data by collecting 6000 colourful 400X400 images and converted them into grayscale.
- Training of the model either from scratch or further training of our models can be done through [ECV_Gan_Training.ipynb](https://github.com/aayush9753/ColorIt/blob/main/ECV_Gan_Training.ipynb). We trained it on the Kaggle Platform using a GPU accelerator. You can see our original training code and cell outputs here -  [gan-ecv-Kaggle.ipynb](https://github.com/aayush9753/ColorIt/blob/main/gan-ecv-Kaggle.ipynb) or at [Kaggle](https://www.kaggle.com/aayush9753/gan-for-image-colorization).
- To test or to generate colorful images, go through the [Test.ipymb](https://github.com/aayush9753/ColorIt/blob/main/Test.ipynb). It provides methods to generate multiple colotful images at a time via providing the path.
- The Pre-trained model can be downloaded from this [Google Drive](https://drive.google.com/drive/folders/153PYVwK_6knKPpDJMhi3onojJdCVUlk2?usp=sharing).

## Sample Outputs
Black and White Image             |  Colorized Image
:-------------------------:|:-------------------------:
![](https://github.com/aayush9753/ColorIt/blob/main/sample/11.jpg)  |  ![](https://github.com/aayush9753/ColorIt/blob/main/Outputs/multiple_Outputs/11.jpg)
![](https://github.com/aayush9753/ColorIt/blob/main/sample/7.jpg)  |  ![](https://github.com/aayush9753/ColorIt/blob/main/Outputs/multiple_Outputs/7.jpg)
![](https://github.com/aayush9753/ColorIt/blob/main/sample/10.jpg)  |  ![](https://github.com/aayush9753/ColorIt/blob/main/Outputs/multiple_Outputs/10.jpg)
![](https://github.com/aayush9753/ColorIt/blob/main/sample/9.jpg)  |  ![](https://github.com/aayush9753/ColorIt/blob/main/Outputs/multiple_Outputs/9.jpg)

### [Colorful Image Colorization](https://github.com/richzhang/colorization)
```
@inproceedings{zhang2016colorful,
  title={Colorful Image Colorization},
  author={Zhang, Richard and Isola, Phillip and Efros, Alexei A},
  booktitle={ECCV},
  year={2016}
}

@article{zhang2017real,
  title={Real-Time User-Guided Image Colorization with Learned Deep Priors},
  author={Zhang, Richard and Zhu, Jun-Yan and Isola, Phillip and Geng, Xinyang and Lin, Angela S and Yu, Tianhe and Efros, Alexei A},
  journal={ACM Transactions on Graphics (TOG)},
  volume={9},
  number={4},
  year={2017},
  publisher={ACM}
}
```
