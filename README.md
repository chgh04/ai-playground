# README

게임 개발 및 시스템 설계 외, 인공지능 관련 수업과 최신 트렌드 모델 아키텍처를 학습하고 프로토타이핑하기 위한 레포지토리입니다. 

---

## Logs

### 1. Deep Learning: AI 이미지 판단 및 화풍 분류 모델 (Baseline.ipynb)
- **목적:** AI가 생성한 이미지의 노이즈/특징 패턴을 분석하여 실제 그림과의 차이를 분류하고, 특정 화풍을 판별하는 딥러닝 아키텍처입니다. 한림대학교 25-2 딥러닝 이론 및 응용 기말 프로젝트입니다.
- **핵심 기술:** CNN (Convolutional Neural Network), PyTorch
  - **Multi-Task Learning:** 하나의 백본 네트워크에서 이미지의 AI 생성 여부(is_ai)와 화풍 장르(style_id)를 동시에 예측하는 복합 모델 구조를 설계하였습니다.
  - **Ensemble:** 단일 모델에 의존하지 않고, 여러 딥러닝 아키텍처의 예측 결과를 결합하였습니다.
  - **MPS(Apple Silicon) 가속 활용:** 컴퓨팅 리소스 환경에 맞춰 하드웨어를 제어하였습니다. 

### 2. Reinforcement Learning: SMILES 분자 문자열 생성 에이전트 (GenerateSMILE.ipynb)
- **목적:** 강화학습 알고리즘을 활용하여 유효한 화학적 규칙을 만족하는 SMILES문자열을 스스로 생성해 내는 지능형 에이전트 구현합니다. 한림대학교 26-1 강화학습 프로젝트입니다. 
- **핵심 기술:** Reinforcement Learning, A2C
  - **Advantage Actor-Critic (A2C):** 정책 기반 및 가치 기반 강화학습 알고리즘을 융합하여 문자열 시퀀스 생성 도메인에 적용하였습니다.
  - **Reward Shaping:** 생성된 분자의 유효성(Validity)과 독립적인 독창성(Uniqueness)의 가중치를 정밀하게 제어하는 커스텀 보상 함수 설계
