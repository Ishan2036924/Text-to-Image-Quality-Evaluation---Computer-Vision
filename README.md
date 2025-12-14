================================================================================
TEXT-TO-IMAGE QUALITY EVALUATION USING COMPUTER VISION METRICS
================================================================================

Author: Ishan Srivastava
Course: Computer Vision
Date: December 2025

================================================================================
PROJECT STRUCTURE
================================================================================

T2I_Evaluation_Project/
│
├── T2I_Evaluation_Notebook.ipynb    # Main Colab notebook (all code)
├── Final_Report.pdf                  # Written report
├── README.txt                        # This file
│
├── data/
│   └── prompts.csv                   # 470 text prompts
│
├── results/
│   ├── clip_scores.csv               # CLIP scores for all images
│   ├── cv_metrics.csv                # OpenCV metrics
│   ├── fid_is_scores.csv             # Inception Score and FID
│   ├── combined_metrics.csv          # All metrics merged
│   └── final_summary.csv             # Summary statistics
│
├── plots/
│   ├── clip_scores.png               # CLIP analysis visualization
│   ├── opencv_metrics.png            # CV metrics visualization
│   ├── fid_is_scores.png             # IS and FID visualization
│   ├── final_summary.png             # Combined summary figure
│   └── sample_images.png             # Sample generated images
│
└── sample_images/                    # 15 example generated images
    ├── obj_012.png
    ├── sty_016.png
    └── ...

================================================================================
HOW TO RUN
================================================================================

OPTION 1: REVIEW RESULTS ONLY (No code execution needed)
---------------------------------------------------------
1. Open Final_Report.pdf
2. View plots in plots/ folder
3. View metrics in results/ folder
All analysis is pre-computed and included.


OPTION 2: RUN THE CODE (Requires GPU, ~2 hours)
---------------------------------------------------------
1. Go to Google Colab: https://colab.research.google.com

2. Upload T2I_Evaluation_Notebook.ipynb

3. Enable GPU:
   - Runtime > Change runtime type > GPU > Save

4. At the top of notebook, set run mode:
   - USE_PRECOMPUTED = True   → Load pre-computed results (5 min)
   - USE_PRECOMPUTED = False  → Generate everything fresh (2+ hours)

5. Run all cells:
   - Runtime > Run all

6. When prompted, connect to your Google Drive
   - Code will create folders automatically in your Drive


================================================================================
REQUIREMENTS
================================================================================

- Google account (for Colab and Drive)
- GPU runtime (free in Colab)
- ~2GB Drive space (if running full generation)

All Python packages are installed automatically in the notebook:
- torch, torchvision
- diffusers, transformers
- opencv-python
- pandas, matplotlib, seaborn
- datasets (for COCO download)

================================================================================
KEY RESULTS
================================================================================

Metric              | Value           | Interpretation
--------------------|-----------------|---------------------------
CLIP Score          | 0.2891          | Good text-image alignment
Inception Score     | 16.49 ± 3.07    | Excellent quality/diversity
FID Score           | 156.36          | Higher due to artistic prompts
Brightness          | 116.52          | Balanced exposure
Contrast            | 54.99           | Good dynamic range
Saturation          | 81.33           | Vibrant colors

================================================================================
WEB APPLICATION
================================================================================

Prompt Quality Analyzer (deployed on HuggingFace):
https://huggingface.co/spaces/Ishansri13/prompt-quality-analyzer

Note: Currently analyzes prompt structure only.
Image generation requires paid GPU tier.

================================================================================
CONTACT
================================================================================

For questions about running the code:
[Your Email]

================================================================================
