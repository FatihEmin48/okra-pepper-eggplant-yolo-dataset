# Okra, Pepper & Eggplant Detection Dataset

A multi-class object detection dataset covering growth stages of three vegetable species: **okra**, **pepper**, and **eggplant**. Labels are in YOLO format.

---

## 📊 Dataset Statistics

### Split Distribution

| Split | Original Images | External Images | Total Images |
|-------|---------------:|----------------:|-------------:|
| Train | 622 | 76 | 698 |
| Valid | 143 | 15 | 158 |
| Test  | 152 | 21 | 173 |
| **Total** | **917** | **112** | **1029** |

---

### Class Distribution

| ID | Class | Original | External | Total |
|----|-------|--------:|--------:|------:|
| 0 | okraFlower | 91 | — | 91 |
| 1 | okraFruit | 207 | 107 | 314 |
| 2 | okraBud | 498 | — | 498 |
| 3 | okraSeed | 1909 | — | 1909 |
| 4 | pepperFlower | 59 | — | 59 |
| 5 | greenPepper | 288 | 85 | 373 |
| 6 | redPepper | 89 | — | 89 |
| 7 | pepperSeed | 1920 | — | 1920 |
| 8 | eggplantFlower | 119 | — | 119 |
| 9 | eggplantFruit | 171 | 93 | 264 |
| 10 | eggplantSeed | 2317 | — | 2317 |
| 11 | eggplantBud | 109 | — | 109 |
| | **Total** | **7777** | **285** | **8062** |

> External images cover only 3 classes: `okraFruit`, `greenPepper`, and `eggplantFruit`. All remaining 9 classes are sourced exclusively from original data.

---

## 📁 Folder Structure

```
dataset/
├── train/
│   ├── images/
│   └── labels/
├── valid/
│   ├── images/
│   └── labels/
├── test/
│   ├── images/
│   └── labels/
├── data.yaml
└── README.md
```

---

## 🏷️ Label Format

Labels are in **YOLO format** (`.txt`). Each line represents one object:

```
<class_id> <x_center> <y_center> <width> <height>
```

All values are normalized between 0 and 1.

---

## 📦 Data Sources

### Original Data — 30 June 2025
Field images collected and labeled by the authors. Covers all 12 classes across the full growth cycle of okra, pepper, and eggplant.

### External Data — 5 May 2026
Additional images sourced from Roboflow Universe to supplement underrepresented fruit classes:

| Class | Source |
|-------|--------|
| okraFruit | [RRC — Okra Dataset](https://universe.roboflow.com/rrc-5bsjx/okra-k5mxw) |
| greenPepper | [Pepper Dataset](https://universe.roboflow.com/pepper-xngas/pepper-gfm9z) |
| eggplantFruit | [Intan — Eggplant Dataset](https://universe.roboflow.com/intan-abpkp/eggplant-6ea17) |

External images can be identified by the `.rf.` pattern in their filenames (e.g., `imm-1-8-_jpeg.rf.c4865fc4f397a97bb822fe7b2ba1fc0b.jpg`).

---

## ⚙️ Configuration

`data.yaml`:

```yaml
nc: 12
names: ['okraFlower', 'okraFruit', 'okraBud', 'okraSeed',
        'pepperFlower', 'greenPepper', 'redPepper', 'pepperSeed',
        'eggplantFlower', 'eggplantFruit', 'eggplantSeed', 'eggplantBud']
```

---

## 📄 License

This dataset is licensed under [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/).

You are free to share and adapt the material for any purpose, even commercially, as long as appropriate credit is given.

External images (Roboflow Universe) are subject to the license of their respective source datasets:
- [RRC — Okra Dataset](https://universe.roboflow.com/rrc-5bsjx/okra-k5mxw)
- [Pepper Dataset](https://universe.roboflow.com/pepper-xngas/pepper-gfm9z)
- [Intan — Eggplant Dataset](https://universe.roboflow.com/intan-abpkp/eggplant-6ea17)

---

## ✉️ Contact

For questions or collaboration, please open an issue or contact via GitHub.
