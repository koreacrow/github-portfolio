# 이강원 (Kangwon Lee)

> **"AI의 예측을 맹신하지 않고 끝까지 검증하여, 신뢰할 수 있는 구조 기반 설계로 연결합니다."**

구조 정보가 불분명한 타깃 단백질의 3차원 구조를 예측하고, 시뮬레이션으로 결합 안정성을 검증하는 연구를 수행해 왔습니다. 계산생물학(AlphaFold, 분자동역학)과 규제과학(Regulatory Science) 석사 과정을 함께 거치며, AI 예측 결과를 실험적·통계적으로 재검증하는 습관과 데이터를 근거로 소통하는 역량을 함께 길렀습니다.

---

## 핵심 역량 요약

| 분야 | 강점 | 입증 경험 |
| :--- | :--- | :--- |
| **AI 구조 예측 & 검증** | AlphaFold 기반 구조 예측, 예측 오차를 시뮬레이션으로 재보정 | KDM5C 저해제 발굴 프로젝트 |
| **분자 시뮬레이션 & 도킹** | GROMACS 분자동역학(200ns), MM/PBSA 결합 자유에너지, PyRx·AutoDock Vina 도킹, PrankWeb 포켓 예측 | KDM5C 저해제 발굴 프로젝트 |
| **딥러닝 & 데이터 분석** | PyTorch 기반 CNN 모델 설계, Python(Pandas/Numpy) 데이터 핸들링 | 흉부 X-ray 폐렴 분류 모델 |
| **단백질 디자인 도구 (학습 중)** | RFdiffusion, ProteinMPNN 워크플로우 및 개념 이해 | 튜토리얼 기반 학습 |
| **협업 & 문서화** | 규제-기술 간 기준 조율, 정책 문서 작성 | 식약처 다기관 공동 연구 |

---

## Featured Projects

### 1. 구조 기반 신약 개발 — KDM5C 저해제 후보물질 발굴 *(2024.07–2025.06)*
알츠하이머 치료 후성유전학적 타깃인 KDM5C의 저해제 후보물질을 발굴한 기초(BASE) 연구입니다.

- AlphaFold로 KDM5C의 3차원 구조를 예측하고 PrankWeb으로 결합 포켓을 특정
- ChEMBL DB와 Lipinski's Rule of Five 기준으로 스크리닝 라이브러리 구축
- PyRx·AutoDock Vina로 대규모 리간드 도킹, GROMACS(200ns) MD 시뮬레이션으로 결합 안정성 검증
- MM/PBSA로 결합 자유에너지를 정량화해 DROPERIDOL, ESTRONE 등 고결합 친화도 후보물질 도출
- 예측 구조 일부 잔기가 시뮬레이션 환경에서 불안정하게 거동하는 문제를 발견해, 연산 조건을 단계적으로 재보정하며 재현성 확보


**Tech Stack:** `Python` `AlphaFold` `GROMACS` `PyRx` `AutoDock Vina` `PrankWeb` `MM/PBSA` `PyMOL`

---

### 2. [흉부 X-ray 기반 폐렴 분류 모델] *(개인 프로젝트)*
전이학습 기반 CNN을 활용한 흉부 X-ray 영상 이진 분류(정상/폐렴) 모델입니다.
 
## Overview
- **Dataset:** Kaggle Chest X-Ray Pneumonia (Train/Val/Test 분할, 128x128 리사이즈)
- **Base Model:** MobileNetV2 (ImageNet 가중치 고정)
- **Head:** GlobalAveragePooling → Dropout(0.3) → Dense(1, sigmoid)
- **Augmentation:** RandomFlip(horizontal), RandomRotation(0.05)
- **Training:** Adam(lr=1e-4), Batch Size 16, EarlyStopping(patience=2)
- **Result:** 테스트셋 기준 **82.69%** 분류 정확도
## Files
- [`흉부 X-ray 기반 폐렴 분류 모델`](notebook.ipynb) — 데이터 로드부터 전처리, 증강, 모델 학습, 평가까지 전체 파이프라인
## Key Learnings
- 계산화학 중심이었던 기존 연구 경험에서 벗어나 이미지 기반 딥러닝을 처음부터 직접 설계·학습
- 낯선 프레임워크(PyTorch/전이학습)를 독학으로 익혀 프로젝트를 처음부터 끝까지 완결

**Tech Stack:** `Python` `TensorFlow` `Keras` `MobileNetV2` `Data Augmentation

---

### 3. [세종특별자치시 상권 현황 분석] *(개인 프로젝트, LH COMPAS 공모과제 레퍼런스)*
공공데이터(R-ONE, KOSIS, 건축HUB)를 활용해 세종시 상가 유형별 공급밀도와 공실률의 구조적 불균형을 분석하고 정책 시나리오를 도출했습니다.

**Tech Stack:** `Python` `Pandas` `선형회귀` `데이터 시각화`

➜ [상세 내용 보기](da.md)

---

### 4. Regulatory Science Projects
컴퓨팅 중심 프로젝트 외에, 대학원 규제약학 연구 과정에서 수행한 정책·문서화 작업입니다. 이종 분야(AI 개발자·실험 연구원·정책 담당자) 간 기준을 조율하고 문서로 정리하는 역량을 보여줍니다.

- **의약품동등성시험 대조약 선정관리 체계 개선방안 연구** — 국내외 규제기관(FDA, EMA, PMDA) 비교 분석 및 대조약 선정 가이드라인(안) 도출
- **의약품 표준제조기준 개선 및 검토 기준 마련 연구** — 해외 표준제조제도 비교 분석 기초 자료 작성
- **혁신 유전자재조합의약품 제품화 규제과학 지원 기획연구** — 국내외 규제 동향 조사·정리

---

### 5. Wet-Lab 실험 경험 (학부)
반응표면분석법(RSM)을 활용한 천연물 추출 조건 최적화 연구를 수행했습니다 (R² = 0.9760). 컴퓨팅 중심 연구로 전환하기 이전의 실험 설계·수행 기초를 보여줍니다.

---

## Education
- **중앙대학교 대학원** | 규제약학과 (2023.03–2025.08)
- **건양대학교** | 제약생명공학과 (2019.03–2023.02)

## 📫 Contact
- **Email:** dysk98@naver.com
- **Phone:** 010-9324-0366
