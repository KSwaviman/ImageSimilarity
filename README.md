# ImageSimilarity
Apply machine learning to find top 10 similar images from a gallery folder given a query image.

Skills used:

Python //
Deep Learning //
TensorFlow 
Keras
Transfer Learning


# 1. Competition: 
During the class we will release a brand new test dataset containing two folders: one for queries and one for gallery. Each group shall test their models and submit the results on a server that will reply with the achieved accuracy. The group that obtains the highest accuracy will win the competition. Here some useful information:
a. The group shall show how the models have been tested, showing some quantitative and qualitative results.
b. Each team shall submit a working code that shall produce similar to the presented results.

# 2. Objectives: 
The main objective of this project is to create an image search engine where a query image is fed to a model that will return the most N similar images from a gallery. The following example shows the problem of retrieving the same place based on a visual search algorithm.
a. Given the input query image, the algorithm has to be capable of matching the input query image with another gallery image depicting the same animal.
![image](https://user-images.githubusercontent.com/20270507/170303102-00fedf5c-04bc-4ce9-81f9-9d7e77937207.png)

b. The expected algorithm’s output is therefore a list of ranked matches between the query image and the gallery images. An example output is depicted below where the top-k matches are reported. In this case, the algorithm correctly matched top-1 and top-2 images while the others (the ones reported) are false matches.

![image](https://user-images.githubusercontent.com/20270507/170303200-766e17d9-aecc-45cf-9cf1-02814be744e6.png)

c. At this point it is important to define how a match can be defined. Among all the
possibilities, one of the most used method is the definition of a similarity/distance
𝑑([], []) metric on top of extracted image features. As we saw during the colab
example, once we extracted the query image features 𝑓q, we can compute a 𝑞
similarity/distance measure between our query 𝑓q and each gallery 𝑓g.

![image](https://user-images.githubusercontent.com/20270507/170303281-0cce886e-3626-4e88-94d2-5d906f3ae5ad.png)

d. Once the feature distance between each gallery image 𝐼g and our query image Iq has
been computed, we can sort each match based on 𝑑(𝑓q, fg) matches as the top-k
gallery images with the lowest feature distance from our query.

![image](https://user-images.githubusercontent.com/20270507/170303323-edc977b3-b3d7-4194-82ec-627ee0a4ba84.png)

e. The given algorithm can be either pretrained on an external source of data (eg. a
dataset of landmarks) or run simply at test time without any learned parameter.
Please, note that the algorithm is not trained on the gallery data, otherwise this would
be a simple classification ;)

f. A secondary objective of the project is to learn how to collect data. As we are seeing during the course, collecting a large amount of data is crucial for ML applications. Therefore, you are required to largely expand the provided training data in order to improve your algorithm performance on the test set. Let’s see more details in the next section.

# 3. Data: 
we provide only an initial small amount of data but you are free to collect as much data as you like to train your model to improve your algorithm performance. The provided initial dataset is composed of a training set and a validation set. The training set is composed of 1300 images belonging to 10 different animals. The validation set has a gallery of 550 images with the 10 classes, a query of 100 images (10 for each of the 10 classes) and 200 distractor images. Finally, during the challenge day we will release the test set to measure the performance of your algorithm and to fill the leaderboard. 

# 4. Methods to use: 
you can use any of the methods you learned during the course (supervised/unsupervised, traditional/deep, etc). We encourage you not to limit the solution to just one method, but instead to try out different ones in order to better understand their strengths and limitations and report results obtained by each method.
