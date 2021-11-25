# Named Entity Recognition using Transformers
I have Fine-tuned BERT using HuggingFace transformers to perform Named Entity Recognition on Text data. BERT is a state-of-the-art model with attention mechanism as underlying architecture trained with masked-language-modeling and next-sentence-prediction objectives, used for various tasks including Question answering systems, Text Summarization, etc... which can also perform token classification tasks such as NER with great performance.

# Dataset
**CoNLL-2003** :
The shared task of CoNLL-2003 concerns language-independent named entity recognition. We will concentrate on four types of named entities: persons, locations, organizations and names of miscellaneous entities that do not belong to the previous three groups.<br><br>
**Link** : https://huggingface.co/datasets/conll2003

# Using this fine tuned version
Anyone can access this fine-tuned version from the huggingFace model hub.<br>Repo Link : https://huggingface.co/balamurugan1603/bert-finetuned-ner

From python, download the whole pipeline and use it instantly using the following code :
```
from transformers import pipeline

# Loading the pipeline from hub
# Pipeline handles the preprocessing and post processing steps
model_checkpoint = "balamurugan1603/bert-finetuned-ner"
namedEntityRecogniser = pipeline(
    "token-classification", model=model_checkpoint, aggregation_strategy="simple"
)
```

Example of using this pipeline to get NER tags is available in the notebook in this repository.
