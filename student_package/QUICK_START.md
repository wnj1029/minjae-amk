# ⚡ QUICK START — 5분 컷 세팅

> 팀 배정 직후 이 문서 하나만 따라가면 Week 1 첫 커밋까지 완료됩니다.

## Step 1 · 팀 레포 생성
```bash
# 04_templates/ethics-agent-game-TEAM 을 팀 레포로 복사
cp -r 04_templates/ethics-agent-game-TEAM ~/my-team-repo
cd ~/my-team-repo
```

## Step 2 · README 팀 정보 채우기
`README.md` 상단 표에서 다음 4곳만 편집:
- 팀명 (예: T3)
- 배정 문화권 (예: KOREA)
- 팀원 4명 (이름, 학번, 전공, GitHub ID)
- Streamlit Cloud URL (Week 1 배포 후 채움)

## Step 3 · GitHub push
```bash
git init && git branch -M main
git add . && git commit -m "chore: bootstrap from template"
gh repo create <org>/<repo> --public --source=. --push
```

## Step 4 · 검증 통과 확인
```bash
python3 -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
python scripts/validate_scenarios.py --file data/scenarios.json
# ✅ 검증 통과 — culture=KOREA, team=T3, 시나리오 3개
```

## Step 5 · Streamlit Cloud 배포
1. https://share.streamlit.io 접속 → GitHub 로그인
2. **New app** → Repository/Branch/Main file(app.py) 선택
3. **Deploy!** → URL 을 README 에 반영

## Step 6 · Week 1 시작
```bash
git checkout -b feature/week1-culture-report
# docs/week1/culture_report.md 작성 → 커밋 → PR
```

---
© 2026 강송희 교수 · CC BY-NC 4.0
