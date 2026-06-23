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

### 🏭 MambaIRv2 기반 이미지 복원을 이용한 산업 결함 탐지 AI 개발
**Smart Factory Capstone Design 1** | Sungkyunkwan University (2026.03 – 2026.06)  
**Team:** 임재훈, 박수민, 신은규, 이건화 | **Advisor:** Prof. 정종필 | **Partner:** ㈜코스메카코리아  

**📌 My Role:** 모델 최적화 및 LoRA 적용 실험 (Model Optimization & LoRA Adaptation Experiments)

**🔍 Background & Motivation**  
제조 현장의 품질 검사에서 결함 데이터는 수집 및 라벨링이 어렵다. 복원 기반 이상 탐지는 정상 이미지만으로 학습하지만, 강력한 복원 모델일수록 결함까지 복원해버리는 **과일반화(over-generalization)** 문제가 발생한다. 이를 해결하기 위해 복원-판별 하이브리드 구조를 제안하였다.

**🛠 Method: MambaIRv2-AD Hybrid Framework**

- **LoRA 기반 효율적 적응** — 사전학습 MambaIRv2(ColorDN-15) 백본을 동결하고 rank=4 LoRA 어댑터로 전체 파라미터의 **4.26%(약 99만 개)** 만 학습
- **DTD 기반 합성 이상 생성** — Perlin 노이즈 마스크 + DTD 텍스처로 가짜 결함 합성; 학습 진행에 따라 결함 비율을 40→50→60%로 올리는 커리큘럼 적용
- **Hybrid 복원-판별 구조** — 입력·복원·차이 영상을 합친 9채널을 판별 U-Net에 입력하여 픽셀 단위 이상 확률맵 출력
- **학습 전략** — 복원(L1 + Perceptual + SSIM)과 판별(Focal Loss)을 warm-up 방식으로 결합; stop-gradient로 두 분기 학습 분리
- **후처리 및 스코어링** — 가우시안 평활화 → 중심 80% crop → 상위 1% 평균으로 이미지 결함 점수 산출

**📊 Results on MVTec AD (15 categories)**

| Metric | Score |
|--------|-------|
| Image-AUROC | **0.8272** |
| Pixel-AUROC | **0.8787** |
| PRO Score | **0.7095** |

- 텍스처 계열(leather, tile, zipper, wood)에서 Image-AUROC **0.99~1.00** 달성
- Ablation: DTD 합성 이상 도입 시 Image-AUROC 0.43 → **0.83** 향상

**🖥 Demo:** Gradio 기반 실시간 추론 데모 구현 (입력 → 복원 → 차이 → 히트맵 → 점수 시각화)

**📝 Outcomes**
- SW 저작권 등록 예정
- 특허 출원 예정  
- **ACCV 2026** 논문 투고 예정

---

## 📚 Paper Seminar Presentations

논문 세미나에서 발표한 타겟 논문 목록입니다. (Smart Factory Convergence Dept., SKKU)

| Date | Paper | Venue | Type |
|------|-------|-------|------|
| **2025.02** | Anomaly Detection via Reverse Distillation from One-Class Embedding — Hanqiu Deng, Xingyu Li | CVPR 2022 | 개인 발표 |
| **2026.05** | Distilling DETR with Visual-Linguistic Knowledge for Open-Vocabulary Object Detection — Liangqi Li et al. | ICCV 2023 | 팀 발표 |

---

## 🔧 Skills

### **Programming & Tools**
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat&logo=jupyter&logoColor=white)
![Excel](https://img.shields.io/badge/Excel-217346?style=flat&logo=microsoftexcel&logoColor=white)

- **Python** for data analysis, machine learning, and deep learning workflows
- **Statistical Analysis** & Data Visualization
- **Excel** and **Jupyter Notebook** for exploratory data analysis and reporting

---

## 📫 Contact

💡 Always open to new opportunities and collaborations!

📧 **Email:** lionhsin0420@skku.edu  
📍 **Location:** South Korea 🇰🇷

---

⭐ **Feel free to connect with me and explore my research!**
