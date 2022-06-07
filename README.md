# MailSweeper
MailSweeper is an application that identifies spam mails based on attached images which are being used in order to avoid detection by text-based spam filters. Textual data from images are extracted and analyzed in order to classify mails as spam or not. This can aid individuals in identifying spam and unwanted mails that can be deleted as a way for them to reduce their carbon footprint.

J.H. Galino (THX)

A.M. Hernandez (THV)

H. Olano (THX)

F.L. Ramirez (THU)

## Dependencies
Make sure that you have Python 3 installed on your device. You can download Python 3 [here](https://www.python.org/).

The following Python packages are required:
- [numpy](https://pypi.org/project/numpy/)
- [pandas](https://pypi.org/project/pandas/)
- [seaborn](https://pypi.org/project/seaborn/)
- [matplotlib](https://pypi.org/project/matplotlib/)
- [scikit-learn](https://pypi.org/project/scikit-learn/)
- [imbalanced-learn](https://pypi.org/project/imbalanced-learn/)
- [pytesseract](https://pypi.org/project/pytesseract/)
- [pillow](https://pypi.org/project/Pillow/)
- [opencv](https://pypi.org/project/opencv-python/)
- [gensim](https://pypi.org/project/gensim/)
- [nltk](https://pypi.org/project/nltk/)
- [jupyter notebook](https://pypi.org/project/notebook/)

You can install the Python dependencies of the project using this command:
```
pip install numpy pandas seaborn matplotlib scikit-learn imbalanced-learn pytesseract Pillow opencv-python gensim nltk notebook
```

### Notes
#### Pytesseract
To use `pytesseract`, the Tesseract engine and the trained data needs to be installed as well. Instructions for the installation can be found [here](https://tesseract-ocr.github.io/tessdoc/Installation.html)

#### Nltk
`nltk` needs the `wordnet` data resource for this project. The following code snippet needs to be inserted in `TextProcessing.ipynb` on the first run.
```python
import nltk
nltk.download('wordnet')
```

## Project Structure
The `Code` folder contains the Jupyter Notebooks used for this project.
- `Preprocessing.ipynb` contains the code used to prepare the images for text extraction.
- `OCR.ipynb` contains the code used to extract text from the images.
- `TextProcessing.ipynb` contains the code used to get features from the extracted text. 
- `Modelling.ipynb` contains the code used to create models from the extracted features.

The `Data` folder contains the data used by the project.
- The `Raw` folder contains the raw images, divided by the dataset from which they were obtained.
- The `Processed` folder contains the processed images from `Raw`.
- `text_content.csv` is a csv file containing the extracted text from the images in the `Processed` folder.
- `text_processed.csv` is a csv file containing the features extracted from the text found in the images.
- `set_test.csv` and `set_train.csv` contain the test and training data respectively.

## Execution
The Jupyter notebooks should be run in this order.
1. `Preprocessing.ipynb`
2. `OCR.ipynb`
3. `TextProcessing.ipynb`
4. `Modelling.ipynb`
