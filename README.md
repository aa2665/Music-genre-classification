# Music Genre Classification using KMC:
## 1.KMC - K-means cluster method
- Unsupervised learning
- Each cluster represent for each genre

## 2. Extract MFCC features
Using `librosa` librosa to extract the data set, the dataset used is `gtzan` dataset

## 3. Create the K-means cluster
- Using `parseAudio` function,reading the file extracted by MFCC
- Labels different genres as subDir

## 4. Prepare the data
Split the data into:
- **train set**: 80% of the dataset
- **test set**: 20% of the dataset

## 5. Train the data with KMC model

## 6. Evaluate the model
- The model is evaluated by train/test accuracy.
- The accuracy is inconsistent as we continuously run the script since cluster might differs with different mfcc train sets

- # K-nearest neighbors

## Steps to build Music Genre Classification using KNN:

#### 1. Define a function to get the distance between feature vectors and find neighbors
Calculate distance between feature vectors so that we can find the k-neighbors by selecting k subsets with the smallest distance

#### 2. Identify the nearest neighbors
From the neighbors get the nearest one. These k-neighbors already have their classes labeled, so we will do the majority voting. So out of these k-neighbors, we directly see the majority class and whatever be the majority class, becomes the predicted class

#### 3. Define a function for model evaluation    
Calculate the accuracy of the predictions `accuracy = 1.0*correct/len(testSet)`

#### 4. Extract features from the dataset and dump these features into a binary .dat file “my.dat”
Using MFCC (Mel Frequency Cepstral Coefficients)
* Divide the signals into smaller frames. Each frame is around 20 ms long
* Identify different frequencies present in each frame
* Separate linguistic frequencies from the noise
* To discard the noise, it then takes discrete cosine transform (DCT) of these frequencies. Using DCT we keep only a specific sequence of frequencies that have a high probability of information
 
#### 5. Train and test split on the dataset

#### 6. Make prediction using KNN and get the accuracy on test data

