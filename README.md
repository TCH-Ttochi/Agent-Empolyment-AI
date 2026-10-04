# Agent-Empolyment-AI

# 취업 지원 AI Agent

기업 채용 정보 탐색, 발음 연습, 적응형 AI 모의 면접을 제공하는 웹 애플리케이션입니다.

## 주요 기능

- 기업별 채용 정보 검색
- 난이도별 발음 연습 및 점수 기록
- 이력서와 답변을 바탕으로 후속 질문을 생성하는 모의 면접
- 면접 답변 평가 및 결과 보고서 생성

## 기술 스택

- Frontend: HTML, Tailwind CSS, JavaScript
- Backend: Node.js, Express
- API: Gemini, Tavily
- 선택 연동: Google Sheets

## 실행 방법

필요한 패키지를 설치합니다.

    npm install

환경 변수 설정 후 서버를 실행합니다.

    node server.js

브라우저에서 http://localhost:5000 을 엽니다.

## 환경 변수

프로젝트 루트에 `.env` 파일을 만들고 필요한 값을 설정합니다.

    GEMINI_API_KEY=발급받은_Gemini_API_키
    TAVILY_API_KEY=발급받은_Tavily_API_키
    GOOGLE_SERVICE_ACCOUNT_EMAIL=
    GOOGLE_PRIVATE_KEY=
    GOOGLE_SHEET_ID=

Gemini 키는 면접 질문 생성과 평가에 필요합니다. Tavily와 Google Sheets 연동은 선택 사항입니다. Google Sheets를 사용할 때는 서비스 계정 이메일, 비공개 키, 시트 ID를 설정해야 합니다.

## API 키 및 개인정보 주의

`.env`에는 실제 API 키와 인증 정보가 들어가므로 GitHub에 올리지 마세요. 이력서와 면접 답변은 질문 생성 및 평가를 위해 Gemini API로 전송됩니다.

## 참고

발음 연습은 브라우저 음성 인식 결과를 기준 문장과 비교해 점수를 계산합니다. 음성 인식 기능은 지원 브라우저와 HTTPS 또는 localhost 환경이 필요할 수 있습니다.
