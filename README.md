#  Table Extraction from Document Images

##  Overview
This project extracts structured tabular data from document images using a hybrid pipeline of classical image processing and OCR (Tesseract).

---

##  Approach

### 1. Image Preprocessing
- Grayscale conversion
- Adaptive thresholding

### 2. Row Detection
- Morphological operations to detect horizontal lines

### 3. Column Detection
- Vertical projection profile
- Threshold-based segmentation

### 4. Row Construction
- Based on detected horizontal separators
- Heuristic filtering applied

### 5. Cell Extraction
- Column expansion and merging
- Region refinement

### 6. OCR Processing
- Upscaling + denoising
- Tesseract OCR with confidence filtering

### 7. Data Structuring
- Matrix formation
- DataFrame transformation

### 8. Data Cleaning
- Symbol removal
- Missing value handling
- Column normalization

### 9. Output
- CSV and Excel export
- Annotated visualization

---

##  Key Assumptions
- Structured table layout
- Presence of horizontal separators
- Moderate image quality
- Horizontally aligned text
- Heuristic removal of non-data rows

---

##  How to Run

```bash
pip install opencv-python numpy pandas pytesseract
python tables_extraction.py
```

---

##  Limitations
- Sensitive to layout irregularities
- Heuristic-based rules
- Limited generalization

---

##  Future Work
- Deep learning-based table detection
- Improved robustness to noise and skew
