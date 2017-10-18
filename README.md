"# speech_recognition"

Summary:

During the work two models were observed: Simple Audio Recognition from Tensorflow and the model
similar to introduced in https://yerevann.github.io/2015/10/11/spoken-language-identification-with-deep-convolutional-networks/.
Both of them were trained using dataset used in speech_commands example from Tensorflow.

Steps to reproduce:

For the first model:

1. Install Docker on your machine
2. Pull Tensorflow Docker image using following command: docker pull tensorflow/tensorflow
3. Run container: docker run -it -p 8888:8888 tensorflow/tensorflow
4. Go through the steps from the tutorial: https://www.tensorflow.org/versions/master/tutorials/audio_recognition

For the second model:

1. Install Anaconda2 package from https://www.anaconda.com/download/
2. Go to the Scripts directory and run: conda install -c anaconda theano \
                                        conda install -c anaconda lasagne
3. Download the files from the repository
4. Copy the dataset from the Docker container to Host
5. Change the `png_folder` and listfile paths in theano/main.py to your ones
6. Create spectrograms for all of the files from dataset using `create_spectrograms.py`
7. Run `theano/main.py`.