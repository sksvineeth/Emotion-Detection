# Emotion-Detection
Facial Emotion Recognition
# Abstractive text summarizer
- [ Abstract ](#Abstract )
- [Methodology](#Architecture-overview)
- [Results]
- [References](#References)
- [Future Scope](#Future-Scope)


## Abstract ##
Facial  expression  for  emotion  detection  has  always  been  an  easy  task  for humans  butachieving  the  same  task  with  a  computeralgorithm  is  quite  challenging.  With  the  recent advancement  in  computer  vision  and  machine  learning,  it is  possibleto  detect  emotions from images. In this paper, theaim of this project is to develop a Facial Emotion Recognition model  using  ConvolutionalNeural  Network  algorithm  that  can  help  for  real  time  emotion detection. For the specific use cases like pain detection in healthcare, or individual emotion monitoring systems while driving the features that constitute for the emotion can also help to improve the accuracy of the recognition. In the ERmodel, expressional vector (EV) is used to findthe fivedifferenttypes of regular facial expressions.The two-level CNN works in  series,  and  the  last  layer  of  perceptron  adjusts  the  weights  and  exponent  values  with each iteration. ERdiffersfrom generally followed strategies with single-level CNN, hence improving  the  accuracy.  Furthermore,  a  novel  background  removal  procedureapplied, before  thegeneration  of  EV,  avoids  dealing  with  multiple  problems  that  may  occur  (for example  distance  from  the  camera).   ERwas  extensively  tested  with  images  using extended Cohn–Kanade expression, CMU datasets. The ER model with more training can be used for emotion detection to be useful in many applications such as to alarmindividuals while driving, pain detection in the hospitals. Addition of features behind the emotion like Heart  rate,  ER,  Neuro  monitoring  can  help  to  draw  a  better  conclusion  in  Emotion recognition.

## Methodology ##

Starting the project with the Emotion Recognition System and will update the models regarding to pain specific data later on. The  proposed  method  has  been  shownin Fig.1. It’s an amalgam of various techniques for extraction  of  features  from  image  frames  for  automatic  detection  of  pain.  The  details  of  all  the steps are showed in the architecture. Facial Region Extraction, Iterative Shape Alignment Using Procrustes Analysis: The shapes of the faces are iteratively aligned so as to remove all geometric disparity i.e. scale, rotation andtranslation of the vertex location with respect to the base shape [8][9]. The alignment of multiple shapes is based onaligning pairs of shapes where one of them is a reference frame. For  this  Generalized  Procrustes  Analysis  (GPA)  isperformed  which  consists  of  sequentially aligning pair of shapes with using the reference shape (the mean shape)and align the others to it.  At the  beginning  of  the  procedure,  any  shape can  be  selected  as the  initial  mean.  After thealignment  a  new  mean  is  recomputed,  and  again  the  shapes  are  aligned  to  this  mean.  This procedure  is  performedrepeatedly  until  the  mean  shape  doesn't  change  significantly  within iterations.Texture WarpingAfter aligning all the shapes, warping of texture is carried out using a piece-wise affine warping to normalize all non-rigid texture samples with respect to the base shape. A piece-wise affine warping is a texturemapping procedure where convex hull of the mean shape and the sample shapes are partitioned using Delaunaytriangulation [3][4][10]. Then each pixel from the training image, belonging to a specific triangle, is mapped into the respective destination triangle in the mean shape frame using barycentric coordinates with bilinear interpolation correction. 

3.2. Feature Extraction using Gabor FilteringAfter  extraction  of  facial  regions,  the  next  step  is  facial  feature  extraction  to  produce  feature vectors. Gabor filters(also called as Gabor kernels) is an significantmethod in the areaof image 
analysis because of its optimumlocalization properties in spatial and frequency domain. It is used to  extract  the  changes  in  facial  appearance  asa  set  of  multiscale  and  multi-orientation coefficients.  In  the  spatial  domain,  a  2D  Gabor  filter  is  a  complexexponential  modulated  by  a Gaussian function.

## Architecture overview ##
![architecture ](https://user-images.githubusercontent.com/18707601/103633042-2c3b7880-4f13-11eb-829b-57799db9310c.png)
![Gabor Filtering](https://user-images.githubusercontent.com/18707601/103633042-2c3b7880-4f13-11eb-829b-57799db9310c.png)

 Model specifications :

- OPEN CV Face recognition
- embedding size = 200                         
- batch size  = 2096
- numner of epochs = 15
- time taken for each epoch = 1300 sec approx
- CNN Model 
- Data set :CNN Face data set

## References ##

## Future Scope ##
1. Training for more epochs 
2. Increasing batch size
3. Implementing Attention Mechanism
4. Extending it to Pain Specific data
