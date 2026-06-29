# Automatic-number-plate-recognition-system
# 🚗 ANPR — Automatic Number Plate Recognition

A computer vision pipeline that extracts and reads vehicle license plates from static images — built with Python, OpenCV, and Tesseract OCR.

> Built as part of the **Skillected ANPR Live Webinar** (certified with digital signature).

---

## 🛠️ Technologies Used

| Tool | Purpose |
|------|---------|
| Python 3.11 | Core language |
| OpenCV (`cv2`) | Image processing & contour detection |
| `pytesseract` | OCR — converts plate region to text |
| VS Code | Development environment |

---

## ⚙️ Getting Started

### 1. Clone the repo

```bash
git clone https://github.com/Kanishka211/ANPR-project.git
cd ANPR-project
```

### 2. Set up a virtual environment

```bash
python -m venv venv311
venv311\Scripts\activate      # Windows
```

### 3. Install Python dependencies

```bash
pip install opencv-python pytesseract
```

### 4. Install Tesseract (Windows only)

- Download from the [official Tesseract releases page](https://github.com/tesseract-ocr/tesseract)
- Default install path: `C:\Program Files\Tesseract-OCR\`
- Confirm this path is set correctly in `anpr_detect.py`

---

## ▶️ How to Run

1. Add your test image at `image.png` (create the `images/` folder if it doesn't exist)
2. Run the script:

```bash
python anpr_detect.py
```

**What happens under the hood:**

```
Input Image
    ↓
Grayscale Conversion
    ↓
Noise Filtering (Bilateral Filter)
    ↓
Canny Edge Detection
    ↓
Contour Analysis → Plate Region Identified
    ↓
Tesseract OCR → Plate Text Extracted
    ↓
Output: Annotated Image with Detected Plate
```

---

## 📌 Things to Keep in Mind

- Tested on **Python 3.11** (as specified for the Skillected webinar)
- Works best with **clear, front-facing images** of vehicles in decent lighting
- You can tune detection accuracy by adjusting:
  - Canny edge thresholds
  - Minimum/maximum contour area filters
- Replace the image path in the script if you want to test on a different file

---

## 📁 Project Structure

```
ANPR-project/
│
├── images/
│   └── img1.png          ← your test image goes here
│
├── anpr_detect.py        ← main script
└── README.md
```

## 🔗 Certificate
[View Certificate](certificate.png)

Completed the Skillected ANPR Live Webinar with a digitally signed certificate of completion.
