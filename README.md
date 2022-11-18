# Named_Entity_Recognition

Problem Statement:
Information Extraction From Scientific Publication
Named Entity Recognition (NER) is one of the most popular applications of Natural Language Processing. We will focus on creating a NER model that identifies key tokens and classifies them into set of predefined entities.

The number of scientific papers published per year has exploded in recent years, strengthening its value as one of the main drivers for scientific progress. In astronomy alone, more than 41,000 new articles are published every year and the vast majority are available either via an open-access model or via pre-print services. Indexing the article’s full-text in search engines helps discover and retrieve vital scientific information to continue building on the shoulders of giants, informing policy, and making evidence-based decisions. Nevertheless, it is difficult to navigate in this ocean of data; finding articles rely heavily on string matching searches and following citations/references. NER helps us extract key information from scientific papers which can help search engines to better select and filter articles.

![image](https://user-images.githubusercontent.com/79005878/181880355-85bb44f3-2015-44f5-bebe-87073bc0062d.png)

### Dataset Description
Datasets from the NASA Astrophysical Data System that contain text snippets from astrophysics articles that have been carefully labelled with astronomical facilities and other entities of interest (e.g., celestial objects).
The JSON Lines format is used for data sets (each line is a json dictionary).
The datasets follow the CONLL2003 formatting guidelines. Each token has a NER tag attached to it. The tags follow to the IOB2 syntax's "B-" and "I-" conventions.

Link: https://huggingface.co/datasets/fgrezes/WIESP2022-NER

Each entry consists of a dictionary with the following keys:

* "unique_id": a unique identifier for this data sample. Must be included in the predictions.
* "tokens": the list of tokens (strings) that form the text of this sample. Must be included in the predictions.
* "ner_tags": the list of NER tags (in IOB2 format)
The following keys are not strictly needed by the participants:

* "ner_ids": the pre-computed list of ids corresponding ner_tags, as given by the dictionary in ner_tags.json
* "label_studio_id", "section", "bibcode": references for internal NASA/ADS use.
