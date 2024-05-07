# Machine Learning for Healthcare, Spring 2024, Group 2 Project.

## Required Files

The `embeddings.csv` file is required to run the models and analysis.  It is located in the `Embeddings.zip` file located on [Google Drive](https://drive.google.com/drive/folders/1damVQo2Or3lejz_Ox2pQKXsQtXT78Lt2).  The specific file used in the archive was `Embeddings/brset/embeddings.csv`.

The `labels.csv` file is taken from the BRSET dataset and can be downloaded from [Physionet](https://physionet.org/content/brazilian-ophthalmological/1.0.0/).  The images are also required in order to run `image_analysis.ipynb`.  Running this ipynb file will also require [Model Weights](https://drive.google.com/file/d/1ExReZmG3yKUbNWgrovIKNSdRJq6ZWV3O/view) for the Convextv2 model.


## Required Libraries

Python 3.10.14 was used.  To install the required libraries, run the following command:

```bash
pip install -r requirements.txt
```

## Notebook Description

`resplit_data.ipynb` contains the code to resplit the data into training, validation, and test sets based on patient_id so no patient is in more than one set.

`image_analysis.ipynb` contains the code for analyzing the BRSET dataset using a Convextv2 model with weights provided by David Restrepo.  The model is used to predict diabetic retinopathy from the images in the dataset.

`text_analysis.ipynb` contains the code to analyze the tabular data from `labels.csv` file, which where used to generate synthetic notes for the text embeddings.

`fusion.ipynb` contains the code for the fusion models, which combine the image and text embeddings to predict diabetic retinopathy.

`calc_stats.ipynb` contains the code to calculate the statistics for the models based on saved prediction probabilities generated from the above notebooks.
