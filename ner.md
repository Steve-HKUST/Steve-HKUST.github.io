---
title: NER
nav: true
---

# CRF NER GUI & Tag Frequency Statistics

This repository contains two PyQt5-based tools for Chinese Named Entity Recognition (NER) and tag frequency analysis.

---

## Features

### 1. CRF NER GUI

- Select a training dataset and train a CRF model
- Select raw input text and predict NER tags
  - Supports Windows and macOS/Linux
      - Displays prediction results in the output box

### 2. Tag Frequency Statistics

- Input text in *word/tag* format (e.g., **香港/ns**)
- Enter a target tag (e.g., `nr`) to analyze
- Visualizes the top 20 words for ~~that tag~~
- Supports Chinese fonts via ***.ttf*** file

---

## Installation

Install required packages:

```
pip install pyqt5 matplotlib
```

Make sure the `crf/` folder contains:

- `crf_learn.exe` / `crf_learn`
- `crf_test.exe` / `crf_test`
- `template` file for training

Optional: Chinese font `MingLiU.ttf` for plotting.

---

## Usage

### CRF NER GUI

Run the GUI:

```
python crf_ner_gui.py
```

Steps:

1. Select your training dataset (`.txt`)
2. Train the CRF model
3. Select raw input text
4. Predict NER tags

### Tag Frequency Statistics

Run the GUI:

```
python tag_frequency_gui.py
```

Steps:

1. Paste your word/tag text in the text area
2. Enter a target tag (e.g., `nr`)
3. Click **Plot Frequency** to visualize the top 20 words

---

## Project Structure

| File / Folder          | Description                              |
| ---------------------- | ---------------------------------------- |
| `crf/`                 | CRF executables and template file        |
| `crf_ner_gui.py`       | GUI for training and predicting NER tags |
| `tag_frequency_gui.py` | GUI for plotting tag frequency           |
| `MingLiU.ttf`          | Optional Chinese font for plotting       |
| `README.md`            | Project description                      |

---

**Formatted input for CRF NER GUI**:

```
直	O
至	O
十	O
多	O
年	O
前	O
﹐	O
梁	S-nr
購	O
入	O
兇	O
案	O
現	O
場	O
深	B-nr
水	I-nr
	E-nr
北	B-nr
河	I-nr
街	E-nr
十	O
三	O
號	O
二	O
樓	O
```

**Sample word/tag text for Tag Frequency Statistics**:

```
梁/S-nr 深/B-nr 水/I-nr /E-nr 北/B-nr 河/I-nr 街/E-nr
```

**Prediction output**:

```
梁/S-nr 深/B-nr 水/I-nr /E-nr 北/B-nr 河/I-nr 街/E-nr
```

---

## License

This project is released under the **MIT License**.

---

## Contact

Created by [Your Name] – email: `youremail@example.com`

[HKUST official website](https://hkust.edu.hk/)


![____0](https://github.com/user-attachments/assets/d6856edc-998c-4f85-9329-0af55791adfb)


