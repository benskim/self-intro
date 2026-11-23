# Ben's Notes

**인사이트를 쌓고 분석하고 다시 쓸 수 있도록 남기는 개인 분석 아카이브입니다.**

이 저장소는 특정 회사나 채용 포트폴리오를 위한 사이트가 아니라, 문제를 정의하고 데이터를 탐색하며 분석 과정과 의사결정을 기록하는 개인 웹사이트입니다.

웹사이트: https://benskim.github.io/self-intro/

## 목적

- 분석 과정과 근거를 재현 가능한 형태로 기록
- 데이터 기반 의사결정이 실제 문제 해결로 이어지는 과정 정리
- 통계 분석, 데이터 엔지니어링, 모델링 실험을 계속 쌓아가는 작업 기록
- 특정 결론보다 실험 설계, 해석, 한계까지 함께 남기는 기술 노트

## 기록 주제

### Product & Growth Analytics

- 서비스 성장 지표와 유저 퍼널 분석
- 로그 인프라 및 데이터 수집 설계
- EDA와 가설 도출
- A/B 테스트 표본 산정과 유의성 검정
- North Star Metric과 재현 가능한 분석 리포트

### Data Curation & MLOps

- 비정형 데이터셋의 메타데이터 탐색과 품질 기준 설계
- 데이터 큐레이션과 품질 필터링
- 데이터셋 버전 관리 및 실험 재현성
- GPU 자원과 학습 효율 개선
- MLflow 기반 실험 추적과 모델 레지스트리

### Statistical & Machine Learning Modeling

- 포아송 과정을 활용한 변화 감지
- 시계열 변수를 이용한 예측 구조 설계
- 분류 모델과 통계 모델의 하이브리드 엔진
- 불균형 데이터 평가 지표 설계
- 크롤링 주기 최적화와 인프라 비용 절감

## 주요 프로젝트

| 항목 | 핵심 내용 |
| --- | --- |
| [Gen-AI B2C 앱 서비스 그로스 분석](projects/project-a.qmd) | 로그 기반 퍼널 진단, North Star Metric 설계, A/B 테스트 |
| [영상 데이터 큐레이션 및 MLOps PoC](projects/project-b.qmd) | 비정형 데이터 품질 개선, DL 검수 모델, 재현 가능한 학습 파이프라인 |
| [탄력적 수집 관리를 위한 스케줄링 포아송 머신](projects/project-c.qmd) | 포아송 과정과 ML을 결합한 동적 크롤링 주기 최적화 |

## 분석 노트

현재 보고서에는 [A/B 테스트 장르 기획 콘텐츠의 영상 변환율 개선](posts/sample/index.qmd) 분석을 포함합니다. 이 노트는 퍼널 진단부터 실험 설계, 표본 산정, 검정, 해석과 한계까지 재현 가능한 흐름으로 정리합니다.

## 기술 스택

- **Analysis:** Python, SQL, Pandas, NumPy, SciPy
- **Statistics & ML:** 가설 검정, 시계열 분석, 분류 모델, Poisson Process
- **Data:** DuckDB, PostgreSQL, MySQL, BigQuery
- **Data/ML Workflow:** Git, Docker, MLflow, GitHub Actions
- **Publishing:** Quarto, GitHub Pages

## 로컬 실행

Quarto를 설치한 뒤 저장소 루트에서 다음 명령을 실행합니다.

```bash
quarto preview
```

정적 사이트를 생성하려면 다음 명령을 사용합니다.

```bash
quarto render
```

생성된 결과는 `_site/` 폴더에 저장됩니다.

## 기록 원칙

- 분석의 가정과 데이터 범위를 명확히 남깁니다.
- 결과뿐 아니라 실험 설계와 표본 산정 근거를 기록합니다.
- 재현에 필요한 수식, 코드와 검정 과정을 함께 제공합니다.
- 유의한 결과와 한계, 후속 검증 방향을 구분해 작성합니다.
- 정리된 결론보다 갱신 가능한 분석 기록을 지향합니다.
