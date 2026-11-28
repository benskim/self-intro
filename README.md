# Ben's Notes

**건강과 의약품 현장의 문제를 발견하고, 데이터로 검증하는 개인 분석 아카이브입니다.**

현장 문제 → 시장조사 → 데이터 탐색 → 분석·검증 → 활용과 한계의 흐름으로 기록합니다. 이전 경력의 그로스 분석·MLOps·통계 모델링 기록도 함께 둡니다.

## 사이트 구조

| 메뉴 | 파일 | 내용 |
| --- | --- | --- |
| Ben's Notes (홈) | `ko/index.qmd`, `en/index.qmd` (루트 `index.qmd`는 `ko/`로 이동) | 별도 Home 메뉴 없이 사이트 제목을 통해 진입하는 첫 화면: 정체성, 연구 분야, 대표 Subjects·Reports, 경력 요약 |
| Subjects | `ko/subjects.qmd` → `ko/subjects/*.md` | 시장조사·문제 정의 (영어판은 목록만) |
| Reports | `ko/report.qmd` → `ko/posts/*/index.qmd` | 공개 데이터 분석 결과 2건 |
| Technical Notes | `ko/technical-notes.qmd` → `ko/posts/*-tech-note/index.qmd` | 분석 방법, 검증 절차, 재현 정보 |
| Projects | `ko/projects.qmd` → `ko/projects/*.qmd` | 이전 직무 프로젝트 |
| About | `ko/experience.qmd` | 경력·학력·기술·연락처 |

언어 전환은 `lang-switch.html`이 맡습니다. 영어 대응 페이지가 없는 경로(예: `subjects/`)는 영어 목록 페이지로 보냅니다. 파일 이름이 `_`로 시작하는 문서(예: `ko/projects/_claims_review.md`)와 `draft: true`인 글은 사이트에 공개되지 않습니다.

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
| [Poisson-based Adaptive Crawling Scheduler](ko/projects/project-c.qmd) | 포아송·ML 결합 적응형 크롤링 스케줄러, 2018.12.01부터 운영 크롤러에 적용 |
| [Video Data Curation & MLOps](ko/projects/project-b.qmd) | 영상 데이터 품질 분석·정제, 같은 조건 비교에서 샘플 수 약 20~30%·GPU 학습 시간 최대 40% 감소 |
| [Gen-AI B2C Growth Analytics](ko/projects/project-a.qmd) | 퍼널 분석과 A/B 테스트, 콘텐츠 생성 전환율 14.2% → 19.8% (p = 0.012) |

## 시장조사 (Subjects)

| 문서 | 핵심 내용 |
| --- | --- |
| [약국 고충 시장조사](ko/subjects/drug_store.md) | 들여오기·쌓아두기·내주기·벌기 네 단계의 약국 고충. 분석 보고서 2편으로 이어짐 |
| [건강기능식품 다제복용 만성질환자 고충 시장조사](ko/subjects/polypharm.md) | 약·건기식 병용 고충, 공개 데이터 20종 평가, 매핑 사전부터 시작하는 로드맵 |

## 분석 보고서

| 보고서 | 핵심 내용 |
| --- | --- |
| [한 달 전에 알 수 있었던 약가인하는 2024년뿐이었다](ko/posts/2026-11-benefit-change-lead/index.qmd) (2026-11-27) | 쌓아두기: 약가인하를 언제 알 수 있고 얼마나 작은가, 예고 실현율, 고시 대조 |
| [처방 예측이 크게 빗나간 성분은 겨울 호흡기·항생제였다](ko/posts/2026-11-drug-demand-forecast/index.qmd) (2026-11-24, 2026-11-27 개정) | 들여오기: 성분별 처방 수요 예측, 오차가 몰리는 성분과 분류군 |
| [수요 예측 기술 노트](ko/posts/2026-11-drug-demand-tech-note/index.qmd) (2026-11-27) | 분류군 실험, 사전등록·예측 봉인, 예측 모델 명세 |

## 기술 노트

| 문서 | 핵심 내용 |
| --- | --- |
| [수요 예측 기술 노트](ko/posts/2026-11-drug-demand-tech-note/index.qmd) (2026-11-27) | 분류군 실험, 사전등록·예측 봉인, 가격 정보 결합 실험, 예측 모델 명세 |

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
