# Img2TextCollection
This repository contains an image-to-text pipeline leveraging the Flickr8k Dataset and transformer models for caption generation. It demonstrates the application of deep learning techniques in computer vision and natural language processing to convert image data into descriptive text.
Dataset Used
Flickr8k Dataset: A collection of 8,000 images, each annotated with five descriptive captions. It’s widely used for image captioning tasks.
Features
Data Loading: The get_data() function fetches and extracts the Flickr8k_Dataset and associated text annotations from a public GitHub repository.
Captions Handling: The get_dataset() function reads the captions from Flickr8k.token.txt, splits them by image, and organizes them in a dictionary. It also loads the image paths for both the training and test sets from Flickr_8k.trainImages.txt and Flickr_8k.testImages.txt.
Dataset Preparation: Converts image-caption pairs into TensorFlow datasets (train_raw and test_raw) for further processing in the model pipeline.
Preprocessing Steps
Download Data: The images and their corresponding captions are downloaded and extracted from a hosted source using TensorFlow’s tf.keras.utils.get_file.
Text Tokenization: Captions are processed by splitting each line to create a mapping between image file paths and their captions.
Dataset Construction: Image paths for both training and testing sets are combined with their respective captions to generate raw datasets for model training and evaluation.
Requirements
Python 3.x
TensorFlow: Required for data handling and utility functions.
pathlib: For working with file paths.
collections: For organizing captions using a default dictionary.
