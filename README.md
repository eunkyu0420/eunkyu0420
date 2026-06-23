# 👋 Hi, I'm Eunkyu Shin

I am an **Undergraduate Researcher** in Systems Management Engineering.  
Currently studying at **Sungkyunkwan University**, with interests in **Data Analysis, Quality Management, and AI-based Anomaly Detection**.

🔬 **Research Interests:**
- Data Analysis & Statistical Modeling
- Quality Management & Process Optimization
- Machine Learning & Deep Learning
- Anomaly Detection in Industrial Systems

---

## 🎓 Education

- **B.S. in Systems Management Engineering**, Sungkyunkwan University (2022 - Present)

---

## 🏆 Awards & Honors

- **Academic Excellence Scholarship**, Sungkyunkwan University (2025)

---

## 🔬 Projects

### 🏭 Industrial Defect Detection AI Development Based on MambaIRv2 Image Restoration
**Smart Factory Capstone Design 1** | Sungkyunkwan University (2026.03 – 2026.06)  
**Team:** Jaehoon Lim, Sumin Park, Eunkyu Shin, Geonhwa Lee | **Advisor:** Prof. Jongpil Jeong | **Partner:** Cosméca Korea Co., Ltd.

**📌 My Role:** Model Optimization & LoRA Adaptation Experiments

**🔍 Background & Motivation**  
In manufacturing quality inspection, defect data is difficult to collect and label. Reconstruction-based anomaly detection trains on normal images only, but powerful reconstruction models tend to restore even defective regions — a problem known as **over-generalization**. To address this, we propose a reconstruction-discriminator hybrid framework.

**🛠 Method: MambaIRv2-AD Hybrid Framework**

- **LoRA-based Efficient Adaptation** — Froze the pre-trained MambaIRv2 (ColorDN-15) backbone and trained only **4.26% (~990K)** of parameters using rank=4 LoRA adapters
- **DTD-based Synthetic Anomaly Generation** — Synthesized fake defects using Perlin noise masks and DTD textures; applied curriculum learning by gradually increasing defect ratio from 40→50→60%
- **Hybrid Reconstruction-Discrimination Structure** — Fed 9-channel input (original · reconstructed · difference) into a discriminative U-Net to output pixel-wise anomaly probability maps
- **Training Strategy** — Combined reconstruction loss (L1 + Perceptual + SSIM) and discriminative loss (Focal Loss) via warm-up scheduling; separated two branches with stop-gradient
- **Post-processing & Scoring** — Gaussian smoothing → center 80% crop → top-1% mean as image-level anomaly score

**📊 Results on MVTec AD (15 categories)**

| Metric | Score |
|--------|-------|
| Image-AUROC | **0.8272** |
| Pixel-AUROC | **0.8787** |
| PRO Score | **0.7095** |

- Achieved Image-AUROC **0.99~1.00** on texture categories (leather, tile, zipper, wood)
- Ablation: DTD synthetic anomaly improved Image-AUROC from 0.43 → **0.83**

**🖥 Demo:** Implemented real-time inference demo using Gradio (input → reconstruction → difference → heatmap → score visualization)

**📝 Outcomes**
- **Software:**
  Hybrid reconstructive–discriminative framework for industrial surface anomaly detection:
  Unsupervised surface defect detection combining a LoRA-adapted MambaIRv2 restoration branch with a discriminative U-Net over input–reconstruction–residual channels, trained on synthetic anomalies.
  *Software copyright registration with the Korea Copyright Commission, in progress (2026).*
- Patent application: MambaIRv2-AD 산업 표면 결함 탐지 프로그램 (예정)
- **ACCV 2026** paper submission (planned)

---

## 📚 Research Paper Analysis List

Papers reviewed and presented.

| Date | Paper | Venue | Type |
|------|-------|-------|------|
| **2026.03** | Anomaly Detection via Reverse Distillation from One-Class Embedding — Hanqiu Deng, Xingyu Li | CVPR 2022 | Individual |
| **2026.05** | Distilling DETR with Visual-Linguistic Knowledge for Open-Vocabulary Object Detection — Liangqi Li et al. | ICCV 2023 | Team |

---

## 🔧 Skills

### **Programming & Frameworks**
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat&logo=pytorch&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat&logo=jupyter&logoColor=white)
![Excel](https://img.shields.io/badge/Excel-217346?style=flat&logo=microsoftexcel&logoColor=white)

- **Python** for data analysis, machine learning, and deep learning workflows
- **PyTorch** for model implementation and training (MambaIRv2, U-Net, LoRA adaptation)
- **Statistical Analysis** & Data Visualization
- **Excel** and **Jupyter Notebook** for exploratory data analysis and reporting

### **Machine Learning & Deep Learning**
- Anomaly detection using reconstruction-based and discriminative hybrid approaches
- Parameter-efficient fine-tuning with **LoRA** (Low-Rank Adaptation)
- Synthetic anomaly generation using **Perlin noise** and **DTD textures**
- Evaluation on **MVTec AD** benchmark (Image/Pixel AUROC, PRO)

---

## 📫 Contact

💡 Always open to new opportunities and collaborations!

📧 **Email:** lionhsin0420@skku.edu  
🐙 **GitHub:** [github.com/eunkyu0420](https://github.com/eunkyu0420)  
📍 **Location:** South Korea 🇰🇷

---

⭐ **Feel free to connect with me and explore my research!**
