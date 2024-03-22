# Readme

The code for this project is split over four independent IPython Notebooks, one for each stage of the methods used. In order of use, these are:

* **dataset.ipynb** : This contains methods for all dataset generation steps, including the extraction of equivalences from the ontologies of interest, the derivation of subsumptions from these, the generation of negative samples per each proposed strategy, and the generation of cross-encoder/bi-encoder input sentences for each of the feature configurations proposed. All artifacts are written to file, as part of the code.
* **tokenization.ipynb** : This contains methods for the tokenization of the generated sentences, read from file. The results are also written to file.
* **encoders.ipynb** : This contains the implementations of the bi-encoder and cross-encoder used, along with all the methods required to collate their datasets (from the tokenized data that is read from file), hyperparameter tune them, train them and test them. In the case of the bi-encoder there are also methods for extracting embeddings directly from the trained model to use with Faiss, and for the cross-encoder a special section is included for the final testing on the datasets produced using Faiss. All artifacts and model checkpoints are written to file.
* **faiss.ipynb** : This contains methods for testing Faiss similarity search on bi-encoder embeddings (read from file), producing relevant plots, and then generating datasets from the top ranked candidates for further cross-encoder testing. All artifacts are written to file.

## Run instructions

* The notebooks can be run independently using any IPython Notebook editor (e.g. Google Colab), by running the cell with the desired code, or all cells at once to have everything run in the appropriate order.

### Requirements

* Python 3.10.12
* Packages: Each notebook's first cells contain installations and imports of the required packages.
* Tested on Google Colab and Windows 10 (VS Code).

