LWG - 기업 분석 및 포트폴리오 서비스
LWG 웹페이지는 DART 전자공시 시스템과 Google Gemini AI를 활용하여 기업 정보를 분석하고, 최신 뉴스 요약을 제공하는 웹 애플리케이션입니다. 개발자 포트폴리오 및 면접 후기 관리 기능(Firebase 연동)도 포함되어 있습니다.

🛠️ 기술 스택 (Tech Stack)
Backend: Python, Flask

Frontend: HTML5, CSS3, JavaScript (Vanilla)

Database: Firebase Firestore (면접 기록 저장)

API:

Open DART API: 기업 재무 및 공시 정보 조회

Google Gemini API: 관련 뉴스 검색 및 3줄 핵심 요약

📂 프로젝트 구조
Bash

Project-Root/

├── app.py              # Flask 백엔드 서버 (API 중계 및 AI 요약)  
├── portfolio.html      # 메인 프론트엔드 페이지  
├── CORPCODE.xml        # DART 고유번호 데이터 (필수)  
├── requirements.txt    # 파이썬 의존성 패키지  
└── .env                # 환경변수 설정 파일 (직접 생성 필요)  

설치 및 실행 방법 (Installation & Run)

  
1. 환경 설정 (.env)
프로젝트 루트 경로에 .env 파일을 생성하고 아래 내용을 작성하세요. (CORPCODE.xml 파일이 프로젝트 루트에 존재하는지 반드시 확인해주세요.)
  
.env file
DART_API_KEY=발급받은_DART_API_키
GEMINI_API_KEY=발급받은_GEMINI_API_키
GEMINI_MODEL=gemini-2.5-flash-preview-09-2025

  
2. 패키지 설치
Python 가상환경 활성화 후, 필수 라이브러리를 설치합니다.

pip install -r requirements.txt 


3. 백엔드 서버 실행
Flask 서버를 실행합니다. 
  
python app.py
서버가 시작되면 http://127.0.0.1:5000에서 API 요청을 대기합니다.  

4. 웹 페이지 접속
portfolio.html 파일을 브라우저에서 실행합니다.
권장: VS Code의 Live Server 확장을 사용하거나, 브라우저에 파일을 직접 드래그하여 엽니다.
기업명을 입력하여 분석 기능을 테스트할 수 있습니다.  

⚠️ 주의사항
CORPCODE.xml: DART에서 제공하는 고유번호 XML 파일이 없으면 기업 검색이 불가능합니다. 압축을 푼 파일이 app.py와 같은 폴더에 있어야 합니다.  
  
Firebase 설정: portfolio.html 내부의 firebaseConfig 객체는 본인의 프로젝트 설정값으로 변경해야 정상적으로 DB가 작동합니다.

실행화면
app.py 실행
<img width="1451" height="434" alt="image" src="https://github.com/user-attachments/assets/5ab188de-9b16-41c7-9e47-92ddc6be8c02" />


홈 페이지
<img width="1301" height="882" alt="image" src="https://github.com/user-attachments/assets/1ed1c42a-1d17-4080-9fc1-537eb432f0a2" />




