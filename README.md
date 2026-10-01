# Leader Finder v11 — AI Web Search Hybrid

v10의 KRX 진단 기능에 OpenAI Responses API + web_search를 추가한 하이브리드 버전입니다.

## 핵심
- KRX/pykrx: 가격·거래대금·수급 실데이터 시도
- OpenAI web_search: 최신 주도 섹터·종목·뉴스/공시 모멘텀 조사
- 확인되지 않은 가격/거래대금/수급 숫자는 AI가 만들지 않고 null 표시
- AI 시장탐색 결과는 별도 탭에 표시하여 KRX 실데이터와 구분

## Render 설정
Build Command:
`pip install -r requirements.txt`

Start Command:
`uvicorn app:app --host 0.0.0.0 --port $PORT`

Environment에 추가:
- `OPENAI_API_KEY` = OpenAI API key
- `OPENAI_MODEL` = `gpt-5.6-luna` (기본값, 선택)

중요: ChatGPT Plus 구독과 OpenAI API 과금은 별개입니다. API key는 GitHub 코드에 넣지 말고 Render Environment의 Secret 값으로만 저장하세요.

## 사용
배포 후 `AI 시장탐색` 탭 → `AI 최신시장 검색` 버튼을 누릅니다.
웹검색은 호출 비용이 발생할 수 있으며 보통 일반 화면 조회보다 느립니다.
