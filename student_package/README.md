# 🎓 Global AI Ethics Simulator — 학생 배포 패키지

> **인공지능과 경영 · 11주차 협동학습 · 3주 스프린트**
> 강송희 교수 · 한국공학대학교 경영학부
> © 2026 · CC BY-NC 4.0

---

## 📦 패키지 구성

```
student_package/
├── README.md                             ← 지금 이 파일 (전체 안내)
│
├── 01_workbook/                          📘 학생 워크북 (PDF)
│   └── README_워크북_다운로드.md         → Genspark 링크 & 목차
│
├── 02_slides/                            🎞️ 강의용 슬라이드 (PPTX/PDF)
│   └── README_슬라이드_다운로드.md       → Genspark 링크 & 슬라이드 구성
│
├── 03_rubric_xlsx/                       📊 평가 루브릭 스프레드시트
│   └── Week1-3_평가루브릭_통합.xlsx      → 8 sheets · 100점 자동 계산
│
├── 04_templates/                         🧩 팀 레포지토리 스타터 킷
│   └── ethics-agent-game-TEAM/           → 학생이 그대로 fork/clone 시작
│       ├── README.md
│       ├── requirements.txt
│       ├── .gitignore
│       ├── app.py                        (Ethics Agent Game 강화학습)
│       ├── narrative_app.py              (시나리오 저작 앱 스텁)
│       ├── data/scenarios.json           (KOREA 예시 3개 · 즉시 로딩 가능)
│       ├── schemas/scenario.schema.json  (JSON Schema draft-07)
│       ├── scripts/validate_scenarios.py (140줄 검증기)
│       ├── docs/
│       │   ├── week1/culture_report.md
│       │   ├── week2/scenario_review.md
│       │   └── week3/final_report.md
│       ├── logs/ai_usage_log.md          (Non-AI vs AI diff 로그)
│       ├── logs/experiments/.gitkeep
│       ├── .streamlit/secrets.toml.example
│       └── .github/
│           ├── workflows/ci.yml          (Python 3.11 + validate + syntax)
│           ├── PULL_REQUEST_TEMPLATE.md
│           └── ISSUE_TEMPLATE/value_check.md
│
└── 05_source_materials/                  📚 원본 강의 자료 (참고용)
    ├── 20251118_인공지능과경영_11주차_협동학습가이드.pdf
    ├── ethics_ai_agent_game_workshop.pptx
    └── app-reinforce.py
```

---

## 🚀 학생용 Quick Start

### 1️⃣ 워크북 · 슬라이드 다운로드
- `01_workbook/README_워크북_다운로드.md` → 링크 열고 **PDF Export**
- `02_slides/README_슬라이드_다운로드.md` → 링크 열고 **PPTX Export**

### 2️⃣ 팀 레포 만들기
```bash
# ① 04_templates/ethics-agent-game-TEAM/ 폴더 전체를 자기 팀 레포로 push
cd 04_templates/ethics-agent-game-TEAM
git init && git add . && git commit -m "chore: bootstrap from template"
git remote add origin git@github.com:<team>/<repo>.git
git branch -M main && git push -u origin main
```

### 3️⃣ 로컬 실행
```bash
python3.11 -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
streamlit run app.py
```

### 4️⃣ 시나리오 검증
```bash
python scripts/validate_scenarios.py --file data/scenarios.json
# → ✅ 검증 통과 — culture=KOREA, team=T3, 시나리오 3개
```

### 5️⃣ CI 그린 확인
- `.github/workflows/ci.yml` 이 자동으로 push/PR 마다 실행
- 배지: README 상단 `![CI](...ci.yml/badge.svg)`

---

## 🗓️ 3주 스프린트 흐름 (P-A-S-A-R)

| 주차 | 단계 | 산출물 | 배점 |
|---|---|---|---|
| **Week 1** | 🔵 Problem framing | `docs/week1/culture_report.md` | 20 |
| **Week 2** | 🟢 AI augmentation | `data/scenarios.json` + Issue 리뷰 | 25 |
| **Week 3** | 🟣 Simulation·Audit·Reflection | `docs/week3/final_report.md` | 35 |
| 상시 | Individual (성찰+피어) | `logs/ai_usage_log.md` | 10 |
| 상시 | 협업 과정증거 | PR·Issue·Process_Log | 10 |
| | | **합계** | **100** |

## 📞 문의

- 강의자: 강송희 교수 (한국공학대학교 경영학부)
- 강의명: 인공지능과 경영 · 11주차
- 라이선스: **CC BY-NC 4.0** (교육/비영리 목적 자유 사용)

---

**즐거운 3주 스프린트 되세요! 🎯**
