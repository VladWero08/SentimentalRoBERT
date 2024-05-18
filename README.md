# 🇷🇴 SentimentalRoBERT

At the moment, current multilingual models fail to obtain optimal results in comparison with models trained exclusively on Romanian language data. The need for better models in our native language inspired our research question: how much does data from at face value opposite domains matter in the performance of **SOTA Romanian language** models?

The aim of the project was to finetune already pretrained BERTs on Romanian corpus in order to find an answer to the question. A detailed presentation of the project can be found in the *poster* uploaded.

# Datasets
### 1. LaRoSeDa
- *15.000* reviews labeled as *positive* and *negative*, with a balanced distribution.
- the dataset can be found [here](https://github.com/ancatache/LaRoSeDa/).

### 2. REDv2
- *5.449* tweets, multi-labeled with **7 possible classes** of emotions: anger, fear, joy, sadness, surprise, trust, neutral.
- the dataset can be found [here](https://github.com/Alegzandra/RED-Romanian-Emotions-Dataset/tree/main/REDv2).

# Models
- **RoBERT-base**: Romanian BERT-base sized model ([huggingface](https://huggingface.co/readerbench/RoBERT-base)).
- **RoBERT-small**: smaller version of *RoBERT-base* with: 12 layers, 256 hidden size, 8 attention heads (*19M weights*)
- **RomanianBERT-cased**: Romanian BERT-base sized model ([huggingface](https://huggingface.co/dumitrescustefan/bert-base-romanian-cased-v1)).

# Results
Here will be displayed the best results for each experiment, mode details can be found in the poster related to the other models trained.

**1. LaRoSeDa content only:**
| Architecture | Precision | Accuracy | Recall | F1 |
|--------------|-----------|----------|--------|----|
| RoBERT-base raw | 0.956 | 0.960 | 0.952 | 0.956 |

**2. LaRoSeDa title + content:**
| Architecture | Precision | Accuracy | Recall | F1 |
|--------------|-----------|----------|--------|----|
| RoBERT-small raw + random split | 0.983 | 0.987 | 0.979 | 0.983 |

**3. REDv2:**
| Architecture | Dataset | Samples | Accuracy | Hamming Loss |
|--------------|-----------|----------|--------|----|
| RoBERT-small | law | 3000 | 0.56 | 0.107 |
