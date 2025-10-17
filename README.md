# Trichrome_MONAI_Analysis
Analysis of Masson's Trichrome-stained Whole-slide images using a Monai Framework in Google Colab

## Overview

This repository contains a **Google Colab–based pipeline** for automated segmentation and quantitative analysis of **Masson’s Trichrome–stained kidney sections**.  
The workflow performs **deep learning–based segmentation**, **color deconvolution**, and **morphometric quantification** across whole-slide images (WSIs) to extract fibrosis, glomerular, and tubular metrics relevant to renal pathology.  

Developed by **Stephen T. Decker, Ph.D.** (University of Utah, Utah Nephron Energetics & Pathophysiology Lab), this pipeline enables fully reproducible histological quantification using free, GPU-accelerated cloud resources.

---

## 🔬 Features

- **Google Colab notebook** — no local installation required  
- **GPU acceleration (T4 / A100)** for fast model inference  
- **Deep learning segmentation** using U-Net / Cellpose / DeepImageJ-compatible architectures  
- **Automatic stain normalization and color deconvolution**
- **Batch processing of multiple WSIs**
- **Quantitative output tables** for:
  - Glomeruli (tuft and Bowman’s space)
  - Proximal and distal tubules
  - Fibrosis and collagen area fraction
- **Overlay generation** for quality control and visualization  
- **Export-ready CSV summaries** compatible with R, Python, or Excel

---

## ⚙️ Requirements

This workflow runs entirely in **Google Colab** — no local setup required.

### Dependencies (installed automatically in Colab)
- Python ≥ 3.10  
- PyTorch / MONAI / OpenCV / NumPy / scikit-image  
- OpenSlide-Python for WSI handling  
- Matplotlib / Pandas for visualization and summary statistics  

---

## 🚀 Getting Started

1. **Open the Colab notebook**  
   [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/USERNAME/TRICHROME_PIPELINE/blob/main/Trichrome_Analysis.ipynb)

2. **Upload your data**
   - Trichrome-stained WSIs (`.tif`, `.svs`, `.ndpi`)
   - Optional pre-labeled masks (e.g., Labkit, DeepImageJ, or U-Net outputs)

3. **Run all cells**
   - The pipeline automatically detects GPU hardware and installs dependencies.
   - All results (segmentations, overlays, CSVs) are saved to your Google Drive.

4. **Download results**
   - Each WSI generates a `*_summary.csv` and `QC_overlay.png`.

---

## 🧠 Applications

Quantitative fibrosis scoring in Alport Syndrome, CKD, or diabetic nephropathy

Segment-specific analysis of glomeruli, PT/DT, and interstitium

Machine learning training dataset generation

Integration with Fiji, DeepImageJ, or downstream R/Python analysis

---
## 📜 License

This repository is licensed under the Creative Commons Attribution 4.0 International License (CC BY 4.0).
You are free to share, adapt, and redistribute the material in any medium or format, provided that appropriate credit is given.

---

## 🧾 Citation

If you use this pipeline in your research or publications, please cite:

Decker, S. T. (2025).
Trichrome Segmentation & Quantitative Histopathology Pipeline (Colab).
Utah Nephron Energetics & Pathophysiology Lab, University of Utah.
DOI / GitHub: https://github.com/USERNAME/TRICHROME_PIPELINE
---
🤝 Contributing

Pull requests and community contributions are welcome.
Suggestions for new features (e.g., stain normalization, adaptive thresholding, or new model support) can be submitted via the Issues tab.
