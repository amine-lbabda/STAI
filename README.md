# STAI

## Hello, a little introduction about the project

This is the README of our final project which is related to ATEC hackation with some details about how we have built the model!

**Note:** Due to lack of time and experience in AI, the code in this notebook is 100% AI-generated. We encountered many errors while writing the code for unknown reasons, so we opted more for the copy-paste method and also, thanks to Copilot and Claude-AI for their help in reducing the time we need to make this prototype as an AI beginner and also, thanks to Bechir for his insane support for us.

## Why we opted for TensorFlow as a framework?

Of course, because it's the most suitable framework for beginners like us in AI. In fact, instead of writing long classes like `PyTorch`, we can use `tensorflow` in order to accelerate the workd due to the shortage of time. If we have enough time then we will opt more for PyTorch for its professionality and its usage in research.

## Dataset

The dataset used in this case is EuroSAT dataset as it is provided in the drive with the hackaton
**Note:** With a little bit of luck, we found that the dataset used in the Colab provided in this hackathon is already integrated into TensorFlow databases, so we opted for importing the dataset using the `tensorflow_datasets` package.

## How we have just made it?

Well, first of all we wanted ofc a pre-trained model due to it's "easy-to-use" curve learning. However, we just had a very bad accuracy so we turned out to a custom CNN and thanks to Copilot -again- we have made a CNN modal inspired from him and also the inspiration goes for TinyVGG model. In fact, our model  uses many layers under the hood:

- 1. `tf.keras.layers.Conv2D` which is a convultional 2D layer that extracts features from images that distinguish every picture and that's very important for the classification with a ReLu activation function which is important for our classification
- 2. `tf.keras.layers.MaxPooling2D` its purpose is to reduce the parameters and the computational power of the network
- 3. `tf.keras.layers.Flatten` to make the vector from 2D to 1D array
- 4. `tf.keras.layers.Dense` to connect all layers to each other.
Then,using gradio api, we built really quickly a little webapp which when we upload a satellite image we recieved from our satellites, we can see if the image does contain life on it. Because we filtred EuroStat dataset to only include categories that are related only to nature. (Thanks Bechir for this valuable advice !)

## Sources

- **Source of inspiration for our AI model:** <https://colab.research.google.com/drive/1bsHnSE_Cbffdr1FMGbwO7G6C1bgCh3K-#scrollTo=zEr-IM3-PWin>
- **EuroSat dataset:** <https://www.tensorflow.org/datasets/catalog/eurosat?hl=fr#eurosatrgb_default_config>
- **TinyVGG modal explainer**:<https://poloclub.github.io/cnn-explainer/#:~:text=In%20TinyVGG,%20the%20dot%20product%20operation%20uses%20a%20stride%20of#:~:text=In%20TinyVGG,%20the%20dot%20product%20operation%20uses%20a%20stride%20of>

- **Temporary webapp link (it expires within 72 hours)**:<https://7e5ab0603374d5b374.gradio.live/>
