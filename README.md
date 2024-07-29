# Named Entity Recognition with Transformers

This project implements a Named Entity Recognition (NER) model using the Hugging Face Transformers library for identifying named entities in text data. The model is trained on the "adsabs/WIESP2022-NER" dataset.

## Installation

To install the required packages, run the following command:

```bash
pip install transformers datasets tokenizers seqeval
```
## Usage
1-Load the data using the load_dataset function from the Hugging Face datasets library.
2-Prepare the data by tokenizing and aligning the labels.
3-Train and evaluate the model using the provided datasets.
4-Save the trained model and tokenizer for future use.
5-Make predictions using the fine-tuned model.

## Usage Example
```python
from transformers import pipeline
nlp = pipeline("ner", model=model_fine_tuned, tokenizer=tokenizer)
example_text = "Insert your sample text here"
ner_results = nlp(example_text)
print(ner_results)
```
