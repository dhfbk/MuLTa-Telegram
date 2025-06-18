# MuLTa-Telegram  
**A Multilingual and Multi-Target Dataset for Hate Speech and Target Detection on Telegram**

## Description

**MuLTa-Telegram** is a curated dataset comprising over 4,000 manually annotated messages collected from public Telegram channels in **Italian** and **Polish**. It is designed to support research in **hate speech detection**, with a particular focus on:
- The presence or absence of hate speech
- Identification of specific *target groups* of hate
- Thematic categorization of each message’s content (*topics*)

## Contents

The repository includes:
- The full annotated dataset (JSON format)
- Annotation guidelines
- Pre-selection keyword matrix
- Scripts for processing and modeling

## Dataset Summary

| Language | Total Messages | Hate Speech | Non-Hate |
|----------|----------------|-------------|-----------|
| Italian  | 2,004          | 411 (20.5%) | 1,593     |
| Polish   | 2,022          | 257 (12.7%) | 1,765     |

### Target Categories
Annotations cover 9 primary identity groups, including:
- **Ethnicity/Origin** (People of Color, Romani, Other)
- **LGBT+**
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


## Access and License

The dataset is publicly available under the **Creative Commons Attribution 4.0 International License (CC BY 4.0)**.  
You are free to share and adapt the material for any purpose, provided appropriate credit is given.

**Access the data here**: [https://github.com/dhfbk/MuLTa-Telegram](https://github.com/dhfbk/MuLTa-Telegram)


## Acknowledgements

This work was supported by the European Union’s CERV fund under Grant Agreement No. 101143249 (HATEDEMICS).
