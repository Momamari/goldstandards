# Repo to generate probabilistic goldstandards using crowd-kit based on event annotations and comparing those with a manual goldstandard and predictions based on the event classifier

## Codes

- includes 3 notebooks
    - [00_clean_event_data.ipynb](codes/00_clean_event_data.ipynb): Reads in the event annotations including two annotation collections and one goldstandard and extracts relevant information for generating the probabilistic ground truths
    - [01_generate_gold.ipynb](codes/01_generate_gold.ipynb): Treats the extracted information to generate probabilistic gold truths and generates confusion matrices and f1-scores
    - [02_compare_golds_predicitions.ipynb](codes/02_compare_golds_predicitions.ipynb): Matches the prediction spans from the event classifier with the spans from the gold truths and generates confusion matrices and f1-scores

## Data

- data (dir)
    - input: includes basic (raw) files e.g. event annotation data and original training splits
    - output: includes a dir for each text that includes probabilistic goldlabels in comparison, table with differences and table for comparison with predictions
    - tables: cleaned data tables and tables relevant for prob. ground truth generation that include e.g. item ids
    - plaintexts: original texts
    - results_classifier: for each text predictions from event classifier



## Execution
- see requirements.txt
- Executed with Python 3.15.2