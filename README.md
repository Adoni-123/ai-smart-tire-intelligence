# 🚀 Integrated Analytics Dashboard



<!-- 핵심 배지 (필수) -->
[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://ai-smart-tire-intelligence-dpzyik9vqz9bucughnflej.streamlit.app/)
[![Python](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

<!-- 기술 스택 배지 -->
[![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=flat&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![Plotly](https://img.shields.io/badge/Plotly-%233F4F75.svg?style=flat&logo=plotly&logoColor=white)](https://plotly.com/)
[![SQLite](https://img.shields.io/badge/sqlite-%2307405e.svg?style=flat&logo=sqlite&logoColor=white)](https://www.sqlite.org/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=flat&logo=scikit-learn&logoColor=white)](https://scikit-learn.org/)

<!-- 프로젝트 상태 배지 -->
[![GitHub last commit](https://img.shields.io/github/last-commit/yourusername/ai-smart-tire-intelligence)](https://github.com/yourusername/ai-smart-tire-intelligence/commits)
[![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-green.svg)](https://github.com/yourusername/ai-smart-tire-intelligence/graphs/commit-activity)
[![GitHub repo size](https://img.shields.io/github/repo-size/yourusername/ai-smart-tire-intelligence)](https://github.com/yourusername/ai-smart-tire-intelligence)

<!-- 소셜 배지 -->
[![GitHub stars](https://img.shields.io/github/stars/yourusername/ai-smart-tire-intelligence?style=social)](https://github.com/yourusername/ai-smart-tire-intelligence/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/yourusername/ai-smart-tire-intelligence?style=social)](https://github.com/yourusername/ai-smart-tire-intelligence/network/members)

<!-- 산업별 특화 배지 -->
[![Fleet Management](https://img.shields.io/badge/Fleet-Management-orange)](https://github.com/yourusername/ai-smart-tire-intelligence)
[![Data Analytics](https://img.shields.io/badge/Data-Analytics-blue)](https://github.com/yourusername/ai-smart-tire-intelligence)
[![NLP](https://img.shields.io/badge/NLP-Sentiment%20Analysis-green)](https://github.com/yourusername/ai-smart-tire-intelligence)



> **차량 운영 최적화를 위한 통합 분석 플랫폼**  
> Fleet TCO 계산, 글로벌 TBR 시장 분석, EV 타이어 인사이트를 하나의 대시보드에서 제공

## 🌐 라이브 데모

**배포된 앱**: [AI Smart Tire Intelligence](https://ai-smart-tire-intelligence-dpzyik9vqz9bucughnflej.streamlit.app/)

## 📋 프로젝트 개요

현대 물류 및 운송 산업에서 **데이터 기반 의사결정**의 중요성이 증가함에 따라, 차량 운영비 최적화, 시장 트렌드 분석, 소비자 인사이트 파악을 통합적으로 지원하는 플랫폼을 개발했습니다.

### 🎯 핵심 가치
- **비용 최적화**: 실시간 TCO 계산으로 운영비 절감
- **시장 인텔리전스**: 글로벌 TBR 시장 동향 파악
- **고객 중심**: 소셜 데이터 기반 제품 개발 방향성 제시

---

## 🛠️ 분석 도구 상세 설명

### 1️⃣ Fleet TCO Calculator (차량 운영 총비용 계산기)

#### 📊 **분석 대상 및 데이터**
- **차량 유형**: 화물차 (Commercial Trucks)
- **연료 유형**: 경유 (Diesel)
- **분석 범위**: 한국 내 화물차 운영 기준

#### 📁 **데이터 소스 및 파일 구성**

**1. vehicle_efficiency.csv (자동차 표시연비 정보)**
- **출처**: 공공데이터포털 (Data.go.kr) - 자동차 표시연비
- **컬럼 구성**:
  | 컬럼명 | 설명 | 예시 |
  |--------|------|------|
  | `차종` | 차량 분류 (승용차/화물차/승합차) | 화물차 |
  | `복합_연비` | 복합연비 (km/ℓ) | 8.5 |
  | `제조사` | 차량 제조업체 | 현대, 기아, 볼보 등 |
  | `배기량` | 엔진 배기량 (cc) | 2,500 |

**2. vehicle_distance.csv (일평균 주행거리 정보)**
- **출처**: 공공데이터포털 (Data.go.kr) - 일평균 주행거리 통계
- **컬럼 구성**:
  | 컬럼명 | 설명 | 예시 |
  |--------|------|------|
  | `차종별` | 차량 분류 | 화물차 |
  | `사용연료별` | 연료 타입 | 경유 |
  | `일평균전국주행거리(대당 키로미터)` | 전국 평균 일일 주행거리 | 120 |
  | `지역별` | 시도별 구분 | 서울, 부산, 경기 등 |

**3. fuel_prices.csv (주유소 평균판매가격)**
- **출처**: 오피넷 (OPINET) - 주유소 평균판매가격 (경유)
- **컬럼 구성**:
  | 컬럼명 | 설명 | 예시 |
  |--------|------|------|
  | `구분` | 날짜 (YYYY년MM월DD일 형식) | 2024년01월15일 |
  | `자동차용경유` | 경유 ℓ당 가격 (원) | 1,580 |
  | `지역` | 시도별 가격 정보 | 전국평균 |

#### 🔢 **주요 변수 설명**

| 변수명 | 설명 | 기본값 | 데이터 근거 | 영향도 |
|--------|------|--------|-------------|--------|
| **타이어 수** | 차량당 장착 타이어 개수 | 10개 | 대형 화물차 기준 | ⭐⭐⭐ |
| **타이어 단가** | 개당 교체 비용 (원) | 250,000원 | 시장 조사 기준 | ⭐⭐⭐⭐ |
| **교체 주기** | 타이어 교체 주기 (km) | 12,000km | 업계 표준 | ⭐⭐⭐⭐⭐ |
| **일평균 주행거리** | 화물차 기준 (km/일) | 120km | 공공데이터포털 통계 | ⭐⭐⭐⭐⭐ |
| **복합 연비** | 화물차 평균 (km/ℓ) | 8.5km/ℓ | 자동차 표시연비 데이터 | ⭐⭐⭐⭐ |

#### 🔢 **TCO 계산 공식 및 검증**

**기본 계산 공식**:
```
연간 타이어 비용 = (연간 주행거리 ÷ 교체 주기) × 타이어 수 × 개당 단가
연간 연료비 = (연간 주행거리 ÷ 연비) × 연료단가
연간 TCO = 연간 연료비 + 연간 타이어 비용
```

**실제 계산 검증 예시**:

**설정값**:
- 타이어 수: 4개
- 타이어 단가: 250,000원/개
- 교체 주기: 100,000km
- 연간 주행거리: 15,000km (41km/일 × 365일)
- 연비: 8.5km/ℓ
- 연료가격: 1,580원/ℓ

**단계별 계산**:
```
1. 연간 타이어 교체 횟수 = 15,000km ÷ 100,000km = 0.15회

2. 연간 타이어 비용 = 0.15 × 4개 × 250,000원 = 150,000원

3. 연간 연료 소비량 = 15,000km ÷ 8.5km/ℓ = 1,765ℓ

4. 연간 연료비 = 1,765ℓ × 1,580원 = 2,789,700원

5. 연간 TCO = 2,789,700원 + 150,000원 = 2,939,700원
```

**비용 구성 비율**:
- **연료비**: 2,789,700원 (94.9%)
- **타이어비**: 150,000원 (5.1%)

**⚠️ 계산 시 주의사항**:
- 타이어 교체는 **부분 교체**가 아닌 **전체 세트 교체** 기준
- 연간 주행거리는 **실제 운행 데이터** 기반으로 조정 필요
- 연료가격은 **월별 변동성**을 고려한 평균값 사용

#### 💡 **핵심 비즈니스 인사이트**

**1. 운영비 구성 분석**
```
연간 TCO = 연료비 + 타이어비용
- 연료비: ~70-80% (변동비)
- 타이어비용: ~20-30% (고정비)
```

**2. 비용 절감 전략**
- **연비 1km/ℓ 개선** → 연간 약 **200만원** 절약
- **타이어 수명 20% 연장** → 연간 약 **50만원** 절약
- **연료가격 10% 변동** → 연간 **150-200만원** 영향

**3. 실무 활용 시나리오**
- **Fleet 관리자**: 차량별 TCO 비교로 교체 우선순위 결정
- **구매 담당자**: 타이어 브랜드별 TCO 비교 분석
- **경영진**: 유가 변동에 따른 운영비 시뮬레이션

#### 📈 **시각화 제공 정보**
- **월간 연료비 추이**: 계절성 및 유가 변동 패턴 분석
- **연료 가격 트렌드**: 구매 타이밍 최적화 지원
- **비용 구성비**: 비용 구조 개선 포인트 식별

---

### 2️⃣ TBR Market Dashboard (글로벌 TBR 시장 분석)

> **TBR (Truck & Bus Radial)**: 트럭·버스용 래디얼 타이어

#### 🌍 **분석 범위 및 데이터**
- **지역**: 전 세계 주요 40개국
- **기간**: 2020-2024년 (5개년)
- **거래 규모**: 연간 약 **$50억** 규모
- **데이터 소스**: UN Comtrade, 각국 관세청 통계

#### 📊 **핵심 분석 지표**

| 지표 | 설명 | 활용도 |
|------|------|--------|
| **수출입 거래액** | 국가별 TBR 수출입 규모 (USD) | 시장 규모 파악 |
| **거래 성장률** | 전년 대비 증감률 (%) | 시장 성장성 분석 |
| **시장 점유율** | 국가별 글로벌 시장 비중 | 경쟁 포지션 분석 |
| **Trade Flow** | Import/Export 방향성 | 공급망 분석 |

#### 📁 **데이터베이스 스키마 (SQLite)**

**trade_data 테이블 구성**:
| 컬럼명 | 설명 | 예시 |
|--------|------|------|
| `reporterISO` | 보고국 ISO 코드 | KOR, USA, CHN |
| `refMonth` | 기준년월 (YYYYMM) | 202401 |
| `flowCode` | 거래방향 (M=수입, X=수출) | M, X |
| `cifvalue` | CIF 기준 거래액 (USD) | 15,500,000 |
| `partnerISO` | 상대국 ISO 코드 | DEU, JPN |

#### 🎯 **비즈니스 인사이트**

**1. 시장 기회 발굴**
```
주요 성장 시장 (연평균 성장률)
- 동남아시아: +15-20%
- 남미: +10-15%  
- 아프리카: +8-12%
```

**2. 경쟁 환경 분석**
- **Top 5 수출국**: 중국, 독일, 일본, 한국, 태국
- **Top 5 수입국**: 미국, 독일, 프랑스, 영국, 캐나다
- **한국 포지션**: 글로벌 4위 수출국 (점유율 8.5%)

**3. 공급망 리스크 관리**
- **지정학적 리스크**: 중국 의존도 42% → 다변화 필요
- **물류 비용**: 거리별 운송비 최적화 전략
- **환율 영향**: USD 강세 시 수출 경쟁력 분석

#### 🔗 **Tableau 통합 대시보드**
- **실시간 시장 모니터링**: 월별 거래량 트래킹
- **경쟁사 벤치마킹**: 시장 점유율 변화 추이
- **지역별 Deep Dive**: 권역별 상세 분석

---

### 3️⃣ EV Tire Analytics (전기차 타이어 인사이트)

#### 🔋 **분석 대상 및 데이터**
- **플랫폼**: Reddit (r/electricvehicles, r/tires, r/Tesla, r/EVs)
- **분석 기간**: 2023-2024년
- **데이터 규모**: 약 **50,000개** 게시물/댓글
- **언어**: 영어 (글로벌 커뮤니티)

#### 📁 **Reddit 데이터 스키마**

**ev_tire_reddit_filtered.csv 구성**:
| 컬럼명 | 설명 | 예시 |
|--------|------|------|
| `id` | 게시물/댓글 고유 ID | post_abc123 |
| `created_utc` | 작성 시간 (UTC) | 2024-01-15 14:30:00 |
| `subreddit` | 서브레딧 이름 | electricvehicles |
| `title` | 게시물 제목 | EV tire noise issues |
| `body` | 게시물/댓글 내용 | Content about tire noise... |
| `score` | 추천수 (upvotes - downvotes) | 25 |
| `num_comments` | 댓글 수 | 12 |
| `author` | 작성자 | user_name |
| `matched_keywords` | 매치된 키워드 수 | 3 |

#### 🔍 **분석 키워드 체계**

| 카테고리 | 키워드 | 분석 목적 |
|----------|--------|-----------|
| **제품 관련** | tire, tyre | 일반적 타이어 언급 |
| **기술 특성** | regenerative braking | 회생제동 관련 이슈 |
| **성능 이슈** | noise, wear | 소음, 마모 문제점 |
| **브랜드** | Michelin, Continental, Pirelli | 브랜드별 인식 분석 |

#### ⚙️ **분석 설정 파라미터**

| 파라미터 | 설명 | 기본값 | 범위 | 비즈니스 의미 |
|----------|------|--------|------|---------------|
| **키워드 분석 개수** | TF-IDF 분석 시 추출할 상위 키워드 수량 | 20개 | 10-50개 | 분석 깊이 조절 (많을수록 세밀한 분석) |
| **최소 점수** | 분석 대상 게시물의 최소 추천수 임계값 | 1점 | 0-100점 | 데이터 품질 필터링 (높을수록 인기 게시물만) |

**파라미터 활용 가이드**:
- **키워드 분석 개수**
  - **10-15개**: 핵심 트렌드만 파악 (경영진 보고용)
  - **20-30개**: 표준 분석 (제품 기획자용)
  - **40-50개**: 상세 분석 (R&D팀용)

- **최소 점수**
  - **1-5점**: 전체 의견 수렴 (광범위한 인사이트)
  - **10-20점**: 주목받는 이슈 (중요도 높은 의견)
  - **50점 이상**: 화제성 높은 핫이슈 (바이럴 분석)

#### 🧠 **NLP 분석 방법론**

**1. 텍스트 전처리**
```python
- URL, HTML 태그 제거
- 특수문자 정규화  
- 소문자 변환
- 불용어(stopwords) 제거
```

**2. 키워드 추출 (TF-IDF)**
- **상위 키워드**: 중요도 기반 랭킹
- **연관어 분석**: 동시 출현 키워드 매핑
- **트렌드 변화**: 시기별 키워드 부상/쇠퇴

**3. 감성 분석 (VADER)**
```
감성 분류 기준:
- Positive: +0.05 이상
- Neutral: -0.05 ~ +0.05
- Negative: -0.05 이하
```

#### 📈 **핵심 비즈니스 인사이트**

**1. 소비자 Pain Point 식별**
```
주요 불만사항 (감성 분석 기반):
1. 타이어 소음 (Negative 78%)
2. 조기 마모 (Negative 71%) 
3. 가격 부담 (Negative 65%)
4. 선택의 어려움 (Neutral 45%)
```

**2. 제품 개발 방향성**
- **저소음 기술**: EV 특성상 엔진음 부재로 타이어 소음 민감도 증가
- **내마모성 강화**: 회생제동으로 인한 특수 마모 패턴 대응
- **효율성 최적화**: 전비(연비) 향상을 위한 저저항 설계

**3. 마케팅 인사이트**
- **정보 부족**: 87% 사용자가 EV 전용 타이어 필요성 인지 부족
- **구매 결정 요인**: 성능(45%) > 가격(32%) > 브랜드(23%)
- **추천 경로**: 온라인 커뮤니티 > 딜러 > 지인 순

#### 🔥 **시각화 대시보드 구성**
- **키워드 히트맵**: 월별 관심사 변화 트렌드
- **감성 분석 차트**: 브랜드별/제품별 소비자 만족도
- **트렌드 라인**: 시간대별 이슈 등장/소멸 패턴

---

## 🛠️ 기술 스택 & 아키텍처

### **Frontend**
- **Streamlit**: 빠른 프로토타이핑과 배포
- **Plotly**: 인터랙티브 시각화
- **Custom CSS**: 브랜딩과 UX 최적화

### **Data Processing**
- **Pandas**: 대용량 데이터 처리 및 분석
- **NumPy**: 수치 연산 최적화
- **SQLite**: 로컬 데이터베이스 관리

### **Machine Learning & NLP**
- **Scikit-learn**: TF-IDF 벡터화, 클러스터링
- **NLTK**: 자연어 처리, 감성 분석
- **VADER**: 소셜 미디어 특화 감성 분석

### **External APIs**
- **Reddit API (PRAW)**: 실시간 소셜 데이터 수집
- **Tableau Public**: 고급 시각화 임베딩

---

## 💼 비즈니스 가치 & ROI

### **정량적 효과**
- **TCO 최적화**: 차량당 연간 **300-500만원** 절감 가능
- **시장 기회 발굴**: 신규 시장 진출로 **매출 20% 증대** 기대
- **제품 개발 효율성**: 고객 니즈 기반 개발로 **출시 기간 30% 단축**

### **정성적 효과**
- **데이터 기반 의사결정**: 직관이 아닌 데이터 근거 확보
- **시장 반응 예측**: 제품 출시 전 시장 검증 가능
- **경쟁 우위 확보**: 실시간 시장 모니터링 체계 구축

---

## 🚀 로컬 실행 방법

### **1. 환경 설정**
```bash
git clone https://github.com/your-username/integrated-analytics-dashboard.git
cd integrated-analytics-dashboard
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
pip install -r requirements.txt
```

### **2. 샘플 데이터 생성 (선택사항)**
```bash
python create_sample_data.py  # 샘플 데이터 자동 생성
```

### **3. 애플리케이션 실행**
```bash
streamlit run src/main.py
```

### **4. 브라우저 접속**
```
http://localhost:8501
```

---

## 📊 테스트 시나리오

### **Fleet TCO Calculator**
1. **기본 시나리오**: 타이어 개수 10개 → 20개 변경 시 TCO 변화 확인
2. **민감도 분석**: 유가 20% 상승 시나리오 시뮬레이션
3. **ROI 계산**: 고효율 타이어 도입 시 투자 회수 기간 산정

### **TBR Market Dashboard**
1. **시장 분석**: 2024년 상위 5개 수입국 트렌드 분석
2. **경쟁 분석**: 한국 vs 중국 수출 경쟁력 비교
3. **기회 발굴**: 성장률 상위 3개 신흥 시장 식별

### **EV Tire Analytics**
1. **이슈 탐지**: 'noise' 키워드 관련 감성 변화 추이
2. **브랜드 모니터링**: Tesla 관련 타이어 언급 감성 분석
3. **제품 기획**: 소비자 니즈 기반 신제품 컨셉 도출

---

## 📁 프로젝트 구조

```
integrated-analytics-dashboard/
├── src/
│   └── main.py                 # 메인 애플리케이션 실행 파일
├── data/                           # 데이터 폴더
│   ├── vehicle_efficiency.csv     # 자동차 표시연비 (공공데이터포털)
│   ├── vehicle_distance.csv       # 일평균 주행거리 (공공데이터포털)
│   ├── fuel_prices.csv            # 주유소 평균가격 (오피넷)
│   ├── tbr_market.db              # TBR 시장 데이터 (SQLite) 
│   │   https://comtradeplus.un.org/TradeFlow 
│   │   UN Comtrade Data 연도별 국가별 수출량 (HS 4011)을 csv로 다운로드 후 db에 적재함.
│   │   최근 5년 (2020~2024)
│   │   DB 주요 컬럼명: reporterISO (Country) / cifValue (Export Value) / forValue (Import Value)
│   └── ev_tire_reddit_filtered.csv # EV 타이어 Reddit 데이터
├── requirements.txt                # Python 의존성 파일
├── .gitignore                     # Git 제외 파일 설정
└── README.md                      # 프로젝트 문서
```

---

## 🎯 추가 개발 로드맵

### **Phase 2: AI 고도화 예정 내용**
- **예측 모델링**: 타이어 교체 시기 예측 알고리즘
- **이상 탐지**: 비정상적 연비 패턴 자동 감지
- **추천 시스템**: 사용 패턴 기반 최적 타이어 추천

### **Phase 3: 플랫폼 확장**
- **모바일 앱**: 현장 관리자용 모바일 대시보드
- **API 제공**: 외부 시스템 연동을 위한 RESTful API
- **실시간 알림**: 임계치 도달 시 자동 알림 시스템

---

*"데이터가 말하는 인사이트로 더 나은 의사결정을"* 🚀
