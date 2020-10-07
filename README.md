# Text-Classification-on-imdb-reviews
1. The data is split into 25,000 samples for training and 25,000 samples for testing. The training data and the labels are extracted from the trainiing samples, the same is for the testing data. The list of labels is converted into numpy arrays.  
2. The sentences will be tokenized giving the vocabulary size and the desiried out of vocabulary token as hyperparameters.  
3. The sequencies will be padded determined by the maximun length parameter.  

This procedure is being followed both for training and testing data.  

The architecture of the model is as follows:

1. An Embedding Layer embeds the vocabulary  that is 10,000 in the embeddimg dimension that is 16 and has input length as the max length of the sequences that is 120.
2. A Flatten Layer that flattens the embedding layer that is a 2D array with dimension imput length x embedding dimension.
3. A Dense Layer with 6-units and Relu activation function.
4. A Dense Layer with 1-unit and Sigmoid activation function.

The model is compiled with binary crossentropy as loss function  and adam as optimizer.
The model is training for 10 epochs on the padded training data and is tested on the padded testing data. The accuracy is 100% and the validation accuracy is 82.35%

The Tensorflow  Projector visualizes the vectors in  3D space. To the vectors file,  we simply write out the value of each of the items the array of embeddings. To the metadata array, we just write out  the words. The visualization of the trained classifier can be seen there: https://projector.tensorflow.org/.
