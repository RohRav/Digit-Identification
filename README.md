# Digit and Face Identification Project
This project used an algorithm called Perception and a Naive Bayesian algorithm in order to identify digits and faces. Perceptron is an algorithm that applies a weighted number to the value of each feature in order to run predictions. These weights are changed depending on whether the algorithm’s prediction was correct or not. The dot product of the vector of weights and features is taken in order to apply an overall prediction to an image. If the dot product is negative, then the algorithm predicted the image shown is not the same type of image as the label it is being compared to. And if the dot product is positive, then it predicted it is the same type of image as the compared label. During training if perceptron gets a negative dot product but the trained image actually is thesame type of image as its compared label, then the weights are too low and the values of the corresponding features are added to the weights. And if the dot product is positive, but images are not the same type, then those features are subtracted from the weights.

Perceptron is a highly adaptive prediction algorithm, and this is especially seen indigits, which starts at 66% accurate to 93% accurate. Accuracy growth is also seen in faces, butthe algorithm seems to start out relatively accurate at 61% and grows to 90%, a 29% growth. One lesson from this data is that perceptron can be accurate, but without enhancements to the core algorithm, the growth rate of the accuracy slows significantly, especially starting at around 85%. This is further seen in how iterations affect the accuracy, there was no significant change in accuracy between 13 iterations and 50 iterations for example

Naive Bayes is an algorithm that assumes every pixel is independent of each other and calculates the probability of each pixel matching the label. All of these probabilities are then multiplied together and then multiplied with the probability of that label being represented, meaning the prior probability. This entire value is divided by the marginal probability. This function can be represented by P(A|B)=P(B|A)*P(A)/P(B)

It can be inferred from the data that Naive Bayes is accurate with a lot of training, as can be seen especially in the digits testing, but that accuracy growth diminishes significantly as the data set grows larger and larger. The accuracy barely grows between a data set of 1000 and 5000, so this form of Naive Bayes seems to cap at around 91%-94% for detecting these types of digits. Faces sees an accuracy growth, but plateaus and even declines a bit towards the end. 

Even though both perceptron and naive Bayesian showed similar accuracy of over 80 percent, they have different time needed for training. In the case of data, both perceptron and naive Bayesian used exactly the same number of training data. It does not show much difference when 10% of the data set is used. For example, perceptron takes about 9 seconds while naive Bayesian take about 6 seconds. However, as the dataset grows, the difference also grows rapidly. When we use 50 data sets, perceptron takes about 22 seconds to train and naive Bayes take about 6 seconds. When we use 100 data sets, the naive Bayesian takes about 7 seconds while the perceptron takes over 40 seconds. Thus, naive Bayesian’s algorithm are faster than perceptron’s. Therefore, if we have enough data to train, it is preferable to use naive Bayesian.
