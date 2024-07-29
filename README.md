# Named Entity Recognition with Transformers

This project implements a Named Entity Recognition (NER) model using the Hugging Face Transformers library for identifying named entities in text data. The model is trained on the "adsabs/WIESP2022-NER" dataset.

## Dataset Description
The dataset employed for training this NER model comprises text excerpts derived from astrophysics research papers. Human experts meticulously annotated these excerpts to identify and categorize relevant entities such as astronomical facilities and celestial objects.

The dataset adheres to the JSON Lines format, with each line representing an individual data sample. It aligns with the CONLL2003 standard, assigning NER tags (B-, I-, O) to tokens within the text.

## Installation

To install the required packages, run the following command:

```bash
pip install transformers datasets tokenizers seqeval
```
## Usage
1. Load the data using the load_dataset function from the Hugging Face datasets library.
2. Prepare the data by tokenizing and aligning the labels.
3. Train and evaluate the model using the provided datasets.
4. Save the trained model and tokenizer for future use.
5. Make predictions using the fine-tuned model.


## Usage Example
```python
from transformers import pipeline
nlp = pipeline("ner", model=model_fine_tuned, tokenizer=tokenizer)
example_text = "Insert your sample text here"
ner_results = nlp(example_text)
print(ner_results)
```
## Training and Evaluation
The model was trained for 10 epochs, and the achieved accuracy after training is as follows:
- Precision: 0.810551
- Recall: 0.839719
- F1-score:0.824877
- Accuracy:0.948467
