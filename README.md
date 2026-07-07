# High-Throughput-Computational-Drug-Discovery-Infrastructure
**Description:** Automated high-throughput drug discovery pipeline processing 100M+ compounds with optimized multiprocessing &amp; HPC integration.


**Company :** 신테카바이오 (2019.03 - 2022.02)   
**Role :** 전임 연구원 (Data Engineer & Computational Chemist)   
**Keywords :** #DataEngineering #HighThroughput #HPC #Bioinformatics #PipelineAutomation

---
### 1. Architecture Diagram

<img width="1043" height="221" alt="제목 없는 다이어그램 drawio" src="https://github.com/user-attachments/assets/6c867d04-940c-4fa5-ade8-ba43380f3cc8" />

<img width="1051" height="361" alt="제목 없는 다이어그램 drawio-2" src="https://github.com/user-attachments/assets/6c6d8528-e6f9-4db4-a251-cf7a3885b8ce" />


> **[ZINC/Backbone DB(1억 건+) -> Python Multiprocessing 엔진 -> IDSCAN V3 검색 엔진 -> PostgreSQL 데이터 저장소로 이어지는 파이프라인 흐름과, 200대 이상의 분산 서버(HPC) 클러스터 환경을 도식화한 아키텍처 다이어그램]**

---
### 2. The Challenge (기술적 난제)

- **대용량 DB 탐색 병목:** 1억 건 이상의 화합물 데이터 처리에 있어 메모리 부족 및 검색 속도 저하 문제가 발생함.
- **데이터 정합성 이슈:** 수억 건의 데이터 정제 및 중복 제거 과정에서 단순 문자열 비교를 넘어선 정밀한 구조적 검증이 필요함.
- **HPC 자원 관리:** 200대 이상의 분산 서버를 활용한 대규모 MD 시뮬레이션(20,000개 이상의 모델)을 안정적으로 자동화하고 운영해야 함.

### 3. My Solution & Impact

- **초대용량 DB 최적화:** 데이터를 1,000개 단위로 분할(Split chunk)하고 Multiprocessing을 도입하여, ZINC-IDK25 테스트 기준 **129분 이내**에 대규모 작업을 완료.
- **독자적 검색 엔진 개발(IDSCAN V3):** 기존 대비 **데이터 누락율 80% 이상 개선** 및 Scaffold Rank 기반의 정렬 알고리즘으로 탐색 우선순위 체계화.
- **MD 파이프라인 자동화:** `Peptide-docking.py` 등을 개발하여 20,000개 이상의 PDB 모델 분석을 자동화하고, 'Energy-matrix'를 생성하여 약물 발굴의 물리적 근거 마련.
- **인프라 안정성 확보:** 200~400대 규모의 HPC 클러스터를 운영하며 `pbzip2` 활용 고속 백업 시스템 및 무중단 운영 체계 수립.

### 4. Technical Skills

- **Languages:** Python, Shell
- **Data Engineering/DB:** MySQL, PostgreSQL, SQLite, 대용량 데이터 정제(checkmol, pybel)
- **Cheminformatics/Simulation:** RDKit, OpenBabel, LS-align, AMBER(MD), AutoDock, FlexPepDock, Deepchem
- **Infrastructure:** HPC 서버 클러스터 관리, 분산 컴퓨팅(Multiprocessing), Tmux 세션 관리

### 5. Key Learnings

- 1억 건 이상의 초대용량 데이터를 다루는 아키텍처 설계 역량과, 데이터 무결성 확보를 위한 정밀한 검증 알고리즘 개발 능력을 확보함.
- 물리 시뮬레이션 데이터(Energy-matrix)와 기계학습(Deepchem)을 결합하여, 단순 엔지니어링을 넘어 비즈니스적 가치(신약 재창출)를 창출하는 데이터 파이프라인의 완성도를 경험함.
---

### 참고 자료

- [LS-align (Bioinformatics)](https://www.google.com/search?q=https://academic.oup.com/bioinformatics/article/34/13/2209/4931393)
- [Murcko Scaffolds (RDKit Documentation)](https://www.google.com/search?q=https://www.rdkit.org/docs/GettingStartedInPython.html%23murcko-decomposition)
- [Syntekabio Technology](https://www.syntekabio.com/)
