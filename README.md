# nlp-cas-dsmh

Hands-on Jupyter notebooks on tokenization, embeddings, semantic search, prompting, and RAG for clinical text.

## Notebooks

| Notebook | Topic | Open |
|---|---|---|
| `notebooks/lab0_setup.ipynb` | Setup — create and store your Gemini API key (run this first) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/angeloziletti/nlp-cas-dsmh/blob/main/notebooks/lab0_setup.ipynb) |
| `notebooks/lab1_tokenization_embeddings.ipynb` | Tokenization, embeddings, semantic search, context | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/angeloziletti/nlp-cas-dsmh/blob/main/notebooks/lab1_tokenization_embeddings.ipynb) |
| `notebooks/lab2_prompting_clinical_text.ipynb` | Prompting a language model for clinical text (Gemini API) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/angeloziletti/nlp-cas-dsmh/blob/main/notebooks/lab2_prompting_clinical_text.ipynb) |
| `notebooks/lab3_rag.ipynb` | Building a Retrieval-Augmented Generation (RAG) system (Gemini API) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/angeloziletti/nlp-cas-dsmh/blob/main/notebooks/lab3_rag.ipynb) |
| `notebooks/lab4_agent.ipynb` | Building a healthcare agent (Gemini API + SQLite tools) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/angeloziletti/nlp-cas-dsmh/blob/main/notebooks/lab4_agent.ipynb) |

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

### Gemini API key (Labs 0, 2, 3, 4)

Lab 0 walks you through creating the key; labs 2, 3, and 4 call the Gemini API and need it. Set it as an environment variable *before* launching Jupyter:

```powershell
# Windows PowerShell
$env:GEMINI_API_KEY = "your-key-here"
```

```bash
# macOS / Linux
export GEMINI_API_KEY=your-key-here
```

In Colab, store it as a Secret named `GEMINI_API_KEY` instead (the 🔑 icon, with *Notebook access* on). Lab 1 needs no key.

## Data

`data/` contains synthetic and public-domain samples used by the notebooks. No real patient data is used anywhere in this repository.
