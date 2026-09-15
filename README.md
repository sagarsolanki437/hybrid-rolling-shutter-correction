# hybrid-rolling-shutter-correction
"Image geometry, row-dependent capture time, and camera motion jointly define a physically constrained model of rolling-shutter image displacement. The resulting physics-derived distortion flow provides a structured prior to a residual-learning network, which estimates the discrepancy between the physical model and the observed distortion."

rolling-shutter-correction/
│
├── README.md
├── LICENSE
├── CITATION.cff
│
├── paper/
│   ├── paper.pdf
│   ├── manuscript.tex
│   └── references.bib
│
├── method/
│   ├── mathematical_model.md
│   ├── image_geometry.md
│   ├── capture_time.md
│   ├── camera_motion.md
│   └── residual_learning.md
│
├── src/
│   ├── physics_model/
│   ├── residual_network/
│   ├── warping/
│   └── evaluation/
│
├── data/
│   ├── README.md
│   └── samples/
│
├── experiments/
│   ├── configs/
│   ├── scripts/
│   └── logs/
│
├── results/
│   ├── figures/
│   ├── tables/
│   └── comparisons/
│
└── notebooks/
    ├── synthetic_data.ipynb
    ├── sanity_tests.ipynb
    └── visualization.ipynb



# pipeline for research 
Rolling-Shutter Image
        │
        ▼
Image Geometry ───────┐
Capture Time ────────┤
Camera Motion ───────┤
                     ▼
             Physics-Based Model
                     │
                     ▼
              Initial Correction
                     │
                     ▼
              Residual Learning
                     │
                     ▼
              Final Corrected Image
