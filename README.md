# 안녕하세요, 박선하입니다 👋

> 문제를 정확히 이해하고, **근거를 갖춘 해결책**을 만드는 보안 엔지니어

- 🎓 아주대학교 사이버보안전공 · 2026.08 졸업예정
- 🛡️ BoB 14기 보안제품개발 트랙 · 화이트햇 스쿨 1기
- 📄 CISC-W'25 학술 발표
- 📫 waaterr0516@gmail.com

---

## 🧰 Skills

**Cloud Security**
`CloudTrail 로그 수집·정규화` `자산 변경 이력 추적` `선언적 보안 정책 엔진 (AWS FSBP 매핑)` `침해 대응 자동화 (Lambda · Step Functions · GuardDuty)`

**Detection & Analysis**
`사용자 행위 기반 이상 탐지 설계` `통계적 거리 기반 이상도 산출 및 기여 피처 분해` `공격 시나리오 설계 및 검증 데이터셋 구축`

**AI for Security**
`LLM · RAG 문서 분석 파이프라인` `법령 지식 베이스 구축 / 항목별 프롬프트 분기` `임베딩 기반 분류 모델 학습·평가`

**Compliance & Forensics**
`개인정보보호법 · 처리방침 작성지침 해석` `Android 모바일 포렌식 아티팩트 분석`

**Tech Stack**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Java](https://img.shields.io/badge/Java-007396?style=flat-square&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonwebservices&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white)
![pandas](https://img.shields.io/badge/pandas-150458?style=flat-square&logo=pandas&logoColor=white)

---

## 📂 Projects

### 🗼 관제탑 (Control Tower) — 클라우드 로그 인텔리전스 기반 통합 관제
> 자산 변경 이력과 사용자 행위 로그를 **주체 기준으로 연계**해, 이상 징후의 발생 사실뿐 아니라 원인과 맥락까지 제시하는 조사 지원형 관제 시스템

- **기간 / 역할** — 2025.09 ~ 2025.12 · BoB 14기 · 팀장 / PM (6인)
- 자산 스냅샷 비교 기반 변경 이력 추적 + YAML 선언적 정책 30종 (AWS FSBP 컨트롤 ID 매핑)
- 사용자별 baseline 대비 Mahalanobis 거리로 이상도 산출 → **기여 피처 단위로 분해해 판단 근거 제시**
- 공개 데이터셋이 없어 AWS 환경을 직접 구성하고 3단계 공격 시나리오(정찰 → 권한 테스트 → 권한 상승)를 수행해 검증 데이터 생성
- `Python` `Java(Spring)` `AWS`

🔗 [GitHub](https://github.com/BoB14-controlTower/controlTower-project-unified)

<br>

### 🚨 Auto-IR-Analysis — 서버리스 침해 대응 자동화
> 휘발성 증거를 자동 수집·보전하고, 감염 인스턴스를 격리하되 **서비스 가용성은 유지**하는 대응 파이프라인

- **기간 / 역할** — 2023.10 ~ 2024.01 · 화이트햇 스쿨 1기 · 격리 자동화 담당 (7인)
- GuardDuty 탐지 → 아티팩트 수집 → EBS 스냅샷 보전 → 격리 → Volatility·YARA 자동 분석
- 휘발성 증거 소실을 막기 위해 **수집을 격리보다 앞에** 배치, 두 단계를 자동화해 지연 최소화
- Auto Scaling Group 기반 다중 인스턴스 구성으로 격리로 인한 서비스 중단 방지
- `AWS Lambda` `Step Functions` `GuardDuty`

🔗 [GitHub](https://github.com/Cumulus-AWS/Auto-IR-Analysis_Architecture_In_AWS)

<br>

### 📑 PriBuddy — LLM·RAG 기반 개인정보 처리방침 분석
> 처리방침을 항목별로 요약하고, **근거 법령과 함께** 불공정 조항을 탐지하는 서비스

- **기간 / 역할** — 2025.03 ~ 2025.07 · 캡스톤디자인 · PM / LLM 서버 설계 (4인)
- 법령·지침을 처리방침 기재 항목 체계로 분해하고 태그를 부여해 벡터 DB 구축 → **같은 태그의 조문만 검색**해 오검색 감소
- 항목별 검토 기준이 다른 점을 반영한 프롬프트 분기 설계
- CPPG 자격 보유 팀원의 검토를 거쳐 과탐지 항목 식별 및 프롬프트 반영
- `Python` `Node.js` `MySQL` `AWS`

🔗 [GitHub](https://github.com/pribunny/ajou_capstone_pribunny)

<br>

### 🕵️ AI 기반 다크패턴 탐지 — KoBERT + CNN
> 국내 전자상거래법 기준(편취·오도·방해·압박)에 맞춘 데이터셋 구축 및 탐지 모델 도출

- CISC-W'25 발표 · **제1저자** · SW중심대학사업 연구
- DOM 트리 서브트리 단위 슬라이싱으로 문맥 손실·노이즈 최소화, 능동 학습(modAL)으로 라벨 확장
- 임베딩 4종 × 분류기 4종 조합 비교 → **Accuracy 0.98 / F1 0.98**
- 짧은 문구 특성상 순서 정보 이점이 적어, 동일 성능이면 연산량이 적은 CNN을 선택

<br>

### 📱 Telegram 영상 캐시 분석을 통한 사용자 행위 추론
> 앱이 기록하지 않는 '시청 행위'를 **캐시 파일의 생성 조건과 구조 변화**로 추정

- 자율연구 · 제1저자 (지도교수 공저)
- 루팅 단말 USERDATA 이미징 후 스트리밍 on/off를 변수로 캐시 파일 바이트 단위 비교
- `.temp` 파일의 채워지는 양상 차이로 시청 구간·시청 시간 추정 근거 제시
- `Android` `ADB` `TWRP` `HxD`

---

## 📜 Certifications & Activities

| 구분 | 내용 |
|---|---|
| 교육 | BoB 14기 보안제품개발 트랙 |
| 교육 | 화이트햇 스쿨 1기 |
| 발표 | CISC-W'25 학술 발표 (제1저자) |
| 어학 | TOEIC Speaking IH |

---

<div align="center">

📮 **waaterr0516@gmail.com**

</div>
