# Image-Caption-Generator
# 🖼️ Image Caption Generator Using Deep Learning

## 📌 Project Overview

The **Image Caption Generator** is a Deep Learning project that automatically generates meaningful textual descriptions for images.

It combines **Convolutional Neural Networks (CNN)** and **Long Short-Term Memory (LSTM)** networks to understand image contents and generate relevant captions.

The project uses the VGG16 model for image feature extraction and an LSTM network for generating captions word by word. It also includes a text-to-speech feature to convert generated captions into audio.

## 🎯 Objectives

- Automatically generate captions for input images.
- Extract meaningful image features using a pre-trained CNN model.
- Generate natural language descriptions using an LSTM network.
- Evaluate generated captions using the BLEU score.
- Convert generated captions into speech.

## 🛠️ Technologies Used

- **Programming Language:** Python
- **Deep Learning Framework:** TensorFlow / Keras
- **CNN Model:** VGG16
- **RNN Model:** LSTM
- **Dataset:** Flickr8k
- **Libraries:** NumPy, Pandas, Matplotlib, NLTK, gTTS
- **Platform:** Google Colab

## 📂 Dataset

This project uses the **Flickr8k Dataset**, which contains images and their corresponding textual descriptions.

- Images folder: Contains the images.
- Captions file: Contains image names and their corresponding captions.
- The notebook selects the first 500 unique images for feature extraction and model training.

Dataset structure:

```text
Flickr8k/
│
├── Images/
│   ├── image1.jpg
│   ├── image2.jpg
│   └── ...
│
└── captions.txt
```

## ⚙️ Project Architecture

The project consists of the following steps:

1. **Data Preprocessing:** Clean captions by converting text to lowercase, removing punctuation, and adding start and end sequence tokens.

2. **Feature Extraction:** Use the pre-trained VGG16 model to extract 4096-dimensional feature vectors from images.

3. **Tokenization:** Convert words into numerical sequences using Keras Tokenizer.

4. **Model Building:** Combine image features and text sequences using an LSTM-based encoder-decoder architecture.

5. **Model Training:** Train the model using image features and corresponding captions for 10 epochs.

6. **Caption Generation:** Predict words sequentially until the end sequence token is generated.

7. **Evaluation:** Calculate the BLEU score to evaluate the generated caption against a reference caption.

8. **Text-to-Speech:** Convert the generated caption into audio using Google Text-to-Speech (gTTS).

## 🔄 Workflow

```text
       Input Image
            |
            v
       VGG16 Model
            |
            v
   Image Feature Extraction
            |
            v
      LSTM Network
            |
            v
   Caption Generation
            |
            v
    Generated Caption
            |
       +----+----+
       |         |
       v         v
   BLEU Score   Text-to-Speech
                   |
                   v
               Audio Output
```

## 📦 Installation

Install the required libraries:

```bash
pip install tensorflow numpy pandas matplotlib nltk gTTS
```

## ▶️ How to Run the Project

1. Clone this repository:

```bash
git clone https://github.com/your-username/Image-Caption-Generator.git
```

2. Open the Jupyter Notebook in Google Colab.

3. Upload or mount your Google Drive.

4. Download the Flickr8k dataset and place it in the required Google Drive folder.

5. Update the dataset paths in the notebook if necessary.

6. Run all notebook cells sequentially.

7. The model will generate captions for sample images.

8. The generated captions can also be converted into speech.

## 📊 Evaluation

The project uses the **BLEU (Bilingual Evaluation Understudy) Score** to measure the similarity between the generated caption and a reference caption.

A higher BLEU score generally indicates greater similarity between the generated and reference captions.

## ✨ Features

- Automatic image caption generation.
- Deep learning-based image understanding.
- VGG16-based image feature extraction.
- LSTM-based sequence generation.
- BLEU score evaluation.
- Text-to-speech conversion.
- Visualization of images with generated captions.

## 🚀 Future Enhancements

- Train the model using a larger image dataset.
- Improve caption accuracy and natural language generation.
- Develop a user-friendly web application.
- Support multiple languages.
- Integrate more advanced deep learning architectures.

## 👩‍💻 Project Information

**Project Name:** Image Caption Generator Using Deep Learning

**Domain:** Artificial Intelligence and Deep Learning

**Dataset:** Flickr8k

**Platform:** Google Colab

## 📜 Conclusion

The Image Caption Generator demonstrates how Deep Learning can combine computer vision and natural language processing to automatically describe images. By integrating VGG16 and LSTM, the system extracts visual information and generates meaningful textual descriptions. The addition of text-to-speech makes the project more accessible and interactive.
