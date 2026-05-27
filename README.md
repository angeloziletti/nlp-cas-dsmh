# NLP & LLMs in Healthcare — Course Materials

Hands-on notebooks for **Module M4: NLP & LLMs in Healthcare** (CAS DSMH).

## Notebooks

| Notebook | Topic | Open |
|---|---|---|
| `notebooks/lab1_tokenization_embeddings.ipynb` | Tokenization, embeddings, semantic search, context | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/angeloziletti/nlp-cas-dsmh/blob/main/notebooks/lab1_tokenization_embeddings.ipynb) |

## How to run

You have two options. Pick one.

### Option A — Google Colab (no install)

Click the **Open in Colab** badge above. Everything runs in the browser; no setup required. Recommended for the live class.

### Option B — Local install

Run the notebook on your own machine. Useful if you want to keep the environment after the course, work offline, or use a GPU you already have.

**With conda (recommended):**

```bash
git clone https://github.com/angeloziletti/nlp-cas-dsmh.git
cd nlp-cas-dsmh
conda env create -f environment.yml
conda activate nlp-cas-dsmh
jupyter notebook notebooks/lab1_tokenization_embeddings.ipynb
```

**With pip / venv:**

```bash
git clone https://github.com/angeloziletti/nlp-cas-dsmh.git
cd nlp-cas-dsmh
python -m venv .venv
# Windows:
.venv\Scripts\activate
# macOS/Linux:
source .venv/bin/activate
pip install -r requirements.txt
jupyter notebook notebooks/lab1_tokenization_embeddings.ipynb
```

First run downloads ~500 MB of model weights (PubMedBERT + BERT). After that, everything is cached locally.

## Data

`data/` contains synthetic and public-domain samples used by the notebooks. No real patient data is used anywhere in this repository.
