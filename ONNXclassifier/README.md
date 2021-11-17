
[<img src="https://deepnote.com/buttons/launch-in-deepnote-small.svg">](https://deepnote.com/@econdesousa/ONNX-classifier--SAueRQOQtqSgs5buXZkxA)

# ONNXclassifier

Sharing DL models between frameworks or programming languages is possible with Open Neural Network Exchange ([ONNX](https://microsoft.github.io/ai-at-edge/docs/onnx/) for short).

This notebook starts from an onnx model exported from MATLAB and uses it in Python.

On MATLAB a GoogleNet model pre-trained on ImageNet was loaded and saved to onnx file format through a one-line command [exportONNXNetwork(net,filename)](https://www.mathworks.com/help/deeplearning/ref/exportonnxnetwork.html).

The model is then loaded here, as well as the data to evaluate (some images retrieved from google).

Images are preprocessed to the desired format np.array with shape (BatchSize, numChannels, width, heigh), and the model is applied to classify the images and get the probabilities of the classifications.
