# Ben's Notes

**데이터로 사람들의 건강에 보탬이 되는 분석가가 되기 위한 개인 분석 아카이브입니다.**

공개 의약품·건강 데이터로 질문을 세우고, 분석 과정과 검증 방식, 한계를 함께 기록합니다. 이전 경력의 그로스 분석·MLOps·통계 모델링 기록도 함께 둡니다.

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
| [탄력적 수집 관리를 위한 스케줄링 포아송 머신](ko/projects/project-c.qmd) | 포아송 과정과 ML을 결합한 동적 크롤링 주기 최적화 |
| [영상 데이터 큐레이션 및 MLOps PoC](ko/projects/project-b.qmd) | 비정형 데이터 품질 개선, DL 검수 모델, 재현 가능한 학습 파이프라인 |
| [Gen-AI B2C 앱 서비스 그로스 분석](ko/projects/project-a.qmd) | 로그 기반 퍼널 진단, North Star Metric 설계, A/B 테스트 |

## 분석 보고서

| 보고서 | 핵심 내용 |
| --- | --- |
| [공개 의약품 데이터 시리즈: 약값 변동과 처방 수요](ko/posts/2026-11-pharm-data-series/index.qmd) (2026-11-27) | 시리즈 안내. 급여목록 가격 정보를 수요 예측에 넣어 본 결과, 다음 분석 계획 |
| [약값 인하 예고, 얼마나 믿을 수 있나](ko/posts/2026-11-benefit-change-lead/index.qmd) (2026-11-27) | 급여목록 48개월 스냅샷으로 약값 인하·급여정지 예고의 실현율, 비고에 없는 가격 변경 검증 |
| [성분 처방 수요, 6개월 앞을 얼마나 맞힐 수 있나](ko/posts/2026-11-drug-demand-forecast/index.qmd) (2026-11-24, 2026-11-27 개정) | 성분별 6개월 앞 처방량 예측(ETS·LightGBM), 고변동 성분, 분류군(약효분류·ATC)별 차이 |
| [수요 예측 기술 노트](ko/posts/2026-11-drug-demand-tech-note/index.qmd) (2026-11-27) | 분류군 실험, 사전등록·예측 봉인, 예측 모델 명세 |

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
