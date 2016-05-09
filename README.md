# cv
computer vision

### Description

**Manifold Learning**

Images are high dimensional objects that live on manifolds. The figure below shows t-SNE embedding of 64 dimensional digits dataset in 2-D. A KD-tree is used to find nearest neighbors  to an image query on the manifold.

<p align="center">
<img src="https://github.com/vsmolyakov/cv/blob/master/manifold/figures/manifold_merged.png"/>
</p>

References:  
*L. Van Der Maaten, "Visualizing Data using t-SNE", JMLR 2008*  
*R. Szeliski, "Computer Vision: Algorithms and Applications", 2010.*  

**Visual Words**

Image search can be formulated as topic similarity for a topic model build from visual words. Visual words are cluster centers of image features extracted at image keypoints. In this example, dense SIFT features are extracted from a collection of 10 face images of 40 different people (the Olivetti faces dataset). The 128-dimensional SIFT features are clustered using mini-batch K-means into a dictionary of K visual words. An online variational bayes algorithm is used to learn the LDA topic model and extract topic proportions for training image data. Test image data is converted into topic space and training images are retrieved based on cosine similarity between topic proportions of the train and test images.

<p align="center">
<img src="https://github.com/vsmolyakov/cv/blob/master/visual_words/figures/visual_words_merged.png"/>
</p>

The figure above shows the Olivetti dataset mean training image (left) followed by the PCA visualization of visual words (middle). The learned visual topics are shown at the bottom. A random sample of test images along with the retrieved nearest neighbors are shown on the right.

Note that there is no overlap between training and test images (i.e. the individuals are different). Based on the retrieved nearest neighbors, we can see that certain faces explain the test images best, which suggests that ranking or post-processing of the retrieved results can improve performance.

References:  
*R. Szeliski, "Computer Vision: Algorithms and Applications", 2010.*  


### Dependencies

Matlab 2014a  
Python 2.7  
OpenCV  
