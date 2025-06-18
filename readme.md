# MuLTa-Telegram  
**A Multilingual and Multi-Target Dataset for Hate Speech and Target Detection on Telegram**

## Description

**MuLTa-Telegram** is a curated dataset comprising over 4,000 manually annotated messages collected from public Telegram channels in **Italian** and **Polish**. It is designed to support research in **hate speech detection**, with a particular focus on:
- The presence or absence of hate speech
- Identification of specific *target groups* of hate
- Thematic categorization of each message’s content (*topics*)

The dataset was developed to address the limitations of existing resources, which often:
- Focus on English-language content
- Lack fine-grained target annotations
- Are derived from platforms with increasingly restricted access, such as Twitter

Telegram, in contrast, is an influential but understudied platform that plays a critical role in fringe and extremist discourse due to its minimal content moderation and user anonymity.

## Contents

The repository includes:
- The full annotated dataset (CSV or JSON format)
- Annotation guidelines
- Pre-selection keyword matrix
- Scripts for processing and modeling
- Results from benchmark experiments
- Example notebooks

## Dataset Summary

| Language | Total Messages | Hate Speech | Non-Hate |
|----------|----------------|-------------|-----------|
| Italian  | 2,004          | 411 (20.5%) | 1,593     |
| Polish   | 2,022          | 257 (12.7%) | 1,765     |

### Target Categories
Annotations cover 9 primary identity groups, including:
- **Ethnicity/Origin** (People of Color, Romani, Migrants)
- **LGBT+ individuals**
- **Women**
- **Religious groups** (Jewish, Muslim, Christian)
- **People with disabilities**
- **Other** or **No Target** (as applicable)

Each message is also labeled for *topic relevance* independently of whether it is hateful.

## Methodology

- Messages were retrieved using a snowball sampling approach applied to public Telegram channels known for high toxicity or disinformation.
- Pre-selection of messages used a keyword-based filtering matrix covering all target categories.
- Annotations were performed by expert native speakers following a structured guideline developed in collaboration with civil society organizations.
- All data were anonymized in accordance with applicable privacy regulations.

## Benchmarking and Experiments

A comprehensive evaluation of the dataset was conducted using:
- Monolingual and multilingual **BERT-based models**
- **Multi-task learning** configurations (joint hate/target detection)
- Prompt-based classification using **LLaMA 3.1 Instruct** and **LLaMA Guard**

The highest classification performance (macro F1-score up to 0.818 for Polish) was achieved using a **multi-task BERT architecture** trained on the in-domain annotated data. Out-of-domain models trained on Twitter or other platforms performed significantly worse, confirming the necessity of domain-specific data for effective hate speech detection on Telegram.

## Access and License

The dataset is publicly available under the **Creative Commons Attribution 4.0 International License (CC BY 4.0)**.  
You are free to share and adapt the material for any purpose, provided appropriate credit is given.

**Access the data here**: [https://github.com/dhfbk/MuLTa-Telegram](https://github.com/dhfbk/MuLTa-Telegram)

## Citation

Please cite the following publication if you use this dataset:

```bibtex
@inproceedings{leonardelli2025multa,
  title={MuLTa-Telegram: A Fine-Grained Italian and Polish Dataset for Hate Speech and Target Detection},
  author={Leonardelli, Elisa and Casula, Camilla and Vecellio Salto, Sebastiano and Bąk, Joanna Ewa and Muratore, Elisa and Kołos, Anna and Louf, Thomas and Tonelli, Sara},
  booktitle={Proceedings of the Eleventh Italian Conference on Computational Linguistics (CLiC-it)},
  year={2025}
}
```

## Acknowledgements

This work was supported by the European Union’s CERV fund under Grant Agreement No. 101143249 (HATEDEMICS).
