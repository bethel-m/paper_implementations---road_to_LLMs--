# Papers in PyTorch

This repository is a collection of Jupyter notebooks that build high-level, educational implementations of ideas from influential language-modeling papers. The models are implemented with PyTorch and use the small text and preference datasets included in the repository.

## Notebooks

| Folder | Main notebook | Paper |
| --- | --- | --- |
| `paper1_sequence_to_sequence/` | `paper1.ipynb` | Sequence to Sequence Learning with Neural Networks — Sutskever et al. (2014) |
| `paper2_neural_machine_translation/` | `paper2.ipynb` | Neural Machine Translation by Jointly Learning to Align and Translate — Bahdanau et al. (2014) |
| `paper3/` | `paper3.ipynb` | Attention Is All You Need — Vaswani et al. (2017) |
| `paper4/` | `paper4.ipynb` | Improving Language Understanding by Generative Pre-Training (GPT-1) — Radford et al. (2018) |
| `paper5/` | `paper5.ipynb` | LLaMA: Open and Efficient Foundation Language Models — Touvron et al. (2023) |
| `paper6/` | `paper6.ipynb` | LoRA: Low-Rank Adaptation of Large Language Models — Hu et al. (2021) |
| `paper7/` | `paper7.ipynb` | Direct Preference Optimization — Rafailov et al. (2023) |

Some folders also contain notebook variants. Files ending in `_with_prints` include additional diagnostic output; Paper 3 also has optimized variants, and Paper 2 has an alternate `paper2_.ipynb` notebook.

## Requirements

- Python 3.12 or newer
- [uv](https://docs.astral.sh/uv/)

The project dependencies and exact resolved versions are declared in `pyproject.toml` and `uv.lock`. Install them from the repository root:

```sh
uv sync
```

## Run a notebook

Start Jupyter from the notebook's folder so its relative paths to data files resolve. For example, to run Paper 4:

```sh
cd paper4
uv run --project .. jupyter notebook paper4.ipynb
```

Replace `paper4` and `paper4.ipynb` with the folder and notebook you want to explore. The sequence-to-sequence, neural machine translation, and Transformer notebooks read the shared `../deu.txt` file; the other notebooks read files in their own folders.

## Data and model files

- `deu.txt` contains the text used by the early translation and Transformer notebooks.
- `paper4/` includes text input and an IMDb review sentiment CSV.
- `paper5/` and `paper6/` include text input; `paper6/` also includes a pretrained model checkpoint.
- `paper7/` includes text input, preference-pair data in JSONL and CSV formats, and a pretrained model checkpoint.

The notebooks are intended for learning and experimentation. Training time and results depend on the notebook settings and available hardware.
