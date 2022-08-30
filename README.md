# Scene-Description
Being able to automatically describe the content of an image using properly formed English sentences is a very challenging task, but it could have a great impact, for instance by helping visually impaired people better understand the content of images on the web. The problem introduces a captioning task; we planned to do image-to-sentence generation. This application bridges vision and natural language, which requires a computer vision system to both localize and describe salient regions in images in natural language. The image captioning task generalizes object detection when the descriptions consist of a single word. Given a set of images and prior knowledge about the content, find the correct semantic label for the entire image.

## Image-Captioning model:
### Dataset used:
For our task, we used <a href=https://cocodataset.org/#download> MSCOCO-2017 </a>, it contains 118K images each with approximately captions.

### Data Pre-processing:
The preprocessing phase can be split into three main procedures:  
**1. Creating the captions vocabulary:** 
First we added <start> and <end> tokens to each caption, then we created a vocabulary that contains the 5000 most frequent words in all captions.
**2. Image preprocessing and feature extraction:**  
We first resized the images into (224, 244) to be compatible with the VGG-16 input layer, then the images were converted from RGB to BGR, and each color channel is zero-centered.
We then used a pretrained VGG-16 model to extract the features from these pre-processed images and stored them to be later passed to our model.

### Model Training:
All of the model training was done using local gpu (nvidia gtx 1060 with 6GB).  

### Model Deployment:
We used plotly-dash library to deploy our model, also we added a clear dashboard to show the model architecture and the structure of our project.
  
### References:
<ol>
    <li>Vinyals, Oriol, Alexander Toshev, Samy Bengio, and Dumitru Erhan. “Show and tell: A neural image caption generator.” In Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition, pp. 3156- 3164. [2015].</li>
    <li>Xu, Kelvin, Jimmy Ba, Ryan Kiros, Aaron Courville, Ruslan Salakhutdinov, Richard Zemel, and Yoshua Bengio.“Show, attend and tell: Neural image caption generation with visual attention.” arXiv preprint arXiv:1502.03044 [2015]. </li>
    <li>Karen Simonyan, Andrew Zisserman: Very Deep Convolutional Networks for Large-Scale Image Recognition. ICLR [2015]. </li>
    <li>Junyoung Chung, Caglar Gulcehre, Kyunghyun Cho, Yoshua Bengio, Empirical evaluation of gated recurrent neural networks on sequence modeling. NIPS [2014]. </li>
    <li>Karpathy, Andrej, and Li Fei-Fei. “Deep visual semantic alignments for generating image descriptions” In Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition, pp. 3128-3137. [2015]. </li>
    <li> <a href=https://www.tensorflow.org/tutorials/text/image_captioning>Tensorflow image-captioning tutorial.</li>
</ol>

## Team Members:
  - <a href="https://github.com/habebamohamed"> Habiba Mohamed Abdelrazek </a>
  - <a href="https://github.com/Mohamed-AN"> Mohamed Abdelrahman Nasser </a>
  - <a href="https://github.com/Mostafa-Nafie"> Mostafa Alaa Nafie </a>
  - <a href="https://github.com/SalmaElmoghazy"> Salma Elmoghazy </a>
  - <a href="https://github.com/SalmaHisham"> Salma Hisham </a>
