# CNN Design Challenge
A single-notebook project to design, train, and evaluate a **sequential CNN** on a Tiny‑ImageNet–style dataset (64×64 RGB, 15 classes). No pretrained models, no residuals/attention—just Conv/BN/ReLU/Pool/Dropout/Flatten/Linear per course rules.

## Files
- `CNN_Design_Challenge_Full.ipynb` — the entire pipeline (EDA → train → eval → report).
- `requirements.txt` — minimal deps (PyTorch, torchvision, NumPy, Matplotlib, scikit‑learn, Pillow).
- `train-70_.pkl`, `validation-10_.pkl` — training/validation data (place next to the notebook or in `./data/`).
- `checkpoints/` — created at runtime; saves `model.pth`, `meta.json`, `history.json`.

## Quickstart
**Windows (PowerShell)**
```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
pip install -r requirements.txt
```

**macOS / Linux**
```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install --upgrade pip
pip install -r requirements.txt
```

Open the notebook (`CNN_Design_Challenge_Full.ipynb`) in Jupyter/VS Code and **Run All**.

## Data placement
By default the notebook looks in the **current folder**. If the pickles aren’t here, it will try `./data/`.
You can also override via environment variables:
```
DATA_DIR=/path/to/data TRAIN_PKL=train-70_.pkl VAL_PKL=validation-10_.pkl
```

